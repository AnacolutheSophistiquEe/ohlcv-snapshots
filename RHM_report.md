# RHM

**Generated** : 2026-08-31T21:36:10.369658+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1110.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1110.80 (+9.7% vs entrée) · entrée €1012.74 · stop €973.22 · T1 €1038.38 · R/R 0.65  
> ↳ P(T1 av. stop) 63 % · EV/risk -0.013 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €1007.61–€1017.86 (mid €1012.74)
- Spot actuel : €1110.80 (+9.7% au-dessus de la zone — repli à attendre)
- Stop : €973.22 (stop swing_plan-based (-12.39%))
- Targets : T1 €1038.38 · R/R 0.65 | T2 €1064.03 · R/R 1.3 | T3 €1089.68 · R/R 1.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €973.22


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.39 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **10.039 pt plus bas** dans le cas TYPIQUE (médiane), 10.039 au p90, **10.039 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 12.39 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0079 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3192** [0.2532 ; 0.3912] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.3802** [0.3302 ; 0.4322] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3616** [0.3123 ; 0.4132] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.86 %** | CVaR **-6.73 %** | vol 2.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.98 % contre 3.27 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.61 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.847 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5014** (β de hausse 0.5828, asymétrie 0.8603) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.124× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 992.2572 sur atr_grid (3.0 ATR, 10.672 %) — p(stop avant cible) 0.255 [0.21 ; 0.30], R/R 1.699, perte reelle 22.429 % (gap inclus), CVaR 10.681 %, EV -3.232 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.33 ATR (stop 3.044 %) — p(stop avant cible) 0.7299 [0.68 ; 0.77], R/R 7.492, perte reelle 5.085 % (gap inclus), EV -1.3466 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.730, borne haute 0.775 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 0.1 % x 38.10 % + P(rien) 26.9 % x 8.68 % ne couvrent pas P(stop) 73.0 % x 5.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.336 %) — p(stop avant cible) 0.5618 [0.51 ; 0.61], R/R 3.145, perte reelle 12.114 % (gap inclus), EV -3.8462 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.562, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.85 %) : P(cible) 0.1 % x 38.10 % + P(rien) 43.8 % x 6.70 % ne couvrent pas P(stop) 56.2 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.61 ATR (stop 18.249 %) — p(stop avant cible) 0.0733 [0.05 ; 0.10], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -0.7123 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 0.1 % x 38.10 % + P(rien) 92.5 % x 0.95 % ne couvrent pas P(stop) 7.3 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.33 ATR (stop 2.247 %) — p(stop avant cible) 0.8114 [0.77 ; 0.85], R/R 9.379, perte reelle 4.062 % (gap inclus), EV -1.2509 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 9.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.811, borne haute 0.850 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.1 % x 38.10 % + P(rien) 18.8 % x 10.74 % ne couvrent pas P(stop) 81.1 % x 4.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.557 %) — p(stop avant cible) 0.6812 [0.63 ; 0.73], R/R 6.736, perte reelle 5.656 % (gap inclus), EV -1.2209 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.1 % x 38.10 % + P(rien) 31.8 % x 8.19 % ne couvrent pas P(stop) 68.1 % x 5.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.447 %) — p(stop avant cible) 0.617 [0.56 ; 0.67], R/R 4.849, perte reelle 7.856 % (gap inclus), EV -1.947 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 0.1 % x 38.10 % + P(rien) 38.2 % x 7.51 % ne couvrent pas P(stop) 61.7 % x 7.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.225 %) — p(stop avant cible) 0.497 [0.44 ; 0.55], R/R 2.516, perte reelle 15.141 % (gap inclus), EV -4.4732 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.47 %) : P(cible) 0.1 % x 38.10 % + P(rien) 50.1 % x 5.97 % ne couvrent pas P(stop) 49.7 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.115 %) — p(stop avant cible) 0.4278 [0.38 ; 0.48], R/R 2.516, perte reelle 15.141 % (gap inclus), EV -3.4777 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.48 %) : P(cible) 0.1 % x 38.10 % + P(rien) 57.1 % x 5.16 % ne couvrent pas P(stop) 42.8 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.004 %) — p(stop avant cible) 0.3869 [0.34 ; 0.44], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -5.7428 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.74 %) : P(cible) 0.1 % x 38.10 % + P(rien) 61.2 % x 4.71 % ne couvrent pas P(stop) 38.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.893 %) — p(stop avant cible) 0.3436 [0.29 ; 0.39], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -4.8453 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.85 %) : P(cible) 0.1 % x 38.10 % + P(rien) 65.5 % x 4.28 % ne couvrent pas P(stop) 34.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.783 %) — p(stop avant cible) 0.2976 [0.25 ; 0.35], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -3.997 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.00 %) : P(cible) 0.1 % x 38.10 % + P(rien) 70.1 % x 3.74 % ne couvrent pas P(stop) 29.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.672 %) — p(stop avant cible) 0.255 [0.21 ; 0.30], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -3.232 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.23 %) : P(cible) 0.1 % x 38.10 % + P(rien) 74.4 % x 3.27 % ne couvrent pas P(stop) 25.5 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.45 %) — p(stop avant cible) 0.2045 [0.16 ; 0.25], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -2.3847 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.38 %) : P(cible) 0.1 % x 38.10 % + P(rien) 79.4 % x 2.70 % ne couvrent pas P(stop) 20.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 14.229 %) — p(stop avant cible) 0.139 [0.11 ; 0.18], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -1.4319 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.43 %) : P(cible) 0.1 % x 38.10 % + P(rien) 86.0 % x 1.89 % ne couvrent pas P(stop) 13.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.61 ATR (stop 17.452 %) — p(stop avant cible) 0.091 [0.06 ; 0.12], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -0.8757 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 0.1 % x 38.10 % + P(rien) 90.8 % x 1.22 % ne couvrent pas P(stop) 9.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 19.565 %) — p(stop avant cible) 0.058 [0.04 ; 0.09], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -0.5939 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.1 % x 38.10 % + P(rien) 94.0 % x 0.69 % ne couvrent pas P(stop) 5.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 21.344 %) — p(stop avant cible) 0.0369 [0.02 ; 0.06], R/R 1.699, perte reelle 22.429 % (gap inclus), EV -0.3923 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.1 % x 38.10 % + P(rien) 96.2 % x 0.39 % ne couvrent pas P(stop) 3.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 23.122 %) — p(stop avant cible) 0.0151 [0.01 ; 0.03], R/R 1.648, perte reelle 23.122 % (gap inclus), EV -0.2101 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.1 % x 38.10 % + P(rien) 98.3 % x 0.08 % ne couvrent pas P(stop) 1.5 % x 23.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 24.901 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 1.53, perte reelle 24.901 % (gap inclus), EV -0.1955 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.1 % x 38.10 % + P(rien) 99.2 % x -0.08 % ne couvrent pas P(stop) 0.7 % x 24.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 26.68 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 1.428, perte reelle 26.68 % (gap inclus), EV -0.1733 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.1 % x 38.10 % + P(rien) 99.2 % x -0.07 % ne couvrent pas P(stop) 0.6 % x 26.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 28.458 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 1.339, perte reelle 28.458 % (gap inclus), EV -0.1591 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.1 % x 38.10 % + P(rien) 99.3 % x -0.06 % ne couvrent pas P(stop) 0.5 % x 28.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1110.8, ATR14 39.5143 (3.557 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.391 ATR = 1.391 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.178 % | 1108.8243 | 89.25 % | 92.1 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.356 % | 1106.8486 | 83.23 % | 87.76 % | 89.72 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.534 % | 1104.8729 | 76.13 % | 82.82 % | 85.57 % | 88.22 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.711 % | 1102.8972 | 69.63 % | 78.38 % | 81.52 % | 85.15 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.889 % | 1100.9215 | 62.13 % | 72.56 % | 76.48 % | 80.99 % | 88.36 % | 91.36 % |
| 0.35 ATR | 1.245 % | 1096.97 | 53.65 % | 65.65 % | 70.95 % | 76.63 % | 85.77 % | 89.25 % |
| 0.5 ATR | 1.779 % | 1091.0429 | 40.14 % | 54.49 % | 61.26 % | 68.91 % | 80.1 % | 83.62 % |
| 0.75 ATR | 2.668 % | 1081.1643 | 23.47 % | 38.8 % | 46.84 % | 57.33 % | 70.25 % | 76.88 % |
| 1.0 ATR | 3.557 % | 1071.2858 | 12.92 % | 26.46 % | 35.97 % | 48.12 % | 62.09 % | 70.35 % |
| 1.25 ATR | 4.447 % | 1061.4072 | 7.4 % | 17.87 % | 26.19 % | 38.71 % | 53.83 % | 63.72 % |
| 1.5 ATR | 5.336 % | 1051.5286 | 3.94 % | 12.93 % | 20.45 % | 31.29 % | 45.57 % | 56.48 % |
| 2.0 ATR | 7.115 % | 1031.7715 | 1.78 % | 6.91 % | 11.96 % | 20.59 % | 33.83 % | 46.73 % |
| 2.5 ATR | 8.893 % | 1012.0143 | 0.49 % | 3.36 % | 6.23 % | 12.48 % | 24.68 % | 37.49 % |
| 3.0 ATR | 10.672 % | 992.2572 | 0.1 % | 1.38 % | 3.85 % | 7.52 % | 16.92 % | 30.85 % |
| 4.0 ATR | 14.229 % | 952.7429 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.46 % | 19.8 % |
| 6.0 ATR | 21.344 % | 873.7143 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.57 ATR | 0.65 ATR | 0.87 ATR | 1.04 ATR | 1.19 ATR | 1.74 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.69 ATR | 0.79 ATR | 1.08 ATR | 1.30 ATR | 1.53 ATR | 2.17 ATR | 2.76 ATR |
| **5 s.** | 0.38 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.79 ATR | 2.04 ATR | 2.75 ATR | 3.59 ATR |
| **10 s.** | 0.63 ATR | 1.37 ATR | 1.52 ATR | 2.04 ATR | 2.48 ATR | 2.80 ATR | 3.82 ATR | 4.90 ATR |
| **20 s.** | 0.82 ATR | 1.83 ATR | 2.09 ATR | 2.84 ATR | 3.53 ATR | 3.98 ATR | 5.20 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.446–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.651–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.668 %, prix 1081.1639), p(touche) 38.8 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.792–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.557 %, prix 1071.2889), p(touche) 35.97 % (en stress 95.1 %)  ✅ optimum identifie (67.2 % des re-echantillons)
- **5 seance(s)** : plage utile 1.083–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.447 %, prix 1061.4028), p(touche) 38.71 % (en stress 98.02 %)  ✅ optimum identifie (87.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.524–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.115 %, prix 1031.7666), p(touche) 33.83 % (en stress 96.04 %)  ✅ optimum identifie (99.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.094–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.893 %, prix 1012.0166), p(touche) 37.49 % (en stress 98.0 %)  ✅ optimum identifie (99.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : €-1.452 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 36 % | T3 23 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 75.2 | bear 18.4 | side 6.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.07% (p90 6.55%) · excursion haute méd. +2.05% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.607% vs midi 0.944% vs clôture 1.074% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. -0.139% ; recovery-V 25%
- **σ réalisé intraday** 2.561% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 56% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 1164.115 (VA 1161.985–1174.055 ; dernier close 1153.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 40% · rebond 64% · **stop −3.05%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.53% · baisse 29% (gap-down >1% 9% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.74%) · haut méd +0.49% · range méd 1.34%
- Excursion ouverture 15min (n=160) : bas méd −0.92% (p90 −1.97%) · haut méd +0.61% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.96% (p90 −2.16%) · haut méd +0.8% · range méd 1.98%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.57%) · haut méd +0.93% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1154.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 68% (105/159) · gap 20% · délai 1.0min · rebond 55% (57/105) (MFE +1.07%)
   - −1.0% : fill 30min 38% · séance 62% (93/159) · gap 9% · délai 6.3min · rebond 65% (57/93) (MFE +1.29%)
   - −1.5% : fill 30min 24% · séance 48% (77/159) · gap 6% · délai 29.8min · rebond 62% (45/77) (MFE +1.39%)
   - −2.0% : fill 30min 16% · séance 40% (64/159) · gap 4% · délai 54.5min · rebond 64% (40/64) (MFE +1.51%)
   - −3.0% : fill 30min 6% · séance 21% (32/159) · gap 3% · délai 151.5min · rebond 46% (16/32) (MFE +0.93%)
   - −4.0% : fill 30min 4% · séance 13% (23/159) · gap 2% · délai 174.9min · rebond 69% (14/23) (MFE +1.69%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −1.47%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.7%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.74%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=540 jambes) : jambe baissière méd −1.04% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (34 séances) :
      · −1.0% : fill 96% (33/34) · rebond 80% (25/33)
      · −2.0% : fill 76% (28/34) · rebond 66% (19/28)
      · −3.0% : fill 40% (13/34) · rebond 60% (8/13)
      · −4.0% : fill 34% (11/34) · rebond 72% (8/11)
      · −5.0% : fill 23% (7/34) · rebond 100% (7/7)
   - **flat** (19 séances) :
      · −1.0% : fill 82% (13/19) · rebond 68% (10/13)
      · −2.0% : fill 46% (7/19) · rebond 64% (5/7)
      · −3.0% : fill 20% (3/19) · rebond 0% (0/3)
      · −4.0% : fill 10% (2/19) · rebond 62% (1/2)
      · −5.0% : fill 10% (2/19) · rebond 62% (1/2)
   - **gap-up** (106 séances) :
      · −1.0% : fill 45% (47/106) · rebond 52% (22/47)
      · −2.0% : fill 26% (29/106) · rebond 61% (16/29)
      · −3.0% : fill 14% (16/106) · rebond 49% (8/16)
      · −4.0% : fill 7% (10/106) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/106) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 60% si les 15 1res min sont vertes (75 cas) · 35% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 66% si début vert vs 27% si rouge (base 46% · écart 39 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **66%** · continue >prix actuel 40% ; creux résiduel méd -1.25% (q20 -2.93%) → **SL/trailing à −2.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.27% / q75 +1.88% → **scale +1.27% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **27%** (continue à baisser 49%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.22%** (au-delà de la MAE q10 -4.22%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.21%] · haut q95 +3.63% · bas q05 -2.93%
   - 60min (n=160) : retour [-2.74% .. +3.19%] · haut q95 +4.31% · bas q05 -3.69%
   - 2h (n=160) : retour [-3.14% .. +2.96%] · haut q95 +4.36% · bas q05 -4.34%
   - 4h (n=160) : retour [-3.28% .. +3.12%] · haut q95 +4.85% · bas q05 -4.59%
   - 6h (n=160) : retour [-4.01% .. +3.24%] · haut q95 +4.89% · bas q05 -4.97%
   - session (n=160) : retour [-4.61% .. +3.66%] · haut q95 +5.02% · bas q05 -5.69%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist -8.24  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 10.6%
- **ATR** : 39.51 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.285  _(distribution)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 55.3  _(transition)_
- **MA** : MA20 1163.55 · MA50 1089.7 · MA200 1400.19  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 +1.9% · MA200 -20.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (790673 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
