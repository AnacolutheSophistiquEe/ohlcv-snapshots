# SMR

**Generated** : 2026-08-27T00:34:17.754061+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.27  

> 🟡 **WAIT-FOR-DIP** — spot +1.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $9.27 (+1.1% vs entrée) · entrée $9.17 · stop $8.92 · T1 $9.66 · R/R 1.96  
> ↳ P(T1 av. stop) 26 % _(réel 5 s)_ · EV/risk 0.063 _(réel 5 s)_ (GBM 0.091) · ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.71% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 280 % hors [0,100] (R² max 0.71). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.11–$9.22 (mid $9.17)
- Spot actuel : $9.27 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $8.92 (stop swing_plan-based (-10.06%))
- Targets : T1 $9.66 · R/R 1.96 | T2 $9.84 · R/R 2.68 | T3 $10.01 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.92


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.31 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.06 %)** : le gap seul le franchit 0.533 % des séances (6 fois sur 1126).
   - exécution **4.114 pt plus bas** dans le cas TYPIQUE (médiane), 13.718 au p90, **20.263 au pire**
   - perte réelle **16.461 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 10.06 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0341 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.431 % | p01 -6.963 % | pire -30.323 % _(sur 1126 séances)_
- **P(stop avant cible)** _(source : daily, 1127 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5546** [0.4802 ; 0.6272] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.5257** [0.473 ; 0.578] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.5166** [0.4639 ; 0.569] _(largeur 10.5 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.3 pt), swing (34.0 pt), deep (33.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.93 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.03 % contre 5.91 % aujourd'hui, rapport 1.87)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.97 % vs -18.69 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6004** (β de hausse 1.3683, asymétrie 1.1696) vs IWM — 534 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.008× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.0306 sur atr_grid (1.75 ATR, 13.37 %) — p(stop avant cible) 0.4645 [0.41 ; 0.52], R/R 0.931, perte reelle 18.976 % (gap inclus), CVaR 13.39 %, EV -3.4583 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1158 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 13.39 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.68 ATR (stop 7.787 %) — p(stop avant cible) 0.6959 [0.65 ; 0.74], R/R 1.308, perte reelle 13.499 % (gap inclus), EV -5.0137 % — **REFUSE**
      - refuse : p_stop_first 0.696, borne haute 0.743 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.01 %) : P(cible) 23.7 % x 17.66 % + P(rien) 6.7 % x 2.92 % ne couvrent pas P(stop) 69.6 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.04 ATR (stop 10.611 %) — p(stop avant cible) 0.5794 [0.53 ; 0.63], R/R 1.0, perte reelle 17.667 % (gap inclus), EV -5.2358 % — **REFUSE**
      - refuse : p_stop_first 0.579, borne haute 0.631 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.58 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.451 ; 0.510] sur 1199 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.24 %) : P(cible) 28.1 % x 17.66 % + P(rien) 13.9 % x 0.23 % ne couvrent pas P(stop) 57.9 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.91 ATR (stop 24.85 %) — p(stop avant cible) 0.1386 [0.11 ; 0.18], R/R 0.582, perte reelle 30.323 % (gap inclus), EV -1.5265 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.53 %) : P(cible) 32.6 % x 17.66 % + P(rien) 53.6 % x -5.74 % ne couvrent pas P(stop) 13.9 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.91 %) — p(stop avant cible) 0.9045 [0.87 ; 0.93], R/R 4.502, perte reelle 3.923 % (gap inclus), EV -2.0374 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.904, borne haute 0.932 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 8.5 % x 17.66 % + P(rien) 1.1 % x 0.93 % ne couvrent pas P(stop) 90.5 % x 3.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 13.37 %) — p(stop avant cible) 0.4645 [0.41 ; 0.52], R/R 0.931, perte reelle 18.976 % (gap inclus), EV -3.4583 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.46 %) : P(cible) 30.7 % x 17.66 % + P(rien) 22.8 % x -0.32 % ne couvrent pas P(stop) 46.5 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 15.28 %) — p(stop avant cible) 0.4046 [0.35 ; 0.46], R/R 0.743, perte reelle 23.778 % (gap inclus), EV -4.4196 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.42 %) : P(cible) 31.8 % x 17.66 % + P(rien) 27.8 % x -1.47 % ne couvrent pas P(stop) 40.5 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 17.19 %) — p(stop avant cible) 0.3339 [0.29 ; 0.38], R/R 0.743, perte reelle 23.778 % (gap inclus), EV -3.1111 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.11 %) : P(cible) 32.1 % x 17.66 % + P(rien) 34.5 % x -2.47 % ne couvrent pas P(stop) 33.4 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 19.1 %) — p(stop avant cible) 0.2625 [0.22 ; 0.31], R/R 0.582, perte reelle 30.323 % (gap inclus), EV -3.702 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.70 %) : P(cible) 32.3 % x 17.66 % + P(rien) 41.4 % x -3.51 % ne couvrent pas P(stop) 26.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 26.739 %) — p(stop avant cible) 0.0926 [0.07 ; 0.13], R/R 0.582, perte reelle 30.323 % (gap inclus), EV -0.8676 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 32.6 % x 17.66 % + P(rien) 58.2 % x -6.55 % ne couvrent pas P(stop) 9.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 30.559 %) — p(stop avant cible) 0.0568 [0.04 ; 0.09], R/R 0.578, perte reelle 30.559 % (gap inclus), EV -0.5809 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 32.6 % x 17.66 % + P(rien) 61.8 % x -7.45 % ne couvrent pas P(stop) 5.7 % x 30.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 34.379 %) — p(stop avant cible) 0.0326 [0.02 ; 0.06], R/R 0.514, perte reelle 34.379 % (gap inclus), EV -0.5217 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 32.6 % x 17.66 % + P(rien) 64.1 % x -8.04 % ne couvrent pas P(stop) 3.3 % x 34.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 38.199 %) — p(stop avant cible) 0.023 [0.01 ; 0.04], R/R 0.462, perte reelle 38.199 % (gap inclus), EV -0.5995 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 32.6 % x 17.66 % + P(rien) 65.1 % x -8.41 % ne couvrent pas P(stop) 2.3 % x 38.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 42.019 %) — p(stop avant cible) 0.0136 [0.01 ; 0.03], R/R 0.42, perte reelle 42.019 % (gap inclus), EV -0.5694 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 32.6 % x 17.66 % + P(rien) 66.0 % x -8.71 % ne couvrent pas P(stop) 1.4 % x 42.02 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 45.839 %) — p(stop avant cible) 0.0105 [0.00 ; 0.03], R/R 0.385, perte reelle 45.839 % (gap inclus), EV -0.6013 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 32.6 % x 17.66 % + P(rien) 66.4 % x -8.85 % ne couvrent pas P(stop) 1.1 % x 45.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 49.659 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.356, perte reelle 49.659 % (gap inclus), EV -0.5979 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 32.6 % x 17.66 % + P(rien) 67.2 % x -9.29 % ne couvrent pas P(stop) 0.2 % x 49.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 53.479 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.33, perte reelle 53.479 % (gap inclus), EV -0.5952 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 32.6 % x 17.66 % + P(rien) 67.4 % x -9.41 % ne couvrent pas P(stop) 0.0 % x 53.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 57.299 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.308, perte reelle 57.299 % (gap inclus), EV -0.5909 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 32.6 % x 17.66 % + P(rien) 67.4 % x -9.41 % ne couvrent pas P(stop) 0.0 % x 57.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 61.119 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.289, perte reelle 61.119 % (gap inclus), EV -0.5909 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 61.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 32.6 % x 17.66 % + P(rien) 67.4 % x -9.41 % ne couvrent pas P(stop) 0.0 % x 61.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.27, ATR14 0.7082 (7.64 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.428 ATR = 3.27 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.382 % | 9.2346 | 92.61 % | 95.14 % | 96.41 % | 97.1 % | 97.9 % | 98.35 % |
| 0.1 ATR | 0.764 % | 9.1992 | 86.95 % | 91.33 % | 93.29 % | 94.66 % | 96.15 % | 97.4 % |
| 0.15 ATR | 1.146 % | 9.1638 | 80.95 % | 87.05 % | 89.7 % | 91.65 % | 93.82 % | 96.1 % |
| 0.2 ATR | 1.528 % | 9.1284 | 75.4 % | 82.77 % | 86.46 % | 89.21 % | 92.18 % | 95.04 % |
| 0.25 ATR | 1.91 % | 9.0929 | 70.09 % | 79.65 % | 83.8 % | 87.01 % | 90.55 % | 93.86 % |
| 0.35 ATR | 2.674 % | 9.0221 | 58.31 % | 72.14 % | 77.43 % | 82.83 % | 87.51 % | 91.5 % |
| 0.5 ATR | 3.82 % | 8.9159 | 42.38 % | 59.19 % | 67.25 % | 74.25 % | 82.96 % | 88.43 % |
| 0.75 ATR | 5.73 % | 8.7388 | 20.67 % | 37.46 % | 47.92 % | 59.86 % | 72.35 % | 80.76 % |
| 1.0 ATR | 7.64 % | 8.5618 | 11.32 % | 25.9 % | 36.0 % | 49.42 % | 64.41 % | 75.21 % |
| 1.25 ATR | 9.55 % | 8.3847 | 4.73 % | 16.07 % | 25.35 % | 38.75 % | 54.84 % | 68.83 % |
| 1.5 ATR | 11.46 % | 8.2077 | 2.31 % | 9.83 % | 16.32 % | 28.42 % | 45.51 % | 62.1 % |
| 2.0 ATR | 15.28 % | 7.8536 | 0.35 % | 3.24 % | 6.48 % | 14.62 % | 31.51 % | 49.82 % |
| 2.5 ATR | 19.1 % | 7.4995 | 0.12 % | 1.27 % | 2.78 % | 6.84 % | 20.65 % | 38.96 % |
| 3.0 ATR | 22.92 % | 7.1454 | 0.12 % | 0.58 % | 1.74 % | 3.71 % | 11.9 % | 28.93 % |
| 4.0 ATR | 30.559 % | 6.4371 | 0.0 % | 0.23 % | 0.35 % | 1.04 % | 4.55 % | 13.93 % |
| 6.0 ATR | 45.839 % | 5.0207 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.65 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.61 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.99 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.30 ATR | 2.79 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.52 ATR | 1.95 ATR | 2.30 ATR | 2.54 ATR | 3.26 ATR | 3.94 ATR |
| **20 s.** | 1.01 ATR | 1.99 ATR | 2.22 ATR | 2.80 ATR | 3.26 ATR | 3.60 ATR | 4.64 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.475–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.82 %, prix 8.9159), p(touche) 42.38 % (en stress 81.61 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.73 %, prix 8.7388), p(touche) 37.46 % (en stress 88.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.2 % des re-echantillons)
- **3 seance(s)** : plage utile 0.811–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.64 %, prix 8.5618), p(touche) 36.0 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.104–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.55 %, prix 8.3847), p(touche) 38.75 % (en stress 95.4 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.518–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (15.28 %, prix 7.8535), p(touche) 31.51 % (en stress 96.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.222–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (19.1 %, prix 7.4994), p(touche) 38.96 % (en stress 98.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.091 | EV/share : $0.023 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.117 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.5 | bear 7.1 | side 9.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 158.0 (= 17 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.1% → cible +5.42% / stop −2.709%, p_fill 82%, n_eff≈34.4) : P(cible|rempli) **26%** · **EV/risk +0.063** (×p_fill ; si rempli +0.21% du capital)
  - **swing** (entrée dip −2.421% → cible +12.04% / stop −7.829%, p_fill 75%, n_eff≈30.6) : P(cible|rempli) **20%** · **EV/risk -0.155** (×p_fill ; si rempli -1.61% du capital)
  - **deep** (entrée dip −3.741% → cible +14.709% / stop −11.904%, p_fill 67%, n_eff≈29.6) : P(cible|rempli) **39%** · **EV/risk -0.003** (×p_fill ; si rempli -0.05% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→81% · +2.0%→66% · +3.0%→61% · +5.0%→39% · +8.0%→11%
- Range intraday médian 7.39% (p90 12.48%) · excursion haute méd. +3.55% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.824% vs midi 1.503% vs clôture 1.831% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. 0.265% ; recovery-V 38%
- **σ réalisé intraday** 4.596% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 66% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 9.4947 (VA 9.3901–9.5761 ; dernier close 9.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 48% · rebond 76% · **stop −5.09%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 58% (gap-down >1% 36% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −2.96%) · haut méd +1.2% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.8%) · haut méd +1.86% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.73% (p90 −4.61%) · haut méd +2.25% · range méd 4.41%
- Excursion ouverture 60min (n=160) : bas méd −2.09% (p90 −5.56%) · haut méd +2.62% · range méd 5.22%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 81% (131/159) · gap 50% · délai 0.0min · rebond 67% (83/131) (MFE +1.9%)
   - −1.0% : fill 30min 66% · séance 78% (125/159) · gap 36% · délai 0.0min · rebond 67% (81/125) (MFE +2.13%)
   - −1.5% : fill 30min 63% · séance 73% (118/159) · gap 31% · délai 0.0min · rebond 74% (87/118) (MFE +2.12%)
   - −2.0% : fill 30min 56% · séance 65% (110/159) · gap 26% · délai 0.6min · rebond 70% (78/110) (MFE +2.23%)
   - −3.0% : fill 30min 43% · séance 54% (96/159) · gap 10% · délai 4.4min · rebond 76% (78/96) (MFE +2.23%)
   - −4.0% : fill 30min 34% · séance 48% (84/159) · gap 5% · délai 8.8min · rebond 76% (64/84) (MFE +2.53%)
   - −5.0% : fill 30min 24% · séance 40% (66/159) · gap 2% · délai 22.4min · rebond 76% (50/66) (MFE +2.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.66%) → stop au-delà de −1.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.68%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −3.23%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1164 jambes) : jambe baissière méd −1.33% (p90 −3.11%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (87 séances) :
      · −1.0% : fill 98% (86/87) · rebond 64% (55/86)
      · −2.0% : fill 91% (81/87) · rebond 74% (61/81)
      · −3.0% : fill 81% (75/87) · rebond 79% (63/75)
      · −4.0% : fill 74% (67/87) · rebond 79% (54/67)
      · −5.0% : fill 61% (51/87) · rebond 80% (41/51)
   - **flat** (11 séances) :
      · −1.0% : fill 92% (9/11) · rebond 49% (5/9)
      · −2.0% : fill 80% (7/11) · rebond 41% (3/7)
      · −3.0% : fill 80% (7/11) · rebond 51% (4/7)
      · −4.0% : fill 80% (7/11) · rebond 61% (4/7)
      · −5.0% : fill 61% (5/11) · rebond 79% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 48% (30/61) · rebond 82% (21/30)
      · −2.0% : fill 28% (22/61) · rebond 61% (14/22)
      · −3.0% : fill 12% (14/61) · rebond 73% (11/14)
      · −4.0% : fill 9% (10/61) · rebond 54% (6/10)
      · −5.0% : fill 9% (10/61) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 66% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 88% si début vert vs 10% si rouge (base 47% · écart 79 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **88%** · continue >prix actuel 55% ; creux résiduel méd -1.59% (q20 -3.4%) → **SL/trailing à −3.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.43% / q75 +3.62% → **scale +2.43% / runner +3.62%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **10%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +1.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.33% .. +4.9%] · haut q95 +6.22% · bas q05 -5.82%
   - 60min (n=160) : retour [-5.34% .. +5.47%] · haut q95 +6.78% · bas q05 -6.38%
   - 2h (n=160) : retour [-6.34% .. +5.53%] · haut q95 +8.67% · bas q05 -8.0%
   - 4h (n=160) : retour [-7.02% .. +7.27%] · haut q95 +9.67% · bas q05 -8.84%
   - 6h (n=160) : retour [-7.2% .. +8.26%] · haut q95 +10.85% · bas q05 -9.15%
   - session (n=160) : retour [-7.12% .. +9.14%] · haut q95 +10.99% · bas q05 -9.57%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 48.4  _(neutre)_
- **ADX** : 13.3  _(pas de tendance nette)_
- **MACD** : hist 0.029  _(pas de croisement recent)_
- **BB** : %B 0.49 · largeur 17.9%
- **ATR** : 0.71 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.041  _(neutre)_
- **Vol ratio** : 1.51  _(volume au-dessus de la moyenne)_
- **Choppiness** : 66.3  _(marche en range (choppy))_
- **MA** : MA20 9.29 · MA50 9.26 · MA200 13.57  _(prix < MA20)_
- **Dist MA** : MA20 -0.2% · MA50 +0.1% · MA200 -31.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (805690 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
