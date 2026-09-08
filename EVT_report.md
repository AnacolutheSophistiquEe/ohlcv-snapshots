# EVT

**Generated** : 2026-09-08T21:43:04.985698+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.16  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €3.16 (+3.6% vs entrée) · entrée €3.05 · stop €2.81 · T1 €3.18 · R/R 0.54  
> ↳ P(T1 av. stop) 51 % · EV/risk -0.04 · ¼-Kelly 0.003 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.04–€3.06 (mid €3.05)
- Spot actuel : €3.16 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : €2.81 (stop swing_plan-based (-10.48%))
- Targets : T1 €3.18 · R/R 0.54 | T2 €3.19 · R/R 0.58 | T3 €3.20 · R/R 0.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €2.81


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.36 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.48 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1273).
   - exécution **7.237 pt plus bas** dans le cas TYPIQUE (médiane), 18.692 au p90, **21.933 au pire**
   - perte réelle **19.926 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 10.48 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0297 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.985 % | pire -32.413 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0211** [0.0068 ; 0.0511] _(largeur 4.4 pt, n_eff 173.1)_
   - swing : **0.4504** [0.3986 ; 0.5031] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4394** [0.3878 ; 0.492] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.89 %** | CVaR **-9.26 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 6.11 % contre 3.76 % aujourd'hui, rapport 1.63)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.165 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1216** (β de hausse 0.9465, asymétrie 1.185) vs GDAXI — 599 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.8583 sur atr_grid (2.75 ATR, 9.604 %) — p(stop avant cible) 0.3156 [0.27 ; 0.37], R/R 1.347, perte reelle 18.001 % (gap inclus), CVaR 9.637 %, EV -3.3238 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.6 ATR (stop 4.361 %) — p(stop avant cible) 0.6466 [0.60 ; 0.70], R/R 2.069, perte reelle 11.717 % (gap inclus), EV -4.8796 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.647, borne haute 0.696 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.88 %) : P(cible) 4.3 % x 24.24 % + P(rien) 31.1 % x 5.34 % ne couvrent pas P(stop) 64.7 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.237 %) — p(stop avant cible) 0.5781 [0.53 ; 0.63], R/R 2.069, perte reelle 11.717 % (gap inclus), EV -3.8161 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.578, borne haute 0.629 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.82 %) : P(cible) 5.1 % x 24.24 % + P(rien) 37.1 % x 4.67 % ne couvrent pas P(stop) 57.8 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.873 %) — p(stop avant cible) 0.9116 [0.88 ; 0.94], R/R 10.694, perte reelle 2.267 % (gap inclus), EV -1.0469 % — **REFUSE**
      - refuse : cible atteinte seulement 1.9 % du temps (< 15 %) meme a 10 seances : le R/R de 10.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.912, borne haute 0.938 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 1.9 % x 24.24 % + P(rien) 6.9 % x 8.06 % ne couvrent pas P(stop) 91.2 % x 2.27 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.6 ATR (stop 3.138 %) — p(stop avant cible) 0.7289 [0.68 ; 0.77], R/R 3.563, perte reelle 6.804 % (gap inclus), EV -2.6481 % — **REFUSE**
      - refuse : cible atteinte seulement 3.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.729, borne haute 0.774 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.65 %) : P(cible) 3.7 % x 24.24 % + P(rien) 23.4 % x 6.07 % ne couvrent pas P(stop) 72.9 % x 6.80 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.112 %) — p(stop avant cible) 0.5189 [0.47 ; 0.57], R/R 1.865, perte reelle 12.996 % (gap inclus), EV -3.7687 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.519, borne haute 0.571 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.77 %) : P(cible) 5.3 % x 24.24 % + P(rien) 42.8 % x 3.95 % ne couvrent pas P(stop) 51.9 % x 13.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.985 %) — p(stop avant cible) 0.4566 [0.40 ; 0.51], R/R 1.498, perte reelle 16.186 % (gap inclus), EV -4.5829 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.58 %) : P(cible) 5.3 % x 24.24 % + P(rien) 49.0 % x 3.11 % ne couvrent pas P(stop) 45.7 % x 16.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.858 %) — p(stop avant cible) 0.3995 [0.35 ; 0.45], R/R 1.347, perte reelle 18.001 % (gap inclus), EV -4.5338 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.53 %) : P(cible) 5.3 % x 24.24 % + P(rien) 54.8 % x 2.51 % ne couvrent pas P(stop) 40.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.731 %) — p(stop avant cible) 0.3659 [0.32 ; 0.42], R/R 1.347, perte reelle 18.001 % (gap inclus), EV -4.0381 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.04 %) : P(cible) 5.3 % x 24.24 % + P(rien) 58.1 % x 2.18 % ne couvrent pas P(stop) 36.6 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.604 %) — p(stop avant cible) 0.3156 [0.27 ; 0.37], R/R 1.347, perte reelle 18.001 % (gap inclus), EV -3.3238 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.32 %) : P(cible) 5.3 % x 24.24 % + P(rien) 63.1 % x 1.70 % ne couvrent pas P(stop) 31.6 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.477 %) — p(stop avant cible) 0.2929 [0.25 ; 0.34], R/R 1.217, perte reelle 19.926 % (gap inclus), EV -3.5989 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 5.3 % x 24.24 % + P(rien) 65.4 % x 1.46 % ne couvrent pas P(stop) 29.3 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.223 %) — p(stop avant cible) 0.2322 [0.19 ; 0.28], R/R 1.072, perte reelle 22.616 % (gap inclus), EV -3.4048 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.40 %) : P(cible) 5.4 % x 24.24 % + P(rien) 71.4 % x 0.76 % ne couvrent pas P(stop) 23.2 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.969 %) — p(stop avant cible) 0.174 [0.14 ; 0.22], R/R 0.897, perte reelle 27.012 % (gap inclus), EV -3.3097 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.31 %) : P(cible) 5.4 % x 24.24 % + P(rien) 77.2 % x 0.11 % ne couvrent pas P(stop) 17.4 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.716 %) — p(stop avant cible) 0.1438 [0.11 ; 0.18], R/R 0.897, perte reelle 27.012 % (gap inclus), EV -2.7499 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.75 %) : P(cible) 5.4 % x 24.24 % + P(rien) 80.2 % x -0.21 % ne couvrent pas P(stop) 14.4 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 17.462 %) — p(stop avant cible) 0.1259 [0.09 ; 0.16], R/R 0.897, perte reelle 27.012 % (gap inclus), EV -2.4037 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.40 %) : P(cible) 5.4 % x 24.24 % + P(rien) 82.0 % x -0.38 % ne couvrent pas P(stop) 12.6 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 19.208 %) — p(stop avant cible) 0.1086 [0.08 ; 0.14], R/R 0.897, perte reelle 27.012 % (gap inclus), EV -2.1404 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 5.4 % x 24.24 % + P(rien) 83.7 % x -0.62 % ne couvrent pas P(stop) 10.9 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 20.954 %) — p(stop avant cible) 0.101 [0.07 ; 0.14], R/R 0.897, perte reelle 27.012 % (gap inclus), EV -2.0355 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 5.4 % x 24.24 % + P(rien) 84.5 % x -0.73 % ne couvrent pas P(stop) 10.1 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 22.7 %) — p(stop avant cible) 0.0972 [0.07 ; 0.13], R/R 0.748, perte reelle 32.413 % (gap inclus), EV -2.5232 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.52 %) : P(cible) 5.4 % x 24.24 % + P(rien) 84.9 % x -0.81 % ne couvrent pas P(stop) 9.7 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 24.447 %) — p(stop avant cible) 0.0856 [0.06 ; 0.12], R/R 0.748, perte reelle 32.413 % (gap inclus), EV -2.3642 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.36 %) : P(cible) 5.4 % x 24.24 % + P(rien) 86.0 % x -1.05 % ne couvrent pas P(stop) 8.6 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 26.193 %) — p(stop avant cible) 0.0753 [0.05 ; 0.11], R/R 0.748, perte reelle 32.413 % (gap inclus), EV -2.2607 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 5.4 % x 24.24 % + P(rien) 87.1 % x -1.30 % ne couvrent pas P(stop) 7.5 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 27.939 %) — p(stop avant cible) 0.0611 [0.04 ; 0.09], R/R 0.748, perte reelle 32.413 % (gap inclus), EV -2.1573 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.16 %) : P(cible) 5.4 % x 24.24 % + P(rien) 88.5 % x -1.68 % ne couvrent pas P(stop) 6.1 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.162, ATR14 0.1104 (3.492 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.282 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.175 % | 3.1565 | 88.94 % | 91.8 % | 93.57 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.349 % | 3.151 | 81.54 % | 86.96 % | 89.61 % | 92.77 % | 95.62 % | 97.18 % |
| 0.15 ATR | 0.524 % | 3.1454 | 75.22 % | 83.1 % | 86.55 % | 89.99 % | 93.82 % | 96.08 % |
| 0.2 ATR | 0.698 % | 3.1399 | 68.9 % | 79.05 % | 83.28 % | 87.22 % | 91.93 % | 94.77 % |
| 0.25 ATR | 0.873 % | 3.1344 | 63.28 % | 75.79 % | 80.22 % | 84.84 % | 90.04 % | 93.56 % |
| 0.35 ATR | 1.222 % | 3.1233 | 51.83 % | 67.59 % | 73.79 % | 79.88 % | 86.16 % | 91.55 % |
| 0.5 ATR | 1.746 % | 3.1068 | 35.54 % | 54.94 % | 62.81 % | 70.76 % | 80.08 % | 88.23 % |
| 0.75 ATR | 2.619 % | 3.0792 | 19.15 % | 37.94 % | 47.68 % | 59.37 % | 71.71 % | 81.89 % |
| 1.0 ATR | 3.492 % | 3.0516 | 10.17 % | 24.9 % | 35.91 % | 47.47 % | 62.35 % | 75.25 % |
| 1.25 ATR | 4.365 % | 3.024 | 4.84 % | 17.39 % | 27.5 % | 39.54 % | 55.58 % | 70.02 % |
| 1.5 ATR | 5.239 % | 2.9964 | 3.06 % | 11.26 % | 19.78 % | 31.42 % | 48.41 % | 64.69 % |
| 2.0 ATR | 6.985 % | 2.9411 | 1.48 % | 5.24 % | 9.89 % | 19.43 % | 34.76 % | 52.41 % |
| 2.5 ATR | 8.731 % | 2.8859 | 0.49 % | 2.77 % | 5.74 % | 12.39 % | 27.59 % | 44.57 % |
| 3.0 ATR | 10.477 % | 2.8307 | 0.39 % | 1.68 % | 3.76 % | 8.92 % | 20.72 % | 37.42 % |
| 4.0 ATR | 13.969 % | 2.7203 | 0.2 % | 0.89 % | 1.98 % | 4.46 % | 11.65 % | 24.45 % |
| 6.0 ATR | 20.954 % | 2.4994 | 0.0 % | 0.4 % | 0.89 % | 2.08 % | 5.48 % | 14.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.49 ATR | 1.99 ATR | 2.69 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.84 ATR | 3.88 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.62 ATR | 2.12 ATR | 2.69 ATR | 3.08 ATR | 4.54 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.15 ATR | 2.47 ATR | 3.34 ATR | 3.96 ATR | 4.86 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.619 %, prix 3.0792), p(touche) 37.94 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.2 % des re-echantillons)
- **3 seance(s)** : plage utile 0.807–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.492 %, prix 3.0516), p(touche) 35.91 % (en stress 96.08 %)  ✅ optimum identifie (64.9 % des re-echantillons)
- **5 seance(s)** : plage utile 1.078–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.365 %, prix 3.024), p(touche) 39.54 % (en stress 95.05 %)  ✅ optimum identifie (75.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.625–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.985 %, prix 2.9411), p(touche) 34.76 % (en stress 98.02 %)  ✅ optimum identifie (72.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.473–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.731 %, prix 2.8859), p(touche) 44.57 % (en stress 98.0 %)  ✅ optimum identifie (84.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.061 | EV/share : €-0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 9 % | T2 6 % | T3 6 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.4 | bear 5.0 | side 77.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→69% · +2.0%→41% · +3.0%→21% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.26%) · excursion haute méd. +1.57% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.39% vs midi 1.183% vs clôture 1.156% _(ouverture ~2.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.092 ; mean-reverting — autocorr -0.184)_ ; drift intra méd. -0.657% ; recovery-V 22%
- **σ réalisé intraday** 2.883% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 75% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 3.2156 (VA 3.191–3.2341 ; dernier close 3.203)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 55% · rebond 63% · **stop −2.51%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 40% (gap-down >1% 9% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.2%) · haut méd +0.37% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.65%) · haut méd +0.56% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.77%) · haut méd +0.71% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.93%) · haut méd +0.88% · range méd 2.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.212 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 79% (131/159) · gap 22% · délai 1.0min · rebond 65% (88/131) (MFE +1.39%)
   - −1.0% : fill 30min 38% · séance 67% (112/159) · gap 9% · délai 6.9min · rebond 63% (74/112) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 55% (95/159) · gap 5% · délai 25.1min · rebond 63% (61/95) (MFE +1.33%)
   - −2.0% : fill 30min 19% · séance 44% (79/159) · gap 5% · délai 43.0min · rebond 50% (44/79) (MFE +0.99%)
   - −3.0% : fill 30min 9% · séance 23% (49/159) · gap 3% · délai 59.4min · rebond 66% (35/49) (MFE +1.5%)
   - −4.0% : fill 30min 4% · séance 10% (26/159) · gap 1% · délai 46.7min · rebond 53% (16/26) (MFE +1.13%)
   - −5.0% : fill 30min 3% · séance 6% (15/159) · gap 1% · délai 30.3min · rebond 59% (10/15) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −2.19%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.83%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −1.85%) → stop au-delà de −1.58% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=808 jambes) : jambe baissière méd −1.07% (p90 −2.28%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (47/55) · rebond 64% (32/47)
      · −2.0% : fill 62% (37/55) · rebond 48% (21/37)
      · −3.0% : fill 35% (25/55) · rebond 68% (18/25)
      · −4.0% : fill 21% (18/55) · rebond 42% (11/18)
      · −5.0% : fill 15% (12/55) · rebond 40% (7/12)
   - **flat** (35 séances) :
      · −1.0% : fill 85% (28/35) · rebond 49% (16/28)
      · −2.0% : fill 62% (21/35) · rebond 44% (9/21)
      · −3.0% : fill 35% (13/35) · rebond 79% (10/13)
      · −4.0% : fill 7% (3/35) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/35) · rebond 100% (1/1)
   - **gap-up** (69 séances) :
      · −1.0% : fill 49% (37/69) · rebond 73% (26/37)
      · −2.0% : fill 24% (21/69) · rebond 60% (14/21)
      · −3.0% : fill 9% (11/69) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/69) · rebond 95% (4/5)
      · −5.0% : fill 3% (2/69) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 62% si début vert vs 33% si rouge (base 45% · écart 29 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **62%** · continue >prix actuel 35% ; creux résiduel méd -1.77% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.42% → **scale +1.38% / runner +2.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **33%** (continue à baisser 55%) → **RÉDUIRE ~67%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.16%** (au-delà de la MAE q10 -4.16%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +2.07%] · haut q95 +2.96% · bas q05 -3.91%
   - 60min (n=160) : retour [-2.99% .. +2.44%] · haut q95 +3.08% · bas q05 -3.96%
   - 2h (n=160) : retour [-3.46% .. +2.37%] · haut q95 +3.72% · bas q05 -4.16%
   - 4h (n=160) : retour [-3.35% .. +3.62%] · haut q95 +4.28% · bas q05 -4.28%
   - 6h (n=160) : retour [-3.3% .. +3.75%] · haut q95 +5.24% · bas q05 -4.99%
   - session (n=160) : retour [-4.11% .. +4.05%] · haut q95 +5.66% · bas q05 -5.54%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.2  _(momentum baissier)_
- **ADX** : 30.2  _(tendance etablie)_
- **MACD** : hist 0.011  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 20.3%
- **ATR** : 0.11 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.301  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 56.9  _(transition)_
- **MA** : MA20 3.37 · MA50 3.75 · MA200 4.92  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -15.7% · MA200 -35.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760540 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
