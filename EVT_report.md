# EVT

**Generated** : 2026-08-26T21:39:24.017839+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.35  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.35 (+1.2% vs entrée) · entrée €3.31 · stop €3.26 · T1 €3.38 · R/R 1.4  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk 0.059 _(réel 5 s)_ (GBM -0.015) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.30–€3.32 (mid €3.31)
- Spot actuel : €3.35 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €3.26 (stop swing_plan-based (-7.51%))
- Targets : T1 €3.38 · R/R 1.4 | T2 €3.42 · R/R 2.2 | T3 €3.47 · R/R 3.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.26


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.51 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **6.314 pt plus bas** dans le cas TYPIQUE (médiane), 20.582 au p90, **24.903 au pire**
   - perte réelle **18.001 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 7.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0412 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5234** [0.4491 ; 0.5969] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.383** [0.3329 ; 0.435] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3566** [0.3075 ; 0.4081] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.2 pt), swing (45.8 pt), deep (44.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-5.11 %** | CVaR **-9.26 %** | vol 3.8 %/j
   - _fenêtre arrêtée : rupture de regime a 1260 seances en arriere (volatilite 2.13 % contre 3.91 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1105** (β de hausse 0.9427, asymétrie 1.178) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.9686 sur atr_grid (2.5 ATR, 11.489 %) — p(stop avant cible) 0.2747 [0.23 ; 0.32], R/R 1.607, perte reelle 19.926 % (gap inclus), CVaR 11.515 %, EV -3.1194 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.82 ATR (stop 5.894 %) — p(stop avant cible) 0.5243 [0.47 ; 0.58], R/R 2.732, perte reelle 11.717 % (gap inclus), EV -3.0223 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.02 %) : P(cible) 1.4 % x 32.01 % + P(rien) 46.2 % x 5.82 % ne couvrent pas P(stop) 52.4 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.15 ATR (stop 7.421 %) — p(stop avant cible) 0.42 [0.37 ; 0.47], R/R 1.778, perte reelle 18.001 % (gap inclus), EV -4.6064 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.61 %) : P(cible) 1.4 % x 32.01 % + P(rien) 56.6 % x 4.41 % ne couvrent pas P(stop) 42.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.149 %) — p(stop avant cible) 0.8911 [0.85 ; 0.92], R/R 11.401, perte reelle 2.808 % (gap inclus), EV -1.3659 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 11.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.921 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 0.6 % x 32.01 % + P(rien) 10.3 % x 9.11 % ne couvrent pas P(stop) 89.1 % x 2.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.298 %) — p(stop avant cible) 0.8061 [0.76 ; 0.85], R/R 6.032, perte reelle 5.307 % (gap inclus), EV -2.4964 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.806, borne haute 0.845 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.50 %) : P(cible) 0.8 % x 32.01 % + P(rien) 18.6 % x 8.27 % ne couvrent pas P(stop) 80.6 % x 5.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.82 ATR (stop 5.159 %) — p(stop avant cible) 0.5689 [0.52 ; 0.62], R/R 2.732, perte reelle 11.717 % (gap inclus), EV -3.6022 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.569, borne haute 0.620 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 1.2 % x 32.01 % + P(rien) 41.9 % x 6.38 % ne couvrent pas P(stop) 56.9 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.15 ATR (stop 6.686 %) — p(stop avant cible) 0.4772 [0.42 ; 0.53], R/R 2.154, perte reelle 14.861 % (gap inclus), EV -4.0474 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.05 %) : P(cible) 1.4 % x 32.01 % + P(rien) 50.8 % x 5.09 % ne couvrent pas P(stop) 47.7 % x 14.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.043 %) — p(stop avant cible) 0.3926 [0.34 ; 0.44], R/R 1.778, perte reelle 18.001 % (gap inclus), EV -4.2354 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.24 %) : P(cible) 1.4 % x 32.01 % + P(rien) 59.3 % x 4.00 % ne couvrent pas P(stop) 39.3 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.192 %) — p(stop avant cible) 0.3368 [0.29 ; 0.39], R/R 1.778, perte reelle 18.001 % (gap inclus), EV -3.4305 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.43 %) : P(cible) 1.4 % x 32.01 % + P(rien) 64.9 % x 3.35 % ne couvrent pas P(stop) 33.7 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 10.341 %) — p(stop avant cible) 0.3064 [0.26 ; 0.36], R/R 1.607, perte reelle 19.926 % (gap inclus), EV -3.5987 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 1.4 % x 32.01 % + P(rien) 67.9 % x 3.02 % ne couvrent pas P(stop) 30.6 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.489 %) — p(stop avant cible) 0.2747 [0.23 ; 0.32], R/R 1.607, perte reelle 19.926 % (gap inclus), EV -3.1194 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.12 %) : P(cible) 1.4 % x 32.01 % + P(rien) 71.1 % x 2.67 % ne couvrent pas P(stop) 27.5 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 12.638 %) — p(stop avant cible) 0.2285 [0.19 ; 0.27], R/R 1.416, perte reelle 22.616 % (gap inclus), EV -3.147 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.15 %) : P(cible) 1.4 % x 32.01 % + P(rien) 75.7 % x 2.06 % ne couvrent pas P(stop) 22.9 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 13.787 %) — p(stop avant cible) 0.1841 [0.15 ; 0.23], R/R 1.416, perte reelle 22.616 % (gap inclus), EV -2.5376 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.54 %) : P(cible) 1.4 % x 32.01 % + P(rien) 80.2 % x 1.46 % ne couvrent pas P(stop) 18.4 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 16.085 %) — p(stop avant cible) 0.1468 [0.11 ; 0.19], R/R 1.185, perte reelle 27.012 % (gap inclus), EV -2.6101 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 1.4 % x 32.01 % + P(rien) 83.9 % x 1.07 % ne couvrent pas P(stop) 14.7 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 18.383 %) — p(stop avant cible) 0.1145 [0.08 ; 0.15], R/R 1.185, perte reelle 27.012 % (gap inclus), EV -2.0502 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 1.4 % x 32.01 % + P(rien) 87.1 % x 0.67 % ne couvrent pas P(stop) 11.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 20.681 %) — p(stop avant cible) 0.1059 [0.08 ; 0.14], R/R 1.185, perte reelle 27.012 % (gap inclus), EV -1.9326 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 1.4 % x 32.01 % + P(rien) 88.0 % x 0.53 % ne couvrent pas P(stop) 10.6 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 22.979 %) — p(stop avant cible) 0.1012 [0.07 ; 0.14], R/R 0.988, perte reelle 32.413 % (gap inclus), EV -2.4312 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.43 %) : P(cible) 1.4 % x 32.01 % + P(rien) 88.4 % x 0.44 % ne couvrent pas P(stop) 10.1 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 25.277 %) — p(stop avant cible) 0.0852 [0.06 ; 0.12], R/R 0.988, perte reelle 32.413 % (gap inclus), EV -2.2347 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.23 %) : P(cible) 1.4 % x 32.01 % + P(rien) 90.0 % x 0.08 % ne couvrent pas P(stop) 8.5 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 27.575 %) — p(stop avant cible) 0.0726 [0.05 ; 0.10], R/R 0.988, perte reelle 32.413 % (gap inclus), EV -2.124 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 1.4 % x 32.01 % + P(rien) 91.3 % x -0.25 % ne couvrent pas P(stop) 7.3 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 29.873 %) — p(stop avant cible) 0.0492 [0.03 ; 0.08], R/R 0.988, perte reelle 32.413 % (gap inclus), EV -1.9428 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 1.4 % x 32.01 % + P(rien) 93.7 % x -0.86 % ne couvrent pas P(stop) 4.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 32.171 %) — p(stop avant cible) 0.0492 [0.03 ; 0.08], R/R 0.988, perte reelle 32.413 % (gap inclus), EV -1.9428 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 1.4 % x 32.01 % + P(rien) 93.7 % x -0.86 % ne couvrent pas P(stop) 4.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 34.468 %) — p(stop avant cible) 0.0489 [0.03 ; 0.08], R/R 0.929, perte reelle 34.468 % (gap inclus), EV -2.0409 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 1.4 % x 32.01 % + P(rien) 93.7 % x -0.87 % ne couvrent pas P(stop) 4.9 % x 34.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 36.766 %) — p(stop avant cible) 0.0326 [0.02 ; 0.06], R/R 0.871, perte reelle 36.766 % (gap inclus), EV -2.0342 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.03 %) : P(cible) 1.4 % x 32.01 % + P(rien) 95.3 % x -1.36 % ne couvrent pas P(stop) 3.3 % x 36.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.354, ATR14 0.1541 (4.596 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.365 ATR = 1.677 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.23 % | 3.3463 | 88.86 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.46 % | 3.3386 | 81.56 % | 87.07 % | 89.82 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.689 % | 3.3309 | 75.35 % | 83.22 % | 86.76 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.919 % | 3.3232 | 68.93 % | 79.07 % | 83.4 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.149 % | 3.3155 | 63.21 % | 75.81 % | 80.34 % | 84.75 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.609 % | 3.3001 | 51.68 % | 67.62 % | 73.81 % | 79.6 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.298 % | 3.2769 | 35.4 % | 54.89 % | 62.75 % | 70.59 % | 80.1 % | 88.24 % |
| 0.75 ATR | 3.447 % | 3.2384 | 19.13 % | 37.71 % | 47.63 % | 59.21 % | 71.64 % | 81.91 % |
| 1.0 ATR | 4.596 % | 3.1999 | 10.16 % | 24.68 % | 35.77 % | 47.43 % | 62.19 % | 75.48 % |
| 1.25 ATR | 5.745 % | 3.1613 | 4.83 % | 17.47 % | 27.47 % | 39.5 % | 55.52 % | 70.25 % |
| 1.5 ATR | 6.894 % | 3.1228 | 3.06 % | 11.45 % | 19.86 % | 31.49 % | 48.56 % | 65.03 % |
| 2.0 ATR | 9.192 % | 3.0457 | 1.48 % | 5.23 % | 9.98 % | 19.41 % | 35.12 % | 52.86 % |
| 2.5 ATR | 11.489 % | 2.9686 | 0.49 % | 2.76 % | 5.83 % | 12.48 % | 27.96 % | 45.03 % |
| 3.0 ATR | 13.787 % | 2.8916 | 0.39 % | 1.68 % | 3.75 % | 9.01 % | 21.0 % | 38.19 % |
| 4.0 ATR | 18.383 % | 2.7374 | 0.2 % | 0.89 % | 1.98 % | 4.55 % | 11.94 % | 25.33 % |
| 6.0 ATR | 27.575 % | 2.4291 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.57 % | 14.27 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 0.99 ATR | 1.16 ATR | 1.62 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.08 ATR | 1.33 ATR | 1.50 ATR | 2.00 ATR | 2.70 ATR |
| **5 s.** | 0.43 ATR | 0.94 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.86 ATR | 3.90 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.15 ATR | 2.71 ATR | 3.11 ATR | 4.61 ATR | hors grille |
| **20 s.** | 1.02 ATR | 2.18 ATR | 2.50 ATR | 3.40 ATR | 4.06 ATR | 4.96 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (61.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.644–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.447 %, prix 3.2384), p(touche) 37.71 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.8 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.596 %, prix 3.1999), p(touche) 35.77 % (en stress 96.08 %)  ✅ optimum identifie (61.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.077–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.745 %, prix 3.1613), p(touche) 39.5 % (en stress 95.05 %)  ✅ optimum identifie (74.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.632–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.192 %, prix 3.0457), p(touche) 35.12 % (en stress 98.02 %)  ✅ optimum identifie (71.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.502–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.787 %, prix 2.8916), p(touche) 38.19 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.015 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 15 % | T3 6 %
- Kelly (position) : f* 0.019 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.1 | bear 6.5 | side 80.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.331% → cible +2.13% / stop −1.499%, p_fill 68%, n_eff≈25.3) : P(cible|rempli) **27%** · **EV/risk +0.059** (×p_fill ; si rempli +0.13% du capital)
  - **swing** (entrée dip −2.915% → cible +3.609% / stop −4.733%, p_fill 42%, n_eff≈15.7) : P(cible|rempli) **46%** · **EV/risk -0.066** (×p_fill ; si rempli -0.73% du capital)
  - **deep** (entrée dip −4.506% → cible +5.105% / stop −7.219%, p_fill 25%, n_eff≈17.0) : P(cible|rempli) **18%** · **EV/risk -0.119** (×p_fill ; si rempli -3.47% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→69% · +2.0%→44% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.57%) · excursion haute méd. +1.74% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.692% vs midi 1.22% vs clôture 1.193% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; mean-reverting — autocorr -0.134)_ ; drift intra méd. -0.771% ; recovery-V 27%
- **σ réalisé intraday** 3.137% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 72% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 3.3443 (VA 3.3227–3.3569 ; dernier close 3.348)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−0.5%** sous le close veille · fill 79% · rebond 76% · **stop −3.3%** sous le fill (sous le bruit) · cible +1.62% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 39% (gap-down >1% 11% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.34%) · haut méd +0.49% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.83%) · haut méd +0.75% · range méd 1.78%
- Excursion ouverture 30min (n=160) : bas méd −1.05% (p90 −2.83%) · haut méd +0.81% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.26%) · haut méd +0.95% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.356 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 79% (131/159) · gap 24% · délai 0.4min · rebond 76% (91/131) (MFE +1.62%)
   - −1.0% : fill 30min 40% · séance 66% (112/159) · gap 11% · délai 6.4min · rebond 70% (74/112) (MFE +1.56%)
   - −1.5% : fill 30min 32% · séance 56% (96/159) · gap 6% · délai 19.3min · rebond 67% (61/96) (MFE +1.57%)
   - −2.0% : fill 30min 20% · séance 45% (80/159) · gap 6% · délai 36.8min · rebond 55% (47/80) (MFE +1.43%)
   - −3.0% : fill 30min 11% · séance 25% (51/159) · gap 4% · délai 50.1min · rebond 64% (36/51) (MFE +1.45%)
   - −4.0% : fill 30min 5% · séance 13% (28/159) · gap 1% · délai 46.7min · rebond 54% (18/28) (MFE +1.15%)
   - −5.0% : fill 30min 4% · séance 8% (16/159) · gap 1% · délai 35.6min · rebond 59% (11/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.49%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.72%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.89%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=813 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 86% (49/56) · rebond 73% (32/49)
      · −2.0% : fill 61% (38/56) · rebond 59% (23/38)
      · −3.0% : fill 42% (27/56) · rebond 68% (19/27)
      · −4.0% : fill 26% (20/56) · rebond 43% (13/20)
      · −5.0% : fill 18% (13/56) · rebond 42% (8/13)
   - **flat** (35 séances) :
      · −1.0% : fill 80% (27/35) · rebond 67% (17/27)
      · −2.0% : fill 60% (20/35) · rebond 42% (9/20)
      · −3.0% : fill 36% (13/35) · rebond 74% (10/13)
      · −4.0% : fill 8% (3/35) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/35) · rebond 100% (1/1)
   - **gap-up** (68 séances) :
      · −1.0% : fill 49% (36/68) · rebond 69% (25/36)
      · −2.0% : fill 28% (22/68) · rebond 60% (15/22)
      · −3.0% : fill 10% (11/68) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/68) · rebond 95% (4/5)
      · −5.0% : fill 4% (2/68) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 35% si rouge (base 48% · écart 31 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.75% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.43% → **scale +1.56% / runner +2.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **35%** (continue à baisser 51%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.58%** (au-delà de la MAE q10 -4.58%), cible rebond +1.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +2.3%] · haut q95 +3.38% · bas q05 -3.94%
   - 60min (n=160) : retour [-3.32% .. +2.7%] · haut q95 +3.45% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.68% .. +2.64%] · haut q95 +3.9% · bas q05 -4.81%
   - 4h (n=160) : retour [-3.48% .. +3.03%] · haut q95 +3.94% · bas q05 -6.47%
   - 6h (n=160) : retour [-3.71% .. +3.37%] · haut q95 +4.79% · bas q05 -6.47%
   - session (n=160) : retour [-4.59% .. +4.21%] · haut q95 +6.42% · bas q05 -7.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 47.0  _(neutre)_
- **ADX** : 31.4  _(tendance etablie)_
- **MACD** : hist 0.018  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 16.7%
- **ATR** : 0.15 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.346  _(distribution)_
- **Vol ratio** : 1.13  _(volume normal)_
- **Choppiness** : 46.1  _(transition)_
- **MA** : MA20 3.45 · MA50 3.99 · MA200 5.0  _(prix < MA20)_
- **Dist MA** : MA20 -2.9% · MA50 -15.9% · MA200 -32.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (829158 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
