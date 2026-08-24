# SMR

**Generated** : 2026-08-24T00:31:36.095684+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.40  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $9.40 (+1.2% vs entrée) · entrée $9.29 · stop $9.10 · T1 $9.66 · R/R 1.95  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk 0.111 _(réel 5 s)_ (GBM 0.051) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.08% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 225 % hors [0,100] (R² max 0.71). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.24–$9.35 (mid $9.29)
- Spot actuel : $9.40 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $9.10 (stop swing_plan-based (-9.34%))
- Targets : T1 $9.66 · R/R 1.95 | T2 $10.13 · R/R 4.42 | T3 $10.15 · R/R 4.53
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.10


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.32 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.34 %)** : le gap seul le franchit 0.623 % des séances (7 fois sur 1123).
   - exécution **4.224 pt plus bas** dans le cas TYPIQUE (médiane), 13.129 au p90, **20.983 au pire**
   - perte réelle **15.541 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 9.34 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0387 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.433 % | p01 -6.963 % | pire -30.323 % _(sur 1123 séances)_
- **P(stop avant cible)** _(source : daily, 1124 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3062** [0.2412 ; 0.3776] _(largeur 13.6 pt, n_eff 173.1)_
   - swing : **0.6037** [0.5514 ; 0.6543] _(largeur 10.3 pt, n_eff 345.2)_
   - deep : **0.6188** [0.5667 ; 0.6689] _(largeur 10.2 pt, n_eff 345.1)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.1 pt), swing (33.6 pt), deep (34.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.95 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.97 % contre 5.85 % aujourd'hui, rapport 1.88)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.0 % vs -18.71 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6149** (β de hausse 1.3775, asymétrie 1.1723) vs IWM — 532 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.031× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.1129 sur atr_grid (2.0 ATR, 13.693 %) — p(stop avant cible) 0.4656 [0.41 ; 0.52], R/R 0.849, perte reelle 20.78 % (gap inclus), CVaR 13.712 %, EV -4.1624 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1427 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.85 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 13.71 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.85 ATR (stop 8.159 %) — p(stop avant cible) 0.6674 [0.62 ; 0.72], R/R 1.307, perte reelle 13.499 % (gap inclus), EV -4.3618 % — **REFUSE**
      - refuse : p_stop_first 0.667, borne haute 0.716 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.66 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.36 %) : P(cible) 25.3 % x 17.65 % + P(rien) 8.0 % x 2.34 % ne couvrent pas P(stop) 66.7 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.27 %) — p(stop avant cible) 0.5826 [0.53 ; 0.63], R/R 1.072, perte reelle 16.461 % (gap inclus), EV -4.5488 % — **REFUSE**
      - refuse : p_stop_first 0.583, borne haute 0.634 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.07 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.55 %) : P(cible) 28.3 % x 17.65 % + P(rien) 13.4 % x 0.34 % ne couvrent pas P(stop) 58.3 % x 16.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.09 ATR (stop 23.464 %) — p(stop avant cible) 0.1604 [0.12 ; 0.20], R/R 0.582, perte reelle 30.323 % (gap inclus), EV -1.758 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 33.1 % x 17.65 % + P(rien) 50.8 % x -5.38 % ne couvrent pas P(stop) 16.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.4 ATR (stop 25.605 %) — p(stop avant cible) 0.1122 [0.08 ; 0.15], R/R 0.582, perte reelle 30.323 % (gap inclus), EV -1.0109 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 33.1 % x 17.65 % + P(rien) 55.6 % x -6.21 % ne couvrent pas P(stop) 11.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 13.693 %) — p(stop avant cible) 0.4656 [0.41 ; 0.52], R/R 0.849, perte reelle 20.78 % (gap inclus), EV -4.1624 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.16 %) : P(cible) 31.6 % x 17.65 % + P(rien) 21.9 % x -0.27 % ne couvrent pas P(stop) 46.6 % x 20.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 17.116 %) — p(stop avant cible) 0.343 [0.29 ; 0.39], R/R 0.742, perte reelle 23.778 % (gap inclus), EV -3.1666 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.17 %) : P(cible) 32.7 % x 17.65 % + P(rien) 33.0 % x -2.37 % ne couvrent pas P(stop) 34.3 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 18.828 %) — p(stop avant cible) 0.2708 [0.23 ; 0.32], R/R 0.582, perte reelle 30.323 % (gap inclus), EV -3.8063 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.81 %) : P(cible) 32.9 % x 17.65 % + P(rien) 40.1 % x -3.48 % ne couvrent pas P(stop) 27.1 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 27.386 %) — p(stop avant cible) 0.0845 [0.06 ; 0.12], R/R 0.582, perte reelle 30.323 % (gap inclus), EV -0.7455 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 33.1 % x 17.65 % + P(rien) 58.4 % x -6.90 % ne couvrent pas P(stop) 8.5 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 30.809 %) — p(stop avant cible) 0.0561 [0.04 ; 0.08], R/R 0.573, perte reelle 30.809 % (gap inclus), EV -0.5521 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 33.1 % x 17.65 % + P(rien) 61.2 % x -7.63 % ne couvrent pas P(stop) 5.6 % x 30.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 34.233 %) — p(stop avant cible) 0.0345 [0.02 ; 0.06], R/R 0.515, perte reelle 34.233 % (gap inclus), EV -0.4992 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 33.2 % x 17.65 % + P(rien) 63.4 % x -8.16 % ne couvrent pas P(stop) 3.5 % x 34.23 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 37.656 %) — p(stop avant cible) 0.0242 [0.01 ; 0.04], R/R 0.469, perte reelle 37.656 % (gap inclus), EV -0.5599 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 33.2 % x 17.65 % + P(rien) 64.4 % x -8.54 % ne couvrent pas P(stop) 2.4 % x 37.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 41.079 %) — p(stop avant cible) 0.0166 [0.01 ; 0.03], R/R 0.43, perte reelle 41.079 % (gap inclus), EV -0.5725 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 33.2 % x 17.65 % + P(rien) 65.2 % x -8.81 % ne couvrent pas P(stop) 1.7 % x 41.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 44.502 %) — p(stop avant cible) 0.0131 [0.00 ; 0.03], R/R 0.397, perte reelle 44.502 % (gap inclus), EV -0.5666 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 33.2 % x 17.65 % + P(rien) 65.5 % x -8.90 % ne couvrent pas P(stop) 1.3 % x 44.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 47.926 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.368, perte reelle 47.926 % (gap inclus), EV -0.5724 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 33.2 % x 17.65 % + P(rien) 66.2 % x -9.25 % ne couvrent pas P(stop) 0.6 % x 47.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 51.349 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.344, perte reelle 51.349 % (gap inclus), EV -0.5663 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 33.2 % x 17.65 % + P(rien) 66.8 % x -9.59 % ne couvrent pas P(stop) 0.0 % x 51.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 54.772 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.322, perte reelle 54.772 % (gap inclus), EV -0.567 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 33.2 % x 17.65 % + P(rien) 66.8 % x -9.59 % ne couvrent pas P(stop) 0.0 % x 54.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.051 | EV/share : $0.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.3 | bear 6.3 | side 11.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 17 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.137% → cible +4.0% / stop −2.077%, p_fill 82%, n_eff≈34.4) : P(cible|rempli) **38%** · **EV/risk +0.111** (×p_fill ; si rempli +0.28% du capital)
  - **swing** (entrée dip −2.493% → cible +10.58% / stop −7.022%, p_fill 75%, n_eff≈30.6) : P(cible|rempli) **20%** · **EV/risk -0.197** (×p_fill ; si rempli -1.84% du capital)
  - **deep** (entrée dip −3.863% → cible +21.422% / stop −10.711%, p_fill 67%, n_eff≈29.6) : P(cible|rempli) **17%** · **EV/risk +0.011** (×p_fill ; si rempli +0.18% du capital)
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
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 50% · rebond 78% · **stop −5.05%** sous le fill (sous le bruit) · cible +2.54% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 57% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −2.96%) · haut méd +1.2% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.8%) · haut méd +1.86% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.73% (p90 −4.61%) · haut méd +2.25% · range méd 4.41%
- Excursion ouverture 60min (n=160) : bas méd −2.09% (p90 −5.56%) · haut méd +2.62% · range méd 5.22%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 81% (131/159) · gap 50% · délai 0.0min · rebond 65% (81/131) (MFE +1.84%)
   - −1.0% : fill 30min 66% · séance 78% (126/159) · gap 36% · délai 0.0min · rebond 68% (84/126) (MFE +2.13%)
   - −1.5% : fill 30min 61% · séance 73% (119/159) · gap 31% · délai 0.0min · rebond 71% (86/119) (MFE +2.0%)
   - −2.0% : fill 30min 55% · séance 65% (110/159) · gap 25% · délai 0.4min · rebond 66% (77/110) (MFE +2.15%)
   - −3.0% : fill 30min 43% · séance 55% (97/159) · gap 10% · délai 3.1min · rebond 76% (78/97) (MFE +2.02%)
   - −4.0% : fill 30min 35% · séance 50% (87/159) · gap 5% · délai 9.2min · rebond 78% (68/87) (MFE +2.54%)
   - −5.0% : fill 30min 24% · séance 40% (66/159) · gap 2% · délai 22.4min · rebond 73% (48/66) (MFE +2.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.66%) → stop au-delà de −1.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.68%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −3.23%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1164 jambes) : jambe baissière méd −1.33% (p90 −3.11%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 100% (86/86) · rebond 65% (57/86)
      · −2.0% : fill 93% (81/86) · rebond 71% (60/81)
      · −3.0% : fill 82% (75/86) · rebond 79% (62/75)
      · −4.0% : fill 76% (69/86) · rebond 82% (57/69)
      · −5.0% : fill 62% (51/86) · rebond 75% (39/51)
   - **flat** (11 séances) :
      · −1.0% : fill 79% (8/11) · rebond 54% (5/8)
      · −2.0% : fill 68% (6/11) · rebond 18% (2/6)
      · −3.0% : fill 68% (6/11) · rebond 46% (3/6)
      · −4.0% : fill 68% (6/11) · rebond 56% (3/6)
      · −5.0% : fill 57% (5/11) · rebond 79% (4/5)
   - **gap-up** (62 séances) :
      · −1.0% : fill 49% (32/62) · rebond 81% (22/32)
      · −2.0% : fill 29% (23/62) · rebond 60% (15/23)
      · −3.0% : fill 16% (16/62) · rebond 80% (13/16)
      · −4.0% : fill 12% (12/62) · rebond 67% (8/12)
      · −5.0% : fill 9% (10/62) · rebond 42% (5/10)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 53.6  _(neutre)_
- **ADX** : 13.4  _(pas de tendance nette)_
- **MACD** : hist 0.025  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 26.4%
- **ATR** : 0.64 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.049  _(neutre)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 65.4  _(marche en range (choppy))_
- **MA** : MA20 9.1 · MA50 9.3 · MA200 13.96  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 +1.1% · MA200 -32.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (821392 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
