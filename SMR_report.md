# SMR

**Generated** : 2026-09-23T00:43:49.688091+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $8.89  

> 🟡 **WAIT-FOR-DIP** — spot +0.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $8.89 (+0.6% vs entrée) · entrée $8.84 · stop $8.44 · T1 $9.65 · R/R 2.02  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk 0.062 _(réel 5 s)_ (GBM 0.119) · ¼-Kelly 0.06 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.57% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.4 % ≠ (strike 9.0 − spot 8.89)/spot = +1.2 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.80–$8.89 (mid $8.84)
- Spot actuel : $8.89 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : $8.44 (stop swing_plan-based (-9.41%))
- Targets : T1 $9.65 · R/R 2.02 | T2 $9.66 · R/R 2.05 | T3 $9.84 · R/R 2.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.44


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.47 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.41 %)** : le gap seul le franchit 0.612 % des séances (7 fois sur 1144).
   - exécution **4.154 pt plus bas** dans le cas TYPIQUE (médiane), 13.059 au p90, **20.913 au pire**
   - perte réelle **15.541 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 9.41 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0375 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.482 % | p01 -6.96 % | pire -30.323 % _(sur 1144 séances)_
- **P(stop avant cible)** _(source : daily, 1145 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3233** [0.257 ; 0.3955] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.4549** [0.4029 ; 0.5076] _(largeur 10.5 pt, n_eff 345.3)_
   - deep : **0.4406** [0.3889 ; 0.4933] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.8 pt), swing (29.9 pt), deep (31.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.99 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.82 % contre 6.29 % aujourd'hui, rapport 1.72)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.22 % vs -18.74 % si l'on extrapolait par √5 _(rapport 1.026 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6144** (β de hausse 1.3726, asymétrie 1.1762) vs IWM — 544 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.948× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 7.6837 sur swing_based (1.33 ATR, 13.569 %) — p(stop avant cible) 0.4464 [0.39 ; 0.50], R/R 1.154, perte reelle 20.78 % (gap inclus), CVaR 13.588 %, EV -3.5875 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1323 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 13.59 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.16 ATR (stop 3.718 %) — p(stop avant cible) 0.8501 [0.81 ; 0.88], R/R 3.692, perte reelle 6.497 % (gap inclus), EV -2.7409 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.850, borne haute 0.885 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.74 %) : P(cible) 10.3 % x 23.99 % + P(rien) 4.7 % x 6.48 % ne couvrent pas P(stop) 85.0 % x 6.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 0.48 ATR (stop 6.431 %) — p(stop avant cible) 0.7528 [0.71 ; 0.80], R/R 2.061, perte reelle 11.636 % (gap inclus), EV -4.3818 % — **REFUSE**
      - refuse : p_stop_first 0.753, borne haute 0.796 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.06 ATR du spot — compartiment <1, mesure a 47.1 % de casse (IC clusterise [0.438 ; 0.505] sur 1121 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.38 %) : P(cible) 15.8 % x 23.99 % + P(rien) 8.9 % x 6.58 % ne couvrent pas P(stop) 75.3 % x 11.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.33 ATR (stop 13.569 %) — p(stop avant cible) 0.4464 [0.39 ; 0.50], R/R 1.154, perte reelle 20.78 % (gap inclus), EV -3.5875 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.59 %) : P(cible) 20.7 % x 23.99 % + P(rien) 34.6 % x 2.08 % ne couvrent pas P(stop) 44.6 % x 20.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.25 ATR (stop 21.279 %) — p(stop avant cible) 0.1935 [0.15 ; 0.24], R/R 0.791, perte reelle 30.323 % (gap inclus), EV -2.1486 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.15 %) : P(cible) 21.2 % x 23.99 % + P(rien) 59.5 % x -2.28 % ne couvrent pas P(stop) 19.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 8.416 %) — p(stop avant cible) 0.6641 [0.61 ; 0.71], R/R 1.777, perte reelle 13.499 % (gap inclus), EV -3.9314 % — **REFUSE**
      - refuse : p_stop_first 0.664, borne haute 0.712 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.93 %) : P(cible) 17.6 % x 23.99 % + P(rien) 16.0 % x 5.01 % ne couvrent pas P(stop) 66.4 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 14.729 %) — p(stop avant cible) 0.4261 [0.37 ; 0.48], R/R 1.154, perte reelle 20.78 % (gap inclus), EV -3.1274 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.13 %) : P(cible) 20.8 % x 23.99 % + P(rien) 36.5 % x 1.99 % ne couvrent pas P(stop) 42.6 % x 20.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 23.145 %) — p(stop avant cible) 0.1548 [0.12 ; 0.20], R/R 0.791, perte reelle 30.323 % (gap inclus), EV -1.3991 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 21.2 % x 23.99 % + P(rien) 63.4 % x -2.81 % ne couvrent pas P(stop) 15.5 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 25.249 %) — p(stop avant cible) 0.1097 [0.08 ; 0.15], R/R 0.791, perte reelle 30.323 % (gap inclus), EV -0.6765 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 21.2 % x 23.99 % + P(rien) 67.8 % x -3.59 % ne couvrent pas P(stop) 11.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 29.457 %) — p(stop avant cible) 0.0623 [0.04 ; 0.09], R/R 0.791, perte reelle 30.323 % (gap inclus), EV -0.2092 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 21.2 % x 23.99 % + P(rien) 72.6 % x -4.69 % ne couvrent pas P(stop) 6.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 33.665 %) — p(stop avant cible) 0.0352 [0.02 ; 0.06], R/R 0.712, perte reelle 33.665 % (gap inclus), EV -0.102 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 21.2 % x 23.99 % + P(rien) 75.3 % x -5.32 % ne couvrent pas P(stop) 3.5 % x 33.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 37.874 %) — p(stop avant cible) 0.0215 [0.01 ; 0.04], R/R 0.633, perte reelle 37.874 % (gap inclus), EV -0.124 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 21.2 % x 23.99 % + P(rien) 76.6 % x -5.74 % ne couvrent pas P(stop) 2.1 % x 37.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 42.082 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 0.57, perte reelle 42.082 % (gap inclus), EV -0.104 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 21.2 % x 23.99 % + P(rien) 77.6 % x -6.03 % ne couvrent pas P(stop) 1.2 % x 42.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 46.29 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 0.518, perte reelle 46.29 % (gap inclus), EV -0.1274 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 21.2 % x 23.99 % + P(rien) 78.0 % x -6.24 % ne couvrent pas P(stop) 0.7 % x 46.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 50.498 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.475, perte reelle 50.498 % (gap inclus), EV -0.1283 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 21.2 % x 23.99 % + P(rien) 78.6 % x -6.51 % ne couvrent pas P(stop) 0.2 % x 50.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 54.706 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.438, perte reelle 54.706 % (gap inclus), EV -0.1262 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 21.2 % x 23.99 % + P(rien) 78.8 % x -6.60 % ne couvrent pas P(stop) 0.0 % x 54.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 58.915 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.407, perte reelle 58.915 % (gap inclus), EV -0.1211 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 21.2 % x 23.99 % + P(rien) 78.8 % x -6.61 % ne couvrent pas P(stop) 0.0 % x 58.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 63.123 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.38, perte reelle 63.123 % (gap inclus), EV -0.1211 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 63.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 21.2 % x 23.99 % + P(rien) 78.8 % x -6.61 % ne couvrent pas P(stop) 0.0 % x 63.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 67.331 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.356, perte reelle 67.331 % (gap inclus), EV -0.1211 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 67.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 21.2 % x 23.99 % + P(rien) 78.8 % x -6.61 % ne couvrent pas P(stop) 0.0 % x 67.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 8.89, ATR14 0.7482 (8.416 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.427 ATR = 3.594 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.421 % | 8.8526 | 92.42 % | 95.13 % | 96.37 % | 97.05 % | 97.94 % | 98.38 % |
| 0.1 ATR | 0.842 % | 8.8152 | 86.65 % | 91.28 % | 93.31 % | 94.66 % | 96.23 % | 97.46 % |
| 0.15 ATR | 1.262 % | 8.7778 | 80.66 % | 86.98 % | 89.68 % | 91.7 % | 93.94 % | 96.07 % |
| 0.2 ATR | 1.683 % | 8.7404 | 74.89 % | 82.67 % | 86.39 % | 89.2 % | 92.34 % | 95.03 % |
| 0.25 ATR | 2.104 % | 8.7029 | 69.68 % | 79.61 % | 83.79 % | 87.05 % | 90.63 % | 93.87 % |
| 0.35 ATR | 2.946 % | 8.6281 | 58.14 % | 72.14 % | 77.32 % | 82.73 % | 87.66 % | 91.45 % |
| 0.5 ATR | 4.208 % | 8.5159 | 42.19 % | 58.89 % | 66.89 % | 74.09 % | 83.2 % | 88.44 % |
| 0.75 ATR | 6.312 % | 8.3288 | 20.7 % | 37.37 % | 47.62 % | 59.55 % | 72.34 % | 80.92 % |
| 1.0 ATR | 8.416 % | 8.1418 | 11.43 % | 25.93 % | 35.83 % | 49.32 % | 64.46 % | 75.03 % |
| 1.25 ATR | 10.52 % | 7.9547 | 4.75 % | 16.08 % | 25.17 % | 38.64 % | 54.86 % | 68.55 % |
| 1.5 ATR | 12.625 % | 7.7677 | 2.26 % | 9.85 % | 16.33 % | 28.52 % | 45.37 % | 61.73 % |
| 2.0 ATR | 16.833 % | 7.3936 | 0.34 % | 3.28 % | 6.58 % | 14.77 % | 31.2 % | 48.79 % |
| 2.5 ATR | 21.041 % | 7.0195 | 0.11 % | 1.36 % | 2.95 % | 6.93 % | 20.57 % | 38.15 % |
| 3.0 ATR | 25.249 % | 6.6454 | 0.11 % | 0.57 % | 1.93 % | 3.86 % | 11.66 % | 28.32 % |
| 4.0 ATR | 33.665 % | 5.8971 | 0.0 % | 0.23 % | 0.34 % | 1.14 % | 4.46 % | 13.64 % |
| 6.0 ATR | 50.498 % | 4.4007 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.38 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.25 ATR | 1.40 ATR | 1.82 ATR | 2.22 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.63 ATR | 1.81 ATR | 2.30 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.29 ATR | 2.53 ATR | 3.23 ATR | 3.92 ATR |
| **20 s.** | 1.00 ATR | 1.95 ATR | 2.18 ATR | 2.76 ATR | 3.23 ATR | 3.57 ATR | 4.61 ATR | 5.44 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.474–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.208 %, prix 8.5159), p(touche) 42.19 % (en stress 82.02 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.661–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.312 %, prix 8.3289), p(touche) 37.37 % (en stress 88.76 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (70.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.806–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.416 %, prix 8.1418), p(touche) 35.83 % (en stress 89.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.101–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.52 %, prix 7.9548), p(touche) 38.64 % (en stress 95.45 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.513–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.833 %, prix 7.3935), p(touche) 31.2 % (en stress 96.59 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.178–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.119 | EV/share : $0.048 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.242 | ¼-Kelly 0.06 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 50.7 | bear 12.5 | side 36.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.523% → cible +9.143% / stop −4.571%, p_fill 87%, n_eff≈37.1) : P(cible|rempli) **3%** · **EV/risk +0.062** (×p_fill ; si rempli +0.33% du capital)
  - **swing** (entrée dip −0.994% → cible +9.806% / stop −8.5%, p_fill 97%, n_eff≈38.9) : P(cible|rempli) **40%** · **EV/risk +0.143** (×p_fill ; si rempli +1.25% du capital)
  - **deep** (entrée dip −1.395% → cible +16.306% / stop −12.803%, p_fill 91%, n_eff≈35.0) : P(cible|rempli) **23%** · **EV/risk +0.145** (×p_fill ; si rempli +2.04% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→92% · +1.0%→81% · +2.0%→70% · +3.0%→64% · +5.0%→39% · +8.0%→10%
- Range intraday médian 7.03% (p90 12.01%) · excursion haute méd. +3.75% / basse méd. −2.71%
- Profil de vol intra : ouverture 4.625% vs midi 1.437% vs clôture 1.737% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.074)_ ; drift intra méd. 0.451% ; recovery-V 48%
- **σ réalisé intraday** 4.311% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 60% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 9.4737 (VA 9.4479–9.5856 ; dernier close 9.695)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 76% · **stop −4.13%** sous le fill (sous le bruit) · cible +2.5% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. -0.56% · baisse 58% (gap-down >1% 36% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −2.93%) · haut méd +1.22% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.78%) · haut méd +1.87% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.55% (p90 −4.61%) · haut méd +2.23% · range méd 4.13%
- Excursion ouverture 60min (n=160) : bas méd −2.06% (p90 −5.35%) · haut méd +2.64% · range méd 5.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (130/159) · gap 52% · délai 0.0min · rebond 64% (82/130) (MFE +1.62%)
   - −1.0% : fill 30min 63% · séance 75% (123/159) · gap 37% · délai 0.0min · rebond 65% (77/123) (MFE +2.03%)
   - −1.5% : fill 30min 59% · séance 70% (116/159) · gap 27% · délai 0.0min · rebond 71% (83/116) (MFE +1.99%)
   - −2.0% : fill 30min 51% · séance 62% (107/159) · gap 23% · délai 0.7min · rebond 68% (73/107) (MFE +1.98%)
   - −3.0% : fill 30min 39% · séance 53% (93/159) · gap 10% · délai 4.6min · rebond 76% (74/93) (MFE +2.31%)
   - −4.0% : fill 30min 32% · séance 46% (83/159) · gap 4% · délai 8.7min · rebond 76% (63/83) (MFE +2.53%)
   - −5.0% : fill 30min 23% · séance 40% (65/159) · gap 2% · délai 22.3min · rebond 76% (49/65) (MFE +2.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.66%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.68%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.05% (p90 −2.75%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1137 jambes) : jambe baissière méd −1.34% (p90 −3.08%) · ~13.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (89 séances) :
      · −1.0% : fill 96% (87/89) · rebond 63% (55/87)
      · −2.0% : fill 86% (81/89) · rebond 74% (60/81)
      · −3.0% : fill 78% (75/89) · rebond 82% (63/75)
      · −4.0% : fill 69% (67/89) · rebond 82% (54/67)
      · −5.0% : fill 58% (51/89) · rebond 83% (42/51)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 48% (4/8)
      · −2.0% : fill 80% (6/10) · rebond 40% (2/6)
      · −3.0% : fill 80% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 80% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 60% (4/10) · rebond 79% (3/4)
   - **gap-up** (60 séances) :
      · −1.0% : fill 44% (28/60) · rebond 74% (18/28)
      · −2.0% : fill 27% (20/60) · rebond 51% (11/20)
      · −3.0% : fill 14% (12/60) · rebond 49% (8/12)
      · −4.0% : fill 11% (10/60) · rebond 33% (5/10)
      · −5.0% : fill 11% (10/60) · rebond 26% (4/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 65% si les 15 1res min sont vertes (74 cas) · 38% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 85% si début vert vs 20% si rouge (base 52% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **85%** · continue >prix actuel 58% ; creux résiduel méd -1.67% (q20 -3.41%) → **SL/trailing à −3.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.07% / q75 +4.06% → **scale +3.07% / runner +4.06%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **20%** (continue à baisser 55%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.4%** (au-delà de la MAE q10 -5.4%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.92% .. +4.46%] · haut q95 +6.13% · bas q05 -5.65%
   - 60min (n=160) : retour [-4.99% .. +4.69%] · haut q95 +6.67% · bas q05 -6.2%
   - 2h (n=160) : retour [-6.22% .. +5.43%] · haut q95 +7.83% · bas q05 -7.86%
   - 4h (n=160) : retour [-7.13% .. +7.01%] · haut q95 +8.38% · bas q05 -7.96%
   - 6h (n=160) : retour [-6.87% .. +8.08%] · haut q95 +9.95% · bas q05 -8.33%
   - session (n=160) : retour [-6.95% .. +8.67%] · haut q95 +10.49% · bas q05 -8.41%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.83%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 47.7  _(neutre)_
- **ADX** : 14.3  _(pas de tendance nette)_
- **MACD** : hist -0.111  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 34.0%
- **ATR** : 0.75 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.088  _(distribution)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 43.5  _(transition)_
- **MA** : MA20 9.33 · MA50 9.05 · MA200 12.44  _(prix < MA20)_
- **Dist MA** : MA20 -4.7% · MA50 -1.7% · MA200 -28.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (839765 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
