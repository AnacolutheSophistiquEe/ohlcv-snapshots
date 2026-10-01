# HOOD

**Generated** : 2026-10-01T00:32:09.352285+00:00  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $112.52  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $112.52 (+0.8% vs entrée) · entrée $111.68 · stop $105.40 · T1 $122.40 · R/R 1.71  
> ↳ ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -0.2 % ≠ (strike 116.0 − spot 112.52)/spot = +3.1 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $110.84–$112.52 (mid $111.68)
- Spot actuel : $112.52 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $105.40 (plancher anti-bruit (R/R<2) ; -5.62 % depuis l'entree)
- Targets : T1 $122.40 · R/R 1.71 | T2 $129.42 · R/R 2.82 | T3 $136.45 · R/R 3.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $105.40


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.33 %)** : le gap seul le franchit 1.277 % des séances (16 fois sur 1253).
   - exécution **2.719 pt plus bas** dans le cas TYPIQUE (médiane), 6.685 au p90, **11.455 au pire**
   - perte réelle **9.781 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 6.33 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0441 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3112** [0.2458 ; 0.3829] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.49** [0.4376 ; 0.5426] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.434** [0.3825 ; 0.4866] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-7.0 %** | CVaR **-9.78 %** | vol 4.77 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 2.74 % contre 4.71 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7717** (β de hausse 1.6092, asymétrie 1.101) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.397× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 104.662 sur atr_grid (1.25 ATR, 6.984 %) — p(stop avant cible) 0.5409 [0.49 ; 0.59], R/R 2.889, perte reelle 7.363 % (gap inclus), CVaR 10.771 %, EV 1.3989 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1343 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.541, borne haute 0.593 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.34 ATR (stop 4.49 %) — p(stop avant cible) 0.676 [0.63 ; 0.72], R/R 4.511, perte reelle 4.716 % (gap inclus), EV 1.0824 % — **REFUSE**
      - refuse : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.02 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 8.38 %) — p(stop avant cible) 0.4552 [0.40 ; 0.51], R/R 2.416, perte reelle 8.802 % (gap inclus), EV 1.6939 % — **REFUSE**
      - refuse : R/R 2.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 1.88 ATR (stop 13.137 %) — p(stop avant cible) 0.2511 [0.21 ; 0.30], R/R 1.547, perte reelle 13.752 % (gap inclus), EV 2.5447 % — **REFUSE**
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.22 % > budget 12.00 %
   - 🟢 support a 3.35 ATR (stop 21.349 %) — p(stop avant cible) 0.0726 [0.05 ; 0.10], R/R 0.983, perte reelle 21.633 % (gap inclus), EV 2.9199 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.76 % > budget 12.00 %
   - 🔴 grid_snapped a 0.34 ATR (stop 3.551 %) — p(stop avant cible) 0.7366 [0.69 ; 0.78], R/R 5.692, perte reelle 3.737 % (gap inclus), EV 0.8671 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.737, borne haute 0.781 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.587 %) — p(stop avant cible) 0.6179 [0.57 ; 0.67], R/R 3.578, perte reelle 5.945 % (gap inclus), EV 1.117 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.618, borne haute 0.668 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 6.984 %) — p(stop avant cible) 0.5409 [0.49 ; 0.59], R/R 2.889, perte reelle 7.363 % (gap inclus), EV 1.3989 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.541, borne haute 0.593 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 1.88 ATR (stop 12.199 %) — p(stop avant cible) 0.2809 [0.24 ; 0.33], R/R 1.65, perte reelle 12.894 % (gap inclus), EV 2.5107 % — **REFUSE**
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.04 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.967 %) — p(stop avant cible) 0.2283 [0.19 ; 0.27], R/R 1.463, perte reelle 14.535 % (gap inclus), EV 2.5746 % — **REFUSE**
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.56 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.364 %) — p(stop avant cible) 0.1936 [0.15 ; 0.24], R/R 1.337, perte reelle 15.903 % (gap inclus), EV 2.5941 % — **REFUSE**
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.45 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.761 %) — p(stop avant cible) 0.1417 [0.11 ; 0.18], R/R 1.235, perte reelle 17.22 % (gap inclus), EV 2.817 % — **REFUSE**
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
   - 🟢 grid_snapped a 3.35 ATR (stop 20.411 %) — p(stop avant cible) 0.0732 [0.05 ; 0.10], R/R 1.025, perte reelle 20.753 % (gap inclus), EV 2.9816 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.91 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.348 %) — p(stop avant cible) 0.0569 [0.04 ; 0.09], R/R 0.936, perte reelle 22.713 % (gap inclus), EV 2.9836 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.76 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.141 %) — p(stop avant cible) 0.0333 [0.02 ; 0.06], R/R 0.829, perte reelle 25.656 % (gap inclus), EV 2.9963 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.82 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.935 %) — p(stop avant cible) 0.0244 [0.01 ; 0.04], R/R 0.752, perte reelle 28.294 % (gap inclus), EV 3.0069 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.51 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.728 %) — p(stop avant cible) 0.0211 [0.01 ; 0.04], R/R 0.689, perte reelle 30.888 % (gap inclus), EV 3.0072 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.02 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.522 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.628, perte reelle 33.871 % (gap inclus), EV 3.1265 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.93 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 36.315 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.58, perte reelle 36.647 % (gap inclus), EV 3.1404 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.64 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.109 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.544, perte reelle 39.109 % (gap inclus), EV 3.149 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.51 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.902 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.508, perte reelle 41.902 % (gap inclus), EV 3.1583 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.30 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.696 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.476, perte reelle 44.696 % (gap inclus), EV 3.1583 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.30 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 112.52, ATR14 6.2864 (5.587 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 2.084 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.279 % | 112.2057 | 93.05 % | 95.16 % | 96.06 % | 96.56 % | 97.05 % | 98.05 % |
| 0.1 ATR | 0.559 % | 111.8914 | 85.5 % | 90.52 % | 92.23 % | 93.73 % | 94.72 % | 96.41 % |
| 0.15 ATR | 0.838 % | 111.577 | 77.54 % | 85.18 % | 87.99 % | 90.29 % | 92.58 % | 95.07 % |
| 0.2 ATR | 1.117 % | 111.2627 | 71.5 % | 80.14 % | 83.75 % | 86.96 % | 90.35 % | 93.22 % |
| 0.25 ATR | 1.397 % | 110.9484 | 64.65 % | 74.5 % | 79.21 % | 83.42 % | 87.7 % | 90.86 % |
| 0.35 ATR | 1.955 % | 110.3197 | 52.37 % | 65.32 % | 71.95 % | 77.55 % | 83.43 % | 87.99 % |
| 0.5 ATR | 2.793 % | 109.3768 | 37.16 % | 53.43 % | 61.15 % | 68.25 % | 76.52 % | 82.24 % |
| 0.75 ATR | 4.19 % | 107.8052 | 19.54 % | 35.99 % | 45.71 % | 55.51 % | 65.65 % | 73.0 % |
| 1.0 ATR | 5.587 % | 106.2336 | 9.26 % | 22.98 % | 32.69 % | 43.78 % | 54.98 % | 65.4 % |
| 1.25 ATR | 6.984 % | 104.662 | 4.83 % | 14.52 % | 22.3 % | 33.37 % | 46.95 % | 58.83 % |
| 1.5 ATR | 8.38 % | 103.0904 | 2.42 % | 9.78 % | 16.15 % | 26.9 % | 40.04 % | 53.18 % |
| 2.0 ATR | 11.174 % | 99.9471 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.57 % | 43.84 % |
| 2.5 ATR | 13.967 % | 96.8039 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.44 % | 34.6 % |
| 3.0 ATR | 16.761 % | 93.6607 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.59 % |
| 4.0 ATR | 22.348 % | 87.3743 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 33.522 % | 74.8014 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.19 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.97 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.54 ATR | 1.16 ATR | 1.32 ATR | 1.84 ATR | 2.28 ATR | 2.62 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.67 ATR | 1.94 ATR | 2.60 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.423–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.621–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.19 %, prix 107.8054), p(touche) 35.99 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.764–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.587 %, prix 106.2335), p(touche) 32.69 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.1 % des re-echantillons)
- **5 seance(s)** : plage utile 0.974–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.587 %, prix 106.2335), p(touche) 43.78 % (en stress 98.99 %)  ✅ optimum identifie (61.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.321–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.38 %, prix 103.0908), p(touche) 40.04 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.938–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.174 %, prix 99.947), p(touche) 43.84 % (en stress 97.96 %)  ✅ optimum identifie (64.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.006 | EV/share : $0.038 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 80.5 | bear 14.5 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 397.0 (= 4 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.412% → cible +2.805% / stop −3.0%, p_fill 88%, n_eff≈94.6) : P(cible|rempli) **30%** · **EV/risk -0.069** (×p_fill ; si rempli -0.23% du capital)
  - **swing** (entrée dip −0.743% → cible +9.594% / stop −5.629%, p_fill 87%, n_eff≈100.9) : P(cible|rempli) **29%** · **EV/risk -0.026** (×p_fill ; si rempli -0.17% du capital)
  - **deep** (entrée dip −0.989% → cible +9.867% / stop −8.464%, p_fill 87%, n_eff≈97.4) : P(cible|rempli) **52%** · **EV/risk +0.144** (×p_fill ; si rempli +1.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→53% · +3.0%→35% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.77% (p90 8.67%) · excursion haute méd. +2.08% / basse méd. −2.3%
- Profil de vol intra : ouverture 3.621% vs midi 0.975% vs clôture 1.098% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr -0.029)_ ; drift intra méd. -0.141% ; recovery-V 21%
- **σ réalisé intraday** 3.236% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 50% / whipsaw 7%
- POC intraday (dernière séance, temps-au-prix) : 115.5206 (VA 115.0019–116.6619 ; dernier close 116.22)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 74% · **stop −4.65%** sous le fill (sous le bruit) · cible +1.8% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 50% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.99% (p90 −2.73%) · haut méd +1.03% · range méd 2.19%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −3.25%) · haut méd +1.34% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.61% (p90 −3.59%) · haut méd +1.6% · range méd 3.41%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −3.8%) · haut méd +1.71% · range méd 3.84%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 116.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (123/159) · gap 40% · délai 0.0min · rebond 63% (71/123) (MFE +1.49%)
   - −1.0% : fill 30min 60% · séance 68% (108/159) · gap 32% · délai 0.0min · rebond 66% (66/108) (MFE +1.66%)
   - −1.5% : fill 30min 48% · séance 61% (98/159) · gap 22% · délai 1.1min · rebond 57% (54/98) (MFE +1.31%)
   - −2.0% : fill 30min 37% · séance 51% (86/159) · gap 16% · délai 2.0min · rebond 69% (55/86) (MFE +1.36%)
   - −3.0% : fill 30min 24% · séance 34% (64/159) · gap 5% · délai 10.7min · rebond 74% (45/64) (MFE +1.8%)
   - −4.0% : fill 30min 12% · séance 24% (47/159) · gap 2% · délai 28.9min · rebond 65% (32/47) (MFE +2.2%)
   - −5.0% : fill 30min 8% · séance 15% (30/159) · gap 1% · délai 29.8min · rebond 63% (21/30) (MFE +2.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.61%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.63% (p90 −2.25%) → stop au-delà de −1.85% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.17%) → stop au-delà de −1.76% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=760 jambes) : jambe baissière méd −1.12% (p90 −2.69%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 92% (71/75) · rebond 57% (38/71)
      · −2.0% : fill 78% (61/75) · rebond 68% (38/61)
      · −3.0% : fill 59% (49/75) · rebond 80% (35/49)
      · −4.0% : fill 40% (36/75) · rebond 74% (27/36)
      · −5.0% : fill 26% (25/75) · rebond 67% (17/25)
   - **flat** (17 séances) :
      · −1.0% : fill 66% (11/17) · rebond 70% (7/11)
      · −2.0% : fill 47% (9/17) · rebond 53% (5/9)
      · −3.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −4.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −5.0% : fill 16% (2/17) · rebond 15% (1/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 46% (26/67) · rebond 81% (21/26)
      · −2.0% : fill 24% (16/67) · rebond 82% (12/16)
      · −3.0% : fill 13% (11/67) · rebond 73% (9/11)
      · −4.0% : fill 10% (7/67) · rebond 61% (4/7)
      · −5.0% : fill 3% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 68% si les 15 1res min sont vertes (74 cas) · 27% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **26min** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 45% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **72%** · continue >prix actuel 49% ; creux résiduel méd -1.45% (q20 -2.7%) → **SL/trailing à −2.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.89% → **scale +1.69% / runner +2.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **21%** (continue à baisser 55%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.86% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.48% .. +3.98%] · haut q95 +4.34% · bas q05 -4.83%
   - 60min (n=160) : retour [-3.68% .. +4.95%] · haut q95 +5.53% · bas q05 -4.86%
   - 2h (n=160) : retour [-4.64% .. +5.6%] · haut q95 +7.54% · bas q05 -5.15%
   - 4h (n=160) : retour [-4.55% .. +6.96%] · haut q95 +8.32% · bas q05 -6.01%
   - 6h (n=160) : retour [-5.72% .. +6.68%] · haut q95 +8.52% · bas q05 -7.11%
   - session (n=160) : retour [-5.4% .. +7.02%] · haut q95 +8.64% · bas q05 -7.13%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **31%**. Lecture précoce 30 min : signature présente → 20% vs absente 2% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.24% / p90 1.92%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 15.35 min, n=49)
   - −1.0% → **62%** (reprise méd 30.0 min, n=21)
   - −1.5% → **48%** (reprise méd 42.24 min, n=10)
   - −2.0% → **15%** (reprise méd None min, n=5)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.92%** (p90, défaut prudent ; serré/agressif −1.24%) ; extension open→close méd +6.2% (q75 +8.64% / q95 +11.94%), MFE méd +7.69% / q90 +13.19%
   - Échelle scale-out : +7.69% (33%) / +9.01% (33%) / +13.19% (34%)
- **DÉSARMER** : repli > **−1.92%** depuis le plus-haut = décay → P(retournement) **85%** (préavis méd 310.68 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.19% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 73% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.64 · part idiosyncratique 0.36
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.1  _(neutre)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist -0.832  _(bearish_recent)_
- **BB** : %B 0.34 · largeur 20.1%
- **ATR** : 6.29 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.051  _(distribution)_
- **Vol ratio** : 1.39  _(volume normal)_
- **Choppiness** : 47.6  _(transition)_
- **MA** : MA20 116.34 · MA50 105.04 · MA200 94.38  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 +7.1% · MA200 +19.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841733 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
