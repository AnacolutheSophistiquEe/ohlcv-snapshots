# SMR

**Generated** : 2026-10-05T00:30:50.752417+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $7.75  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $7.75 (+1.2% vs entrée) · entrée $7.66 · stop $7.46 · T1 $7.99 · R/R 1.65  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.079 _(réel 5 s)_ (GBM -0.005) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -60 % hors [0,100] (R² max 0.54). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.60–$7.71 (mid $7.66)
- Spot actuel : $7.75 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $7.46 (plancher anti-bruit 5 s — stop EV-optimal −2.5% (first-passage 5 s réel) ; -2.61 % depuis l'entree)
- Targets : T1 $7.99 · R/R 1.65 | T2 $8.25 · R/R 2.95 | T3 $8.51 · R/R 4.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.46


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.42 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.73 %)** : le gap seul le franchit 0.434 % des séances (5 fois sur 1152).
   - exécution **4.055 pt plus bas** dans le cas TYPIQUE (médiane), 14.357 au p90, **19.593 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 10.73 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0301 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.477 % | p01 -6.959 % | pire -30.323 % _(sur 1152 séances)_
- **P(stop avant cible)** _(source : daily, 1153 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5549** [0.4805 ; 0.6275] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4953** [0.4428 ; 0.5479] _(largeur 10.5 pt, n_eff 345.3)_
   - deep : **0.5583** [0.5056 ; 0.61] _(largeur 10.4 pt, n_eff 345.3)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.98 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.67 % contre 6.16 % aujourd'hui, rapport 1.73)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.14 % vs -18.73 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6062** (β de hausse 1.3793, asymétrie 1.1646) vs IWM — 549 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.921× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 6.9661 sur support (1.04 ATR, 10.115 %) — p(stop avant cible) 0.5982 [0.55 ; 0.65], R/R 2.792, perte reelle 10.209 % (gap inclus), CVaR 11.241 %, EV -1.5981 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4352 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.598, borne haute 0.649 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.04 ATR (stop 10.115 %) — p(stop avant cible) 0.5982 [0.55 ; 0.65], R/R 2.792, perte reelle 10.209 % (gap inclus), EV -1.5981 % — **REFUSE**
      - refuse : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.598, borne haute 0.649 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.72 ATR du spot — compartiment <1, mesure a 46.3 % de casse (IC clusterise [0.432 ; 0.495] sur 1140 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 12.2 % x 28.50 % + P(rien) 28.0 % x 3.68 % ne couvrent pas P(stop) 59.8 % x 10.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.681 %) — p(stop avant cible) 0.9377 [0.91 ; 0.96], R/R 16.336, perte reelle 1.745 % (gap inclus), EV -0.4956 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 16.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.938, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 3.3 % x 28.50 % + P(rien) 2.9 % x 6.97 % ne couvrent pas P(stop) 93.8 % x 1.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.362 %) — p(stop avant cible) 0.8823 [0.85 ; 0.91], R/R 8.271, perte reelle 3.446 % (gap inclus), EV -0.8992 % — **REFUSE**
      - refuse : cible atteinte seulement 6.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.882, borne haute 0.913 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 6.0 % x 28.50 % + P(rien) 5.8 % x 7.44 % ne couvrent pas P(stop) 88.2 % x 3.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 5.043 %) — p(stop avant cible) 0.8273 [0.78 ; 0.86], R/R 5.505, perte reelle 5.178 % (gap inclus), EV -1.1939 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.827, borne haute 0.864 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 8.6 % x 28.50 % + P(rien) 8.7 % x 7.46 % ne couvrent pas P(stop) 82.7 % x 5.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 1.04 ATR (stop 8.985 %) — p(stop avant cible) 0.6553 [0.60 ; 0.70], R/R 3.126, perte reelle 9.118 % (gap inclus), EV -1.6143 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.655, borne haute 0.704 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.61 %) : P(cible) 11.6 % x 28.50 % + P(rien) 22.9 % x 4.60 % ne couvrent pas P(stop) 65.5 % x 9.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 11.766 %) — p(stop avant cible) 0.5238 [0.47 ; 0.58], R/R 2.387, perte reelle 11.939 % (gap inclus), EV -1.5927 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.524, borne haute 0.576 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 13.0 % x 28.50 % + P(rien) 34.7 % x 2.80 % ne couvrent pas P(stop) 52.4 % x 11.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 13.447 %) — p(stop avant cible) 0.4513 [0.40 ; 0.50], R/R 2.097, perte reelle 13.592 % (gap inclus), EV -1.2613 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 13.6 % x 28.50 % + P(rien) 41.3 % x 2.45 % ne couvrent pas P(stop) 45.1 % x 13.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 15.128 %) — p(stop avant cible) 0.4028 [0.35 ; 0.46], R/R 1.868, perte reelle 15.258 % (gap inclus), EV -1.4664 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.47 %) : P(cible) 13.8 % x 28.50 % + P(rien) 46.0 % x 1.65 % ne couvrent pas P(stop) 40.3 % x 15.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 16.809 %) — p(stop avant cible) 0.3387 [0.29 ; 0.39], R/R 1.683, perte reelle 16.938 % (gap inclus), EV -1.4759 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.48 %) : P(cible) 13.8 % x 28.50 % + P(rien) 52.3 % x 0.63 % ne couvrent pas P(stop) 33.9 % x 16.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 18.49 %) — p(stop avant cible) 0.2879 [0.24 ; 0.34], R/R 1.522, perte reelle 18.723 % (gap inclus), EV -1.528 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.53 %) : P(cible) 13.8 % x 28.50 % + P(rien) 57.4 % x -0.13 % ne couvrent pas P(stop) 28.8 % x 18.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 20.171 %) — p(stop avant cible) 0.2236 [0.18 ; 0.27], R/R 1.396, perte reelle 20.414 % (gap inclus), EV -1.3562 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 13.8 % x 28.50 % + P(rien) 63.8 % x -1.15 % ne couvrent pas P(stop) 22.4 % x 20.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 23.532 %) — p(stop avant cible) 0.1413 [0.11 ; 0.18], R/R 1.192, perte reelle 23.907 % (gap inclus), EV -1.2397 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 13.9 % x 28.50 % + P(rien) 72.0 % x -2.51 % ne couvrent pas P(stop) 14.1 % x 23.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 26.894 %) — p(stop avant cible) 0.0868 [0.06 ; 0.12], R/R 1.042, perte reelle 27.344 % (gap inclus), EV -1.1198 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 13.9 % x 28.50 % + P(rien) 77.5 % x -3.48 % ne couvrent pas P(stop) 8.7 % x 27.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 30.256 %) — p(stop avant cible) 0.0507 [0.03 ; 0.08], R/R 0.93, perte reelle 30.652 % (gap inclus), EV -1.0802 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 13.9 % x 28.50 % + P(rien) 81.1 % x -4.29 % ne couvrent pas P(stop) 5.1 % x 30.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 33.618 %) — p(stop avant cible) 0.0336 [0.02 ; 0.06], R/R 0.846, perte reelle 33.695 % (gap inclus), EV -1.0361 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 13.9 % x 28.50 % + P(rien) 82.8 % x -4.66 % ne couvrent pas P(stop) 3.4 % x 33.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 36.979 %) — p(stop avant cible) 0.0255 [0.01 ; 0.05], R/R 0.77, perte reelle 37.003 % (gap inclus), EV -1.0503 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 13.9 % x 28.50 % + P(rien) 83.6 % x -4.86 % ne couvrent pas P(stop) 2.5 % x 37.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 40.341 %) — p(stop avant cible) 0.0153 [0.01 ; 0.03], R/R 0.705, perte reelle 40.424 % (gap inclus), EV -1.0677 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 13.9 % x 28.50 % + P(rien) 84.6 % x -5.21 % ne couvrent pas P(stop) 1.5 % x 40.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 43.703 %) — p(stop avant cible) 0.0112 [0.00 ; 0.03], R/R 0.651, perte reelle 43.816 % (gap inclus), EV -1.0515 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 13.9 % x 28.50 % + P(rien) 85.0 % x -5.31 % ne couvrent pas P(stop) 1.1 % x 43.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 47.065 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.606, perte reelle 47.065 % (gap inclus), EV -1.0664 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 13.9 % x 28.50 % + P(rien) 85.4 % x -5.49 % ne couvrent pas P(stop) 0.7 % x 47.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 50.426 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.565, perte reelle 50.426 % (gap inclus), EV -1.0596 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 13.9 % x 28.50 % + P(rien) 85.9 % x -5.73 % ne couvrent pas P(stop) 0.2 % x 50.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 53.788 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.53, perte reelle 53.788 % (gap inclus), EV -1.0593 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 13.9 % x 28.50 % + P(rien) 86.1 % x -5.81 % ne couvrent pas P(stop) 0.0 % x 53.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 7.75, ATR14 0.5211 (6.724 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.425 ATR = 2.857 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.336 % | 7.7239 | 92.49 % | 95.06 % | 96.29 % | 97.07 % | 97.96 % | 98.4 % |
| 0.1 ATR | 0.672 % | 7.6979 | 86.77 % | 91.25 % | 93.26 % | 94.71 % | 96.26 % | 97.48 % |
| 0.15 ATR | 1.009 % | 7.6718 | 80.83 % | 86.98 % | 89.66 % | 91.78 % | 94.0 % | 96.11 % |
| 0.2 ATR | 1.345 % | 7.6458 | 75.0 % | 82.6 % | 86.4 % | 89.3 % | 92.41 % | 95.07 % |
| 0.25 ATR | 1.681 % | 7.6197 | 69.84 % | 79.57 % | 83.82 % | 87.16 % | 90.71 % | 93.93 % |
| 0.35 ATR | 2.353 % | 7.5676 | 58.07 % | 72.05 % | 77.42 % | 82.77 % | 87.66 % | 91.52 % |
| 0.5 ATR | 3.362 % | 7.4895 | 41.93 % | 58.81 % | 67.08 % | 74.1 % | 83.24 % | 88.55 % |
| 0.75 ATR | 5.043 % | 7.3592 | 20.52 % | 37.15 % | 47.53 % | 59.68 % | 72.37 % | 81.1 % |
| 1.0 ATR | 6.724 % | 7.2289 | 11.32 % | 25.7 % | 35.73 % | 49.44 % | 64.55 % | 75.26 % |
| 1.25 ATR | 8.404 % | 7.0987 | 4.71 % | 15.94 % | 24.94 % | 38.4 % | 54.81 % | 68.84 % |
| 1.5 ATR | 10.085 % | 6.9684 | 2.24 % | 9.76 % | 16.18 % | 28.27 % | 45.41 % | 62.08 % |
| 2.0 ATR | 13.447 % | 6.7079 | 0.34 % | 3.25 % | 6.52 % | 14.64 % | 31.26 % | 48.91 % |
| 2.5 ATR | 16.809 % | 6.4473 | 0.11 % | 1.35 % | 2.92 % | 6.87 % | 20.61 % | 38.03 % |
| 3.0 ATR | 20.171 % | 6.1868 | 0.11 % | 0.56 % | 1.91 % | 3.83 % | 11.78 % | 28.18 % |
| 4.0 ATR | 26.894 % | 5.6657 | 0.0 % | 0.22 % | 0.34 % | 1.13 % | 4.53 % | 13.52 % |
| 6.0 ATR | 40.341 % | 4.6236 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.6 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.42 ATR | 0.47 ATR | 0.60 ATR | 0.70 ATR | 0.76 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.80 ATR | 1.06 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.21 ATR |
| **5 s.** | 0.48 ATR | 0.99 ATR | 1.10 ATR | 1.38 ATR | 1.62 ATR | 1.80 ATR | 2.30 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.29 ATR | 2.54 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 1.01 ATR | 1.96 ATR | 2.18 ATR | 2.75 ATR | 3.22 ATR | 3.56 ATR | 4.59 ATR | 5.43 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.471–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.362 %, prix 7.4894), p(touche) 41.93 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.659–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.043 %, prix 7.3592), p(touche) 37.15 % (en stress 88.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (71.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.804–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.724 %, prix 7.2289), p(touche) 35.73 % (en stress 89.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.101–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.404 %, prix 7.0987), p(touche) 38.4 % (en stress 95.51 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.514–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.447 %, prix 6.7079), p(touche) 31.26 % (en stress 96.63 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.18–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.809 %, prix 6.4473), p(touche) 38.03 % (en stress 98.86 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.005 | EV/share : $-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 72.0 | bear 5.0 | side 23.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.21% → cible +4.398% / stop −2.5%, p_fill 79%, n_eff≈84.0) : P(cible|rempli) **25%** · **EV/risk -0.079** (×p_fill ; si rempli -0.25% du capital)
  - **swing** (entrée dip −2.665% → cible +16.571% / stop −8.286%, p_fill 74%, n_eff≈85.5) : P(cible|rempli) **15%** · **EV/risk +0.004** (×p_fill ; si rempli +0.05% du capital)
  - **deep** (entrée dip −4.114% → cible +18.336% / stop −10.519%, p_fill 68%, n_eff≈77.3) : P(cible|rempli) **28%** · **EV/risk +0.027** (×p_fill ; si rempli +0.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→62% · +3.0%→54% · +5.0%→34% · +8.0%→14%
- Range intraday médian 7.02% (p90 12.09%) · excursion haute méd. +3.23% / basse méd. −3.1%
- Profil de vol intra : ouverture 4.766% vs midi 1.404% vs clôture 1.695% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.568% ; recovery-V 32%
- **σ réalisé intraday** 4.046% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 62% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 7.8201 (VA 7.7996–7.8714 ; dernier close 7.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 45% · rebond 75% · **stop −4.75%** sous le fill (sous le bruit) · cible +2.64% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.3% · baisse 53% (gap-down >1% 35% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.94%) · haut méd +1.32% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −4.33%) · haut méd +1.53% · range méd 3.57%
- Excursion ouverture 30min (n=160) : bas méd −1.69% (p90 −4.84%) · haut méd +1.7% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −2.12% (p90 −5.34%) · haut méd +2.25% · range méd 4.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (127/159) · gap 48% · délai 0.0min · rebond 60% (77/127) (MFE +1.63%)
   - −1.0% : fill 30min 63% · séance 75% (121/159) · gap 36% · délai 0.0min · rebond 62% (75/121) (MFE +1.79%)
   - −1.5% : fill 30min 60% · séance 72% (115/159) · gap 26% · délai 0.1min · rebond 67% (80/115) (MFE +1.81%)
   - −2.0% : fill 30min 52% · séance 64% (105/159) · gap 22% · délai 1.0min · rebond 61% (69/105) (MFE +1.75%)
   - −3.0% : fill 30min 40% · séance 52% (90/159) · gap 10% · délai 4.8min · rebond 74% (69/90) (MFE +1.92%)
   - −4.0% : fill 30min 31% · séance 45% (79/159) · gap 4% · délai 7.8min · rebond 75% (60/79) (MFE +2.64%)
   - −5.0% : fill 30min 19% · séance 34% (60/159) · gap 2% · délai 23.4min · rebond 76% (44/60) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.48%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.29%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.99% (p90 −2.71%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1089 jambes) : jambe baissière méd −1.28% (p90 −3.12%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 96% (83/86) · rebond 59% (51/83)
      · −2.0% : fill 89% (78/86) · rebond 68% (56/78)
      · −3.0% : fill 83% (73/86) · rebond 79% (59/73)
      · −4.0% : fill 70% (63/86) · rebond 82% (51/63)
      · −5.0% : fill 53% (47/86) · rebond 80% (37/47)
   - **flat** (11 séances) :
      · −1.0% : fill 94% (9/11) · rebond 66% (5/9)
      · −2.0% : fill 52% (6/11) · rebond 39% (2/6)
      · −3.0% : fill 52% (6/11) · rebond 50% (3/6)
      · −4.0% : fill 52% (6/11) · rebond 62% (4/6)
      · −5.0% : fill 39% (4/11) · rebond 78% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 49% (29/62) · rebond 70% (19/29)
      · −2.0% : fill 36% (21/62) · rebond 46% (11/21)
      · −3.0% : fill 15% (11/62) · rebond 49% (7/11)
      · −4.0% : fill 14% (10/62) · rebond 41% (5/10)
      · −5.0% : fill 11% (9/62) · rebond 49% (4/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 72% si les 15 1res min sont vertes (73 cas) · 29% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 84% si début vert vs 19% si rouge (base 47% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 222min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **84%** · continue >prix actuel 59% ; creux résiduel méd -1.71% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.66% / q75 +4.53% → **scale +2.66% / runner +4.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **19%** (continue à baisser 53%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.68% .. +4.36%] · haut q95 +6.14% · bas q05 -5.36%
   - 60min (n=160) : retour [-5.02% .. +4.72%] · haut q95 +6.47% · bas q05 -5.85%
   - 2h (n=160) : retour [-7.52% .. +5.37%] · haut q95 +7.8% · bas q05 -7.94%
   - 4h (n=160) : retour [-7.67% .. +6.92%] · haut q95 +8.32% · bas q05 -9.19%
   - 6h (n=160) : retour [-6.72% .. +8.0%] · haut q95 +9.66% · bas q05 -9.21%
   - session (n=160) : retour [-7.99% .. +8.0%] · haut q95 +10.29% · bas q05 -9.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.35 · part idiosyncratique 0.65
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.9  _(momentum baissier)_
- **ADX** : 15.7  _(pas de tendance nette)_
- **MACD** : hist -0.11  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 44.9%
- **ATR** : 0.52 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.271  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 56.3  _(transition)_
- **MA** : MA20 8.77 · MA50 9.01 · MA200 11.95  _(prix < MA20)_
- **Dist MA** : MA20 -11.6% · MA50 -14.0% · MA200 -35.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843913 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
