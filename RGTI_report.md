# RGTI

**Generated** : 2026-09-29T00:39:56.221412+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.96  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $15.96 (+1.8% vs entrée) · entrée $15.68 · stop $14.75 · T1 $16.27 · R/R 0.63  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk -0.201 _(réel 5 s)_ (GBM -0.094) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.0 % ≠ (strike 16.5 − spot 15.96)/spot = +3.4 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $15.56–$15.80 (mid $15.68)
- Spot actuel : $15.96 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $14.75 (plancher anti-bruit (R/R<2) ; -5.93 % depuis l'entree)
- Targets : T1 $16.27 · R/R 0.63 | T2 $16.87 · R/R 1.28 | T3 $17.47 · R/R 1.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.75


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.57 %)** : le gap seul le franchit 1.437 % des séances (18 fois sur 1253).
   - exécution **2.925 pt plus bas** dans le cas TYPIQUE (médiane), 8.064 au p90, **23.643 au pire**
   - perte réelle **12.17 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 7.57 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0661 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3929** [0.3224 ; 0.4669] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.423** [0.3717 ; 0.4755] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3971** [0.3466 ; 0.4494] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 29.2 observations effectives », dont la borne haute a 95 % vaut environ 10.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.4 pt), swing (33.8 pt), deep (34.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.95 %** | CVaR **-11.33 %** | vol 6.84 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.61 % contre 6.41 % aujourd'hui, rapport 3.06)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8464** (β de hausse 1.9881, asymétrie 0.9287) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.484× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 15.0759 sur grid_snapped (0.66 ATR, 5.54 %) — p(stop avant cible) 0.7615 [0.71 ; 0.80], R/R 3.491, perte reelle 9.355 % (gap inclus), CVaR 5.644 %, EV -2.8518 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.7388 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.761, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 5.64 % > budget 4.42 %
- Budget de queue : **4.42 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.18 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 47.6 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.66 ATR (stop 6.467 %) — p(stop avant cible) 0.7207 [0.67 ; 0.77], R/R 2.851, perte reelle 11.454 % (gap inclus), EV -3.4192 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.721, borne haute 0.766 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.55 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.42 %) : P(cible) 9.9 % x 32.66 % + P(rien) 18.0 % x 8.83 % ne couvrent pas P(stop) 72.1 % x 11.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 8.689 %) — p(stop avant cible) 0.6486 [0.60 ; 0.70], R/R 2.442, perte reelle 13.376 % (gap inclus), EV -3.0638 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.74 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.06 %) : P(cible) 10.9 % x 32.66 % + P(rien) 24.2 % x 8.43 % ne couvrent pas P(stop) 64.9 % x 13.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 1.68 ATR (stop 12.377 %) — p(stop avant cible) 0.5085 [0.46 ; 0.56], R/R 1.855, perte reelle 17.61 % (gap inclus), EV -3.0696 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.508, borne haute 0.561 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.40 % > budget 4.42 %
      - ⚠ support DETECTE a 0.56 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.441 ; 0.507] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.07 %) : P(cible) 12.0 % x 32.66 % + P(rien) 37.2 % x 5.31 % ne couvrent pas P(stop) 50.8 % x 17.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.71 ATR (stop 24.156 %) — p(stop avant cible) 0.1191 [0.09 ; 0.16], R/R 1.046, perte reelle 31.213 % (gap inclus), EV 0.0461 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.16 % > budget 4.42 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.448 %) — p(stop avant cible) 0.9388 [0.91 ; 0.96], R/R 9.093, perte reelle 3.592 % (gap inclus), EV -2.0157 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 9.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.939, borne haute 0.961 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.23 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 3.1 % x 32.66 % + P(rien) 3.0 % x 11.10 % ne couvrent pas P(stop) 93.9 % x 3.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.66 ATR (stop 5.54 %) — p(stop avant cible) 0.7615 [0.71 ; 0.80], R/R 3.491, perte reelle 9.355 % (gap inclus), EV -2.8518 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.761, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.64 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.85 %) : P(cible) 8.9 % x 32.66 % + P(rien) 14.9 % x 9.06 % ne couvrent pas P(stop) 76.1 % x 9.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.241 %) — p(stop avant cible) 0.6941 [0.64 ; 0.74], R/R 2.739, perte reelle 11.924 % (gap inclus), EV -3.1438 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.694, borne haute 0.741 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.31 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.14 %) : P(cible) 10.4 % x 32.66 % + P(rien) 20.2 % x 8.62 % ne couvrent pas P(stop) 69.4 % x 11.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 1.68 ATR (stop 11.45 %) — p(stop avant cible) 0.5614 [0.51 ; 0.61], R/R 1.941, perte reelle 16.825 % (gap inclus), EV -3.5605 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.561, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.48 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.56 %) : P(cible) 11.7 % x 32.66 % + P(rien) 32.2 % x 6.44 % ne couvrent pas P(stop) 56.1 % x 16.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 14.482 %) — p(stop avant cible) 0.4042 [0.35 ; 0.46], R/R 1.667, perte reelle 19.597 % (gap inclus), EV -2.0791 % — **REFUSE**
      - refuse : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.50 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 12.6 % x 32.66 % + P(rien) 47.0 % x 3.66 % ne couvrent pas P(stop) 40.4 % x 19.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 15.93 %) — p(stop avant cible) 0.3325 [0.28 ; 0.38], R/R 1.33, perte reelle 24.565 % (gap inclus), EV -2.6411 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.94 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.64 %) : P(cible) 13.1 % x 32.66 % + P(rien) 53.6 % x 2.32 % ne couvrent pas P(stop) 33.2 % x 24.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 17.378 %) — p(stop avant cible) 0.2845 [0.24 ; 0.33], R/R 1.33, perte reelle 24.565 % (gap inclus), EV -1.5817 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.39 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 13.9 % x 32.66 % + P(rien) 57.7 % x 1.53 % ne couvrent pas P(stop) 28.4 % x 24.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 3.71 ATR (stop 23.229 %) — p(stop avant cible) 0.129 [0.10 ; 0.17], R/R 1.046, perte reelle 31.213 % (gap inclus), EV -0.1372 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.24 % > budget 4.42 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 14.5 % x 32.66 % + P(rien) 72.6 % x -1.16 % ne couvrent pas P(stop) 12.9 % x 31.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 26.067 %) — p(stop avant cible) 0.0852 [0.06 ; 0.12], R/R 1.046, perte reelle 31.213 % (gap inclus), EV 0.638 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.07 % > budget 4.42 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.963 %) — p(stop avant cible) 0.065 [0.04 ; 0.09], R/R 1.046, perte reelle 31.213 % (gap inclus), EV 0.9327 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.96 % > budget 4.42 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.859 %) — p(stop avant cible) 0.0434 [0.03 ; 0.07], R/R 1.025, perte reelle 31.859 % (gap inclus), EV 1.0732 % — **REFUSE**
      - refuse : cible atteinte seulement 15.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.86 % > budget 4.42 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.756 %) — p(stop avant cible) 0.0264 [0.01 ; 0.05], R/R 0.94, perte reelle 34.756 % (gap inclus), EV 1.1711 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.76 % > budget 4.42 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.652 %) — p(stop avant cible) 0.0166 [0.01 ; 0.03], R/R 0.867, perte reelle 37.652 % (gap inclus), EV 1.1802 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.65 % > budget 4.42 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.548 %) — p(stop avant cible) 0.0116 [0.00 ; 0.03], R/R 0.805, perte reelle 40.548 % (gap inclus), EV 1.2532 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.55 % > budget 4.42 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.445 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.752, perte reelle 43.445 % (gap inclus), EV 1.2526 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.45 % > budget 4.42 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.341 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.705, perte reelle 46.341 % (gap inclus), EV 1.2404 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.34 % > budget 4.42 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.96, ATR14 0.9245 (5.793 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.407 ATR = 2.358 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.29 % | 15.9138 | 91.94 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.579 % | 15.8676 | 86.2 % | 90.93 % | 92.43 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.869 % | 15.8213 | 80.66 % | 87.2 % | 89.1 % | 92.01 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.159 % | 15.7751 | 74.22 % | 82.66 % | 85.57 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.448 % | 15.7289 | 68.08 % | 78.33 % | 81.53 % | 85.64 % | 88.82 % | 92.51 % |
| 0.35 ATR | 2.027 % | 15.6364 | 55.59 % | 68.25 % | 73.66 % | 79.37 % | 84.45 % | 89.63 % |
| 0.5 ATR | 2.896 % | 15.4978 | 40.99 % | 56.85 % | 64.58 % | 71.39 % | 78.96 % | 85.52 % |
| 0.75 ATR | 4.344 % | 15.2666 | 21.95 % | 39.01 % | 49.75 % | 58.75 % | 70.63 % | 79.36 % |
| 1.0 ATR | 5.793 % | 15.0355 | 9.87 % | 23.99 % | 33.8 % | 46.51 % | 61.79 % | 73.1 % |
| 1.25 ATR | 7.241 % | 14.8044 | 4.23 % | 14.72 % | 23.92 % | 36.91 % | 52.85 % | 65.81 % |
| 1.5 ATR | 8.689 % | 14.5733 | 1.81 % | 7.26 % | 13.93 % | 25.58 % | 43.09 % | 57.7 % |
| 2.0 ATR | 11.585 % | 14.111 | 0.4 % | 1.81 % | 4.04 % | 10.72 % | 25.3 % | 41.58 % |
| 2.5 ATR | 14.482 % | 13.6488 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.43 % | 29.26 % |
| 3.0 ATR | 17.378 % | 13.1865 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.45 % |
| 4.0 ATR | 23.17 % | 12.262 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 34.756 % | 10.413 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.11 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.33 ATR | 0.75 ATR | 0.82 ATR | 1.02 ATR | 1.22 ATR | 1.35 ATR | 1.70 ATR | 1.95 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.04 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.62 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.74 ATR | 1.89 ATR | 2.35 ATR | 2.68 ATR | 2.89 ATR | 3.60 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.459–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.896 %, prix 15.4978), p(touche) 40.99 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.666–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.344 %, prix 15.2667), p(touche) 39.01 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.824–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.793 %, prix 15.0354), p(touche) 33.8 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.039–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.241 %, prix 14.8043), p(touche) 36.91 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.689 %, prix 14.5732), p(touche) 43.09 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.894–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.585 %, prix 14.111), p(touche) 41.58 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.094 | EV/share : $-0.086 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 38 % | T3 27 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 30.2 | side 64.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 10 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.81% → cible +1.704% / stop −2.5%, p_fill 75%, n_eff≈31.9) : P(cible|rempli) **48%** · **EV/risk -0.051** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −1.778% → cible +3.811% / stop −5.897%, p_fill 79%, n_eff≈31.0) : P(cible|rempli) **42%** · **EV/risk -0.201** (×p_fill ; si rempli -1.51% du capital)
  - **deep** (entrée dip −2.741% → cible +5.389% / stop −8.934%, p_fill 71%, n_eff≈29.2) : P(cible|rempli) **53%** · **EV/risk -0.127** (×p_fill ; si rempli -1.59% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.4  _(neutre)_
- **ADX** : 10.8  _(pas de tendance nette)_
- **MACD** : hist 0.15  _(pas de croisement recent)_
- **BB** : %B 0.64 · largeur 15.4%
- **ATR** : 0.92 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.088  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 52.4  _(transition)_
- **MA** : MA20 15.62 · MA50 16.09 · MA200 18.53  _(prix > MA20)_
- **Dist MA** : MA20 +2.2% · MA50 -0.8% · MA200 -13.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (867294 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
