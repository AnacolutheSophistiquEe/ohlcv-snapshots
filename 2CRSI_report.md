# AL2SI

**Generated** : 2026-10-01T21:49:54.254898+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €26.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €26.64 (+2.3% vs entrée) · entrée €26.05 · stop €24.29 · T1 €28.00 · R/R 1.11  
> ↳ ¼-Kelly 0.035 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €25.80–€26.30 (mid €26.05)
- Spot actuel : €26.64 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : €24.29 (plancher anti-bruit (R/R<2) ; -6.76 % depuis l'entree)
- Targets : T1 €28.00 · R/R 1.11 | T2 €29.97 · R/R 2.23 | T3 €31.93 · R/R 3.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.29


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.81 %)** : le gap seul le franchit 0.703 % des séances (9 fois sur 1280).
   - exécution **6.476 pt plus bas** dans le cas TYPIQUE (médiane), 20.546 au p90, **29.307 au pire**
   - perte réelle **18.187 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 8.81 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0659 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5615** [0.4871 ; 0.6339] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4142** [0.3632 ; 0.4667] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.34** [0.2916 ; 0.3911] _(largeur 10.0 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.38 % contre 7.06 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2135** (β de hausse 0.9529, asymétrie 1.2736) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.895× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 25.5022 sur grid_snapped (0.35 ATR, 4.271 %) — p(stop avant cible) 0.7163 [0.67 ; 0.76], R/R 4.368, perte reelle 4.547 % (gap inclus), CVaR 8.218 %, EV 0.9784 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.1066 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.716, borne haute 0.762 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 8.22 % > budget 3.02 %
- Budget de queue : **3.02 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.206 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 43.2 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.35 ATR (stop 5.392 %) — p(stop avant cible) 0.6477 [0.60 ; 0.70], R/R 3.415, perte reelle 5.816 % (gap inclus), EV 1.076 % — **REFUSE**
      - refuse : p_stop_first 0.648, borne haute 0.697 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 10.88 % > budget 3.02 %
   - 🔴 support a 0.93 ATR (stop 9.254 %) — p(stop avant cible) 0.4132 [0.36 ; 0.47], R/R 1.879, perte reelle 10.571 % (gap inclus), EV 2.1848 % — **REFUSE**
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.13 % > budget 3.02 %
      - ⚠ support DETECTE a 0.61 ATR du spot — compartiment <1, mesure a 46.7 % de casse (IC clusterise [0.436 ; 0.499] sur 1172 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.3 ATR (stop 18.263 %) — p(stop avant cible) 0.1926 [0.15 ; 0.24], R/R 0.866, perte reelle 22.936 % (gap inclus), EV 1.9959 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.86 % > budget 3.02 %
   - 🟢 support a 3.72 ATR (stop 27.647 %) — p(stop avant cible) 0.0919 [0.06 ; 0.13], R/R 0.581, perte reelle 34.172 % (gap inclus), EV 2.2282 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.64 % > budget 3.02 %
   - ⚪ grid_snapped a 0.35 ATR (stop 4.271 %) — p(stop avant cible) 0.7163 [0.67 ; 0.76], R/R 4.368, perte reelle 4.547 % (gap inclus), EV 0.9784 % — **REFUSE**
      - refuse : p_stop_first 0.716, borne haute 0.762 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.22 % > budget 3.02 %
   - 🔴 grid_snapped a 0.93 ATR (stop 8.133 %) — p(stop avant cible) 0.4884 [0.44 ; 0.54], R/R 2.159, perte reelle 9.196 % (gap inclus), EV 1.7784 % — **REFUSE**
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.52 % > budget 3.02 %
   - ⚪ atr_grid a 1.75 ATR (stop 11.533 %) — p(stop avant cible) 0.3036 [0.26 ; 0.35], R/R 1.487, perte reelle 13.356 % (gap inclus), EV 2.8591 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.60 % > budget 3.02 %
   - ⚪ atr_grid a 2.0 ATR (stop 13.181 %) — p(stop avant cible) 0.2599 [0.22 ; 0.31], R/R 1.196, perte reelle 16.604 % (gap inclus), EV 2.5792 % — **REFUSE**
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.88 % > budget 3.02 %
   - 🟢 grid_snapped a 2.3 ATR (stop 17.142 %) — p(stop avant cible) 0.1991 [0.16 ; 0.24], R/R 0.927, perte reelle 21.426 % (gap inclus), EV 2.2315 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.80 % > budget 3.02 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.772 %) — p(stop avant cible) 0.1593 [0.12 ; 0.20], R/R 0.757, perte reelle 26.225 % (gap inclus), EV 2.0372 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.58 % > budget 3.02 %
   - 🟢 grid_snapped a 3.72 ATR (stop 26.527 %) — p(stop avant cible) 0.0925 [0.07 ; 0.13], R/R 0.591, perte reelle 33.622 % (gap inclus), EV 2.2713 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.63 % > budget 3.02 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.657 %) — p(stop avant cible) 0.0832 [0.06 ; 0.12], R/R 0.554, perte reelle 35.849 % (gap inclus), EV 2.2282 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.96 % > budget 3.02 %
   - ⚪ atr_grid a 5.0 ATR (stop 32.953 %) — p(stop avant cible) 0.0744 [0.05 ; 0.11], R/R 0.52, perte reelle 38.221 % (gap inclus), EV 2.197 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.79 % > budget 3.02 %
   - ⚪ atr_grid a 5.5 ATR (stop 36.248 %) — p(stop avant cible) 0.0522 [0.03 ; 0.08], R/R 0.475, perte reelle 41.811 % (gap inclus), EV 2.5557 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.06 % > budget 3.02 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.543 %) — p(stop avant cible) 0.0391 [0.02 ; 0.06], R/R 0.448, perte reelle 44.375 % (gap inclus), EV 2.6314 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.75 % > budget 3.02 %
   - ⚪ atr_grid a 6.5 ATR (stop 42.838 %) — p(stop avant cible) 0.0308 [0.02 ; 0.05], R/R 0.432, perte reelle 45.943 % (gap inclus), EV 2.8862 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.50 % > budget 3.02 %
   - ⚪ atr_grid a 7.0 ATR (stop 46.134 %) — p(stop avant cible) 0.0308 [0.02 ; 0.05], R/R 0.423, perte reelle 46.989 % (gap inclus), EV 2.854 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.14 % > budget 3.02 %
   - ⚪ atr_grid a 7.5 ATR (stop 49.429 %) — p(stop avant cible) 0.0308 [0.02 ; 0.05], R/R 0.391, perte reelle 50.806 % (gap inclus), EV 2.7365 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.50 % > budget 3.02 %
   - ⚪ atr_grid a 8.0 ATR (stop 52.724 %) — p(stop avant cible) 0.0308 [0.02 ; 0.05], R/R 0.328, perte reelle 60.466 % (gap inclus), EV 2.4389 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.46 % > budget 3.02 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 26.64, ATR14 1.7557 (6.591 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.398 ATR = 2.623 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.33 % | 26.5522 | 86.76 % | 90.38 % | 92.73 % | 94.19 % | 95.35 % | 96.9 % |
| 0.1 ATR | 0.659 % | 26.4644 | 82.16 % | 86.75 % | 89.98 % | 91.93 % | 93.87 % | 96.0 % |
| 0.15 ATR | 0.989 % | 26.3766 | 78.14 % | 83.02 % | 86.84 % | 88.68 % | 91.89 % | 94.81 % |
| 0.2 ATR | 1.318 % | 26.2889 | 72.35 % | 78.9 % | 83.01 % | 85.53 % | 89.52 % | 92.61 % |
| 0.25 ATR | 1.648 % | 26.2011 | 66.37 % | 74.29 % | 78.88 % | 82.19 % | 87.24 % | 91.01 % |
| 0.35 ATR | 2.307 % | 26.0255 | 54.51 % | 65.46 % | 70.73 % | 75.39 % | 82.29 % | 87.51 % |
| 0.5 ATR | 3.295 % | 25.7621 | 40.29 % | 53.58 % | 61.59 % | 68.41 % | 77.65 % | 85.01 % |
| 0.75 ATR | 4.943 % | 25.3232 | 22.35 % | 37.19 % | 47.05 % | 55.31 % | 66.77 % | 76.32 % |
| 1.0 ATR | 6.591 % | 24.8843 | 12.75 % | 24.73 % | 33.5 % | 43.9 % | 56.78 % | 67.83 % |
| 1.25 ATR | 8.238 % | 24.4454 | 7.45 % | 17.37 % | 24.36 % | 35.93 % | 49.75 % | 61.34 % |
| 1.5 ATR | 9.886 % | 24.0064 | 3.63 % | 11.19 % | 17.09 % | 28.25 % | 42.53 % | 54.85 % |
| 2.0 ATR | 13.181 % | 23.1286 | 0.88 % | 5.1 % | 9.53 % | 16.63 % | 30.96 % | 43.06 % |
| 2.5 ATR | 16.476 % | 22.2507 | 0.1 % | 2.16 % | 4.52 % | 9.74 % | 20.87 % | 33.07 % |
| 3.0 ATR | 19.772 % | 21.3729 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 14.94 % | 25.87 % |
| 4.0 ATR | 26.362 % | 19.6171 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.18 % |
| 6.0 ATR | 39.543 % | 16.1057 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.71 ATR | 0.81 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.16 ATR | 1.60 ATR | 2.02 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.01 ATR | 1.23 ATR | 1.40 ATR | 1.97 ATR | 2.45 ATR |
| **5 s.** | 0.36 ATR | 0.87 ATR | 0.98 ATR | 1.34 ATR | 1.64 ATR | 1.85 ATR | 2.48 ATR | 3.42 ATR |
| **10 s.** | 0.56 ATR | 1.24 ATR | 1.41 ATR | 1.91 ATR | 2.29 ATR | 2.57 ATR | 3.77 ATR | 5.11 ATR |
| **20 s.** | 0.79 ATR | 1.71 ATR | 1.92 ATR | 2.50 ATR | 3.10 ATR | 3.67 ATR | 5.56 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.45–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.295 %, prix 25.7622), p(touche) 40.29 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (89.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.631–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.943 %, prix 25.3232), p(touche) 37.19 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.788–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.591 %, prix 24.8842), p(touche) 33.5 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.976–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.591 %, prix 24.8842), p(touche) 43.9 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.414–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.886 %, prix 24.0064), p(touche) 42.53 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.918–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.181 %, prix 23.1286), p(touche) 43.06 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.168 | EV/share : €0.294 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 23 % | T3 12 %
- Kelly (position) : f* 0.141 | ¼-Kelly 0.035 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 80.8 | bear 14.2 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.003% → cible +3.329% / stop −1.997%, p_fill 80%, n_eff≈86.9) : P(cible|rempli) **31%** · **EV/risk -0.122** (×p_fill ; si rempli -0.30% du capital)
  - **swing** (entrée dip −2.22% → cible +7.504% / stop −6.74%, p_fill 68%, n_eff≈80.1) : P(cible|rempli) **43%** · **EV/risk -0.052** (×p_fill ; si rempli -0.51% du capital)
  - **deep** (entrée dip −3.424% → cible +12.808% / stop −10.236%, p_fill 69%, n_eff≈76.4) : P(cible|rempli) **40%** · **EV/risk -0.004** (×p_fill ; si rempli -0.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→76% · +2.0%→69% · +3.0%→54% · +5.0%→37% · +8.0%→18%
- Range intraday médian 7.09% (p90 14.96%) · excursion haute méd. +3.47% / basse méd. −3.27%
- Profil de vol intra : ouverture 4.903% vs midi 1.541% vs clôture 1.736% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 5% · trend ↑1%/↓0% ; spike-down 73% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.279% ; recovery-V 20%
- **σ réalisé intraday** 4.432% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 67% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 28.0577 (VA 27.9027–28.3522 ; dernier close 27.94)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 93% · **stop −3.81%** sous le fill (sous le bruit) · cible +2.18% · R/R 0.57 (high win-rate)
- Gaps overnight (n=158) : méd. 0.28% · baisse 41% (gap-down >1% 11% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −3.45%) · haut méd +0.73% · range méd 2.28%
- Excursion ouverture 15min (n=160) : bas méd −1.17% (p90 −4.11%) · haut méd +1.39% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −4.39%) · haut méd +1.93% · range méd 3.58%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −5.61%) · haut méd +2.05% · range méd 4.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.16 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 80% (122/158) · gap 21% · délai 0.3min · rebond 63% (81/122) (MFE +1.88%)
   - −1.0% : fill 30min 50% · séance 74% (116/158) · gap 11% · délai 3.2min · rebond 60% (77/116) (MFE +1.56%)
   - −1.5% : fill 30min 43% · séance 68% (103/158) · gap 7% · délai 7.0min · rebond 59% (64/103) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 62% (95/158) · gap 5% · délai 13.6min · rebond 54% (57/95) (MFE +1.11%)
   - −3.0% : fill 30min 20% · séance 44% (77/158) · gap 2% · délai 37.6min · rebond 55% (51/77) (MFE +1.4%)
   - −4.0% : fill 30min 13% · séance 37% (66/158) · gap 1% · délai 65.6min · rebond 70% (52/66) (MFE +1.57%)
   - −5.0% : fill 30min 9% · séance 25% (51/158) · gap 1% · délai 58.4min · rebond 93% (48/51) (MFE +2.18%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −3.1%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −3.86%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −3.92%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1482 jambes) : jambe baissière méd −1.2% (p90 −2.96%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 91% (45/47) · rebond 54% (26/45)
      · −2.0% : fill 84% (41/47) · rebond 49% (22/41)
      · −3.0% : fill 69% (37/47) · rebond 50% (25/37)
      · −4.0% : fill 61% (33/47) · rebond 58% (24/33)
      · −5.0% : fill 44% (27/47) · rebond 86% (24/27)
   - **flat** (32 séances) :
      · −1.0% : fill 75% (24/32) · rebond 69% (17/24)
      · −2.0% : fill 52% (18/32) · rebond 49% (11/18)
      · −3.0% : fill 35% (14/32) · rebond 43% (8/14)
      · −4.0% : fill 31% (13/32) · rebond 66% (10/13)
      · −5.0% : fill 22% (9/32) · rebond 100% (9/9)
   - **gap-up** (79 séances) :
      · −1.0% : fill 64% (47/79) · rebond 60% (34/47)
      · −2.0% : fill 54% (36/79) · rebond 62% (24/36)
      · −3.0% : fill 34% (26/79) · rebond 67% (18/26)
      · −4.0% : fill 26% (20/79) · rebond 88% (18/20)
      · −5.0% : fill 16% (15/79) · rebond 100% (15/15)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 54% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:02** → P(séance verte=clôture>ouverture) 73% si début vert vs 13% si rouge (base 41% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 44% ; creux résiduel méd -2.43% (q20 -4.91%) → **SL/trailing à −4.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.1% / q75 +3.38% → **scale +2.1% / runner +3.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **13%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.97%** (au-delà de la MAE q10 -5.97%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.46% .. +5.28%] · haut q95 +6.86% · bas q05 -5.79%
   - 60min (n=160) : retour [-5.38% .. +4.99%] · haut q95 +7.41% · bas q05 -6.96%
   - 2h (n=160) : retour [-5.21% .. +7.21%] · haut q95 +9.11% · bas q05 -7.49%
   - 4h (n=160) : retour [-6.32% .. +7.44%] · haut q95 +9.97% · bas q05 -8.3%
   - 6h (n=160) : retour [-6.06% .. +8.24%] · haut q95 +11.4% · bas q05 -8.6%
   - session (n=160) : retour [-7.23% .. +9.92%] · haut q95 +12.71% · bas q05 -9.64%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.18 · part idiosyncratique 0.82
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.0  _(momentum baissier)_
- **ADX** : 20.3  _(pas de tendance nette)_
- **MACD** : hist -0.203  _(bearish_recent)_
- **BB** : %B 0.01 · largeur 14.8%
- **ATR** : 1.76 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.047  _(neutre)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 60.3  _(transition)_
- **MA** : MA20 28.7 · MA50 27.56 · MA200 28.15  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -3.3% · MA200 -5.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (840982 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
