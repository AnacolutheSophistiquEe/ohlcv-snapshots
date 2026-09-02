# SMR

**Generated** : 2026-09-02T00:31:53.373555+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.21  

> 🟡 **WAIT-FOR-DIP** — spot +1.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $9.21 (+1.0% vs entrée) · entrée $9.12 · stop $8.85 · T1 $9.66 · R/R 2.0  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk 0.137 _(réel 5 s)_ (GBM 0.104) · ¼-Kelly 0.031 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.97% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.08–$9.17 (mid $9.12)
- Spot actuel : $9.21 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $8.85 (stop swing_plan-based (-9.29%))
- Targets : T1 $9.66 · R/R 2.0 | T2 $9.75 · R/R 2.33 | T3 $9.84 · R/R 2.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.85


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.37 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.29 %)** : le gap seul le franchit 0.619 % des séances (7 fois sur 1130).
   - exécution **4.274 pt plus bas** dans le cas TYPIQUE (médiane), 13.179 au p90, **21.033 au pire**
   - perte réelle **15.541 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 9.29 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0387 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.455 % | p01 -6.962 % | pire -30.323 % _(sur 1130 séances)_
- **P(stop avant cible)** _(source : daily, 1131 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5339** [0.4595 ; 0.6071] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5375** [0.4848 ; 0.5896] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.5342** [0.4815 ; 0.5864] _(largeur 10.5 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.3 pt), swing (32.6 pt), deep (33.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.93 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.02 % contre 5.91 % aujourd'hui, rapport 1.86)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.96 % vs -18.66 % si l'on extrapolait par √5 _(rapport 1.016 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6027** (β de hausse 1.3622, asymétrie 1.1765) vs IWM — 537 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.974× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.0475 sur atr_grid (1.75 ATR, 12.622 %) — p(stop avant cible) 0.4875 [0.44 ; 0.54], R/R 0.895, perte reelle 18.976 % (gap inclus), CVaR 12.644 %, EV -4.1452 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0537 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.64 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.62 ATR (stop 7.199 %) — p(stop avant cible) 0.7156 [0.67 ; 0.76], R/R 1.258, perte reelle 13.499 % (gap inclus), EV -5.5066 % — **REFUSE**
      - refuse : p_stop_first 0.716, borne haute 0.761 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.51 %) : P(cible) 23.1 % x 16.98 % + P(rien) 5.3 % x 4.29 % ne couvrent pas P(stop) 71.6 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.02 ATR (stop 10.088 %) — p(stop avant cible) 0.584 [0.53 ; 0.64], R/R 1.032, perte reelle 16.461 % (gap inclus), EV -4.827 % — **REFUSE**
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 46.1 % de casse (IC clusterise [0.427 ; 0.494] sur 1133 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.83 %) : P(cible) 28.0 % x 16.98 % + P(rien) 13.6 % x 0.27 % ne couvrent pas P(stop) 58.4 % x 16.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.01 ATR (stop 24.42 %) — p(stop avant cible) 0.1326 [0.10 ; 0.17], R/R 0.56, perte reelle 30.323 % (gap inclus), EV -1.3768 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 33.0 % x 16.98 % + P(rien) 53.7 % x -5.52 % ne couvrent pas P(stop) 13.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.803 %) — p(stop avant cible) 0.9164 [0.88 ; 0.94], R/R 4.538, perte reelle 3.742 % (gap inclus), EV -2.122 % — **REFUSE**
      - refuse : cible atteinte seulement 7.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.916, borne haute 0.942 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 7.6 % x 16.98 % + P(rien) 0.7 % x 1.13 % ne couvrent pas P(stop) 91.6 % x 3.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 12.622 %) — p(stop avant cible) 0.4875 [0.44 ; 0.54], R/R 0.895, perte reelle 18.976 % (gap inclus), EV -4.1452 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.15 %) : P(cible) 30.9 % x 16.98 % + P(rien) 20.4 % x -0.66 % ne couvrent pas P(stop) 48.8 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.425 %) — p(stop avant cible) 0.4241 [0.37 ; 0.48], R/R 0.817, perte reelle 20.78 % (gap inclus), EV -3.5443 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.54 %) : P(cible) 31.8 % x 16.98 % + P(rien) 25.8 % x -0.50 % ne couvrent pas P(stop) 42.4 % x 20.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.228 %) — p(stop avant cible) 0.3509 [0.30 ; 0.40], R/R 0.714, perte reelle 23.778 % (gap inclus), EV -3.4617 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.46 %) : P(cible) 32.6 % x 16.98 % + P(rien) 32.3 % x -2.01 % ne couvrent pas P(stop) 35.1 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 18.032 %) — p(stop avant cible) 0.2968 [0.25 ; 0.35], R/R 0.56, perte reelle 30.323 % (gap inclus), EV -4.425 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.42 %) : P(cible) 32.8 % x 16.98 % + P(rien) 37.5 % x -2.64 % ne couvrent pas P(stop) 29.7 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 19.835 %) — p(stop avant cible) 0.2272 [0.19 ; 0.27], R/R 0.56, perte reelle 30.323 % (gap inclus), EV -2.9998 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.00 %) : P(cible) 32.9 % x 16.98 % + P(rien) 44.4 % x -3.83 % ne couvrent pas P(stop) 22.7 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 28.851 %) — p(stop avant cible) 0.0701 [0.05 ; 0.10], R/R 0.56, perte reelle 30.323 % (gap inclus), EV -0.5167 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 33.0 % x 16.98 % + P(rien) 60.0 % x -6.67 % ne couvrent pas P(stop) 7.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 32.457 %) — p(stop avant cible) 0.0407 [0.02 ; 0.07], R/R 0.523, perte reelle 32.457 % (gap inclus), EV -0.4031 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 33.0 % x 16.98 % + P(rien) 62.9 % x -7.46 % ne couvrent pas P(stop) 4.1 % x 32.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 36.063 %) — p(stop avant cible) 0.0296 [0.02 ; 0.05], R/R 0.471, perte reelle 36.063 % (gap inclus), EV -0.4258 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 33.0 % x 16.98 % + P(rien) 64.0 % x -7.76 % ne couvrent pas P(stop) 3.0 % x 36.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 39.67 %) — p(stop avant cible) 0.0187 [0.01 ; 0.04], R/R 0.428, perte reelle 39.67 % (gap inclus), EV -0.4719 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 33.0 % x 16.98 % + P(rien) 65.1 % x -8.21 % ne couvrent pas P(stop) 1.9 % x 39.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 43.276 %) — p(stop avant cible) 0.0128 [0.00 ; 0.03], R/R 0.392, perte reelle 43.276 % (gap inclus), EV -0.4489 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 33.0 % x 16.98 % + P(rien) 65.7 % x -8.38 % ne couvrent pas P(stop) 1.3 % x 43.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 46.882 %) — p(stop avant cible) 0.008 [0.00 ; 0.02], R/R 0.362, perte reelle 46.882 % (gap inclus), EV -0.4649 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 33.0 % x 16.98 % + P(rien) 66.1 % x -8.62 % ne couvrent pas P(stop) 0.8 % x 46.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 50.489 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.336, perte reelle 50.489 % (gap inclus), EV -0.4603 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 33.0 % x 16.98 % + P(rien) 66.8 % x -8.94 % ne couvrent pas P(stop) 0.2 % x 50.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 54.095 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.314, perte reelle 54.095 % (gap inclus), EV -0.4597 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 33.0 % x 16.98 % + P(rien) 66.9 % x -9.05 % ne couvrent pas P(stop) 0.0 % x 54.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 57.701 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.294, perte reelle 57.701 % (gap inclus), EV -0.4551 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 33.0 % x 16.98 % + P(rien) 67.0 % x -9.06 % ne couvrent pas P(stop) 0.0 % x 57.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.21, ATR14 0.6643 (7.213 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.429 ATR = 3.094 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.361 % | 9.1768 | 92.64 % | 95.17 % | 96.43 % | 97.11 % | 97.91 % | 98.35 % |
| 0.1 ATR | 0.721 % | 9.1436 | 86.9 % | 91.37 % | 93.32 % | 94.69 % | 96.17 % | 97.41 % |
| 0.15 ATR | 1.082 % | 9.1104 | 80.92 % | 87.11 % | 89.75 % | 91.69 % | 93.84 % | 96.0 % |
| 0.2 ATR | 1.443 % | 9.0771 | 75.4 % | 82.85 % | 86.52 % | 89.26 % | 92.22 % | 94.95 % |
| 0.25 ATR | 1.803 % | 9.0439 | 70.11 % | 79.75 % | 83.87 % | 87.07 % | 90.59 % | 93.77 % |
| 0.35 ATR | 2.524 % | 8.9775 | 58.39 % | 72.15 % | 77.42 % | 82.79 % | 87.57 % | 91.3 % |
| 0.5 ATR | 3.606 % | 8.8779 | 42.41 % | 59.15 % | 67.28 % | 74.25 % | 83.04 % | 88.25 % |
| 0.75 ATR | 5.409 % | 8.7118 | 20.69 % | 37.4 % | 47.81 % | 59.58 % | 72.36 % | 80.61 % |
| 1.0 ATR | 7.213 % | 8.5457 | 11.38 % | 25.89 % | 35.94 % | 49.19 % | 64.46 % | 74.85 % |
| 1.25 ATR | 9.016 % | 8.3796 | 4.71 % | 16.0 % | 25.23 % | 38.57 % | 54.94 % | 68.51 % |
| 1.5 ATR | 10.819 % | 8.2136 | 2.3 % | 9.78 % | 16.24 % | 28.29 % | 45.41 % | 61.81 % |
| 2.0 ATR | 14.425 % | 7.8814 | 0.34 % | 3.22 % | 6.45 % | 14.55 % | 31.36 % | 49.59 % |
| 2.5 ATR | 18.032 % | 7.5493 | 0.11 % | 1.27 % | 2.76 % | 6.81 % | 20.56 % | 38.78 % |
| 3.0 ATR | 21.638 % | 7.2171 | 0.11 % | 0.58 % | 1.73 % | 3.7 % | 11.85 % | 28.79 % |
| 4.0 ATR | 28.851 % | 6.5529 | 0.0 % | 0.23 % | 0.35 % | 1.04 % | 4.53 % | 13.87 % |
| 6.0 ATR | 43.276 % | 5.2243 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.65 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.48 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.86 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.29 ATR | 2.79 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.29 ATR | 2.53 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 0.99 ATR | 1.98 ATR | 2.21 ATR | 2.79 ATR | 3.25 ATR | 3.59 ATR | 4.63 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.476–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.606 %, prix 8.8779), p(touche) 42.41 % (en stress 81.61 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.409 %, prix 8.7118), p(touche) 37.4 % (en stress 88.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.1 % des re-echantillons)
- **3 seance(s)** : plage utile 0.809–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.213 %, prix 8.5457), p(touche) 35.94 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.099–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.016 %, prix 8.3796), p(touche) 38.57 % (en stress 95.4 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.515–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.425 %, prix 7.8815), p(touche) 31.36 % (en stress 96.55 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.212–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.032 %, prix 7.5493), p(touche) 38.78 % (en stress 98.84 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.104 | EV/share : $0.028 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.125 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.7 | bear 6.9 | side 9.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.949% → cible +5.94% / stop −2.969%, p_fill 87%, n_eff≈36.2) : P(cible|rempli) **28%** · **EV/risk +0.137** (×p_fill ; si rempli +0.47% du capital)
  - **swing** (entrée dip −2.077% → cible +12.375% / stop −7.366%, p_fill 81%, n_eff≈32.5) : P(cible|rempli) **38%** · **EV/risk +0.188** (×p_fill ; si rempli +1.71% du capital)
  - **deep** (entrée dip −3.212% → cible +15.268% / stop −11.177%, p_fill 75%, n_eff≈29.6) : P(cible|rempli) **32%** · **EV/risk +0.074** (×p_fill ; si rempli +1.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→80% · +2.0%→69% · +3.0%→62% · +5.0%→38% · +8.0%→10%
- Range intraday médian 7.13% (p90 12.01%) · excursion haute méd. +3.55% / basse méd. −3.13%
- Profil de vol intra : ouverture 4.685% vs midi 1.465% vs clôture 1.752% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.071)_ ; drift intra méd. 0.109% ; recovery-V 38%
- **σ réalisé intraday** 4.516% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 9.2767 (VA 9.2312–9.3027 ; dernier close 9.275)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 75% · **stop −4.29%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 57% (gap-down >1% 37% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.1% (p90 −3.03%) · haut méd +1.24% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.83%) · haut méd +1.87% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −1.61% (p90 −4.66%) · haut méd +2.23% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.15% (p90 −5.49%) · haut méd +2.56% · range méd 5.16%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (130/159) · gap 50% · délai 0.0min · rebond 66% (83/130) (MFE +1.68%)
   - −1.0% : fill 30min 64% · séance 77% (124/159) · gap 38% · délai 0.0min · rebond 66% (79/124) (MFE +2.1%)
   - −1.5% : fill 30min 60% · séance 72% (117/159) · gap 27% · délai 0.0min · rebond 70% (84/117) (MFE +2.04%)
   - −2.0% : fill 30min 52% · séance 64% (108/159) · gap 23% · délai 0.8min · rebond 66% (74/108) (MFE +1.98%)
   - −3.0% : fill 30min 40% · séance 53% (94/159) · gap 9% · délai 4.6min · rebond 75% (75/94) (MFE +2.03%)
   - −4.0% : fill 30min 32% · séance 48% (84/159) · gap 4% · délai 9.8min · rebond 75% (64/84) (MFE +2.36%)
   - −5.0% : fill 30min 23% · séance 41% (66/159) · gap 2% · délai 24.0min · rebond 75% (49/66) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −2.67%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.7%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.17% (p90 −2.82%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1151 jambes) : jambe baissière méd −1.34% (p90 −3.15%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (87 séances) :
      · −1.0% : fill 99% (86/87) · rebond 64% (55/86)
      · −2.0% : fill 89% (80/87) · rebond 72% (59/80)
      · −3.0% : fill 80% (74/87) · rebond 80% (62/74)
      · −4.0% : fill 73% (67/87) · rebond 81% (54/67)
      · −5.0% : fill 61% (51/87) · rebond 82% (41/51)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 48% (4/8)
      · −2.0% : fill 80% (6/10) · rebond 40% (2/6)
      · −3.0% : fill 80% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 80% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 60% (4/10) · rebond 79% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 46% (30/62) · rebond 74% (20/30)
      · −2.0% : fill 29% (22/62) · rebond 52% (13/22)
      · −3.0% : fill 15% (14/62) · rebond 51% (10/14)
      · −4.0% : fill 12% (11/62) · rebond 35% (6/11)
      · −5.0% : fill 12% (11/62) · rebond 27% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (74 cas) · 34% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 82% si début vert vs 17% si rouge (base 48% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **82%** · continue >prix actuel 60% ; creux résiduel méd -1.54% (q20 -3.85%) → **SL/trailing à −3.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.2% / q75 +4.13% → **scale +3.2% / runner +4.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.42%** (au-delà de la MAE q10 -5.42%), cible rebond +1.61% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.14% .. +4.67%] · haut q95 +6.17% · bas q05 -5.75%
   - 60min (n=160) : retour [-5.17% .. +4.83%] · haut q95 +6.75% · bas q05 -6.33%
   - 2h (n=160) : retour [-6.23% .. +5.46%] · haut q95 +7.96% · bas q05 -7.96%
   - 4h (n=160) : retour [-7.18% .. +7.07%] · haut q95 +8.86% · bas q05 -8.25%
   - 6h (n=160) : retour [-7.03% .. +8.18%] · haut q95 +10.47% · bas q05 -9.07%
   - session (n=160) : retour [-7.02% .. +8.98%] · haut q95 +10.76% · bas q05 -8.99%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.86%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 46.4  _(neutre)_
- **ADX** : 13.9  _(pas de tendance nette)_
- **MACD** : hist -0.001  _(bearish_recent)_
- **BB** : %B 0.36 · largeur 13.6%
- **ATR** : 0.66 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.035  _(neutre)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 63.8  _(marche en range (choppy))_
- **MA** : MA20 9.39 · MA50 9.15 · MA200 13.2  _(prix < MA20)_
- **Dist MA** : MA20 -1.9% · MA50 +0.7% · MA200 -30.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (772657 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
