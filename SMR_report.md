# SMR

**Generated** : 2026-08-31T00:32:05.900052+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.29  

> 🟡 **WAIT-FOR-DIP** — spot +2.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $9.29 (+2.7% vs entrée) · entrée $9.05 · stop $8.35 · T1 $10.13 · R/R 1.54  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk 0.076 _(réel 5 s)_ (GBM -0.109) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $8.94–$9.17 (mid $9.05)
- Spot actuel : $9.29 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : $8.35 (stop swing_plan-based (-10.07%))
- Targets : T1 $10.13 · R/R 1.54 | T2 $10.45 · R/R 2.0 | T3 $10.76 · R/R 2.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.35


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.29 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.07 %)** : le gap seul le franchit 0.532 % des séances (6 fois sur 1128).
   - exécution **4.104 pt plus bas** dans le cas TYPIQUE (médiane), 13.708 au p90, **20.253 au pire**
   - perte réelle **16.461 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 10.07 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.034 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.429 % | p01 -6.962 % | pire -30.323 % _(sur 1128 séances)_
- **P(stop avant cible)** _(source : daily, 1129 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5754** [0.501 ; 0.6473] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.5279** [0.4752 ; 0.5801] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.5498** [0.4971 ; 0.6017] _(largeur 10.5 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.2 pt), swing (34.5 pt), deep (35.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.94 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.02 % contre 5.92 % aujourd'hui, rapport 1.86)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.96 % vs -18.67 % si l'on extrapolait par √5 _(rapport 1.016 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6018** (β de hausse 1.3622, asymétrie 1.1759) vs IWM — 535 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.022× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.065 sur atr_grid (1.75 ATR, 13.186 %) — p(stop avant cible) 0.462 [0.41 ; 0.51], R/R 0.832, perte reelle 18.976 % (gap inclus), CVaR 13.207 %, EV -3.6411 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1005 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 13.21 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.71 ATR (stop 7.842 %) — p(stop avant cible) 0.6819 [0.63 ; 0.73], R/R 1.17, perte reelle 13.499 % (gap inclus), EV -4.9038 % — **REFUSE**
      - refuse : p_stop_first 0.682, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.90 %) : P(cible) 26.6 % x 15.79 % + P(rien) 5.2 % x 1.95 % ne couvrent pas P(stop) 68.2 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.09 ATR (stop 10.667 %) — p(stop avant cible) 0.5634 [0.51 ; 0.61], R/R 0.894, perte reelle 17.667 % (gap inclus), EV -5.1108 % — **REFUSE**
      - refuse : p_stop_first 0.563, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.61 ATR du spot — compartiment <1, mesure a 45.9 % de casse (IC clusterise [0.428 ; 0.490] sur 1144 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.11 %) : P(cible) 31.3 % x 15.79 % + P(rien) 12.4 % x -0.75 % ne couvrent pas P(stop) 56.3 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.97 ATR (stop 24.876 %) — p(stop avant cible) 0.1307 [0.10 ; 0.17], R/R 0.521, perte reelle 30.323 % (gap inclus), EV -1.3486 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 36.1 % x 15.79 % + P(rien) 50.8 % x -6.07 % ne couvrent pas P(stop) 13.1 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.884 %) — p(stop avant cible) 0.8998 [0.86 ; 0.93], R/R 4.067, perte reelle 3.882 % (gap inclus), EV -2.0566 % — **REFUSE**
      - refuse : cible atteinte seulement 9.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.900, borne haute 0.928 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 9.1 % x 15.79 % + P(rien) 0.9 % x 0.48 % ne couvrent pas P(stop) 90.0 % x 3.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 13.186 %) — p(stop avant cible) 0.462 [0.41 ; 0.51], R/R 0.832, perte reelle 18.976 % (gap inclus), EV -3.6411 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.64 %) : P(cible) 34.0 % x 15.79 % + P(rien) 19.8 % x -1.19 % ne couvrent pas P(stop) 46.2 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 15.07 %) — p(stop avant cible) 0.4011 [0.35 ; 0.45], R/R 0.664, perte reelle 23.778 % (gap inclus), EV -4.5024 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.50 %) : P(cible) 34.9 % x 15.79 % + P(rien) 24.9 % x -1.94 % ne couvrent pas P(stop) 40.1 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.954 %) — p(stop avant cible) 0.3234 [0.28 ; 0.37], R/R 0.664, perte reelle 23.778 % (gap inclus), EV -2.9912 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.99 %) : P(cible) 35.5 % x 15.79 % + P(rien) 32.1 % x -2.84 % ne couvrent pas P(stop) 32.3 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 18.837 %) — p(stop avant cible) 0.2547 [0.21 ; 0.30], R/R 0.521, perte reelle 30.323 % (gap inclus), EV -3.5517 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.55 %) : P(cible) 35.8 % x 15.79 % + P(rien) 38.7 % x -3.84 % ne couvrent pas P(stop) 25.5 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 26.372 %) — p(stop avant cible) 0.0906 [0.06 ; 0.12], R/R 0.521, perte reelle 30.323 % (gap inclus), EV -0.754 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 36.1 % x 15.79 % + P(rien) 54.8 % x -6.76 % ne couvrent pas P(stop) 9.1 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 30.14 %) — p(stop avant cible) 0.0547 [0.03 ; 0.08], R/R 0.521, perte reelle 30.323 % (gap inclus), EV -0.4413 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 36.1 % x 15.79 % + P(rien) 58.4 % x -7.68 % ne couvrent pas P(stop) 5.5 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 33.907 %) — p(stop avant cible) 0.0356 [0.02 ; 0.06], R/R 0.466, perte reelle 33.907 % (gap inclus), EV -0.4268 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 36.1 % x 15.79 % + P(rien) 60.3 % x -8.16 % ne couvrent pas P(stop) 3.6 % x 33.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 37.675 %) — p(stop avant cible) 0.0235 [0.01 ; 0.04], R/R 0.419, perte reelle 37.675 % (gap inclus), EV -0.478 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 36.1 % x 15.79 % + P(rien) 61.5 % x -8.61 % ne couvrent pas P(stop) 2.4 % x 37.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 41.442 %) — p(stop avant cible) 0.0162 [0.01 ; 0.03], R/R 0.381, perte reelle 41.442 % (gap inclus), EV -0.4984 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 36.1 % x 15.79 % + P(rien) 62.3 % x -8.89 % ne couvrent pas P(stop) 1.6 % x 41.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 45.21 %) — p(stop avant cible) 0.0104 [0.00 ; 0.03], R/R 0.349, perte reelle 45.21 % (gap inclus), EV -0.4848 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 36.1 % x 15.79 % + P(rien) 62.8 % x -9.10 % ne couvrent pas P(stop) 1.0 % x 45.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 48.977 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.322, perte reelle 48.977 % (gap inclus), EV -0.4868 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 36.1 % x 15.79 % + P(rien) 63.6 % x -9.56 % ne couvrent pas P(stop) 0.2 % x 48.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 52.745 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.299, perte reelle 52.745 % (gap inclus), EV -0.4846 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 36.1 % x 15.79 % + P(rien) 63.8 % x -9.68 % ne couvrent pas P(stop) 0.0 % x 52.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 56.512 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.279, perte reelle 56.512 % (gap inclus), EV -0.4854 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 36.1 % x 15.79 % + P(rien) 63.8 % x -9.68 % ne couvrent pas P(stop) 0.0 % x 56.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 60.28 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.262, perte reelle 60.28 % (gap inclus), EV -0.4803 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 36.1 % x 15.79 % + P(rien) 63.9 % x -9.68 % ne couvrent pas P(stop) 0.0 % x 60.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.29, ATR14 0.7 (7.535 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.429 ATR = 3.233 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.377 % | 9.255 | 92.63 % | 95.16 % | 96.42 % | 97.11 % | 97.9 % | 98.35 % |
| 0.1 ATR | 0.753 % | 9.22 | 86.98 % | 91.35 % | 93.3 % | 94.68 % | 96.16 % | 97.41 % |
| 0.15 ATR | 1.13 % | 9.185 | 80.99 % | 87.08 % | 89.72 % | 91.67 % | 93.83 % | 96.0 % |
| 0.2 ATR | 1.507 % | 9.15 | 75.46 % | 82.81 % | 86.49 % | 89.24 % | 92.2 % | 94.94 % |
| 0.25 ATR | 1.884 % | 9.115 | 70.16 % | 79.7 % | 83.83 % | 87.04 % | 90.57 % | 93.76 % |
| 0.35 ATR | 2.637 % | 9.045 | 58.41 % | 72.09 % | 77.37 % | 82.87 % | 87.54 % | 91.4 % |
| 0.5 ATR | 3.767 % | 8.94 | 42.4 % | 59.17 % | 67.21 % | 74.31 % | 83.0 % | 88.34 % |
| 0.75 ATR | 5.651 % | 8.765 | 20.74 % | 37.49 % | 47.81 % | 59.72 % | 72.41 % | 80.68 % |
| 1.0 ATR | 7.535 % | 8.59 | 11.41 % | 25.95 % | 35.91 % | 49.31 % | 64.49 % | 75.03 % |
| 1.25 ATR | 9.419 % | 8.415 | 4.72 % | 16.03 % | 25.29 % | 38.66 % | 54.95 % | 68.67 % |
| 1.5 ATR | 11.302 % | 8.24 | 2.3 % | 9.8 % | 16.28 % | 28.36 % | 45.52 % | 61.96 % |
| 2.0 ATR | 15.07 % | 7.89 | 0.35 % | 3.23 % | 6.47 % | 14.58 % | 31.43 % | 49.71 % |
| 2.5 ATR | 18.837 % | 7.54 | 0.12 % | 1.27 % | 2.77 % | 6.83 % | 20.61 % | 38.87 % |
| 3.0 ATR | 22.605 % | 7.19 | 0.12 % | 0.58 % | 1.73 % | 3.7 % | 11.87 % | 28.86 % |
| 4.0 ATR | 30.14 % | 6.49 | 0.0 % | 0.23 % | 0.35 % | 1.04 % | 4.54 % | 13.9 % |
| 6.0 ATR | 45.21 % | 5.09 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.65 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.48 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.61 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.86 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.29 ATR | 2.79 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.52 ATR | 1.94 ATR | 2.30 ATR | 2.54 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 1.00 ATR | 1.99 ATR | 2.22 ATR | 2.79 ATR | 3.26 ATR | 3.59 ATR | 4.64 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.476–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.767 %, prix 8.94), p(touche) 42.4 % (en stress 81.61 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.651 %, prix 8.765), p(touche) 37.49 % (en stress 88.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.8 % des re-echantillons)
- **3 seance(s)** : plage utile 0.809–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.535 %, prix 8.59), p(touche) 35.91 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.101–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.419 %, prix 8.415), p(touche) 38.66 % (en stress 95.4 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.518–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (15.07 %, prix 7.89), p(touche) 31.43 % (en stress 96.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.217–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.837 %, prix 7.54), p(touche) 38.87 % (en stress 98.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.109 | EV/share : $-0.076 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 21 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 78.4 | bear 8.5 | side 13.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 158.0 (= 17 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.147% → cible +5.248% / stop −2.623%, p_fill 86%, n_eff≈34.6) : P(cible|rempli) **24%** · **EV/risk +0.061** (×p_fill ; si rempli +0.19% du capital)
  - **swing** (entrée dip −2.535% → cible +11.928% / stop −7.731%, p_fill 74%, n_eff≈29.1) : P(cible|rempli) **32%** · **EV/risk +0.076** (×p_fill ; si rempli +0.79% du capital)
  - **deep** (entrée dip −3.907% → cible +22.928% / stop −11.763%, p_fill 70%, n_eff≈28.4) : P(cible|rempli) **12%** · **EV/risk +0.033** (×p_fill ; si rempli +0.55% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→80% · +2.0%→69% · +3.0%→62% · +5.0%→39% · +8.0%→11%
- Range intraday médian 7.24% (p90 12.17%) · excursion haute méd. +3.65% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.755% vs midi 1.485% vs clôture 1.763% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 80% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. 0.068% ; recovery-V 38%
- **σ réalisé intraday** 4.599% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 65% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 9.3034 (VA 9.1853–9.4722 ; dernier close 9.275)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 42% · rebond 75% · **stop −4.26%** sous le fill (sous le bruit) · cible +2.38% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.43% · baisse 56% (gap-down >1% 36% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −1.13% (p90 −3.04%) · haut méd +1.14% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.84%) · haut méd +1.75% · range méd 3.7%
- Excursion ouverture 30min (n=160) : bas méd −1.67% (p90 −4.67%) · haut méd +2.22% · range méd 4.36%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −5.51%) · haut méd +2.54% · range méd 5.16%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 79% (130/159) · gap 49% · délai 0.0min · rebond 65% (82/130) (MFE +1.62%)
   - −1.0% : fill 30min 63% · séance 76% (124/159) · gap 37% · délai 0.0min · rebond 65% (78/124) (MFE +2.08%)
   - −1.5% : fill 30min 59% · séance 72% (117/159) · gap 28% · délai 0.0min · rebond 69% (83/117) (MFE +2.04%)
   - −2.0% : fill 30min 53% · séance 65% (109/159) · gap 24% · délai 0.7min · rebond 66% (75/109) (MFE +1.98%)
   - −3.0% : fill 30min 41% · séance 54% (95/159) · gap 9% · délai 4.6min · rebond 75% (76/95) (MFE +2.04%)
   - −4.0% : fill 30min 33% · séance 49% (85/159) · gap 4% · délai 9.7min · rebond 75% (65/85) (MFE +2.37%)
   - −5.0% : fill 30min 24% · séance 42% (67/159) · gap 2% · délai 23.9min · rebond 75% (50/67) (MFE +2.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.68%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.81% (p90 −2.71%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −2.87%) → stop au-delà de −2.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1157 jambes) : jambe baissière méd −1.34% (p90 −3.15%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (87 séances) :
      · −1.0% : fill 99% (86/87) · rebond 63% (54/86)
      · −2.0% : fill 92% (81/87) · rebond 72% (60/81)
      · −3.0% : fill 82% (75/87) · rebond 81% (63/75)
      · −4.0% : fill 76% (68/87) · rebond 81% (55/68)
      · −5.0% : fill 63% (52/87) · rebond 82% (42/52)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 61% si les 15 1res min sont vertes (73 cas) · 34% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 82% si début vert vs 17% si rouge (base 47% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **82%** · continue >prix actuel 63% ; creux résiduel méd -1.67% (q20 -3.89%) → **SL/trailing à −3.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.26% / q75 +4.15% → **scale +3.26% / runner +4.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.42%** (au-delà de la MAE q10 -5.42%), cible rebond +1.61% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.18% .. +4.71%] · haut q95 +6.18% · bas q05 -5.77%
   - 60min (n=160) : retour [-5.2% .. +4.86%] · haut q95 +6.77% · bas q05 -6.34%
   - 2h (n=160) : retour [-6.23% .. +5.47%] · haut q95 +7.99% · bas q05 -7.99%
   - 4h (n=160) : retour [-7.2% .. +7.11%] · haut q95 +9.05% · bas q05 -8.31%
   - 6h (n=160) : retour [-7.06% .. +8.2%] · haut q95 +10.55% · bas q05 -9.09%
   - session (n=160) : retour [-7.04% .. +9.08%] · haut q95 +10.82% · bas q05 -9.12%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.88%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 50.9  _(neutre)_
- **ADX** : 14.3  _(pas de tendance nette)_
- **MACD** : hist 0.029  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 14.0%
- **ATR** : 0.7 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.057  _(accumulation)_
- **Vol ratio** : 1.1  _(volume normal)_
- **Choppiness** : 65.8  _(marche en range (choppy))_
- **MA** : MA20 9.39 · MA50 9.24 · MA200 13.37  _(prix < MA20)_
- **Dist MA** : MA20 -1.1% · MA50 +0.6% · MA200 -30.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (891662 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
