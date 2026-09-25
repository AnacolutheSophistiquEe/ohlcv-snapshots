# SOI

**Generated** : 2026-09-25T21:51:23.250128+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €143.05  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot €143.05 (+2.9% vs entrée) · entrée €139.03 · stop €128.51 · T1 €152.72 · R/R 1.3  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk 0.032 _(réel 5 s)_ (GBM 0.248) · ¼-Kelly 0.027 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €136.89–€141.18 (mid €139.03)
- Spot actuel : €143.05 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €128.51 (stop swing_plan-based (-10.17%))
- Targets : T1 €152.72 · R/R 1.3 | T2 €161.95 · R/R 2.18 | T3 €171.17 · R/R 3.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.51


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.17 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **8.549 pt plus bas** dans le cas TYPIQUE (médiane), 17.009 au p90, **19.124 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0265 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.675 % | p01 -5.132 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4484** [0.3757 ; 0.5228] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3812** [0.3312 ; 0.4332] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.2544** [0.2107 ; 0.3022] _(largeur 9.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.4 pt), swing (37.1 pt), deep (34.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-14.04 %** | vol 6.65 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.86 % contre 7.63 % aujourd'hui, rapport 0.51)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.4 % vs -11.44 % si l'on extrapolait par √5 _(rapport 1.084 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1153** (β de hausse 1.5738, asymétrie 0.7087) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.045× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 127.2571 sur atr_based (1.5 ATR, 11.04 %) — p(stop avant cible) 0.4119 [0.36 ; 0.46], R/R 0.916, perte reelle 21.456 % (gap inclus), CVaR 11.064 %, EV -2.7904 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.73 ATR (stop 7.909 %) — p(stop avant cible) 0.5328 [0.48 ; 0.58], R/R 1.283, perte reelle 15.318 % (gap inclus), EV -2.5506 % — **REFUSE**
      - refuse : p_stop_first 0.533, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.69 ATR du spot — compartiment <1, mesure a 48.0 % de casse (IC clusterise [0.451 ; 0.508] sur 1182 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.55 %) : P(cible) 23.6 % x 19.66 % + P(rien) 23.2 % x 4.23 % ne couvrent pas P(stop) 53.3 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 11.04 %) — p(stop avant cible) 0.4119 [0.36 ; 0.46], R/R 0.916, perte reelle 21.456 % (gap inclus), EV -2.7904 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.79 %) : P(cible) 27.4 % x 19.66 % + P(rien) 31.4 % x 2.11 % ne couvrent pas P(stop) 41.2 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.43 ATR (stop 13.082 %) — p(stop avant cible) 0.3356 [0.29 ; 0.39], R/R 0.916, perte reelle 21.456 % (gap inclus), EV -1.2076 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 28.7 % x 19.66 % + P(rien) 37.8 % x 0.94 % ne couvrent pas P(stop) 33.6 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.47 ATR (stop 20.772 %) — p(stop avant cible) 0.1039 [0.07 ; 0.14], R/R 0.671, perte reelle 29.294 % (gap inclus), EV 1.7875 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.78 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.84 %) — p(stop avant cible) 0.8462 [0.81 ; 0.88], R/R 5.172, perte reelle 3.801 % (gap inclus), EV -0.6917 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.846, borne haute 0.881 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 10.9 % x 19.66 % + P(rien) 4.5 % x 8.45 % ne couvrent pas P(stop) 84.6 % x 3.80 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.72 %) — p(stop avant cible) 0.2934 [0.25 ; 0.34], R/R 0.916, perte reelle 21.456 % (gap inclus), EV -0.5639 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 28.7 % x 19.66 % + P(rien) 42.0 % x 0.22 % ne couvrent pas P(stop) 29.3 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 22.08 %) — p(stop avant cible) 0.0947 [0.07 ; 0.13], R/R 0.671, perte reelle 29.294 % (gap inclus), EV 1.9089 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.09 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 25.76 %) — p(stop avant cible) 0.0498 [0.03 ; 0.08], R/R 0.671, perte reelle 29.294 % (gap inclus), EV 2.6622 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.76 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 29.44 %) — p(stop avant cible) 0.0295 [0.02 ; 0.05], R/R 0.668, perte reelle 29.44 % (gap inclus), EV 2.8014 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.44 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 33.12 %) — p(stop avant cible) 0.0295 [0.02 ; 0.05], R/R 0.594, perte reelle 33.12 % (gap inclus), EV 2.6928 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 36.8 %) — p(stop avant cible) 0.0163 [0.01 ; 0.03], R/R 0.534, perte reelle 36.8 % (gap inclus), EV 2.7073 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.80 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 40.48 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.486, perte reelle 40.48 % (gap inclus), EV 2.766 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.48 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 44.16 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.445, perte reelle 44.16 % (gap inclus), EV 2.7821 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.16 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 47.84 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.411, perte reelle 47.84 % (gap inclus), EV 2.7821 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.84 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 51.52 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.382, perte reelle 51.52 % (gap inclus), EV 2.7821 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.52 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 55.2 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.356, perte reelle 55.2 % (gap inclus), EV 2.7821 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.20 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 58.88 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.334, perte reelle 58.88 % (gap inclus), EV 2.7821 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.88 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 143.05, ATR14 10.5286 (7.36 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 2.642 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.368 % | 142.5236 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.736 % | 141.9971 | 84.8 % | 89.79 % | 91.65 % | 94.29 % | 96.14 % | 97.4 % |
| 0.15 ATR | 1.104 % | 141.4707 | 77.84 % | 84.89 % | 87.52 % | 90.85 % | 93.67 % | 95.3 % |
| 0.2 ATR | 1.472 % | 140.9443 | 69.22 % | 79.69 % | 83.5 % | 87.8 % | 91.39 % | 93.31 % |
| 0.25 ATR | 1.84 % | 140.4179 | 62.75 % | 75.86 % | 80.26 % | 86.12 % | 90.11 % | 92.71 % |
| 0.35 ATR | 2.576 % | 139.365 | 50.88 % | 67.42 % | 73.18 % | 80.91 % | 85.76 % | 90.01 % |
| 0.5 ATR | 3.68 % | 137.7857 | 35.88 % | 55.25 % | 62.57 % | 72.93 % | 80.91 % | 87.21 % |
| 0.75 ATR | 5.52 % | 135.1536 | 17.06 % | 35.13 % | 46.56 % | 58.07 % | 72.6 % | 80.52 % |
| 1.0 ATR | 7.36 % | 132.5214 | 8.43 % | 23.95 % | 34.09 % | 47.24 % | 64.49 % | 75.12 % |
| 1.25 ATR | 9.2 % | 129.8893 | 4.12 % | 15.6 % | 25.05 % | 37.11 % | 56.28 % | 69.33 % |
| 1.5 ATR | 11.04 % | 127.2571 | 2.25 % | 10.5 % | 18.17 % | 29.63 % | 48.47 % | 63.04 % |
| 2.0 ATR | 14.72 % | 121.9929 | 0.59 % | 4.51 % | 8.94 % | 17.91 % | 34.72 % | 52.45 % |
| 2.5 ATR | 18.4 % | 116.7286 | 0.29 % | 2.45 % | 4.91 % | 11.61 % | 23.94 % | 44.46 % |
| 3.0 ATR | 22.08 % | 111.4643 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 16.42 % | 36.36 % |
| 4.0 ATR | 29.44 % | 100.9357 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.4 % | 23.18 % |
| 6.0 ATR | 44.16 % | 79.8786 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.56 ATR | 0.63 ATR | 0.80 ATR | 0.98 ATR | 1.12 ATR | 1.54 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.03 ATR | 1.25 ATR | 1.43 ATR | 1.94 ATR | 2.49 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.05 ATR | 1.39 ATR | 1.70 ATR | 1.91 ATR | 2.68 ATR | 3.59 ATR |
| **10 s.** | 0.68 ATR | 1.45 ATR | 1.63 ATR | 2.08 ATR | 2.45 ATR | 2.76 ATR | 3.92 ATR | 5.78 ATR |
| **20 s.** | 1.00 ATR | 2.15 ATR | 2.47 ATR | 3.25 ATR | 3.86 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.627–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.781–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.36 %, prix 132.5215), p(touche) 34.09 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.055–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.626–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.466–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.248 | EV/share : €2.612 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 26 % | T3 16 %
- Kelly (position) : f* 0.108 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 25.6 | bear 18.5 | side 55.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 572.0 (= 4 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.28% → cible +5.328% / stop −2.664%, p_fill 69%, n_eff≈30.0) : P(cible|rempli) **14%** · **EV/risk +0.020** (×p_fill ; si rempli +0.08% du capital)
  - **swing** (entrée dip −2.81% → cible +9.846% / stop −7.573%, p_fill 56%, n_eff≈23.9) : P(cible|rempli) **37%** · **EV/risk +0.032** (×p_fill ; si rempli +0.43% du capital)
  - **deep** (entrée dip −4.336% → cible +31.536% / stop −15.768%, p_fill 69%, n_eff≈29.0) : P(cible|rempli) **10%** · **EV/risk -0.086** (×p_fill ; si rempli -1.99% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→64% · +3.0%→50% · +5.0%→31% · +8.0%→9%
- Range intraday médian 7.57% (p90 13.58%) · excursion haute méd. +3.14% / basse méd. −2.94%
- Profil de vol intra : ouverture 4.623% vs midi 1.318% vs clôture 1.973% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.422% ; recovery-V 38%
- **σ réalisé intraday** 4.323% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 56% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 128.644 (VA 127.828–129.324 ; dernier close 127.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 44% · rebond 81% · **stop −7.63%** sous le fill (sous le bruit) · cible +3.11% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.59% · baisse 37% (gap-down >1% 26% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −3.4%) · haut méd +0.9% · range méd 2.7%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −4.51%) · haut méd +1.25% · range méd 3.23%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −5.08%) · haut méd +1.36% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.55% (p90 −5.31%) · haut méd +1.64% · range méd 3.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 128.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (124/159) · gap 33% · délai 0.1min · rebond 68% (87/124) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 69% (113/159) · gap 26% · délai 0.2min · rebond 76% (84/113) (MFE +1.99%)
   - −1.5% : fill 30min 48% · séance 61% (104/159) · gap 20% · délai 0.3min · rebond 76% (77/104) (MFE +2.3%)
   - −2.0% : fill 30min 41% · séance 56% (93/159) · gap 18% · délai 0.4min · rebond 70% (70/93) (MFE +2.4%)
   - −3.0% : fill 30min 31% · séance 44% (77/159) · gap 9% · délai 1.5min · rebond 81% (65/77) (MFE +3.11%)
   - −4.0% : fill 30min 24% · séance 37% (64/159) · gap 5% · délai 10.8min · rebond 76% (54/64) (MFE +3.3%)
   - −5.0% : fill 30min 15% · séance 30% (49/159) · gap 2% · délai 31.6min · rebond 72% (39/49) (MFE +2.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.45%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.4%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.25%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1344 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 97% (54/56) · rebond 67% (36/54)
      · −2.0% : fill 93% (51/56) · rebond 68% (38/51)
      · −3.0% : fill 81% (46/56) · rebond 81% (39/46)
      · −4.0% : fill 67% (39/56) · rebond 89% (36/39)
      · −5.0% : fill 54% (31/56) · rebond 77% (26/31)
   - **flat** (13 séances) :
      · −1.0% : fill 93% (10/13) · rebond 77% (8/10)
      · −2.0% : fill 73% (9/13) · rebond 78% (8/9)
      · −3.0% : fill 70% (8/13) · rebond 78% (7/8)
      · −4.0% : fill 56% (7/13) · rebond 58% (5/7)
      · −5.0% : fill 56% (7/13) · rebond 72% (6/7)
   - **gap-up** (90 séances) :
      · −1.0% : fill 51% (49/90) · rebond 84% (40/49)
      · −2.0% : fill 33% (33/90) · rebond 73% (24/33)
      · −3.0% : fill 21% (23/90) · rebond 82% (19/23)
      · −4.0% : fill 18% (18/90) · rebond 57% (13/18)
      · −5.0% : fill 14% (11/90) · rebond 59% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 62% si les 15 1res min sont vertes (77 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 72% si début vert vs 25% si rouge (base 49% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **72%** · continue >prix actuel 49% ; creux résiduel méd -1.81% (q20 -4.92%) → **SL/trailing à −4.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.35% / q75 +4.48% → **scale +2.35% / runner +4.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **25%** (continue à baisser 65%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.65%** (au-delà de la MAE q10 -8.65%), cible rebond +2.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.59% .. +6.13%] · haut q95 +7.22% · bas q05 -5.93%
   - 60min (n=160) : retour [-5.37% .. +6.48%] · haut q95 +7.85% · bas q05 -6.55%
   - 2h (n=160) : retour [-6.01% .. +5.93%] · haut q95 +9.18% · bas q05 -7.41%
   - 4h (n=160) : retour [-6.77% .. +7.89%] · haut q95 +10.91% · bas q05 -8.1%
   - 6h (n=160) : retour [-7.61% .. +9.07%] · haut q95 +12.33% · bas q05 -9.35%
   - session (n=160) : retour [-11.05% .. +10.07%] · haut q95 +13.99% · bas q05 -12.6%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 8% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.8  _(neutre)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist 0.559  _(pas de croisement recent)_
- **BB** : %B 0.64 · largeur 39.9%
- **ATR** : 10.53 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.09  _(accumulation)_
- **Vol ratio** : 0.37  _(volume atone)_
- **Choppiness** : 53.0  _(transition)_
- **MA** : MA20 135.72 · MA50 121.66 · MA200 89.54  _(prix > MA20)_
- **Dist MA** : MA20 +5.4% · MA50 +17.6% · MA200 +59.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (869785 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
