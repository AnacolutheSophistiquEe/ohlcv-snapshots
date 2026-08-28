# SAF

**Generated** : 2026-08-28T00:08:07.475170+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €343.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €343.20 (+8.7% vs entrée) · entrée €315.64 · stop €308.22 · T1 €321.48 · R/R 0.79  
> ↳ P(T1 av. stop) 54 % · EV/risk -0.0 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €314.47–€316.80 (mid €315.64)
- Spot actuel : €343.20 (+8.7% au-dessus de la zone — repli à attendre)
- Stop : €308.22 (stop swing_plan-based (-10.19%))
- Targets : T1 €321.48 · R/R 0.79 | T2 €327.31 · R/R 1.57 | T3 €333.15 · R/R 2.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €308.22


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (10.19 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.405 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1638** [0.1144 ; 0.2243] _(largeur 11.0 pt, n_eff 173.1)_
   - swing : **0.3981** [0.3475 ; 0.4504] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3214** [0.2738 ; 0.372] _(largeur 9.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.06 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.30 % contre 2.49 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3698** (β de hausse 1.339, asymétrie 1.023) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.271× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 306.0928 sur atr_grid (5.0 ATR, 10.812 %) — p(stop avant cible) 0.0665 [0.04 ; 0.10], R/R 0.491, perte reelle 10.812 % (gap inclus), CVaR 10.812 %, EV 0.7766 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.78 ATR (stop 3.069 %) — p(stop avant cible) 0.4394 [0.39 ; 0.49], R/R 1.104, perte reelle 4.809 % (gap inclus), EV -0.0005 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 35.1 % x 5.31 % + P(rien) 21.0 % x 1.19 % ne couvrent pas P(stop) 43.9 % x 4.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 6.85 ATR (stop 16.202 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 0.328, perte reelle 16.202 % (gap inclus), EV 0.7277 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.20 % > budget 12.00 %
   - 🟢 support a 11.25 ATR (stop 25.719 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.206, perte reelle 25.719 % (gap inclus), EV 0.7571 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.72 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.541 %) — p(stop avant cible) 0.8726 [0.83 ; 0.90], R/R 4.136, perte reelle 1.284 % (gap inclus), EV -0.5009 % — **REFUSE**
      - refuse : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.873, borne haute 0.905 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 10.8 % x 5.31 % + P(rien) 1.9 % x 2.37 % ne couvrent pas P(stop) 87.3 % x 1.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.081 %) — p(stop avant cible) 0.7617 [0.71 ; 0.80], R/R 2.741, perte reelle 1.937 % (gap inclus), EV -0.3754 % — **REFUSE**
      - refuse : p_stop_first 0.762, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 18.8 % x 5.31 % + P(rien) 5.0 % x 2.00 % ne couvrent pas P(stop) 76.2 % x 1.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.78 ATR (stop 2.334 %) — p(stop avant cible) 0.5566 [0.50 ; 0.61], R/R 1.373, perte reelle 3.868 % (gap inclus), EV -0.3292 % — **REFUSE**
      - refuse : p_stop_first 0.557, borne haute 0.608 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 29.8 % x 5.31 % + P(rien) 14.5 % x 1.66 % ne couvrent pas P(stop) 55.7 % x 3.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.703 %) — p(stop avant cible) 0.497 [0.44 ; 0.55], R/R 1.2, perte reelle 4.424 % (gap inclus), EV -0.2548 % — **REFUSE**
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 31.8 % x 5.31 % + P(rien) 18.5 % x 1.38 % ne couvrent pas P(stop) 49.7 % x 4.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.784 %) — p(stop avant cible) 0.3516 [0.30 ; 0.40], R/R 0.932, perte reelle 5.698 % (gap inclus), EV 0.2146 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.325 %) — p(stop avant cible) 0.3055 [0.26 ; 0.36], R/R 0.781, perte reelle 6.799 % (gap inclus), EV 0.1309 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.865 %) — p(stop avant cible) 0.2704 [0.23 ; 0.32], R/R 0.781, perte reelle 6.799 % (gap inclus), EV 0.455 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.406 %) — p(stop avant cible) 0.2382 [0.20 ; 0.29], R/R 0.532, perte reelle 9.986 % (gap inclus), EV -0.1102 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 40.6 % x 5.31 % + P(rien) 35.6 % x 0.32 % ne couvrent pas P(stop) 23.8 % x 9.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 5.947 %) — p(stop avant cible) 0.2249 [0.18 ; 0.27], R/R 0.532, perte reelle 9.986 % (gap inclus), EV 0.0603 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.487 %) — p(stop avant cible) 0.1941 [0.16 ; 0.24], R/R 0.532, perte reelle 9.986 % (gap inclus), EV 0.2653 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.568 %) — p(stop avant cible) 0.1384 [0.11 ; 0.18], R/R 0.532, perte reelle 9.986 % (gap inclus), EV 0.5796 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.65 %) — p(stop avant cible) 0.1155 [0.09 ; 0.15], R/R 0.532, perte reelle 9.986 % (gap inclus), EV 0.678 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 9.731 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 0.532, perte reelle 9.986 % (gap inclus), EV 0.7704 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 10.812 %) — p(stop avant cible) 0.0665 [0.04 ; 0.10], R/R 0.491, perte reelle 10.812 % (gap inclus), EV 0.7766 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 11.893 %) — p(stop avant cible) 0.0541 [0.03 ; 0.08], R/R 0.446, perte reelle 11.893 % (gap inclus), EV 0.7495 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.0 ATR (stop 12.975 %) — p(stop avant cible) 0.0446 [0.03 ; 0.07], R/R 0.409, perte reelle 12.975 % (gap inclus), EV 0.735 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.97 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.056 %) — p(stop avant cible) 0.0241 [0.01 ; 0.04], R/R 0.378, perte reelle 14.056 % (gap inclus), EV 0.7258 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.06 % > budget 12.00 %
   - ⚪ grid_snapped a 6.85 ATR (stop 15.467 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 0.343, perte reelle 15.467 % (gap inclus), EV 0.735 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.47 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 17.299 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 0.307, perte reelle 17.299 % (gap inclus), EV 0.7355 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.30 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 343.2, ATR14 7.4214 (2.162 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 0.744 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.108 % | 342.8289 | 89.12 % | 92.44 % | 93.61 % | 95.57 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.216 % | 342.4579 | 81.27 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.324 % | 342.0868 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.432 % | 341.7157 | 68.24 % | 78.12 % | 82.61 % | 85.24 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.541 % | 341.3447 | 61.18 % | 73.41 % | 78.98 % | 83.17 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.757 % | 340.6025 | 49.31 % | 63.0 % | 69.55 % | 76.57 % | 82.59 % | 87.11 % |
| 0.5 ATR | 1.081 % | 339.4893 | 35.39 % | 51.62 % | 59.14 % | 68.41 % | 75.77 % | 81.42 % |
| 0.75 ATR | 1.622 % | 337.6339 | 20.49 % | 35.62 % | 43.12 % | 53.15 % | 63.11 % | 70.93 % |
| 1.0 ATR | 2.162 % | 335.7786 | 9.71 % | 23.75 % | 32.61 % | 41.93 % | 53.31 % | 61.44 % |
| 1.25 ATR | 2.703 % | 333.9232 | 4.31 % | 15.41 % | 24.07 % | 33.27 % | 45.9 % | 54.65 % |
| 1.5 ATR | 3.244 % | 332.0679 | 2.25 % | 10.01 % | 16.6 % | 25.2 % | 37.69 % | 46.65 % |
| 2.0 ATR | 4.325 % | 328.3571 | 0.98 % | 4.51 % | 7.56 % | 15.55 % | 26.71 % | 36.96 % |
| 2.5 ATR | 5.406 % | 324.6464 | 0.2 % | 1.47 % | 3.54 % | 8.96 % | 18.4 % | 28.27 % |
| 3.0 ATR | 6.487 % | 320.9357 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.36 % | 22.08 % |
| 4.0 ATR | 8.65 % | 313.5143 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.04 % | 11.59 % |
| 6.0 ATR | 12.975 % | 298.6714 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.2 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.81 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.96 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.26 ATR | 1.51 ATR | 1.77 ATR | 2.42 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.11 ATR | 1.28 ATR | 1.71 ATR | 2.10 ATR | 2.40 ATR | 3.32 ATR | 4.02 ATR |
| **20 s.** | 0.65 ATR | 1.40 ATR | 1.58 ATR | 2.23 ATR | 2.76 ATR | 3.20 ATR | 4.38 ATR | 5.57 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.622 %, prix 337.6333), p(touche) 35.62 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.721–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.622 %, prix 337.6333), p(touche) 43.12 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.932–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.162 %, prix 335.78), p(touche) 41.93 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.277–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.244 %, prix 332.0666), p(touche) 37.69 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.585–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.325 %, prix 328.3566), p(touche) 36.96 % (en stress 100.0 %)  ✅ optimum identifie (66.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.0 | EV/share : €-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 32 % | T3 18 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.5 | bear 9.3 | side 85.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 343.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→52% · +2.0%→28% · +3.0%→10% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.52% (p90 3.76%) · excursion haute méd. +1.09% / basse méd. −0.91%
- Profil de vol intra : ouverture 1.55% vs midi 0.565% vs clôture 0.698% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 43% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. -0.197% ; recovery-V 17%
- **σ réalisé intraday** 1.597% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 55% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 341.4488 (VA 341.1938–342.9787 ; dernier close 343.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 21% · rebond 46% · **stop −1.61%** sous le fill (sous le bruit) · cible +0.94% · R/R 0.58 (high win-rate)
- Gaps overnight (n=159) : méd. 0.35% · baisse 30% (gap-down >1% 2% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.42% (p90 −1.51%) · haut méd +0.17% · range méd 0.91%
- Excursion ouverture 15min (n=160) : bas méd −0.5% (p90 −1.83%) · haut méd +0.25% · range méd 1.09%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.89%) · haut méd +0.5% · range méd 1.28%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.92%) · haut méd +0.56% · range méd 1.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 343.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 43% · séance 60% (85/159) · gap 10% · délai 0.4min · rebond 39% (35/85) (MFE +0.84%)
   - −1.0% : fill 30min 28% · séance 50% (69/159) · gap 2% · délai 19.2min · rebond 49% (33/69) (MFE +0.93%)
   - −1.5% : fill 30min 11% · séance 28% (43/159) · gap 1% · délai 46.3min · rebond 38% (19/43) (MFE +0.65%)
   - −2.0% : fill 30min 5% · séance 21% (35/159) · gap 0% · délai 217.9min · rebond 46% (17/35) (MFE +0.94%)
   - −3.0% : fill 30min 1% · séance 8% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.12% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=211 jambes) : jambe baissière méd −1.03% (p90 −2.28%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (20 séances) :
      · −1.0% : fill 83% (17/20) · rebond 34% (7/17)
      · −2.0% : fill 60% (12/20) · rebond 42% (6/12)
      · −3.0% : fill 21% (5/20) · rebond 31% (2/5)
      · −4.0% : fill 8% (2/20) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/20) · rebond 0% (0/0)
   - **flat** (35 séances) :
      · −1.0% : fill 45% (17/35) · rebond 57% (10/17)
      · −2.0% : fill 14% (6/35) · rebond 30% (1/6)
      · −3.0% : fill 7% (3/35) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/35) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (104 séances) :
      · −1.0% : fill 42% (35/104) · rebond 52% (16/35)
      · −2.0% : fill 14% (17/104) · rebond 60% (10/17)
      · −3.0% : fill 5% (6/104) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/104) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/104) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 65% si les 15 1res min sont vertes (75 cas) · 29% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 47% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 288min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -0.74% (q20 -1.51%) → **SL/trailing à −1.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.75% / q75 +1.53% → **scale +0.75% / runner +1.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 50%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.33%** (au-delà de la MAE q10 -2.33%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.56% .. +1.57%] · haut q95 +1.97% · bas q05 -2.17%
   - 60min (n=160) : retour [-1.64% .. +2.12%] · haut q95 +2.19% · bas q05 -2.47%
   - 2h (n=160) : retour [-2.07% .. +2.15%] · haut q95 +2.56% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.88% .. +2.19%] · haut q95 +2.77% · bas q05 -3.01%
   - 6h (n=160) : retour [-2.15% .. +2.38%] · haut q95 +3.11% · bas q05 -3.08%
   - session (n=160) : retour [-2.77% .. +2.52%] · haut q95 +3.37% · bas q05 -3.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 37.6  _(momentum baissier)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist -2.297  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 9.3%
- **ATR** : 7.42 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 0.35  _(volume atone)_
- **Choppiness** : 50.2  _(transition)_
- **MA** : MA20 352.59 · MA50 342.85 · MA200 310.13  _(prix < MA20)_
- **Dist MA** : MA20 -2.7% · MA50 +0.1% · MA200 +10.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (834481 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
