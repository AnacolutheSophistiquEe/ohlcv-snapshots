# EVT

**Generated** : 2026-10-30T21:43:16.084655+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.82  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (5 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €2.82 (+2.2% vs entrée) · entrée €2.76 · stop €2.58 · T1 €3.11 · R/R 1.94  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-30 : 2.82 · ATR Wilder 0.1299 (4.61 %)_
- **Swing** : plage **2.64 → 2.51** (-6.21 % a -10.77 % sous la cloture, 0.99 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.34 (-6.89 % sous le bas ; sous le support 2.41-2.41 (- 0,5 ATR)).
- **Deep** : plage **2.51 → 1.98** (-10.77 % a -29.79 % sous la cloture, 4.13 ATR) — touchee 49 % → 15 % du temps en 20 seances ; supports reels dans la plage : 2.41-2.41 (C). stop INDICATIF 1.85 (-6.56 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.29 ATR sous le plus haut 20 s., RSI(2) 20.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 2.71-2.77 (C, -1.85 %) ; 2.41-2.41 (C, -14.62 %)
- Resistances reelles au-dessus : 3.1-3.14 (A, 9.94 %) ; 3.18-3.24 (B, 12.7 %) ; 3.37-3.41 (A, 19.73 %) ; 3.88-3.88 (C, 37.69 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.36 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **5.464 pt plus bas** dans le cas TYPIQUE (médiane), 19.732 au p90, **24.053 au pire**
   - perte réelle **18.001 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 8.36 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0378 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1137** [0.0729 ; 0.1673] _(largeur 9.4 pt, n_eff 173.1)_
   - swing : **0.3391** [0.2907 ; 0.3902] _(largeur 9.9 pt, n_eff 345.8)_
   - deep : **0.4757** [0.4234 ; 0.5284] _(largeur 10.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.8 %** | CVaR **-8.97 %** | vol 3.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 6.12 % contre 3.51 % aujourd'hui, rapport 1.74)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1145** (β de hausse 0.9333, asymétrie 1.1942) vs GDAXI — 599 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.671 sur grid_snapped (0.83 ATR, 5.216 %) — p(stop avant cible) 0.6013 [0.55 ; 0.65], R/R 6.622, perte reelle 5.92 % (gap inclus), CVaR 13.311 %, EV -0.8026 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2858 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 13.31 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.83 ATR (stop 6.015 %) — p(stop avant cible) 0.5521 [0.50 ; 0.60], R/R 5.714, perte reelle 6.86 % (gap inclus), EV -0.9852 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.552, borne haute 0.604 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.98 % > budget 12.00 %
      - ⚠ support DETECTE a 0.83 ATR du spot — compartiment <1, mesure a 47.3 % de casse (IC clusterise [0.443 ; 0.505] sur 1164 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 0.2 % x 39.20 % + P(rien) 44.6 % x 6.14 % ne couvrent pas P(stop) 55.2 % x 6.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.17 ATR (stop 16.803 %) — p(stop avant cible) 0.1405 [0.11 ; 0.18], R/R 2.103, perte reelle 18.645 % (gap inclus), EV -2.06 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 0.2 % x 39.20 % + P(rien) 85.8 % x 0.58 % ne couvrent pas P(stop) 14.1 % x 18.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.153 %) — p(stop avant cible) 0.9065 [0.87 ; 0.93], R/R 29.434, perte reelle 1.332 % (gap inclus), EV -0.3007 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 29.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.906, borne haute 0.934 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.1 % x 39.20 % + P(rien) 9.3 % x 9.47 % ne couvrent pas P(stop) 90.6 % x 1.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.307 %) — p(stop avant cible) 0.8303 [0.79 ; 0.87], R/R 14.726, perte reelle 2.662 % (gap inclus), EV -0.6391 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 14.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.830, borne haute 0.867 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.1 % x 39.20 % + P(rien) 16.9 % x 9.08 % ne couvrent pas P(stop) 83.0 % x 2.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 grid_snapped a 0.83 ATR (stop 5.216 %) — p(stop avant cible) 0.6013 [0.55 ; 0.65], R/R 6.622, perte reelle 5.92 % (gap inclus), EV -0.8026 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 13.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 0.1 % x 39.20 % + P(rien) 39.7 % x 6.81 % ne couvrent pas P(stop) 60.1 % x 5.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 6.92 %) — p(stop avant cible) 0.4995 [0.45 ; 0.55], R/R 4.844, perte reelle 8.092 % (gap inclus), EV -1.3518 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.499, borne haute 0.552 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 18.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 0.2 % x 39.20 % + P(rien) 49.9 % x 5.27 % ne couvrent pas P(stop) 50.0 % x 8.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 8.073 %) — p(stop avant cible) 0.4301 [0.38 ; 0.48], R/R 4.155, perte reelle 9.435 % (gap inclus), EV -1.5523 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.55 %) : P(cible) 0.2 % x 39.20 % + P(rien) 56.8 % x 4.30 % ne couvrent pas P(stop) 43.0 % x 9.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 9.226 %) — p(stop avant cible) 0.3717 [0.32 ; 0.42], R/R 3.672, perte reelle 10.675 % (gap inclus), EV -1.6737 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.67 %) : P(cible) 0.2 % x 39.20 % + P(rien) 62.7 % x 3.56 % ne couvrent pas P(stop) 37.2 % x 10.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 10.38 %) — p(stop avant cible) 0.3413 [0.29 ; 0.39], R/R 3.322, perte reelle 11.802 % (gap inclus), EV -1.89 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.89 %) : P(cible) 0.2 % x 39.20 % + P(rien) 65.7 % x 3.16 % ne couvrent pas P(stop) 34.1 % x 11.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 11.533 %) — p(stop avant cible) 0.3053 [0.26 ; 0.36], R/R 3.03, perte reelle 12.939 % (gap inclus), EV -2.038 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 0.2 % x 39.20 % + P(rien) 69.3 % x 2.67 % ne couvrent pas P(stop) 30.5 % x 12.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 12.686 %) — p(stop avant cible) 0.2627 [0.22 ; 0.31], R/R 2.765, perte reelle 14.179 % (gap inclus), EV -2.16 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.16 %) : P(cible) 0.2 % x 39.20 % + P(rien) 73.6 % x 2.04 % ne couvrent pas P(stop) 26.3 % x 14.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 3.17 ATR (stop 16.004 %) — p(stop avant cible) 0.155 [0.12 ; 0.20], R/R 2.198, perte reelle 17.836 % (gap inclus), EV -2.0985 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.10 %) : P(cible) 0.2 % x 39.20 % + P(rien) 84.3 % x 0.72 % ne couvrent pas P(stop) 15.5 % x 17.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 18.453 %) — p(stop avant cible) 0.1088 [0.08 ; 0.14], R/R 1.931, perte reelle 20.298 % (gap inclus), EV -1.9614 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.96 %) : P(cible) 0.2 % x 39.20 % + P(rien) 88.9 % x 0.21 % ne couvrent pas P(stop) 10.9 % x 20.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 20.759 %) — p(stop avant cible) 0.0915 [0.06 ; 0.13], R/R 1.781, perte reelle 22.006 % (gap inclus), EV -2.0176 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 0.2 % x 39.20 % + P(rien) 90.7 % x -0.07 % ne couvrent pas P(stop) 9.2 % x 22.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 23.066 %) — p(stop avant cible) 0.0748 [0.05 ; 0.11], R/R 1.647, perte reelle 23.805 % (gap inclus), EV -2.0673 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 0.2 % x 39.20 % + P(rien) 92.4 % x -0.38 % ne couvrent pas P(stop) 7.5 % x 23.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 25.373 %) — p(stop avant cible) 0.0649 [0.04 ; 0.09], R/R 1.529, perte reelle 25.643 % (gap inclus), EV -2.1514 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.15 %) : P(cible) 0.2 % x 39.20 % + P(rien) 93.3 % x -0.59 % ne couvrent pas P(stop) 6.5 % x 25.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 27.679 %) — p(stop avant cible) 0.0548 [0.03 ; 0.08], R/R 1.406, perte reelle 27.891 % (gap inclus), EV -2.2538 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 0.2 % x 39.20 % + P(rien) 94.4 % x -0.84 % ne couvrent pas P(stop) 5.5 % x 27.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 29.986 %) — p(stop avant cible) 0.0375 [0.02 ; 0.06], R/R 1.299, perte reelle 30.184 % (gap inclus), EV -2.2837 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.28 %) : P(cible) 0.2 % x 39.20 % + P(rien) 96.1 % x -1.26 % ne couvrent pas P(stop) 3.8 % x 30.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 32.292 %) — p(stop avant cible) 0.0375 [0.02 ; 0.06], R/R 1.21, perte reelle 32.389 % (gap inclus), EV -2.3664 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.37 %) : P(cible) 0.2 % x 39.20 % + P(rien) 96.1 % x -1.26 % ne couvrent pas P(stop) 3.8 % x 32.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 34.599 %) — p(stop avant cible) 0.0373 [0.02 ; 0.06], R/R 1.133, perte reelle 34.615 % (gap inclus), EV -2.4487 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 0.2 % x 39.20 % + P(rien) 96.1 % x -1.27 % ne couvrent pas P(stop) 3.7 % x 34.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 36.906 %) — p(stop avant cible) 0.0249 [0.01 ; 0.05], R/R 1.062, perte reelle 36.906 % (gap inclus), EV -2.4426 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.44 %) : P(cible) 0.2 % x 39.20 % + P(rien) 97.4 % x -1.63 % ne couvrent pas P(stop) 2.5 % x 36.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.818, ATR14 0.13 (4.613 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.693 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.231 % | 2.8115 | 88.86 % | 91.61 % | 93.48 % | 95.45 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.461 % | 2.805 | 81.36 % | 86.67 % | 89.53 % | 92.57 % | 95.72 % | 97.19 % |
| 0.15 ATR | 0.692 % | 2.7985 | 75.25 % | 82.82 % | 86.56 % | 89.9 % | 94.03 % | 96.08 % |
| 0.2 ATR | 0.923 % | 2.792 | 69.13 % | 79.07 % | 83.5 % | 87.33 % | 92.14 % | 94.77 % |
| 0.25 ATR | 1.153 % | 2.7855 | 63.21 % | 75.62 % | 80.24 % | 84.75 % | 90.15 % | 93.57 % |
| 0.35 ATR | 1.615 % | 2.7725 | 51.87 % | 67.32 % | 73.62 % | 79.7 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.307 % | 2.753 | 35.5 % | 54.79 % | 62.75 % | 70.79 % | 80.3 % | 88.34 % |
| 0.75 ATR | 3.46 % | 2.7205 | 19.03 % | 37.61 % | 47.33 % | 59.31 % | 71.74 % | 82.11 % |
| 1.0 ATR | 4.613 % | 2.688 | 9.96 % | 24.88 % | 35.77 % | 47.43 % | 62.49 % | 75.68 % |
| 1.25 ATR | 5.767 % | 2.6555 | 4.73 % | 17.18 % | 27.27 % | 39.6 % | 56.02 % | 70.65 % |
| 1.5 ATR | 6.92 % | 2.623 | 2.96 % | 11.25 % | 19.57 % | 31.58 % | 48.86 % | 65.63 % |
| 2.0 ATR | 9.226 % | 2.558 | 1.38 % | 5.03 % | 9.58 % | 19.6 % | 35.42 % | 53.97 % |
| 2.5 ATR | 11.533 % | 2.493 | 0.49 % | 2.86 % | 5.93 % | 12.48 % | 28.06 % | 46.53 % |
| 3.0 ATR | 13.84 % | 2.428 | 0.39 % | 1.68 % | 3.85 % | 8.81 % | 21.19 % | 39.6 % |
| 4.0 ATR | 18.453 % | 2.298 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 12.04 % | 25.13 % |
| 6.0 ATR | 27.679 % | 2.038 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.73 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.01 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.08 ATR | 1.32 ATR | 1.49 ATR | 1.98 ATR | 2.72 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.46 ATR | 1.77 ATR | 1.98 ATR | 2.84 ATR | 3.82 ATR |
| **10 s.** | 0.66 ATR | 1.46 ATR | 1.64 ATR | 2.16 ATR | 2.72 ATR | 3.13 ATR | 4.59 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.27 ATR | 2.61 ATR | 3.46 ATR | 4.02 ATR | 4.89 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (63.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.642–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.46 %, prix 2.7205), p(touche) 37.61 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (70.2 % des re-echantillons)
- **3 seance(s)** : plage utile 0.8–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.613 %, prix 2.688), p(touche) 35.77 % (en stress 96.08 %)  ✅ optimum identifie (73.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.078–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.767 %, prix 2.6555), p(touche) 39.6 % (en stress 94.06 %)  ✅ optimum identifie (79.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.644–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.226 %, prix 2.558), p(touche) 35.42 % (en stress 98.02 %)  ✅ optimum identifie (72.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.61–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.84 %, prix 2.428), p(touche) 39.6 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (83.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.087 | EV/share : €-0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 7 % | T2 2 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 34.2 | bear 5.0 | side 60.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 158.0 (= 56 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.96% → cible +2.329% / stop −3.999%, p_fill 76%, n_eff≈79.6) : P(cible|rempli) **35%** · **EV/risk -0.021** (×p_fill ; si rempli -0.11% du capital)
  - **swing** (entrée dip −2.111% → cible +12.771% / stop −6.384%, p_fill 58%, n_eff≈65.3) : P(cible|rempli) **4%** · **EV/risk -0.157** (×p_fill ; si rempli -1.74% du capital)
  - **deep** (entrée dip −3.26% → cible +14.111% / stop −7.153%, p_fill 61%, n_eff≈66.4) : P(cible|rempli) **7%** · **EV/risk -0.255** (×p_fill ; si rempli -2.99% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.12 · part idiosyncratique 0.89
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 68.5  _(momentum haussier)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist 0.039  _(pas de croisement recent)_
- **BB** : %B 0.58 · largeur 24.3%
- **ATR** : 0.13 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.195  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 2.76 · MA50 2.93 · MA200 4.38  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 -3.9% · MA200 -35.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (838381 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
