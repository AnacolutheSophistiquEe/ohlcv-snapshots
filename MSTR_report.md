# MSTR

**Generated** : 2026-09-02T22:00:26.109215+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $123.19  

> 🟡 **WAIT-FOR-DIP** — spot +2.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $123.19 (+2.6% vs entrée) · entrée $120.01 · stop $111.25 · T1 $136.25 · R/R 1.85  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk 0.335 _(réel 5 s)_ (GBM -0.08) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $118.38–$121.63 (mid $120.01)
- Spot actuel : $123.19 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : $111.25 (stop swing_plan-based (-9.69%))
- Targets : T1 $136.25 · R/R 1.85 | T2 $140.26 · R/R 2.31 | T3 $144.27 · R/R 2.77
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $111.25


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.29 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.69 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **3.623 pt plus bas** dans le cas TYPIQUE (médiane), 17.285 au p90, **17.682 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 9.69 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.036 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2005** [0.1461 ; 0.2648] _(largeur 11.9 pt, n_eff 173.1)_
   - swing : **0.4342** [0.3827 ; 0.4868] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3786** [0.3287 ; 0.4306] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.7 pt), swing (36.1 pt), deep (35.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.77 %** | CVaR **-10.4 %** | vol 5.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.34 % contre 4.87 % aujourd'hui, rapport 1.71)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.77 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3331** (β de hausse 1.8515, asymétrie 1.2602) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 110.0607 sur atr_based (1.5 ATR, 10.658 %) — p(stop avant cible) 0.4307 [0.38 ; 0.48], R/R 1.315, perte reelle 17.215 % (gap inclus), CVaR 10.689 %, EV -3.168 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.78 ATR (stop 7.707 %) — p(stop avant cible) 0.5615 [0.51 ; 0.61], R/R 1.865, perte reelle 12.134 % (gap inclus), EV -2.6682 % — **REFUSE**
      - refuse : cible atteinte seulement 12.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.561, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.66 ATR du spot — compartiment <1, mesure a 46.8 % de casse (IC clusterise [0.433 ; 0.502] sur 1106 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.67 %) : P(cible) 12.4 % x 22.64 % + P(rien) 31.4 % x 4.24 % ne couvrent pas P(stop) 56.1 % x 12.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.658 %) — p(stop avant cible) 0.4307 [0.38 ; 0.48], R/R 1.315, perte reelle 17.215 % (gap inclus), EV -3.168 % — **REFUSE**
      - refuse : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.17 %) : P(cible) 12.7 % x 22.64 % + P(rien) 44.2 % x 3.08 % ne couvrent pas P(stop) 43.1 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.17 ATR (stop 17.635 %) — p(stop avant cible) 0.2114 [0.17 ; 0.26], R/R 0.839, perte reelle 26.975 % (gap inclus), EV -3.0458 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.05 %) : P(cible) 13.1 % x 22.64 % + P(rien) 65.8 % x -0.45 % ne couvrent pas P(stop) 21.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.88 ATR (stop 29.779 %) — p(stop avant cible) 0.0497 [0.03 ; 0.08], R/R 0.76, perte reelle 29.779 % (gap inclus), EV -1.3133 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 13.1 % x 22.64 % + P(rien) 82.0 % x -3.41 % ne couvrent pas P(stop) 5.0 % x 29.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.776 %) — p(stop avant cible) 0.9068 [0.87 ; 0.93], R/R 6.137, perte reelle 3.688 % (gap inclus), EV -2.055 % — **REFUSE**
      - refuse : cible atteinte seulement 3.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.907, borne haute 0.934 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 3.7 % x 22.64 % + P(rien) 5.6 % x 7.93 % ne couvrent pas P(stop) 90.7 % x 3.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.553 %) — p(stop avant cible) 0.7961 [0.75 ; 0.84], R/R 3.619, perte reelle 6.254 % (gap inclus), EV -2.174 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.796, borne haute 0.836 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.17 %) : P(cible) 9.2 % x 22.64 % + P(rien) 11.2 % x 6.46 % ne couvrent pas P(stop) 79.6 % x 6.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.881 %) — p(stop avant cible) 0.5046 [0.45 ; 0.56], R/R 1.493, perte reelle 15.156 % (gap inclus), EV -3.3277 % — **REFUSE**
      - refuse : cible atteinte seulement 12.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.505, borne haute 0.557 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.33 %) : P(cible) 12.5 % x 22.64 % + P(rien) 37.0 % x 4.03 % ne couvrent pas P(stop) 50.5 % x 15.16 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 12.434 %) — p(stop avant cible) 0.3674 [0.32 ; 0.42], R/R 0.987, perte reelle 22.94 % (gap inclus), EV -4.3931 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.39 %) : P(cible) 12.8 % x 22.64 % + P(rien) 50.4 % x 2.24 % ne couvrent pas P(stop) 36.7 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 19.539 %) — p(stop avant cible) 0.1816 [0.14 ; 0.22], R/R 0.839, perte reelle 26.975 % (gap inclus), EV -2.6195 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.62 %) : P(cible) 13.1 % x 22.64 % + P(rien) 68.8 % x -0.98 % ne couvrent pas P(stop) 18.2 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 21.315 %) — p(stop avant cible) 0.1503 [0.12 ; 0.19], R/R 0.839, perte reelle 26.975 % (gap inclus), EV -2.0848 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 13.1 % x 22.64 % + P(rien) 71.9 % x -1.37 % ne couvrent pas P(stop) 15.0 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.868 %) — p(stop avant cible) 0.0995 [0.07 ; 0.13], R/R 0.839, perte reelle 26.975 % (gap inclus), EV -1.5769 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 13.1 % x 22.64 % + P(rien) 77.0 % x -2.40 % ne couvrent pas P(stop) 10.0 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 31.973 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.708, perte reelle 31.973 % (gap inclus), EV -1.2793 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 13.1 % x 22.64 % + P(rien) 83.8 % x -3.85 % ne couvrent pas P(stop) 3.2 % x 31.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 35.526 %) — p(stop avant cible) 0.0148 [0.01 ; 0.03], R/R 0.637, perte reelle 35.526 % (gap inclus), EV -1.1763 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 13.1 % x 22.64 % + P(rien) 85.5 % x -4.22 % ne couvrent pas P(stop) 1.5 % x 35.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 39.078 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.579, perte reelle 39.078 % (gap inclus), EV -1.0867 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 13.1 % x 22.64 % + P(rien) 86.8 % x -4.58 % ne couvrent pas P(stop) 0.2 % x 39.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 42.631 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.531, perte reelle 42.631 % (gap inclus), EV -1.068 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 13.1 % x 22.64 % + P(rien) 86.9 % x -4.61 % ne couvrent pas P(stop) 0.1 % x 42.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 46.184 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.49, perte reelle 46.184 % (gap inclus), EV -1.0623 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 13.1 % x 22.64 % + P(rien) 86.9 % x -4.62 % ne couvrent pas P(stop) 0.0 % x 46.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 49.736 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.455, perte reelle 49.736 % (gap inclus), EV -1.0631 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 13.1 % x 22.64 % + P(rien) 86.9 % x -4.62 % ne couvrent pas P(stop) 0.0 % x 49.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 53.289 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.425, perte reelle 53.289 % (gap inclus), EV -1.0641 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 13.1 % x 22.64 % + P(rien) 86.9 % x -4.62 % ne couvrent pas P(stop) 0.0 % x 53.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 56.841 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.398, perte reelle 56.841 % (gap inclus), EV -1.0648 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 13.1 % x 22.64 % + P(rien) 86.9 % x -4.62 % ne couvrent pas P(stop) 0.0 % x 56.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 123.19, ATR14 8.7529 (7.105 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.396 ATR = 2.814 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.355 % | 122.7524 | 94.36 % | 96.67 % | 97.07 % | 97.67 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.711 % | 122.3147 | 88.32 % | 92.04 % | 93.44 % | 94.74 % | 96.65 % | 97.33 % |
| 0.15 ATR | 1.066 % | 121.8771 | 81.47 % | 87.1 % | 89.61 % | 91.71 % | 94.11 % | 95.59 % |
| 0.2 ATR | 1.421 % | 121.4394 | 73.82 % | 81.85 % | 84.86 % | 88.07 % | 91.36 % | 93.74 % |
| 0.25 ATR | 1.776 % | 121.0018 | 68.08 % | 78.12 % | 82.14 % | 86.15 % | 89.13 % | 92.2 % |
| 0.35 ATR | 2.487 % | 120.1265 | 55.19 % | 68.75 % | 75.18 % | 80.79 % | 85.67 % | 89.53 % |
| 0.5 ATR | 3.553 % | 118.8136 | 38.27 % | 55.34 % | 63.37 % | 71.18 % | 78.46 % | 84.7 % |
| 0.75 ATR | 5.329 % | 116.6254 | 19.34 % | 37.6 % | 46.92 % | 57.94 % | 68.09 % | 77.41 % |
| 1.0 ATR | 7.105 % | 114.4372 | 9.37 % | 25.2 % | 34.71 % | 46.31 % | 58.94 % | 70.23 % |
| 1.25 ATR | 8.881 % | 112.2489 | 4.13 % | 14.52 % | 25.03 % | 36.0 % | 49.9 % | 62.83 % |
| 1.5 ATR | 10.658 % | 110.0607 | 2.11 % | 8.67 % | 17.36 % | 28.92 % | 42.99 % | 56.98 % |
| 2.0 ATR | 14.21 % | 105.6843 | 0.2 % | 3.12 % | 7.37 % | 16.18 % | 31.3 % | 47.23 % |
| 2.5 ATR | 17.763 % | 101.3079 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.44 % | 37.58 % |
| 3.0 ATR | 21.315 % | 96.9314 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 28.421 % | 88.1786 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 42.631 % | 70.6729 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.03 ATR | 1.36 ATR | 1.65 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.12 ATR | 2.74 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.553 %, prix 118.8131), p(touche) 38.27 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.329 %, prix 116.6252), p(touche) 37.6 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.789–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.105 %, prix 114.4374), p(touche) 34.71 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.032–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.881 %, prix 112.2495), p(touche) 36.0 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.427–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.658 %, prix 110.0604), p(touche) 42.99 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.116–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.763 %, prix 101.3078), p(touche) 37.58 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.08 | EV/share : $-0.697 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 11 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.3 | bear 30.9 | side 35.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 493.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.177% → cible +1.589% / stop −4.0%, p_fill 75%, n_eff≈30.3) : P(cible|rempli) **72%** · **EV/risk +0.127** (×p_fill ; si rempli +0.67% du capital)
  - **swing** (entrée dip −2.585% → cible +13.536% / stop −7.294%, p_fill 61%, n_eff≈25.8) : P(cible|rempli) **40%** · **EV/risk +0.335** (×p_fill ; si rempli +4.04% du capital)
  - **deep** (entrée dip −3.992% → cible +9.53% / stop −11.101%, p_fill 52%, n_eff≈26.1) : P(cible|rempli) **63%** · **EV/risk +0.160** (×p_fill ; si rempli +3.44% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→57% · +3.0%→42% · +5.0%→16% · +8.0%→10%
- Range intraday médian 5.55% (p90 10.3%) · excursion haute méd. +2.46% / basse méd. −2.4%
- Profil de vol intra : ouverture 3.464% vs midi 1.203% vs clôture 1.358% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.0)_ ; drift intra méd. 0.611% ; recovery-V 31%
- **σ réalisé intraday** 3.71% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 81% / bas 60% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 126.2064 (VA 123.6984–127.6171 ; dernier close 124.91)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 74% · **stop −4.23%** sous le fill (sous le bruit) · cible +1.76% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 52% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.05%) · haut méd +0.75% · range méd 1.81%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −2.99%) · haut méd +1.2% · range méd 2.49%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.25%) · haut méd +1.39% · range méd 3.15%
- Excursion ouverture 60min (n=160) : bas méd −1.71% (p90 −3.6%) · haut méd +1.78% · range méd 3.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 74% (122/159) · gap 45% · délai 0.0min · rebond 49% (60/122) (MFE +0.93%)
   - −1.0% : fill 30min 60% · séance 70% (117/159) · gap 41% · délai 0.0min · rebond 53% (65/117) (MFE +1.02%)
   - −1.5% : fill 30min 53% · séance 64% (109/159) · gap 34% · délai 0.0min · rebond 56% (64/109) (MFE +1.4%)
   - −2.0% : fill 30min 47% · séance 57% (99/159) · gap 28% · délai 0.0min · rebond 58% (60/99) (MFE +1.16%)
   - −3.0% : fill 30min 32% · séance 48% (79/159) · gap 14% · délai 1.2min · rebond 56% (47/79) (MFE +1.6%)
   - −4.0% : fill 30min 20% · séance 38% (65/159) · gap 4% · délai 27.6min · rebond 70% (44/65) (MFE +1.79%)
   - −5.0% : fill 30min 14% · séance 27% (47/159) · gap 3% · délai 31.0min · rebond 74% (34/47) (MFE +1.76%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.49%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.01% (p90 −2.48%) → stop au-delà de −2.1% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −2.46%) → stop au-delà de −2.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=962 jambes) : jambe baissière méd −1.13% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (78/78) · rebond 45% (37/78)
      · −2.0% : fill 93% (72/78) · rebond 56% (41/72)
      · −3.0% : fill 83% (64/78) · rebond 58% (38/64)
      · −4.0% : fill 68% (54/78) · rebond 71% (37/54)
      · −5.0% : fill 50% (41/78) · rebond 76% (31/41)
   - **flat** (19 séances) :
      · −1.0% : fill 71% (15/19) · rebond 79% (12/15)
      · −2.0% : fill 46% (10/19) · rebond 60% (7/10)
      · −3.0% : fill 28% (5/19) · rebond 35% (2/5)
      · −4.0% : fill 11% (3/19) · rebond 51% (2/3)
      · −5.0% : fill 9% (2/19) · rebond 0% (0/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 31% (24/62) · rebond 63% (16/24)
      · −2.0% : fill 16% (17/62) · rebond 66% (12/17)
      · −3.0% : fill 11% (10/62) · rebond 57% (7/10)
      · −4.0% : fill 10% (8/62) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/62) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 54% si les 15 1res min sont vertes (82 cas) · 38% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 79% si début vert vs 15% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **79%** · continue >prix actuel 43% ; creux résiduel méd -1.49% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.55% → **scale +1.59% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.76%** (au-delà de la MAE q10 -4.76%), cible rebond +1.62% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.3% .. +3.71%] · haut q95 +3.94% · bas q05 -3.65%
   - 60min (n=160) : retour [-4.43% .. +5.41%] · haut q95 +5.67% · bas q05 -4.97%
   - 2h (n=160) : retour [-4.31% .. +6.52%] · haut q95 +7.99% · bas q05 -5.05%
   - 4h (n=160) : retour [-5.56% .. +8.45%] · haut q95 +10.1% · bas q05 -6.74%
   - 6h (n=160) : retour [-5.77% .. +7.44%] · haut q95 +10.17% · bas q05 -7.15%
   - session (n=160) : retour [-5.05% .. +6.6%] · haut q95 +10.17% · bas q05 -7.27%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 15% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 2.61% / p90 3.53%) · ~3.99 replis/séance, durée méd 49.8 min. P(nouveau plus-haut après repli) :
   - −0.5% → **75%** (reprise méd 15.0 min, n=31)
   - −1.0% → **54%** (reprise méd 21.99 min, n=18)
   - −1.5% → **46%** (reprise méd 37.49 min, n=15)
   - −2.0% → **20%** (reprise méd 89.44 min, n=9)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.53%** (p90, défaut prudent ; serré/agressif −2.61%) ; extension open→close méd +8.34% (q75 +9.19% / q95 +15.39%), MFE méd +10.26% / q90 +14.97%
   - Échelle scale-out : +10.26% (33%) / +12.41% (33%) / +14.97% (34%)
- **DÉSARMER** : repli > **−3.53%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 221.98 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.97% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.51%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 64.3  _(momentum haussier)_
- **ADX** : 33.4  _(tendance etablie)_
- **MACD** : hist 1.904  _(pas de croisement recent)_
- **BB** : %B 0.7 · largeur 55.2%
- **ATR** : 8.75 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.096  _(accumulation)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 35.4  _(marche directionnel)_
- **MA** : MA20 110.99 · MA50 101.34 · MA200 139.62  _(prix > MA20)_
- **Dist MA** : MA20 +11.0% · MA50 +21.6% · MA200 -11.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (499605 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
