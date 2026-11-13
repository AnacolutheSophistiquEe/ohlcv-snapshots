# EVT

**Generated** : 2026-11-13T01:06:08.188661+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €3.14  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €3.14 (+0.3% vs entrée) · entrée €3.13 · stop €3.01 · T1 €3.20 · R/R 0.58  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 3.14 · ATR Wilder 0.1467 (4.67 %)_
- **Swing** : plage **2.94 → 2.8** (-6.27 % a -10.92 % sous la cloture, 1.0 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 2.92-2.99 (C). stop INDICATIF 2.64 (-5.73 % sous le bas ; sous le support 2.71-2.77 (- 0,5 ATR)).
- **Deep** : plage **2.8 → 2.19** (-10.92 % a -30.2 % sous la cloture, 4.13 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 2.71-2.77 (A) ; 2.41-2.41 (C). stop INDICATIF 2.04 (-6.7 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (1.21 ATR sous le plus haut 20 s., RSI(2) 53.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 2.92-2.99 (C, -4.71 %) ; 2.71-2.77 (A, -11.91 %) ; 2.41-2.41 (C, -23.38 %)
- Resistances reelles au-dessus : 3.26-3.32 (A, 3.76 %) ; 3.37-3.41 (A, 7.45 %) ; 3.88-3.88 (C, 23.57 %) ; 3.99-4.01 (B, 27.23 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.81 %)** : le gap seul le franchit 0.863 % des séances (11 fois sur 1274).
   - exécution **2.302 pt plus bas** dans le cas TYPIQUE (médiane), 16.801 au p90, **27.603 au pire**
   - perte réelle **11.717 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 4.81 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0596 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.114** [0.0731 ; 0.1677] _(largeur 9.5 pt, n_eff 173.1)_
   - swing : **0.4811** [0.4288 ; 0.5337] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4755** [0.4233 ; 0.5282] _(largeur 10.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.65 %** | CVaR **-8.97 %** | vol 3.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 6.13 % contre 3.52 % aujourd'hui, rapport 1.74)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0978** (β de hausse 0.9194, asymétrie 1.194) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.9691 sur atr_grid (1.25 ATR, 5.442 %) — p(stop avant cible) 0.5628 [0.51 ; 0.61], R/R 6.713, perte reelle 6.134 % (gap inclus), CVaR 12.991 %, EV -0.4062 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1917 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.563, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 12.99 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.31 ATR (stop 3.452 %) — p(stop avant cible) 0.6972 [0.65 ; 0.74], R/R 10.568, perte reelle 3.896 % (gap inclus), EV -0.2616 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 10.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.697, borne haute 0.744 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.12 ATR du spot — compartiment <1, mesure a 50.7 % de casse (IC clusterise [0.471 ; 0.542] sur 1138 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 0.1 % x 41.18 % + P(rien) 30.2 % x 8.01 % ne couvrent pas P(stop) 69.7 % x 3.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+41.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 6.532 %) — p(stop avant cible) 0.4969 [0.44 ; 0.55], R/R 5.524, perte reelle 7.454 % (gap inclus), EV -0.763 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 0.2 % x 41.18 % + P(rien) 50.1 % x 5.73 % ne couvrent pas P(stop) 49.7 % x 7.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.15 ATR (stop 15.809 %) — p(stop avant cible) 0.1499 [0.12 ; 0.19], R/R 2.331, perte reelle 17.667 % (gap inclus), EV -1.5831 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 0.2 % x 41.18 % + P(rien) 84.9 % x 1.18 % ne couvrent pas P(stop) 15.0 % x 17.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 5.37 ATR (stop 25.49 %) — p(stop avant cible) 0.0616 [0.04 ; 0.09], R/R 1.599, perte reelle 25.745 % (gap inclus), EV -1.639 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.64 %) : P(cible) 0.2 % x 41.18 % + P(rien) 93.7 % x -0.13 % ne couvrent pas P(stop) 6.2 % x 25.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.31 ATR (stop 2.644 %) — p(stop avant cible) 0.7776 [0.73 ; 0.82], R/R 13.688, perte reelle 3.008 % (gap inclus), EV -0.3306 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.778, borne haute 0.819 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.1 % x 41.18 % + P(rien) 22.1 % x 8.90 % ne couvrent pas P(stop) 77.8 % x 3.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+41.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 4.354 %) — p(stop avant cible) 0.6483 [0.60 ; 0.70], R/R 8.506, perte reelle 4.841 % (gap inclus), EV -0.3762 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.648, borne haute 0.697 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.1 % x 41.18 % + P(rien) 35.0 % x 7.74 % ne couvrent pas P(stop) 64.8 % x 4.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 5.442 %) — p(stop avant cible) 0.5628 [0.51 ; 0.61], R/R 6.713, perte reelle 6.134 % (gap inclus), EV -0.4062 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.563, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 0.1 % x 41.18 % + P(rien) 43.6 % x 6.87 % ne couvrent pas P(stop) 56.3 % x 6.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 7.619 %) — p(stop avant cible) 0.4282 [0.38 ; 0.48], R/R 4.582, perte reelle 8.987 % (gap inclus), EV -1.0368 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.2 % x 41.18 % + P(rien) 57.0 % x 4.82 % ne couvrent pas P(stop) 42.8 % x 8.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 8.708 %) — p(stop avant cible) 0.385 [0.33 ; 0.44], R/R 4.09, perte reelle 10.068 % (gap inclus), EV -1.169 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.2 % x 41.18 % + P(rien) 61.4 % x 4.31 % ne couvrent pas P(stop) 38.5 % x 10.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 9.796 %) — p(stop avant cible) 0.3405 [0.29 ; 0.39], R/R 3.67, perte reelle 11.22 % (gap inclus), EV -1.2624 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.2 % x 41.18 % + P(rien) 65.8 % x 3.79 % ne couvrent pas P(stop) 34.1 % x 11.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 10.885 %) — p(stop avant cible) 0.3149 [0.27 ; 0.37], R/R 3.354, perte reelle 12.279 % (gap inclus), EV -1.4683 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.47 %) : P(cible) 0.2 % x 41.18 % + P(rien) 68.4 % x 3.41 % ne couvrent pas P(stop) 31.5 % x 12.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 11.973 %) — p(stop avant cible) 0.27 [0.23 ; 0.32], R/R 3.067, perte reelle 13.424 % (gap inclus), EV -1.5698 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 0.2 % x 41.18 % + P(rien) 72.9 % x 2.73 % ne couvrent pas P(stop) 27.0 % x 13.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 3.15 ATR (stop 15.0 %) — p(stop avant cible) 0.1648 [0.13 ; 0.21], R/R 2.443, perte reelle 16.855 % (gap inclus), EV -1.5924 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 0.2 % x 41.18 % + P(rien) 83.4 % x 1.34 % ne couvrent pas P(stop) 16.5 % x 16.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 17.416 %) — p(stop avant cible) 0.1165 [0.09 ; 0.15], R/R 2.128, perte reelle 19.349 % (gap inclus), EV -1.456 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.46 %) : P(cible) 0.2 % x 41.18 % + P(rien) 88.2 % x 0.83 % ne couvrent pas P(stop) 11.7 % x 19.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 19.593 %) — p(stop avant cible) 0.0964 [0.07 ; 0.13], R/R 1.943, perte reelle 21.191 % (gap inclus), EV -1.5168 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 0.2 % x 41.18 % + P(rien) 90.2 % x 0.51 % ne couvrent pas P(stop) 9.6 % x 21.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 21.77 %) — p(stop avant cible) 0.0809 [0.06 ; 0.11], R/R 1.808, perte reelle 22.777 % (gap inclus), EV -1.5399 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.2 % x 41.18 % + P(rien) 91.8 % x 0.26 % ne couvrent pas P(stop) 8.1 % x 22.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 5.37 ATR (stop 24.682 %) — p(stop avant cible) 0.0643 [0.04 ; 0.09], R/R 1.642, perte reelle 25.075 % (gap inclus), EV -1.598 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 0.2 % x 41.18 % + P(rien) 93.4 % x -0.06 % ne couvrent pas P(stop) 6.4 % x 25.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 26.124 %) — p(stop avant cible) 0.0571 [0.04 ; 0.09], R/R 1.558, perte reelle 26.426 % (gap inclus), EV -1.6591 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 0.2 % x 41.18 % + P(rien) 94.1 % x -0.23 % ne couvrent pas P(stop) 5.7 % x 26.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 28.301 %) — p(stop avant cible) 0.0436 [0.03 ; 0.07], R/R 1.443, perte reelle 28.529 % (gap inclus), EV -1.7286 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 0.2 % x 41.18 % + P(rien) 95.5 % x -0.58 % ne couvrent pas P(stop) 4.4 % x 28.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 30.478 %) — p(stop avant cible) 0.0356 [0.02 ; 0.06], R/R 1.343, perte reelle 30.653 % (gap inclus), EV -1.7752 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.78 %) : P(cible) 0.2 % x 41.18 % + P(rien) 96.3 % x -0.78 % ne couvrent pas P(stop) 3.6 % x 30.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 32.655 %) — p(stop avant cible) 0.0356 [0.02 ; 0.06], R/R 1.258, perte reelle 32.739 % (gap inclus), EV -1.8495 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.85 %) : P(cible) 0.2 % x 41.18 % + P(rien) 96.3 % x -0.78 % ne couvrent pas P(stop) 3.6 % x 32.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 34.832 %) — p(stop avant cible) 0.0354 [0.02 ; 0.06], R/R 1.182, perte reelle 34.841 % (gap inclus), EV -1.9227 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 0.2 % x 41.18 % + P(rien) 96.3 % x -0.78 % ne couvrent pas P(stop) 3.5 % x 34.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.14, ATR14 0.1367 (4.354 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.598 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.218 % | 3.1332 | 88.76 % | 91.51 % | 93.38 % | 95.35 % | 97.21 % | 98.29 % |
| 0.1 ATR | 0.435 % | 3.1263 | 81.36 % | 86.67 % | 89.53 % | 92.38 % | 95.52 % | 97.19 % |
| 0.15 ATR | 0.653 % | 3.1195 | 75.35 % | 82.92 % | 86.56 % | 89.7 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.871 % | 3.1127 | 69.13 % | 79.17 % | 83.5 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.088 % | 3.1058 | 63.21 % | 75.72 % | 80.24 % | 84.55 % | 89.85 % | 93.47 % |
| 0.35 ATR | 1.524 % | 3.0922 | 51.87 % | 67.32 % | 73.52 % | 79.31 % | 85.87 % | 91.46 % |
| 0.5 ATR | 2.177 % | 3.0716 | 35.6 % | 54.89 % | 62.65 % | 70.4 % | 79.8 % | 88.14 % |
| 0.75 ATR | 3.265 % | 3.0375 | 18.84 % | 37.41 % | 47.04 % | 58.81 % | 71.14 % | 81.81 % |
| 1.0 ATR | 4.354 % | 3.0033 | 9.86 % | 24.88 % | 35.47 % | 46.83 % | 61.79 % | 75.38 % |
| 1.25 ATR | 5.442 % | 2.9691 | 4.64 % | 16.88 % | 26.88 % | 38.91 % | 55.22 % | 70.35 % |
| 1.5 ATR | 6.531 % | 2.9349 | 2.86 % | 10.96 % | 19.07 % | 30.89 % | 48.16 % | 65.43 % |
| 2.0 ATR | 8.708 % | 2.8666 | 1.28 % | 4.74 % | 9.09 % | 19.01 % | 34.73 % | 53.77 % |
| 2.5 ATR | 10.885 % | 2.7982 | 0.49 % | 2.67 % | 5.53 % | 11.98 % | 27.46 % | 46.43 % |
| 3.0 ATR | 13.062 % | 2.7299 | 0.39 % | 1.58 % | 3.75 % | 8.51 % | 20.7 % | 39.4 % |
| 4.0 ATR | 17.416 % | 2.5931 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.94 % | 25.03 % |
| 6.0 ATR | 26.124 % | 2.3197 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.73 ATR | 1.00 ATR | 1.23 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.15 ATR | 1.58 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.79 ATR | 1.07 ATR | 1.31 ATR | 1.47 ATR | 1.95 ATR | 2.65 ATR |
| **5 s.** | 0.42 ATR | 0.93 ATR | 1.06 ATR | 1.43 ATR | 1.75 ATR | 1.96 ATR | 2.79 ATR | 3.81 ATR |
| **10 s.** | 0.64 ATR | 1.44 ATR | 1.62 ATR | 2.12 ATR | 2.68 ATR | 3.08 ATR | 4.57 ATR | hors grille |
| **20 s.** | 1.02 ATR | 2.26 ATR | 2.60 ATR | 3.44 ATR | 4.00 ATR | 4.89 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.413 ATR au-dessus du haut de la grille, 0.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.641–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.265 %, prix 3.0375), p(touche) 37.41 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (68.4 % des re-echantillons)
- **3 seance(s)** : plage utile 0.794–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.354 %, prix 3.0033), p(touche) 35.47 % (en stress 96.08 %)  ✅ optimum identifie (68.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.058–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.442 %, prix 2.9691), p(touche) 38.91 % (en stress 94.06 %)  ✅ optimum identifie (75.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.618–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.708 %, prix 2.8666), p(touche) 34.73 % (en stress 98.02 %)  ✅ optimum identifie (73.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.602–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.062 %, prix 2.7299), p(touche) 39.4 % (en stress 98.0 %)  ✅ optimum identifie (82.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : €-0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 12 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.0 | bear 6.0 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 399.0 (= 127 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.303% → cible +2.182% / stop −3.999%, p_fill 88%, n_eff≈93.6) : P(cible|rempli) **30%** · **EV/risk -0.102** (×p_fill ; si rempli -0.46% du capital)
  - **swing** (entrée dip −0.453% → cible +8.238% / stop −4.376%, p_fill 87%, n_eff≈101.1) : P(cible|rempli) **18%** · **EV/risk -0.159** (×p_fill ; si rempli -0.80% du capital)
  - **deep** (entrée dip −0.648% → cible +8.45% / stop −6.574%, p_fill 90%, n_eff≈99.5) : P(cible|rempli) **23%** · **EV/risk -0.276** (×p_fill ; si rempli -2.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→67% · +2.0%→44% · +3.0%→26% · +5.0%→8% · +8.0%→1%
- Range intraday médian 4.09% (p90 6.5%) · excursion haute méd. +1.72% / basse méd. −1.92%
- Profil de vol intra : ouverture 2.643% vs midi 1.227% vs clôture 1.2% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.139)_ ; drift intra méd. -0.506% ; recovery-V 28%
- **σ réalisé intraday** 3.475% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 81% / whipsaw 51%
- POC intraday (dernière séance, temps-au-prix) : 2.7892 (VA 2.7604–2.8204 ; dernier close 2.806)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 28% · rebond 80% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.91% · R/R 0.81 (high win-rate)
- Gaps overnight (n=159) : méd. 0.35% · baisse 41% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.26%) · haut méd +0.43% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −0.96% (p90 −2.47%) · haut méd +0.78% · range méd 1.98%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −2.82%) · haut méd +1.06% · range méd 2.33%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.16%) · haut méd +1.11% · range méd 2.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2.81 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 84% (129/159) · gap 21% · délai 0.3min · rebond 63% (86/129) (MFE +1.64%)
   - −1.0% : fill 30min 42% · séance 72% (112/159) · gap 10% · délai 4.8min · rebond 65% (76/112) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 56% (91/159) · gap 5% · délai 30.8min · rebond 68% (61/91) (MFE +1.46%)
   - −2.0% : fill 30min 19% · séance 47% (76/159) · gap 4% · délai 68.0min · rebond 60% (45/76) (MFE +1.59%)
   - −3.0% : fill 30min 8% · séance 28% (44/159) · gap 2% · délai 112.8min · rebond 80% (32/44) (MFE +1.91%)
   - −4.0% : fill 30min 2% · séance 12% (20/159) · gap 0% · délai 390.8min · rebond 36% (10/20) (MFE +0.51%)
   - −5.0% : fill 30min 1% · séance 6% (11/159) · gap 0% · délai 215.4min · rebond 14% (5/11) (MFE +0.65%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.43%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.02%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.0%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=832 jambes) : jambe baissière méd −1.06% (p90 −2.31%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 80% (41/49) · rebond 67% (29/41)
      · −2.0% : fill 63% (32/49) · rebond 69% (20/32)
      · −3.0% : fill 36% (19/49) · rebond 79% (13/19)
      · −4.0% : fill 15% (10/49) · rebond 15% (4/10)
      · −5.0% : fill 12% (7/49) · rebond 15% (3/7)
   - **flat** (32 séances) :
      · −1.0% : fill 75% (25/32) · rebond 70% (16/25)
      · −2.0% : fill 50% (18/32) · rebond 65% (10/18)
      · −3.0% : fill 36% (11/32) · rebond 90% (9/11)
      · −4.0% : fill 14% (4/32) · rebond 60% (2/4)
      · −5.0% : fill 4% (2/32) · rebond 23% (1/2)
   - **gap-up** (78 séances) :
      · −1.0% : fill 67% (46/78) · rebond 61% (31/46)
      · −2.0% : fill 38% (26/78) · rebond 50% (15/26)
      · −3.0% : fill 20% (14/78) · rebond 73% (10/14)
      · −4.0% : fill 9% (6/78) · rebond 36% (4/6)
      · −5.0% : fill 3% (2/78) · rebond 7% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (79 cas) · 28% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 22% si rouge (base 42% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 281min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **66%** · continue >prix actuel 46% ; creux résiduel méd -1.84% (q20 -2.76%) → **SL/trailing à −2.76%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.97% / q75 +2.56% → **scale +1.97% / runner +2.56%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **22%** (continue à baisser 66%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.22%** (au-delà de la MAE q10 -4.22%), cible rebond +1.56% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +3.32%] · haut q95 +3.93% · bas q05 -3.48%
   - 60min (n=160) : retour [-2.85% .. +3.84%] · haut q95 +4.96% · bas q05 -3.74%
   - 2h (n=160) : retour [-2.98% .. +3.29%] · haut q95 +5.01% · bas q05 -3.91%
   - 4h (n=160) : retour [-3.29% .. +3.8%] · haut q95 +5.1% · bas q05 -4.32%
   - 6h (n=160) : retour [-3.66% .. +4.62%] · haut q95 +5.27% · bas q05 -4.33%
   - session (n=160) : retour [-4.52% .. +4.02%] · haut q95 +5.67% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 3.11%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.1 · part idiosyncratique 0.9
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 70.6  _(surachat)_
- **ADX** : 19.8  _(pas de tendance nette)_
- **MACD** : hist 0.041  _(pas de croisement recent)_
- **BB** : %B 0.82 · largeur 24.4%
- **ATR** : 0.14 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.168  _(accumulation)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 2.91 · MA50 2.89 · MA200 4.24  _(prix > MA20)_
- **Dist MA** : MA20 +7.9% · MA50 +8.7% · MA200 -25.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (726404 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
