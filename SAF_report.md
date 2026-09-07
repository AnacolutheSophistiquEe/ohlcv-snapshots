# SAF

**Generated** : 2026-09-07T21:48:29.924903+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €333.10  

> 🟡 **WAIT-FOR-DIP** — spot +3.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €333.10 (+3.0% vs entrée) · entrée €323.31 · stop €316.84 · T1 €325.46 · R/R 0.33  
> ↳ P(T1 av. stop) 52 % · EV/risk 0.004 · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €322.88–€323.74 (mid €323.31)
- Spot actuel : €333.10 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : €316.84 (stop swing_plan-based (-8.59%))
- Targets : T1 €325.46 · R/R 0.33 | T2 €327.61 · R/R 0.66 | T3 €329.77 · R/R 1.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €316.84


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.59 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.396 pt plus bas** dans le cas TYPIQUE (médiane), 1.396 au p90, **1.396 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0011 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1712** [0.1208 ; 0.2325] _(largeur 11.2 pt, n_eff 173.1)_
   - swing : **0.3674** [0.3179 ; 0.4191] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.3186** [0.2712 ; 0.3691] _(largeur 9.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.06 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.29 % contre 2.48 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3693** (β de hausse 1.3325, asymétrie 1.0276) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.26× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 297.6714 sur atr_grid (5.0 ATR, 10.636 %) — p(stop avant cible) 0.0704 [0.05 ; 0.10], R/R 0.802, perte reelle 10.636 % (gap inclus), CVaR 10.636 %, EV 0.9916 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.191 %) — p(stop avant cible) 0.4644 [0.41 ; 0.52], R/R 1.774, perte reelle 4.809 % (gap inclus), EV 0.1507 % — **REFUSE**
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 5.63 ATR (stop 13.353 %) — p(stop avant cible) 0.0333 [0.02 ; 0.06], R/R 0.639, perte reelle 13.353 % (gap inclus), EV 0.949 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.35 % > budget 12.00 %
   - 🟢 support a 10.36 ATR (stop 23.423 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.364, perte reelle 23.423 % (gap inclus), EV 0.9695 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.42 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.532 %) — p(stop avant cible) 0.8911 [0.85 ; 0.92], R/R 6.745, perte reelle 1.265 % (gap inclus), EV -0.4369 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.921 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 5.5 % x 8.53 % + P(rien) 5.4 % x 4.09 % ne couvrent pas P(stop) 89.1 % x 1.27 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.064 %) — p(stop avant cible) 0.7841 [0.74 ; 0.82], R/R 4.437, perte reelle 1.923 % (gap inclus), EV -0.2689 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.784, borne haute 0.825 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 8.6 % x 8.53 % + P(rien) 12.9 % x 3.87 % ne couvrent pas P(stop) 78.4 % x 1.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.595 %) — p(stop avant cible) 0.7016 [0.65 ; 0.75], R/R 3.377, perte reelle 2.527 % (gap inclus), EV -0.1168 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.702, borne haute 0.748 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 11.8 % x 8.53 % + P(rien) 18.1 % x 3.60 % ne couvrent pas P(stop) 70.2 % x 2.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.127 %) — p(stop avant cible) 0.6141 [0.56 ; 0.66], R/R 2.615, perte reelle 3.263 % (gap inclus), EV -0.0227 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.614, borne haute 0.664 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 13.5 % x 8.53 % + P(rien) 25.1 % x 3.31 % ne couvrent pas P(stop) 61.4 % x 3.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.659 %) — p(stop avant cible) 0.5329 [0.48 ; 0.58], R/R 1.929, perte reelle 4.424 % (gap inclus), EV -0.0989 % — **REFUSE**
      - refuse : p_stop_first 0.533, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 15.8 % x 8.53 % + P(rien) 30.9 % x 2.94 % ne couvrent pas P(stop) 53.3 % x 4.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.723 %) — p(stop avant cible) 0.3909 [0.34 ; 0.44], R/R 1.498, perte reelle 5.698 % (gap inclus), EV 0.2738 % — **REFUSE**
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.254 %) — p(stop avant cible) 0.3443 [0.30 ; 0.40], R/R 1.385, perte reelle 6.163 % (gap inclus), EV 0.4151 % — **REFUSE**
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.786 %) — p(stop avant cible) 0.3004 [0.25 ; 0.35], R/R 1.255, perte reelle 6.799 % (gap inclus), EV 0.5639 % — **REFUSE**
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.318 %) — p(stop avant cible) 0.2625 [0.22 ; 0.31], R/R 1.111, perte reelle 7.683 % (gap inclus), EV 0.5685 % — **REFUSE**
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 5.85 %) — p(stop avant cible) 0.2455 [0.20 ; 0.29], R/R 0.854, perte reelle 9.986 % (gap inclus), EV 0.1994 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.382 %) — p(stop avant cible) 0.2153 [0.17 ; 0.26], R/R 0.854, perte reelle 9.986 % (gap inclus), EV 0.3896 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.445 %) — p(stop avant cible) 0.1417 [0.11 ; 0.18], R/R 0.854, perte reelle 9.986 % (gap inclus), EV 0.7847 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.509 %) — p(stop avant cible) 0.1192 [0.09 ; 0.16], R/R 0.854, perte reelle 9.986 % (gap inclus), EV 0.8878 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 9.572 %) — p(stop avant cible) 0.0856 [0.06 ; 0.12], R/R 0.854, perte reelle 9.986 % (gap inclus), EV 0.9826 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 10.636 %) — p(stop avant cible) 0.0704 [0.05 ; 0.10], R/R 0.802, perte reelle 10.636 % (gap inclus), EV 0.9916 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 5.63 ATR (stop 12.608 %) — p(stop avant cible) 0.0428 [0.03 ; 0.07], R/R 0.677, perte reelle 12.608 % (gap inclus), EV 0.9711 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 13.827 %) — p(stop avant cible) 0.0299 [0.02 ; 0.05], R/R 0.617, perte reelle 13.827 % (gap inclus), EV 0.9399 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 14.89 %) — p(stop avant cible) 0.0161 [0.01 ; 0.03], R/R 0.573, perte reelle 14.89 % (gap inclus), EV 0.9428 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.89 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 15.954 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 0.535, perte reelle 15.954 % (gap inclus), EV 0.9501 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.95 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 17.018 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 0.501, perte reelle 17.018 % (gap inclus), EV 0.9557 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 333.1, ATR14 7.0857 (2.127 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 0.736 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.106 % | 332.7457 | 89.22 % | 92.54 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.213 % | 332.3914 | 81.47 % | 87.24 % | 89.19 % | 91.44 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.319 % | 332.0371 | 75.2 % | 83.32 % | 86.25 % | 88.68 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.425 % | 331.6829 | 68.43 % | 78.21 % | 82.61 % | 85.33 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.532 % | 331.3286 | 61.27 % | 73.41 % | 78.98 % | 83.27 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.745 % | 330.62 | 49.51 % | 63.3 % | 69.84 % | 76.97 % | 82.69 % | 87.01 % |
| 0.5 ATR | 1.064 % | 329.5571 | 35.59 % | 51.82 % | 59.33 % | 68.7 % | 75.87 % | 81.32 % |
| 0.75 ATR | 1.595 % | 327.7857 | 20.59 % | 35.72 % | 43.22 % | 53.35 % | 63.2 % | 70.73 % |
| 1.0 ATR | 2.127 % | 326.0143 | 9.71 % | 23.75 % | 32.71 % | 42.13 % | 53.51 % | 61.24 % |
| 1.25 ATR | 2.659 % | 324.2429 | 4.31 % | 15.51 % | 24.17 % | 33.46 % | 46.19 % | 54.45 % |
| 1.5 ATR | 3.191 % | 322.4714 | 2.25 % | 10.11 % | 16.7 % | 25.39 % | 38.08 % | 46.45 % |
| 2.0 ATR | 4.254 % | 318.9286 | 0.98 % | 4.42 % | 7.56 % | 15.75 % | 27.1 % | 36.76 % |
| 2.5 ATR | 5.318 % | 315.3857 | 0.2 % | 1.47 % | 3.63 % | 9.15 % | 18.79 % | 27.97 % |
| 3.0 ATR | 6.382 % | 311.8429 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.56 % | 21.68 % |
| 4.0 ATR | 8.509 % | 304.7571 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.04 % | 10.89 % |
| 6.0 ATR | 12.763 % | 290.5857 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.1 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.11 ATR | 1.51 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.65 ATR | 0.72 ATR | 0.99 ATR | 1.23 ATR | 1.39 ATR | 1.87 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.82 ATR | 0.94 ATR | 1.26 ATR | 1.52 ATR | 1.78 ATR | 2.44 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.29 ATR | 1.73 ATR | 2.13 ATR | 2.43 ATR | 3.34 ATR | 4.02 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.21 ATR | 2.74 ATR | 3.16 ATR | 4.23 ATR | 5.51 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.595 %, prix 327.7871), p(touche) 35.72 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.722–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.595 %, prix 327.7871), p(touche) 43.22 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.936–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.127 %, prix 326.015), p(touche) 42.13 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.287–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.191 %, prix 322.4708), p(touche) 38.08 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.575–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.254 %, prix 318.9299), p(touche) 36.76 % (en stress 99.01 %)  ✅ optimum identifie (60.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.004 | EV/share : €0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 44 % | T3 28 %
- Kelly (position) : f* 0.066 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.7 | bear 9.0 | side 85.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→52% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.45% (p90 3.72%) · excursion haute méd. +1.09% / basse méd. −0.77%
- Profil de vol intra : ouverture 1.461% vs midi 0.5% vs clôture 0.665% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.3% ; recovery-V 12%
- **σ réalisé intraday** 1.544% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 331.8075 (VA 331.3325–332.7575 ; dernier close 333.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 36% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 31% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.56%) · haut méd +0.18% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.48% (p90 −1.76%) · haut méd +0.31% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.49% (p90 −1.78%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.84%) · haut méd +0.53% · range méd 1.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 333.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 60% (86/159) · gap 10% · délai 0.4min · rebond 38% (34/86) (MFE +0.84%)
   - −1.0% : fill 30min 25% · séance 48% (71/159) · gap 1% · délai 25.1min · rebond 42% (33/71) (MFE +0.79%)
   - −1.5% : fill 30min 11% · séance 29% (45/159) · gap 1% · délai 67.5min · rebond 31% (19/45) (MFE +0.52%)
   - −2.0% : fill 30min 4% · séance 23% (37/159) · gap 0% · délai 240.5min · rebond 36% (16/37) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −0.77%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.77%) → stop au-delà de −0.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=205 jambes) : jambe baissière méd −1.05% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 76% (18/22) · rebond 29% (7/18)
      · −2.0% : fill 48% (12/22) · rebond 42% (6/12)
      · −3.0% : fill 16% (5/22) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/22) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **flat** (38 séances) :
      · −1.0% : fill 49% (20/38) · rebond 40% (10/20)
      · −2.0% : fill 26% (9/38) · rebond 12% (1/9)
      · −3.0% : fill 5% (3/38) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/38) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/38) · rebond 0% (0/0)
   - **gap-up** (99 séances) :
      · −1.0% : fill 39% (33/99) · rebond 53% (16/33)
      · −2.0% : fill 13% (16/99) · rebond 59% (9/16)
      · −3.0% : fill 5% (6/99) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/99) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/99) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 70% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -0.71% (q20 -1.34%) → **SL/trailing à −1.34%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.96% / q75 +1.45% → **scale +0.96% / runner +1.45%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.29%** (au-delà de la MAE q10 -2.29%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.54%] · haut q95 +1.94% · bas q05 -2.06%
   - 60min (n=160) : retour [-1.63% .. +1.81%] · haut q95 +1.99% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.32% .. +2.06%] · haut q95 +2.49% · bas q05 -2.92%
   - 4h (n=160) : retour [-1.87% .. +2.1%] · haut q95 +2.7% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.98%
   - session (n=160) : retour [-2.7% .. +2.39%] · haut q95 +3.33% · bas q05 -3.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.0  _(momentum baissier)_
- **ADX** : 17.1  _(pas de tendance nette)_
- **MACD** : hist -2.344  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 13.0%
- **ATR** : 7.09 (38.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.372  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 345.55 · MA50 342.78 · MA200 311.42  _(prix < MA20)_
- **Dist MA** : MA20 -3.6% · MA50 -2.8% · MA200 +7.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (755574 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
