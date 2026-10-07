# RHM

**Generated** : 2026-10-07T00:05:16.472178+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €948.80  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €948.80 (+0.3% vs entrée) · entrée €945.95 · stop €870.28 · T1 €960.47 · R/R 0.19  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -31 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €943.84–€948.07 (mid €945.95)
- Spot actuel : €948.80 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €870.28 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 €960.47 · R/R 0.19 | T2 €974.99 · R/R 0.38 | T3 €989.51 · R/R 0.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €870.28


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (3.46 %)** : le gap seul le franchit 1.256 % des séances (16 fois sur 1274).
   - exécution **0.853 pt plus bas** dans le cas TYPIQUE (médiane), 3.497 au p90, **18.969 au pire**
   - perte réelle **5.656 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 3.46 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0276 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0098** [0.0018 ; 0.0337] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.5203** [0.4677 ; 0.5726] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.5438** [0.4911 ; 0.5957] _(largeur 10.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-5.0 %** | CVaR **-7.03 %** | vol 3.17 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.92 % contre 3.10 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5282** (β de hausse 0.5873, asymétrie 0.8994) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.215× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 883.4696 sur atr_grid (2.25 ATR, 6.886 %) — p(stop avant cible) 0.4728 [0.42 ; 0.53], R/R 4.017, perte reelle 7.327 % (gap inclus), CVaR 10.718 %, EV -0.9387 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9493 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.16 ATR (stop 2.549 %) — p(stop avant cible) 0.8073 [0.76 ; 0.85], R/R 11.079, perte reelle 2.657 % (gap inclus), EV -0.2429 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 11.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.807, borne haute 0.846 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.4 % x 29.44 % + P(rien) 18.8 % x 9.41 % ne couvrent pas P(stop) 80.7 % x 2.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 0.69 ATR (stop 4.161 %) — p(stop avant cible) 0.6649 [0.61 ; 0.71], R/R 6.689, perte reelle 4.401 % (gap inclus), EV -0.5092 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.665, borne haute 0.713 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.06 ATR du spot — compartiment <1, mesure a 47.1 % de casse (IC clusterise [0.436 ; 0.505] sur 1180 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.4 % x 29.44 % + P(rien) 33.1 % x 6.92 % ne couvrent pas P(stop) 66.5 % x 4.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.16 ATR (stop 1.414 %) — p(stop avant cible) 0.8878 [0.85 ; 0.92], R/R 19.716, perte reelle 1.493 % (gap inclus), EV -0.0084 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 19.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 0.3 % x 29.44 % + P(rien) 10.9 % x 11.30 % ne couvrent pas P(stop) 88.8 % x 1.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.69 ATR (stop 3.026 %) — p(stop avant cible) 0.7571 [0.71 ; 0.80], R/R 9.038, perte reelle 3.257 % (gap inclus), EV -0.4287 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.757, borne haute 0.800 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 0.4 % x 29.44 % + P(rien) 23.8 % x 8.00 % ne couvrent pas P(stop) 75.7 % x 3.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 4.59 %) — p(stop avant cible) 0.6419 [0.59 ; 0.69], R/R 6.026, perte reelle 4.885 % (gap inclus), EV -0.6351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.642, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.5 % x 29.44 % + P(rien) 35.3 % x 6.66 % ne couvrent pas P(stop) 64.2 % x 4.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.355 %) — p(stop avant cible) 0.5941 [0.54 ; 0.64], R/R 5.127, perte reelle 5.741 % (gap inclus), EV -0.8732 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.594, borne haute 0.645 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 0.5 % x 29.44 % + P(rien) 40.0 % x 5.93 % ne couvrent pas P(stop) 59.4 % x 5.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 6.121 %) — p(stop avant cible) 0.5339 [0.48 ; 0.59], R/R 4.494, perte reelle 6.55 % (gap inclus), EV -0.9342 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.534, borne haute 0.586 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 0.8 % x 29.44 % + P(rien) 45.9 % x 5.10 % ne couvrent pas P(stop) 53.4 % x 6.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 6.886 %) — p(stop avant cible) 0.4728 [0.42 ; 0.53], R/R 4.017, perte reelle 7.327 % (gap inclus), EV -0.9387 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.8 % x 29.44 % + P(rien) 52.0 % x 4.43 % ne couvrent pas P(stop) 47.3 % x 7.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 7.651 %) — p(stop avant cible) 0.425 [0.37 ; 0.48], R/R 3.615, perte reelle 8.143 % (gap inclus), EV -1.0494 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.8 % x 29.44 % + P(rien) 56.7 % x 3.86 % ne couvrent pas P(stop) 42.5 % x 8.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 8.416 %) — p(stop avant cible) 0.3985 [0.35 ; 0.45], R/R 3.301, perte reelle 8.918 % (gap inclus), EV -1.2598 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.8 % x 29.44 % + P(rien) 59.4 % x 3.49 % ne couvrent pas P(stop) 39.9 % x 8.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 9.181 %) — p(stop avant cible) 0.3349 [0.29 ; 0.39], R/R 3.039, perte reelle 9.687 % (gap inclus), EV -1.182 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.8 % x 29.44 % + P(rien) 65.8 % x 2.80 % ne couvrent pas P(stop) 33.5 % x 9.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 10.711 %) — p(stop avant cible) 0.2421 [0.20 ; 0.29], R/R 2.627, perte reelle 11.205 % (gap inclus), EV -1.1422 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.8 % x 29.44 % + P(rien) 75.0 % x 1.79 % ne couvrent pas P(stop) 24.2 % x 11.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 12.241 %) — p(stop avant cible) 0.1919 [0.15 ; 0.24], R/R 2.305, perte reelle 12.769 % (gap inclus), EV -1.2207 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.8 % x 29.44 % + P(rien) 80.0 % x 1.26 % ne couvrent pas P(stop) 19.2 % x 12.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 13.771 %) — p(stop avant cible) 0.1438 [0.11 ; 0.18], R/R 2.041, perte reelle 14.423 % (gap inclus), EV -1.2222 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.8 % x 29.44 % + P(rien) 84.9 % x 0.74 % ne couvrent pas P(stop) 14.4 % x 14.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 15.301 %) — p(stop avant cible) 0.1246 [0.09 ; 0.16], R/R 1.852, perte reelle 15.897 % (gap inclus), EV -1.2952 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 0.8 % x 29.44 % + P(rien) 86.8 % x 0.53 % ne couvrent pas P(stop) 12.5 % x 15.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 16.831 %) — p(stop avant cible) 0.0915 [0.06 ; 0.13], R/R 1.688, perte reelle 17.439 % (gap inclus), EV -1.3168 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.8 % x 29.44 % + P(rien) 90.1 % x 0.06 % ne couvrent pas P(stop) 9.2 % x 17.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 18.362 %) — p(stop avant cible) 0.0604 [0.04 ; 0.09], R/R 1.547, perte reelle 19.031 % (gap inclus), EV -1.2516 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.8 % x 29.44 % + P(rien) 93.2 % x -0.35 % ne couvrent pas P(stop) 6.0 % x 19.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 19.892 %) — p(stop avant cible) 0.046 [0.03 ; 0.07], R/R 1.431, perte reelle 20.569 % (gap inclus), EV -1.2721 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 0.8 % x 29.44 % + P(rien) 94.6 % x -0.58 % ne couvrent pas P(stop) 4.6 % x 20.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 21.422 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 1.331, perte reelle 22.116 % (gap inclus), EV -1.201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.8 % x 29.44 % + P(rien) 96.1 % x -0.75 % ne couvrent pas P(stop) 3.2 % x 22.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 22.952 %) — p(stop avant cible) 0.013 [0.00 ; 0.03], R/R 1.225, perte reelle 24.021 % (gap inclus), EV -1.0648 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 0.8 % x 29.44 % + P(rien) 97.9 % x -1.00 % ne couvrent pas P(stop) 1.3 % x 24.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 24.482 %) — p(stop avant cible) 0.0097 [0.00 ; 0.02], R/R 1.169, perte reelle 25.184 % (gap inclus), EV -1.0482 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.8 % x 29.44 % + P(rien) 98.3 % x -1.05 % ne couvrent pas P(stop) 1.0 % x 25.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 948.8, ATR14 29.0357 (3.06 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.393 ATR = 1.203 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.153 % | 947.3482 | 89.55 % | 92.2 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.306 % | 945.8964 | 83.53 % | 87.96 % | 89.82 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.459 % | 944.4446 | 76.53 % | 83.12 % | 85.87 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.612 % | 942.9928 | 69.92 % | 78.68 % | 81.82 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.765 % | 941.5411 | 62.43 % | 72.95 % | 76.88 % | 81.19 % | 88.46 % | 91.36 % |
| 0.35 ATR | 1.071 % | 938.6375 | 53.75 % | 65.84 % | 71.34 % | 76.73 % | 85.87 % | 89.25 % |
| 0.5 ATR | 1.53 % | 934.2821 | 40.63 % | 54.99 % | 61.76 % | 69.21 % | 80.3 % | 83.82 % |
| 0.75 ATR | 2.295 % | 927.0232 | 23.37 % | 38.89 % | 47.23 % | 57.52 % | 70.35 % | 77.09 % |
| 1.0 ATR | 3.06 % | 919.7643 | 13.02 % | 26.55 % | 36.36 % | 48.42 % | 62.29 % | 70.55 % |
| 1.25 ATR | 3.825 % | 912.5054 | 7.4 % | 17.97 % | 26.38 % | 39.41 % | 54.23 % | 64.32 % |
| 1.5 ATR | 4.59 % | 905.2464 | 3.94 % | 13.13 % | 20.55 % | 31.88 % | 46.27 % | 57.49 % |
| 2.0 ATR | 6.121 % | 890.7286 | 1.78 % | 7.01 % | 12.15 % | 21.09 % | 34.63 % | 47.84 % |
| 2.5 ATR | 7.651 % | 876.2107 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 24.98 % | 38.49 % |
| 3.0 ATR | 9.181 % | 861.6929 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 32.56 % |
| 4.0 ATR | 12.241 % | 832.6571 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.6 % |
| 6.0 ATR | 18.362 % | 774.5857 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.04 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.53 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.39 ATR | 0.96 ATR | 1.09 ATR | 1.46 ATR | 1.82 ATR | 2.06 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.63 ATR | 1.38 ATR | 1.55 ATR | 2.08 ATR | 2.50 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.83 ATR | 1.89 ATR | 2.15 ATR | 2.96 ATR | 3.63 ATR | 4.07 ATR | 5.24 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.45–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.655–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.295 %, prix 927.025), p(touche) 38.89 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.06 %, prix 919.7667), p(touche) 36.36 % (en stress 95.1 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.095–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.825 %, prix 912.5084), p(touche) 39.41 % (en stress 98.02 %)  ✅ optimum identifie (84.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.555–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.121 %, prix 890.7239), p(touche) 34.63 % (en stress 96.04 %)  ✅ optimum identifie (98.1 % des re-echantillons)
- **20 seance(s)** : plage utile 2.152–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.651 %, prix 876.2073), p(touche) 38.49 % (en stress 98.0 %)  ✅ optimum identifie (97.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 7.0 | side 8.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.535% / stop −8.0%, p_fill 91%, n_eff≈96.2) : P(cible|rempli) **44%** · **EV/risk -0.053** (×p_fill ; si rempli -0.46% du capital)
  - **swing** (entrée dip −0.4% → cible +3.435% / stop −3.073%, p_fill 93%, n_eff≈107.7) : P(cible|rempli) **43%** · **EV/risk -0.112** (×p_fill ; si rempli -0.37% du capital)
  - **deep** (entrée dip −0.499% → cible +4.863% / stop −4.614%, p_fill 94%, n_eff≈105.1) : P(cible|rempli) **45%** · **EV/risk -0.114** (×p_fill ; si rempli -0.56% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→42% · +3.0%→25% · +5.0%→3% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.51%) · excursion haute méd. +1.53% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.349% vs midi 0.894% vs clôture 1.023% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 7% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.537% ; recovery-V 10%
- **σ réalisé intraday** 2.314% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 64% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 954.8875 (VA 951.8125–962.2675 ; dernier close 959.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 48% · **stop −2.11%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 30% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.74%) · haut méd +0.44% · range méd 1.28%
- Excursion ouverture 15min (n=160) : bas méd −0.86% (p90 −2.06%) · haut méd +0.6% · range méd 1.7%
- Excursion ouverture 30min (n=160) : bas méd −0.94% (p90 −2.14%) · haut méd +0.75% · range méd 1.9%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.41%) · haut méd +0.82% · range méd 2.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 956.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 74% (109/159) · gap 17% · délai 1.1min · rebond 51% (57/109) (MFE +1.03%)
   - −1.0% : fill 30min 40% · séance 65% (97/159) · gap 7% · délai 9.5min · rebond 60% (57/97) (MFE +1.23%)
   - −1.5% : fill 30min 25% · séance 53% (79/159) · gap 5% · délai 33.3min · rebond 55% (45/79) (MFE +1.15%)
   - −2.0% : fill 30min 16% · séance 43% (66/159) · gap 2% · délai 76.1min · rebond 56% (39/66) (MFE +1.22%)
   - −3.0% : fill 30min 6% · séance 24% (37/159) · gap 2% · délai 141.3min · rebond 48% (19/37) (MFE +0.99%)
   - −4.0% : fill 30min 2% · séance 11% (21/159) · gap 1% · délai 149.9min · rebond 65% (12/21) (MFE +1.74%)
   - −5.0% : fill 30min 0% · séance 5% (11/159) · gap 0% · délai 307.4min · rebond 92% (10/11) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −1.32%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.62%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.68%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=561 jambes) : jambe baissière méd −1.02% (p90 −2.36%) · ~7.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 97% (30/31) · rebond 65% (20/30)
      · −2.0% : fill 70% (25/31) · rebond 46% (15/25)
      · −3.0% : fill 48% (14/31) · rebond 33% (7/14)
      · −4.0% : fill 38% (11/31) · rebond 65% (7/11)
      · −5.0% : fill 15% (6/31) · rebond 100% (6/6)
   - **flat** (27 séances) :
      · −1.0% : fill 86% (21/27) · rebond 66% (15/21)
      · −2.0% : fill 52% (12/27) · rebond 75% (9/12)
      · −3.0% : fill 27% (6/27) · rebond 67% (3/6)
      · −4.0% : fill 4% (2/27) · rebond 62% (1/2)
      · −5.0% : fill 4% (2/27) · rebond 62% (1/2)
   - **gap-up** (101 séances) :
      · −1.0% : fill 45% (46/101) · rebond 50% (22/46)
      · −2.0% : fill 28% (29/101) · rebond 49% (15/29)
      · −3.0% : fill 15% (17/101) · rebond 50% (9/17)
      · −4.0% : fill 5% (8/101) · rebond 66% (4/8)
      · −5.0% : fill 1% (3/101) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 49% si les 15 1res min sont vertes (73 cas) · 28% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 58% si début vert vs 20% si rouge (base 38% · écart 38 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **58%** · continue >prix actuel 45% ; creux résiduel méd -1.43% (q20 -2.65%) → **SL/trailing à −2.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.37% / q75 +2.51% → **scale +1.37% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 61%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.38%** (au-delà de la MAE q10 -3.38%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.57% .. +2.77%] · haut q95 +3.12% · bas q05 -2.92%
   - 60min (n=160) : retour [-2.47% .. +2.88%] · haut q95 +3.76% · bas q05 -3.36%
   - 2h (n=160) : retour [-3.19% .. +2.58%] · haut q95 +4.0% · bas q05 -3.76%
   - 4h (n=160) : retour [-3.2% .. +2.65%] · haut q95 +4.43% · bas q05 -4.1%
   - 6h (n=160) : retour [-3.5% .. +3.02%] · haut q95 +4.52% · bas q05 -4.31%
   - session (n=160) : retour [-4.02% .. +3.3%] · haut q95 +4.58% · bas q05 -4.8%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.2 · part idiosyncratique 0.8
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.5  _(momentum baissier)_
- **ADX** : 31.1  _(tendance etablie)_
- **MACD** : hist 0.135  _(bullish_recent)_
- **BB** : %B 0.11 · largeur 10.8%
- **ATR** : 29.04 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.239  _(distribution)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 54.1  _(transition)_
- **MA** : MA20 990.0 · MA50 1080.52 · MA200 1328.92  _(prix < MA20)_
- **Dist MA** : MA20 -4.2% · MA50 -12.2% · MA200 -28.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (534617 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
