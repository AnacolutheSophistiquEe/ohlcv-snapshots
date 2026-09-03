# SAF

**Generated** : 2026-09-03T21:42:26.653297+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €331.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €331.50 (+2.9% vs entrée) · entrée €322.11 · stop €315.67 · T1 €324.40 · R/R 0.36  
> ↳ P(T1 av. stop) 51 % · EV/risk -0.018 · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €321.65–€322.57 (mid €322.11)
- Spot actuel : €331.50 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €315.67 (stop swing_plan-based (-8.45%))
- Targets : T1 €324.40 · R/R 0.36 | T2 €326.69 · R/R 0.71 | T3 €328.98 · R/R 1.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €315.67


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.45 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.536 pt plus bas** dans le cas TYPIQUE (médiane), 1.536 au p90, **1.536 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.45 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0012 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1808** [0.129 ; 0.2432] _(largeur 11.4 pt, n_eff 173.1)_
   - swing : **0.3522** [0.3033 ; 0.4036] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.3179** [0.2705 ; 0.3683] _(largeur 9.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.07 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.24 % contre 2.48 % aujourd'hui, rapport 0.50)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3666** (β de hausse 1.3316, asymétrie 1.0263) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.257× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 298.4571 sur atr_grid (4.5 ATR, 9.968 %) — p(stop avant cible) 0.0829 [0.06 ; 0.12], R/R 0.905, perte reelle 9.986 % (gap inclus), CVaR 9.968 %, EV 1.0836 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.323 %) — p(stop avant cible) 0.4424 [0.39 ; 0.49], R/R 1.702, perte reelle 5.309 % (gap inclus), EV 0.1282 % — **REFUSE**
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 5.22 ATR (stop 12.887 %) — p(stop avant cible) 0.0433 [0.03 ; 0.07], R/R 0.701, perte reelle 12.887 % (gap inclus), EV 1.051 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.89 % > budget 12.00 %
   - 🟢 support a 9.78 ATR (stop 22.998 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.393, perte reelle 22.998 % (gap inclus), EV 1.0583 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.00 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.554 %) — p(stop avant cible) 0.8898 [0.85 ; 0.92], R/R 6.976, perte reelle 1.295 % (gap inclus), EV -0.4401 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.890, borne haute 0.919 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 5.1 % x 9.03 % + P(rien) 5.9 % x 4.25 % ne couvrent pas P(stop) 89.0 % x 1.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.108 %) — p(stop avant cible) 0.7796 [0.73 ; 0.82], R/R 4.652, perte reelle 1.942 % (gap inclus), EV -0.2624 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.780, borne haute 0.821 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 7.4 % x 9.03 % + P(rien) 14.7 % x 4.00 % ne couvrent pas P(stop) 78.0 % x 1.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.661 %) — p(stop avant cible) 0.6824 [0.63 ; 0.73], R/R 3.387, perte reelle 2.667 % (gap inclus), EV -0.0661 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.682, borne haute 0.730 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 10.6 % x 9.03 % + P(rien) 21.1 % x 3.76 % ne couvrent pas P(stop) 68.2 % x 2.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.215 %) — p(stop avant cible) 0.6048 [0.55 ; 0.66], R/R 2.521, perte reelle 3.583 % (gap inclus), EV -0.1361 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.605, borne haute 0.655 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 12.3 % x 9.03 % + P(rien) 27.3 % x 3.39 % ne couvrent pas P(stop) 60.5 % x 3.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.769 %) — p(stop avant cible) 0.513 [0.46 ; 0.57], R/R 2.042, perte reelle 4.424 % (gap inclus), EV 0.0372 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.513, borne haute 0.565 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 3.876 %) — p(stop avant cible) 0.3702 [0.32 ; 0.42], R/R 1.466, perte reelle 6.163 % (gap inclus), EV 0.3477 % — **REFUSE**
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.43 %) — p(stop avant cible) 0.3292 [0.28 ; 0.38], R/R 1.329, perte reelle 6.799 % (gap inclus), EV 0.3583 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.984 %) — p(stop avant cible) 0.2874 [0.24 ; 0.34], R/R 1.329, perte reelle 6.799 % (gap inclus), EV 0.7745 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.538 %) — p(stop avant cible) 0.2566 [0.21 ; 0.30], R/R 0.905, perte reelle 9.986 % (gap inclus), EV 0.1641 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 6.091 %) — p(stop avant cible) 0.2326 [0.19 ; 0.28], R/R 0.905, perte reelle 9.986 % (gap inclus), EV 0.3978 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.645 %) — p(stop avant cible) 0.1958 [0.16 ; 0.24], R/R 0.905, perte reelle 9.986 % (gap inclus), EV 0.5812 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.753 %) — p(stop avant cible) 0.139 [0.11 ; 0.18], R/R 0.905, perte reelle 9.986 % (gap inclus), EV 0.8961 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.86 %) — p(stop avant cible) 0.1108 [0.08 ; 0.15], R/R 0.905, perte reelle 9.986 % (gap inclus), EV 1.0238 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 9.968 %) — p(stop avant cible) 0.0829 [0.06 ; 0.12], R/R 0.905, perte reelle 9.986 % (gap inclus), EV 1.0836 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 5.22 ATR (stop 12.218 %) — p(stop avant cible) 0.0434 [0.03 ; 0.07], R/R 0.739, perte reelle 12.218 % (gap inclus), EV 1.0793 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.22 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 13.29 %) — p(stop avant cible) 0.0337 [0.02 ; 0.06], R/R 0.68, perte reelle 13.29 % (gap inclus), EV 1.0427 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.29 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.398 %) — p(stop avant cible) 0.0197 [0.01 ; 0.04], R/R 0.627, perte reelle 14.398 % (gap inclus), EV 1.0411 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 15.505 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.583, perte reelle 15.505 % (gap inclus), EV 1.0452 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.50 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 16.613 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 0.544, perte reelle 16.613 % (gap inclus), EV 1.0501 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.61 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 17.72 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.51, perte reelle 17.72 % (gap inclus), EV 1.0503 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.72 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 331.5, ATR14 7.3429 (2.215 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 0.766 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.111 % | 331.1329 | 89.12 % | 92.44 % | 93.61 % | 95.57 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.222 % | 330.7657 | 81.27 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.332 % | 330.3986 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.443 % | 330.0314 | 68.33 % | 78.12 % | 82.51 % | 85.24 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.554 % | 329.6643 | 61.27 % | 73.41 % | 78.88 % | 83.17 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.775 % | 328.93 | 49.51 % | 63.2 % | 69.65 % | 76.77 % | 82.69 % | 87.01 % |
| 0.5 ATR | 1.108 % | 327.8286 | 35.59 % | 51.82 % | 59.23 % | 68.5 % | 75.87 % | 81.32 % |
| 0.75 ATR | 1.661 % | 325.9929 | 20.59 % | 35.72 % | 43.12 % | 53.15 % | 63.2 % | 70.73 % |
| 1.0 ATR | 2.215 % | 324.1571 | 9.71 % | 23.75 % | 32.61 % | 41.93 % | 53.51 % | 61.24 % |
| 1.25 ATR | 2.769 % | 322.3214 | 4.31 % | 15.51 % | 24.17 % | 33.27 % | 46.19 % | 54.45 % |
| 1.5 ATR | 3.323 % | 320.4857 | 2.25 % | 10.11 % | 16.7 % | 25.2 % | 37.98 % | 46.45 % |
| 2.0 ATR | 4.43 % | 316.8143 | 0.98 % | 4.42 % | 7.56 % | 15.55 % | 27.0 % | 36.76 % |
| 2.5 ATR | 5.538 % | 313.1428 | 0.2 % | 1.47 % | 3.63 % | 9.06 % | 18.79 % | 27.97 % |
| 3.0 ATR | 6.645 % | 309.4714 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.56 % | 21.78 % |
| 4.0 ATR | 8.86 % | 302.1286 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.04 % | 11.09 % |
| 6.0 ATR | 13.29 % | 287.4428 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.1 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.11 ATR | 1.51 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.23 ATR | 1.39 ATR | 1.87 ATR | 2.33 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.26 ATR | 1.51 ATR | 1.77 ATR | 2.43 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.29 ATR | 1.73 ATR | 2.12 ATR | 2.43 ATR | 3.34 ATR | 4.02 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.21 ATR | 2.74 ATR | 3.17 ATR | 4.27 ATR | 5.52 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.661 %, prix 325.9938), p(touche) 35.72 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.721–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.661 %, prix 325.9938), p(touche) 43.12 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.932–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.215 %, prix 324.1573), p(touche) 41.93 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.286–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.323 %, prix 320.4843), p(touche) 37.98 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.575–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.43 %, prix 316.8145), p(touche) 36.76 % (en stress 99.01 %)  ✅ optimum identifie (61.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.018 | EV/share : €-0.119 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 43 % | T3 25 %
- Kelly (position) : f* 0.056 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 29.5 | bear 64.8 | side 5.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→51% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.52% (p90 3.72%) · excursion haute méd. +1.05% / basse méd. −0.86%
- Profil de vol intra : ouverture 1.472% vs midi 0.522% vs clôture 0.665% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 43% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.084)_ ; drift intra méd. -0.4% ; recovery-V 12%
- **σ réalisé intraday** 1.576% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 331.4575 (VA 330.5975–332.5325 ; dernier close 330.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 24% · rebond 36% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.32% · baisse 30% (gap-down >1% 2% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.71%) · haut méd +0.17% · range méd 0.9%
- Excursion ouverture 15min (n=160) : bas méd −0.5% (p90 −1.8%) · haut méd +0.31% · range méd 1.04%
- Excursion ouverture 30min (n=160) : bas méd −0.5% (p90 −1.81%) · haut méd +0.44% · range méd 1.28%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.85%) · haut méd +0.52% · range méd 1.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 331.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 60% (86/159) · gap 9% · délai 0.4min · rebond 34% (33/86) (MFE +0.79%)
   - −1.0% : fill 30min 27% · séance 51% (72/159) · gap 2% · délai 25.5min · rebond 42% (33/72) (MFE +0.78%)
   - −1.5% : fill 30min 12% · séance 31% (46/159) · gap 1% · délai 70.2min · rebond 31% (19/46) (MFE +0.53%)
   - −2.0% : fill 30min 5% · séance 24% (38/159) · gap 0% · délai 247.8min · rebond 36% (17/38) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.65% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.12% (p90 −0.77%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=212 jambes) : jambe baissière méd −1.04% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (21 séances) :
      · −1.0% : fill 85% (18/21) · rebond 29% (7/18)
      · −2.0% : fill 53% (12/21) · rebond 42% (6/12)
      · −3.0% : fill 18% (5/21) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/21) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/21) · rebond 0% (0/0)
   - **flat** (36 séances) :
      · −1.0% : fill 55% (20/36) · rebond 40% (10/20)
      · −2.0% : fill 29% (9/36) · rebond 12% (1/9)
      · −3.0% : fill 6% (3/36) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/36) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (102 séances) :
      · −1.0% : fill 39% (34/102) · rebond 53% (16/34)
      · −2.0% : fill 13% (17/102) · rebond 60% (10/17)
      · −3.0% : fill 5% (6/102) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/102) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/102) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 67% si les 15 1res min sont vertes (72 cas) · 24% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 75% si début vert vs 19% si rouge (base 45% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 288min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **75%** · continue >prix actuel 54% ; creux résiduel méd -0.7% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.47% → **scale +0.97% / runner +1.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **19%** (continue à baisser 62%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.3%** (au-delà de la MAE q10 -2.3%), cible rebond +0.73% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.5% .. +1.55%] · haut q95 +1.95% · bas q05 -2.09%
   - 60min (n=160) : retour [-1.63% .. +1.99%] · haut q95 +2.02% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.35% .. +2.14%] · haut q95 +2.51% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.87% .. +2.17%] · haut q95 +2.73% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.09% .. +2.33%] · haut q95 +2.79% · bas q05 -3.03%
   - session (n=160) : retour [-2.7% .. +2.41%] · haut q95 +3.35% · bas q05 -3.88%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.3  _(survente)_
- **ADX** : 16.6  _(pas de tendance nette)_
- **MACD** : hist -3.07  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 12.9%
- **ATR** : 7.34 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.289  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 38.8  _(transition)_
- **MA** : MA20 348.25 · MA50 342.83 · MA200 311.0  _(prix < MA20)_
- **Dist MA** : MA20 -4.8% · MA50 -3.3% · MA200 +6.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (754984 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
