# EVT

**Generated** : 2026-08-24T21:38:46.931919+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.27  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.27 (+0.6% vs entrée) · entrée €3.25 · stop €3.18 · T1 €3.38 · R/R 1.86  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.115 _(réel 5 s)_ (GBM -0.144) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.01% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.24–€3.26 (mid €3.25)
- Spot actuel : €3.27 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €3.18 (stop swing_plan-based (-6.38%))
- Targets : T1 €3.38 · R/R 1.86 | T2 €3.39 · R/R 2.0 | T3 €3.41 · R/R 2.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.18


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.38 %)** : le gap seul le franchit 0.706 % des séances (9 fois sur 1274).
   - exécution **3.918 pt plus bas** dans le cas TYPIQUE (médiane), 17.391 au p90, **26.033 au pire**
   - perte réelle **12.996 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 6.38 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0467 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0649** [0.0352 ; 0.109] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.4248** [0.3735 ; 0.4773] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4839** [0.4315 ; 0.5365] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.8 pt), swing (37.4 pt), deep (38.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-5.11 %** | CVaR **-9.26 %** | vol 3.81 %/j
   - _fenêtre arrêtée : rupture de regime a 1260 seances en arriere (volatilite 2.12 % contre 3.91 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1085** (β de hausse 0.9483, asymétrie 1.1689) vs GDAXI — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.8861 sur atr_grid (2.5 ATR, 11.847 %) — p(stop avant cible) 0.2502 [0.21 ; 0.30], R/R 1.768, perte reelle 19.926 % (gap inclus), CVaR 11.872 %, EV -2.7245 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.3 ATR (stop 3.72 %) — p(stop avant cible) 0.6743 [0.62 ; 0.72], R/R 3.916, perte reelle 8.996 % (gap inclus), EV -3.5202 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.674, borne haute 0.722 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 0.3 % x 35.23 % + P(rien) 32.2 % x 7.53 % ne couvrent pas P(stop) 67.4 % x 9.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 0.63 ATR (stop 5.278 %) — p(stop avant cible) 0.5552 [0.50 ; 0.61], R/R 3.007, perte reelle 11.717 % (gap inclus), EV -3.3908 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.555, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.63 ATR du spot — compartiment <1, mesure a 50.9 % de casse (IC clusterise [0.476 ; 0.543] sur 1117 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.39 %) : P(cible) 0.5 % x 35.23 % + P(rien) 44.0 % x 6.70 % ne couvrent pas P(stop) 55.5 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.108 %) — p(stop avant cible) 0.4336 [0.38 ; 0.49], R/R 2.177, perte reelle 16.186 % (gap inclus), EV -4.0464 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.05 %) : P(cible) 0.6 % x 35.23 % + P(rien) 56.0 % x 4.93 % ne couvrent pas P(stop) 43.4 % x 16.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.293 %) — p(stop avant cible) 0.3802 [0.33 ; 0.43], R/R 1.957, perte reelle 18.001 % (gap inclus), EV -3.9901 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.99 %) : P(cible) 0.6 % x 35.23 % + P(rien) 61.4 % x 4.31 % ne couvrent pas P(stop) 38.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 10.662 %) — p(stop avant cible) 0.2903 [0.24 ; 0.34], R/R 1.768, perte reelle 19.926 % (gap inclus), EV -3.297 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.30 %) : P(cible) 0.6 % x 35.23 % + P(rien) 70.4 % x 3.24 % ne couvrent pas P(stop) 29.0 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.847 %) — p(stop avant cible) 0.2502 [0.21 ; 0.30], R/R 1.768, perte reelle 19.926 % (gap inclus), EV -2.7245 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.72 %) : P(cible) 0.6 % x 35.23 % + P(rien) 74.4 % x 2.76 % ne couvrent pas P(stop) 25.0 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 13.031 %) — p(stop avant cible) 0.212 [0.17 ; 0.26], R/R 1.558, perte reelle 22.616 % (gap inclus), EV -2.8322 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.83 %) : P(cible) 0.6 % x 35.23 % + P(rien) 78.2 % x 2.24 % ne couvrent pas P(stop) 21.2 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 14.216 %) — p(stop avant cible) 0.1761 [0.14 ; 0.22], R/R 1.304, perte reelle 27.012 % (gap inclus), EV -3.0531 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.05 %) : P(cible) 0.6 % x 35.23 % + P(rien) 81.8 % x 1.83 % ne couvrent pas P(stop) 17.6 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 16.585 %) — p(stop avant cible) 0.145 [0.11 ; 0.18], R/R 1.304, perte reelle 27.012 % (gap inclus), EV -2.4514 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 0.6 % x 35.23 % + P(rien) 84.9 % x 1.48 % ne couvrent pas P(stop) 14.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 18.955 %) — p(stop avant cible) 0.1152 [0.08 ; 0.15], R/R 1.304, perte reelle 27.012 % (gap inclus), EV -1.943 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 0.6 % x 35.23 % + P(rien) 87.9 % x 1.09 % ne couvrent pas P(stop) 11.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 21.324 %) — p(stop avant cible) 0.107 [0.08 ; 0.14], R/R 1.304, perte reelle 27.012 % (gap inclus), EV -1.8297 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.6 % x 35.23 % + P(rien) 88.7 % x 0.96 % ne couvrent pas P(stop) 10.7 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 23.693 %) — p(stop avant cible) 0.0976 [0.07 ; 0.13], R/R 1.087, perte reelle 32.413 % (gap inclus), EV -2.2731 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.27 %) : P(cible) 0.6 % x 35.23 % + P(rien) 89.6 % x 0.76 % ne couvrent pas P(stop) 9.8 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 26.062 %) — p(stop avant cible) 0.0798 [0.05 ; 0.11], R/R 1.087, perte reelle 32.413 % (gap inclus), EV -2.069 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 0.6 % x 35.23 % + P(rien) 91.4 % x 0.34 % ne couvrent pas P(stop) 8.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 28.432 %) — p(stop avant cible) 0.061 [0.04 ; 0.09], R/R 1.087, perte reelle 32.413 % (gap inclus), EV -1.9275 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 0.6 % x 35.23 % + P(rien) 93.3 % x -0.17 % ne couvrent pas P(stop) 6.1 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 30.801 %) — p(stop avant cible) 0.0498 [0.03 ; 0.08], R/R 1.087, perte reelle 32.413 % (gap inclus), EV -1.8428 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 0.6 % x 35.23 % + P(rien) 94.4 % x -0.46 % ne couvrent pas P(stop) 5.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 33.17 %) — p(stop avant cible) 0.0498 [0.03 ; 0.08], R/R 1.062, perte reelle 33.17 % (gap inclus), EV -1.8805 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.88 %) : P(cible) 0.6 % x 35.23 % + P(rien) 94.4 % x -0.46 % ne couvrent pas P(stop) 5.0 % x 33.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 35.54 %) — p(stop avant cible) 0.0387 [0.02 ; 0.06], R/R 0.991, perte reelle 35.54 % (gap inclus), EV -1.9282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 0.6 % x 35.23 % + P(rien) 95.5 % x -0.80 % ne couvrent pas P(stop) 3.9 % x 35.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 37.909 %) — p(stop avant cible) 0.0174 [0.01 ; 0.04], R/R 0.929, perte reelle 37.909 % (gap inclus), EV -1.8346 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.6 % x 35.23 % + P(rien) 97.7 % x -1.42 % ne couvrent pas P(stop) 1.7 % x 37.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.144 | EV/share : €-0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 7 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.0 | bear 7.2 | side 14.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.745% → cible +4.016% / stop −2.01%, p_fill 85%, n_eff≈33.6) : P(cible|rempli) **4%** · **EV/risk -0.115** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −1.642% → cible +3.568% / stop −4.817%, p_fill 64%, n_eff≈24.8) : P(cible|rempli) **46%** · **EV/risk -0.080** (×p_fill ; si rempli -0.61% du capital)
  - **deep** (entrée dip −2.542% → cible +5.046% / stop −7.293%, p_fill 44%, n_eff≈23.0) : P(cible|rempli) **41%** · **EV/risk -0.104** (×p_fill ; si rempli -1.71% du capital)
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
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 71% · rebond 71% · **stop −3.14%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 38% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.34%) · haut méd +0.49% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.83%) · haut méd +0.75% · range méd 1.78%
- Excursion ouverture 30min (n=160) : bas méd −1.05% (p90 −2.83%) · haut méd +0.81% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.26%) · haut méd +0.95% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.348 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 83% (134/159) · gap 22% · délai 0.4min · rebond 71% (89/134) (MFE +1.59%)
   - −1.0% : fill 30min 47% · séance 71% (117/159) · gap 16% · délai 2.5min · rebond 71% (75/117) (MFE +1.6%)
   - −1.5% : fill 30min 35% · séance 54% (95/159) · gap 11% · délai 7.8min · rebond 66% (60/95) (MFE +1.79%)
   - −2.0% : fill 30min 22% · séance 43% (80/159) · gap 7% · délai 23.5min · rebond 58% (50/80) (MFE +1.32%)
   - −3.0% : fill 30min 11% · séance 26% (55/159) · gap 4% · délai 51.4min · rebond 66% (40/55) (MFE +1.36%)
   - −4.0% : fill 30min 6% · séance 16% (32/159) · gap 2% · délai 53.0min · rebond 60% (20/32) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 8% (18/159) · gap 1% · délai 56.0min · rebond 60% (12/18) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.49%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.72%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.89%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=813 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 95% (54/57) · rebond 70% (31/54)
      · −2.0% : fill 65% (41/57) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/57) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/57) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/57) · rebond 57% (9/13)
   - **flat** (43 séances) :
      · −1.0% : fill 65% (30/43) · rebond 73% (23/30)
      · −2.0% : fill 48% (20/43) · rebond 64% (13/20)
      · −3.0% : fill 34% (13/43) · rebond 77% (10/13)
      · −4.0% : fill 17% (6/43) · rebond 46% (2/6)
      · −5.0% : fill 6% (3/43) · rebond 27% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 58% (33/59) · rebond 69% (21/33)
      · −2.0% : fill 24% (19/59) · rebond 46% (12/19)
      · −3.0% : fill 13% (13/59) · rebond 40% (9/13)
      · −4.0% : fill 8% (6/59) · rebond 90% (4/6)
      · −5.0% : fill 5% (2/59) · rebond 100% (2/2)
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

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 42.7  _(momentum baissier)_
- **ADX** : 32.2  _(tendance etablie)_
- **MACD** : hist 0.018  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 15.5%
- **ATR** : 0.16 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.344  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 3.47 · MA50 4.05 · MA200 5.02  _(prix < MA20)_
- **Dist MA** : MA20 -5.7% · MA50 -19.1% · MA200 -34.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (851864 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
