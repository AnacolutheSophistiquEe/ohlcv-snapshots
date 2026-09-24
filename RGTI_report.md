# RGTI

**Generated** : 2026-09-24T00:40:32.767716+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.00 (+0.8% vs entrée) · entrée $15.87 · stop $15.47 · T1 $16.17 · R/R 0.75  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.057 _(réel 5 s)_ (GBM 0.165) · ¼-Kelly 0.039 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -3.1 % ≠ (strike 16.0 − spot 16.00)/spot = -0.0 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 4302 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.80–$15.93 (mid $15.87)
- Spot actuel : $16.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $15.47 (stop swing_plan-based (-7.72%))
- Targets : T1 $16.17 · R/R 0.75 | T2 $16.47 · R/R 1.5 | T3 $16.77 · R/R 2.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.72 %)** : le gap seul le franchit 1.357 % des séances (17 fois sur 1253).
   - exécution **2.793 pt plus bas** dans le cas TYPIQUE (médiane), 8.24 au p90, **23.493 au pire**
   - perte réelle **12.435 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 7.72 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.064 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4042** [0.3332 ; 0.4784] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4355** [0.384 ; 0.4881] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4349** [0.3834 ; 0.4875] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 29.2 observations effectives », dont la borne haute a 95 % vaut environ 10.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.2 pt), swing (33.9 pt), deep (34.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.95 %** | CVaR **-11.33 %** | vol 6.84 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.58 % contre 6.41 % aujourd'hui, rapport 3.06)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8316** (β de hausse 1.9855, asymétrie 0.9225) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.461× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 13.9545 sur support (1.72 ATR, 12.812 %) — p(stop avant cible) 0.4809 [0.43 ; 0.53], R/R 1.833, perte reelle 17.61 % (gap inclus), CVaR 12.835 %, EV -2.6636 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0696 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.83 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 46.9 % de la queue et il ne reste que -384.52 EUR a partager. Prix du risque -0.123 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.7 ATR (stop 6.921 %) — p(stop avant cible) 0.7141 [0.66 ; 0.76], R/R 2.764, perte reelle 11.681 % (gap inclus), EV -3.4889 % — **REFUSE**
      - refuse : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.714, borne haute 0.760 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.49 %) : P(cible) 10.5 % x 32.28 % + P(rien) 18.1 % x 8.11 % ne couvrent pas P(stop) 71.4 % x 11.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.695 %) — p(stop avant cible) 0.66 [0.61 ; 0.71], R/R 2.413, perte reelle 13.376 % (gap inclus), EV -3.3305 % — **REFUSE**
      - refuse : cible atteinte seulement 11.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.660, borne haute 0.708 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.33 %) : P(cible) 11.1 % x 32.28 % + P(rien) 22.9 % x 8.32 % ne couvrent pas P(stop) 66.0 % x 13.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.72 ATR (stop 12.812 %) — p(stop avant cible) 0.4809 [0.43 ; 0.53], R/R 1.833, perte reelle 17.61 % (gap inclus), EV -2.6636 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.83 % > budget 12.00 %
      - ⚠ support DETECTE a 0.60 ATR du spot — compartiment <1, mesure a 46.2 % de casse (IC clusterise [0.431 ; 0.493] sur 1171 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.66 %) : P(cible) 12.3 % x 32.28 % + P(rien) 39.6 % x 4.65 % ne couvrent pas P(stop) 48.1 % x 17.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.75 ATR (stop 24.558 %) — p(stop avant cible) 0.1206 [0.09 ; 0.16], R/R 1.034, perte reelle 31.213 % (gap inclus), EV -0.1653 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 14.8 % x 32.28 % + P(rien) 73.1 % x -1.62 % ne couvrent pas P(stop) 12.1 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.449 %) — p(stop avant cible) 0.9436 [0.92 ; 0.96], R/R 8.972, perte reelle 3.598 % (gap inclus), EV -2.1102 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.944, borne haute 0.964 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.11 %) : P(cible) 3.2 % x 32.28 % + P(rien) 2.5 % x 10.28 % ne couvrent pas P(stop) 94.4 % x 3.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.7 ATR (stop 5.814 %) — p(stop avant cible) 0.757 [0.71 ; 0.80], R/R 3.233, perte reelle 9.986 % (gap inclus), EV -3.1352 % — **REFUSE**
      - refuse : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.757, borne haute 0.800 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.14 %) : P(cible) 9.5 % x 32.28 % + P(rien) 14.8 % x 9.12 % ne couvrent pas P(stop) 75.7 % x 9.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 1.72 ATR (stop 11.705 %) — p(stop avant cible) 0.5496 [0.50 ; 0.60], R/R 1.919, perte reelle 16.825 % (gap inclus), EV -3.4706 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.550, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.47 %) : P(cible) 12.0 % x 32.28 % + P(rien) 33.0 % x 5.73 % ne couvrent pas P(stop) 55.0 % x 16.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 14.491 %) — p(stop avant cible) 0.4113 [0.36 ; 0.46], R/R 1.647, perte reelle 19.597 % (gap inclus), EV -2.3355 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 12.8 % x 32.28 % + P(rien) 46.0 % x 3.43 % ne couvrent pas P(stop) 41.1 % x 19.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 15.94 %) — p(stop avant cible) 0.3365 [0.29 ; 0.39], R/R 1.314, perte reelle 24.565 % (gap inclus), EV -2.8743 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.87 %) : P(cible) 13.4 % x 32.28 % + P(rien) 53.0 % x 2.04 % ne couvrent pas P(stop) 33.7 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 17.389 %) — p(stop avant cible) 0.2895 [0.24 ; 0.34], R/R 1.314, perte reelle 24.565 % (gap inclus), EV -1.8342 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 14.1 % x 32.28 % + P(rien) 56.9 % x 1.27 % ne couvrent pas P(stop) 28.9 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.75 ATR (stop 23.451 %) — p(stop avant cible) 0.1263 [0.09 ; 0.16], R/R 1.034, perte reelle 31.213 % (gap inclus), EV -0.293 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 14.8 % x 32.28 % + P(rien) 72.6 % x -1.56 % ne couvrent pas P(stop) 12.6 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 26.084 %) — p(stop avant cible) 0.0867 [0.06 ; 0.12], R/R 1.034, perte reelle 31.213 % (gap inclus), EV 0.4207 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.09 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.982 %) — p(stop avant cible) 0.0662 [0.04 ; 0.10], R/R 1.034, perte reelle 31.213 % (gap inclus), EV 0.7216 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.98 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.88 %) — p(stop avant cible) 0.0442 [0.03 ; 0.07], R/R 1.013, perte reelle 31.88 % (gap inclus), EV 0.8607 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.88 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.778 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.928, perte reelle 34.778 % (gap inclus), EV 0.9669 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.78 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.677 %) — p(stop avant cible) 0.0169 [0.01 ; 0.03], R/R 0.857, perte reelle 37.677 % (gap inclus), EV 0.974 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.68 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.575 %) — p(stop avant cible) 0.0095 [0.00 ; 0.02], R/R 0.796, perte reelle 40.575 % (gap inclus), EV 1.0482 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.473 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.743, perte reelle 43.473 % (gap inclus), EV 1.047 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.47 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.371 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.696, perte reelle 46.371 % (gap inclus), EV 1.0387 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.37 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.005, ATR14 0.9277 (5.796 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.408 ATR = 2.365 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.29 % | 15.9586 | 91.94 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.58 % | 15.9122 | 86.3 % | 91.03 % | 92.43 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.869 % | 15.8658 | 80.77 % | 87.3 % | 89.1 % | 92.01 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.159 % | 15.8195 | 74.32 % | 82.76 % | 85.57 % | 88.78 % | 91.57 % | 94.46 % |
| 0.25 ATR | 1.449 % | 15.7731 | 68.18 % | 78.43 % | 81.53 % | 85.64 % | 88.92 % | 92.51 % |
| 0.35 ATR | 2.029 % | 15.6803 | 55.69 % | 68.35 % | 73.76 % | 79.47 % | 84.55 % | 89.63 % |
| 0.5 ATR | 2.898 % | 15.5411 | 40.99 % | 56.75 % | 64.58 % | 71.49 % | 79.07 % | 85.52 % |
| 0.75 ATR | 4.347 % | 15.3092 | 21.85 % | 39.01 % | 49.65 % | 58.85 % | 70.83 % | 79.36 % |
| 1.0 ATR | 5.796 % | 15.0773 | 9.77 % | 23.89 % | 33.6 % | 46.61 % | 61.99 % | 73.1 % |
| 1.25 ATR | 7.246 % | 14.8454 | 4.13 % | 14.62 % | 23.81 % | 37.01 % | 53.15 % | 65.81 % |
| 1.5 ATR | 8.695 % | 14.6134 | 1.71 % | 7.16 % | 13.82 % | 25.68 % | 43.39 % | 57.7 % |
| 2.0 ATR | 11.593 % | 14.1496 | 0.4 % | 1.71 % | 3.94 % | 10.72 % | 25.51 % | 41.68 % |
| 2.5 ATR | 14.491 % | 13.6857 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.43 % | 29.26 % |
| 3.0 ATR | 17.389 % | 13.2219 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.45 % |
| 4.0 ATR | 23.186 % | 12.2941 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 34.778 % | 10.4387 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.59 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.41 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.04 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.62 ATR | 1.33 ATR | 1.46 ATR | 1.79 ATR | 2.02 ATR | 2.25 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.74 ATR | 1.90 ATR | 2.35 ATR | 2.68 ATR | 2.89 ATR | 3.60 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.459–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.898 %, prix 15.5412), p(touche) 40.99 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.666–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.347 %, prix 15.3093), p(touche) 39.01 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.822–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.796 %, prix 15.0773), p(touche) 33.6 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.042–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.246 %, prix 14.8453), p(touche) 37.01 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.459–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.695 %, prix 14.6134), p(touche) 43.39 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.896–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.593 %, prix 14.1495), p(touche) 41.68 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.165 | EV/share : $0.065 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 63 % | T2 40 % | T3 32 %
- Kelly (position) : f* 0.156 | ¼-Kelly 0.039 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 18.7 | side 76.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 144.0 (= 9 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.872% → cible +1.901% / stop −2.5%, p_fill 75%, n_eff≈31.9) : P(cible|rempli) **44%** · **EV/risk -0.057** (×p_fill ; si rempli -0.19% du capital)
  - **swing** (entrée dip −1.924% → cible +4.25% / stop −5.91%, p_fill 78%, n_eff≈30.8) : P(cible|rempli) **41%** · **EV/risk -0.185** (×p_fill ; si rempli -1.40% du capital)
  - **deep** (entrée dip −2.976% → cible +6.011% / stop −8.961%, p_fill 71%, n_eff≈29.2) : P(cible|rempli) **46%** · **EV/risk -0.182** (×p_fill ; si rempli -2.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→80% · +2.0%→70% · +3.0%→52% · +5.0%→38% · +8.0%→11%
- Range intraday médian 7.28% (p90 11.35%) · excursion haute méd. +3.41% / basse méd. −2.46%
- Profil de vol intra : ouverture 5.227% vs midi 1.5% vs clôture 1.718% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. 0.053% ; recovery-V 33%
- **σ réalisé intraday** 3.929% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 47% / whipsaw 3%
- POC intraday (dernière séance, temps-au-prix) : 15.2248 (VA 15.1512–15.2668 ; dernier close 15.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 43% · rebond 74% · **stop −5.86%** sous le fill (sous le bruit) · cible +2.06% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.56% · baisse 61% (gap-down >1% 42% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.84%) · haut méd +1.32% · range méd 2.52%
- Excursion ouverture 15min (n=160) : bas méd −1.38% (p90 −3.63%) · haut méd +1.77% · range méd 3.48%
- Excursion ouverture 30min (n=160) : bas méd −1.68% (p90 −4.49%) · haut méd +2.04% · range méd 4.21%
- Excursion ouverture 60min (n=160) : bas méd −2.04% (p90 −5.47%) · haut méd +2.21% · range méd 5.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (133/159) · gap 50% · délai 0.0min · rebond 61% (83/133) (MFE +1.61%)
   - −1.0% : fill 30min 64% · séance 72% (124/159) · gap 42% · délai 0.0min · rebond 64% (78/124) (MFE +1.58%)
   - −1.5% : fill 30min 59% · séance 66% (117/159) · gap 32% · délai 0.0min · rebond 64% (76/117) (MFE +1.92%)
   - −2.0% : fill 30min 53% · séance 60% (108/159) · gap 26% · délai 0.0min · rebond 64% (72/108) (MFE +1.86%)
   - −3.0% : fill 30min 43% · séance 53% (96/159) · gap 11% · délai 1.2min · rebond 64% (68/96) (MFE +1.9%)
   - −4.0% : fill 30min 34% · séance 43% (75/159) · gap 6% · délai 6.3min · rebond 74% (54/75) (MFE +2.06%)
   - −5.0% : fill 30min 18% · séance 36% (65/159) · gap 2% · délai 25.1min · rebond 57% (45/65) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −2.2%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.85% (p90 −2.77%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.87%) → stop au-delà de −1.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1136 jambes) : jambe baissière méd −1.27% (p90 −3.04%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (88 séances) :
      · −1.0% : fill 90% (84/88) · rebond 57% (48/84)
      · −2.0% : fill 82% (79/88) · rebond 61% (50/79)
      · −3.0% : fill 76% (74/88) · rebond 57% (49/74)
      · −4.0% : fill 64% (60/88) · rebond 72% (42/60)
      · −5.0% : fill 55% (53/88) · rebond 54% (35/53)
   - **flat** (14 séances) :
      · −1.0% : fill 96% (13/14) · rebond 97% (12/13)
      · −2.0% : fill 60% (10/14) · rebond 86% (9/10)
      · −3.0% : fill 40% (5/14) · rebond 92% (4/5)
      · −4.0% : fill 26% (4/14) · rebond 88% (3/4)
      · −5.0% : fill 16% (3/14) · rebond 100% (3/3)
   - **gap-up** (57 séances) :
      · −1.0% : fill 37% (27/57) · rebond 67% (18/27)
      · −2.0% : fill 25% (19/57) · rebond 64% (13/19)
      · −3.0% : fill 21% (17/57) · rebond 90% (15/17)
      · −4.0% : fill 13% (11/57) · rebond 83% (9/11)
      · −5.0% : fill 11% (9/57) · rebond 67% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 75% si les 15 1res min sont vertes (82 cas) · 26% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 95% si début vert vs 9% si rouge (base 52% · écart 86 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **95%** · continue >prix actuel 52% ; creux résiduel méd -1.81% (q20 -2.74%) → **SL/trailing à −2.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +4.04% → **scale +1.54% / runner +4.04%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **9%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.26%** (au-delà de la MAE q10 -5.26%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.98% .. +4.73%] · haut q95 +6.18% · bas q05 -6.02%
   - 60min (n=160) : retour [-5.26% .. +6.01%] · haut q95 +6.6% · bas q05 -6.57%
   - 2h (n=160) : retour [-6.04% .. +6.46%] · haut q95 +8.52% · bas q05 -7.25%
   - 4h (n=160) : retour [-6.16% .. +7.69%] · haut q95 +9.18% · bas q05 -7.73%
   - 6h (n=160) : retour [-6.9% .. +8.52%] · haut q95 +9.73% · bas q05 -8.47%
   - session (n=160) : retour [-7.06% .. +8.89%] · haut q95 +10.31% · bas q05 -8.54%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **27%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 61.6  _(momentum haussier)_
- **ADX** : 9.7  _(pas de tendance nette)_
- **MACD** : hist 0.163  _(pas de croisement recent)_
- **BB** : %B 0.7 · largeur 13.9%
- **ATR** : 0.93 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.144  _(distribution)_
- **Vol ratio** : 1.53  _(volume au-dessus de la moyenne)_
- **Choppiness** : 52.5  _(transition)_
- **MA** : MA20 15.57 · MA50 15.97 · MA200 18.7  _(prix > MA20)_
- **Dist MA** : MA20 +2.8% · MA50 +0.2% · MA200 -14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (851914 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
