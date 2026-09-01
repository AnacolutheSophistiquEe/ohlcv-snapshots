# SAF

**Generated** : 2026-09-01T00:08:01.782920+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €336.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €336.20 (+7.6% vs entrée) · entrée €312.49 · stop €305.11 · T1 €317.58 · R/R 0.69  
> ↳ P(T1 av. stop) 58 % · EV/risk -0.01 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €311.47–€313.51 (mid €312.49)
- Spot actuel : €336.20 (+7.6% au-dessus de la zone — repli à attendre)
- Stop : €305.11 (stop swing_plan-based (-9.25%))
- Targets : T1 €317.58 · R/R 0.69 | T2 €322.68 · R/R 1.38 | T3 €327.78 · R/R 2.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €305.11


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (9.25 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **0.736 pt plus bas** dans le cas TYPIQUE (médiane), 0.736 au p90, **0.736 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 9.25 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0006 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1651** [0.1156 ; 0.2257] _(largeur 11.0 pt, n_eff 173.1)_
   - swing : **0.3594** [0.3102 ; 0.411] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.3094** [0.2624 ; 0.3596] _(largeur 9.7 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.06 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.25 % contre 2.49 % aujourd'hui, rapport 0.50)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3701** (β de hausse 1.3365, asymétrie 1.0251) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.255× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 302.9964 sur atr_grid (4.5 ATR, 9.876 %) — p(stop avant cible) 0.0876 [0.06 ; 0.12], R/R 0.752, perte reelle 9.986 % (gap inclus), CVaR 9.876 %, EV 1.0114 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.292 %) — p(stop avant cible) 0.442 [0.39 ; 0.49], R/R 1.561, perte reelle 4.809 % (gap inclus), EV 0.2354 % — **REFUSE**
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 5.94 ATR (stop 14.378 %) — p(stop avant cible) 0.0201 [0.01 ; 0.04], R/R 0.522, perte reelle 14.378 % (gap inclus), EV 0.9759 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.38 % > budget 12.00 %
   - 🟢 support a 10.37 ATR (stop 24.094 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.312, perte reelle 24.094 % (gap inclus), EV 0.9992 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.09 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.549 %) — p(stop avant cible) 0.8879 [0.85 ; 0.92], R/R 5.814, perte reelle 1.291 % (gap inclus), EV -0.4776 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 6.5 % x 7.51 % + P(rien) 4.7 % x 3.82 % ne couvrent pas P(stop) 88.8 % x 1.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.097 %) — p(stop avant cible) 0.7752 [0.73 ; 0.82], R/R 3.865, perte reelle 1.942 % (gap inclus), EV -0.2767 % — **REFUSE**
      - refuse : cible atteinte seulement 11.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.775, borne haute 0.817 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 11.1 % x 7.51 % + P(rien) 11.3 % x 3.46 % ne couvrent pas P(stop) 77.5 % x 1.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.646 %) — p(stop avant cible) 0.6794 [0.63 ; 0.73], R/R 2.921, perte reelle 2.57 % (gap inclus), EV -0.0401 % — **REFUSE**
      - refuse : p_stop_first 0.679, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 15.8 % x 7.51 % + P(rien) 16.3 % x 3.21 % ne couvrent pas P(stop) 67.9 % x 2.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.195 %) — p(stop avant cible) 0.5972 [0.54 ; 0.65], R/R 2.141, perte reelle 3.506 % (gap inclus), EV -0.1133 % — **REFUSE**
      - refuse : p_stop_first 0.597, borne haute 0.648 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 18.3 % x 7.51 % + P(rien) 22.0 % x 2.77 % ne couvrent pas P(stop) 59.7 % x 3.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.743 %) — p(stop avant cible) 0.5093 [0.46 ; 0.56], R/R 1.697, perte reelle 4.424 % (gap inclus), EV -0.0216 % — **REFUSE**
      - refuse : p_stop_first 0.509, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 20.9 % x 7.51 % + P(rien) 28.1 % x 2.35 % ne couvrent pas P(stop) 50.9 % x 4.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.841 %) — p(stop avant cible) 0.3629 [0.31 ; 0.41], R/R 1.218, perte reelle 6.163 % (gap inclus), EV 0.2579 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.389 %) — p(stop avant cible) 0.3211 [0.27 ; 0.37], R/R 1.104, perte reelle 6.799 % (gap inclus), EV 0.3012 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.938 %) — p(stop avant cible) 0.278 [0.23 ; 0.33], R/R 1.104, perte reelle 6.799 % (gap inclus), EV 0.7112 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.487 %) — p(stop avant cible) 0.248 [0.20 ; 0.30], R/R 0.752, perte reelle 9.986 % (gap inclus), EV 0.0877 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 6.035 %) — p(stop avant cible) 0.225 [0.18 ; 0.27], R/R 0.752, perte reelle 9.986 % (gap inclus), EV 0.366 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.584 %) — p(stop avant cible) 0.1934 [0.15 ; 0.24], R/R 0.752, perte reelle 9.986 % (gap inclus), EV 0.5283 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.681 %) — p(stop avant cible) 0.1415 [0.11 ; 0.18], R/R 0.752, perte reelle 9.986 % (gap inclus), EV 0.8282 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.779 %) — p(stop avant cible) 0.1166 [0.09 ; 0.15], R/R 0.752, perte reelle 9.986 % (gap inclus), EV 0.9363 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 9.876 %) — p(stop avant cible) 0.0876 [0.06 ; 0.12], R/R 0.752, perte reelle 9.986 % (gap inclus), EV 1.0114 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 10.973 %) — p(stop avant cible) 0.0693 [0.05 ; 0.10], R/R 0.684, perte reelle 10.973 % (gap inclus), EV 1.0036 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 12.071 %) — p(stop avant cible) 0.0506 [0.03 ; 0.08], R/R 0.622, perte reelle 12.071 % (gap inclus), EV 1.0001 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.07 % > budget 12.00 %
   - ⚪ grid_snapped a 5.94 ATR (stop 13.702 %) — p(stop avant cible) 0.0308 [0.02 ; 0.05], R/R 0.548, perte reelle 13.702 % (gap inclus), EV 0.9704 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.70 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 15.363 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 0.489, perte reelle 15.363 % (gap inclus), EV 0.9814 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.36 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 16.46 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 0.456, perte reelle 16.46 % (gap inclus), EV 0.9871 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.46 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 17.558 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 0.427, perte reelle 17.558 % (gap inclus), EV 0.9793 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.56 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 336.2, ATR14 7.3786 (2.195 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 0.757 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.11 % | 335.8311 | 89.12 % | 92.44 % | 93.61 % | 95.57 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.219 % | 335.4622 | 81.27 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.329 % | 335.0932 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.439 % | 334.7243 | 68.24 % | 78.12 % | 82.51 % | 85.24 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.549 % | 334.3554 | 61.27 % | 73.41 % | 78.88 % | 83.17 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.768 % | 333.6175 | 49.41 % | 63.0 % | 69.45 % | 76.57 % | 82.59 % | 87.01 % |
| 0.5 ATR | 1.097 % | 332.5107 | 35.49 % | 51.62 % | 59.04 % | 68.31 % | 75.77 % | 81.32 % |
| 0.75 ATR | 1.646 % | 330.6661 | 20.49 % | 35.53 % | 42.93 % | 52.95 % | 63.11 % | 70.73 % |
| 1.0 ATR | 2.195 % | 328.8214 | 9.71 % | 23.65 % | 32.42 % | 41.73 % | 53.31 % | 61.24 % |
| 1.25 ATR | 2.743 % | 326.9768 | 4.31 % | 15.31 % | 23.87 % | 33.07 % | 45.9 % | 54.45 % |
| 1.5 ATR | 3.292 % | 325.1321 | 2.25 % | 9.91 % | 16.4 % | 25.0 % | 37.69 % | 46.45 % |
| 2.0 ATR | 4.389 % | 321.4429 | 0.98 % | 4.42 % | 7.37 % | 15.35 % | 26.71 % | 36.76 % |
| 2.5 ATR | 5.487 % | 317.7536 | 0.2 % | 1.47 % | 3.54 % | 8.96 % | 18.5 % | 28.07 % |
| 3.0 ATR | 6.584 % | 314.0643 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.36 % | 21.88 % |
| 4.0 ATR | 8.779 % | 306.6857 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.04 % | 11.39 % |
| 6.0 ATR | 13.168 % | 291.9286 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.1 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.22 ATR | 1.38 ATR | 1.85 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.25 ATR | 1.50 ATR | 1.76 ATR | 2.42 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.11 ATR | 1.28 ATR | 1.71 ATR | 2.10 ATR | 2.41 ATR | 3.32 ATR | 4.02 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.22 ATR | 2.75 ATR | 3.18 ATR | 4.33 ATR | 5.54 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.646 %, prix 330.6662), p(touche) 35.53 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.718–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.646 %, prix 330.6662), p(touche) 42.93 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.927–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.195 %, prix 328.8204), p(touche) 41.73 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.277–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.292 %, prix 325.1323), p(touche) 37.69 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.575–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.389 %, prix 321.4442), p(touche) 36.76 % (en stress 100.0 %)  ✅ optimum identifie (65.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.01 | EV/share : €-0.074 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 35 % | T3 21 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 37.0 | bear 46.0 | side 17.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→51% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.45% (p90 3.72%) · excursion haute méd. +1.05% / basse méd. −0.86%
- Profil de vol intra : ouverture 1.482% vs midi 0.529% vs clôture 0.672% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 17%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.086)_ ; drift intra méd. -0.223% ; recovery-V 14%
- **σ réalisé intraday** 1.569% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 56% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 346.2463 (VA 346.0013–347.2262 ; dernier close 343.35)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 21% · rebond 42% · **stop −1.37%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.33% · baisse 30% (gap-down >1% 2% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.49%) · haut méd +0.19% · range méd 0.89%
- Excursion ouverture 15min (n=160) : bas méd −0.46% (p90 −1.7%) · haut méd +0.32% · range méd 1.04%
- Excursion ouverture 30min (n=160) : bas méd −0.47% (p90 −1.71%) · haut méd +0.45% · range méd 1.28%
- Excursion ouverture 60min (n=160) : bas méd −0.62% (p90 −1.87%) · haut méd +0.54% · range méd 1.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 344.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 43% · séance 58% (85/159) · gap 9% · délai 0.4min · rebond 37% (34/85) (MFE +0.84%)
   - −1.0% : fill 30min 26% · séance 49% (70/159) · gap 2% · délai 25.6min · rebond 46% (33/70) (MFE +0.87%)
   - −1.5% : fill 30min 10% · séance 28% (44/159) · gap 1% · délai 70.9min · rebond 35% (19/44) (MFE +0.53%)
   - −2.0% : fill 30min 5% · séance 21% (36/159) · gap 0% · délai 249.7min · rebond 42% (17/36) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 8% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.65% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.12% (p90 −0.77%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=210 jambes) : jambe baissière méd −1.03% (p90 −2.27%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (21 séances) :
      · −1.0% : fill 85% (18/21) · rebond 29% (7/18)
      · −2.0% : fill 53% (12/21) · rebond 42% (6/12)
      · −3.0% : fill 18% (5/21) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/21) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/21) · rebond 0% (0/0)
   - **flat** (35 séances) :
      · −1.0% : fill 49% (18/35) · rebond 50% (10/18)
      · −2.0% : fill 20% (7/35) · rebond 20% (1/7)
      · −3.0% : fill 7% (3/35) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/35) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (103 séances) :
      · −1.0% : fill 38% (34/103) · rebond 53% (16/34)
      · −2.0% : fill 13% (17/103) · rebond 60% (10/17)
      · −3.0% : fill 5% (6/103) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/103) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/103) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 67% si les 15 1res min sont vertes (73 cas) · 26% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 74% si début vert vs 20% si rouge (base 46% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 288min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **74%** · continue >prix actuel 54% ; creux résiduel méd -0.71% (q20 -1.45%) → **SL/trailing à −1.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.96% / q75 +1.47% → **scale +0.96% / runner +1.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **20%** (continue à baisser 59%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.3%** (au-delà de la MAE q10 -2.3%), cible rebond +0.83% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.5% .. +1.56%] · haut q95 +1.96% · bas q05 -2.12%
   - 60min (n=160) : retour [-1.64% .. +2.07%] · haut q95 +2.06% · bas q05 -2.38%
   - 2h (n=160) : retour [-1.89% .. +2.14%] · haut q95 +2.52% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.81% .. +2.18%] · haut q95 +2.74% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.11% .. +2.34%] · haut q95 +2.84% · bas q05 -3.03%
   - session (n=160) : retour [-2.71% .. +2.43%] · haut q95 +3.36% · bas q05 -3.94%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 1.25/2 | R/R T1 : 2.0 | extension : stretched_down
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

- **RSI** : 28.4  _(survente)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist -2.519  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 9.7%
- **ATR** : 7.38 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.254  _(distribution)_
- **Vol ratio** : 0.26  _(volume atone)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 352.13 · MA50 343.24 · MA200 310.51  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 -2.1% · MA200 +8.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (777487 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
