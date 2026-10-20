# EVT

**Generated** : 2026-10-20T00:06:22.901393+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.62  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 4/125 fenêtres (p_fill pondéré 3 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €2.62 (+6.9% vs entrée) · entrée €2.45 · stop €2.26 · T1 €2.54 · R/R 0.47  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 184 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-19 : 2.62 · ATR Wilder 0.1533 (5.85 %)_
- **Swing** : plage **2.42 → 2.27** (-7.82 % a -13.49 % sous la cloture, 0.97 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.11 (-6.76 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **2.27 → 1.63** (-13.49 % a -37.82 % sous la cloture, 4.16 ATR) — touchee 48 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 1.48 (-9.41 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (3.39 ATR sous le plus haut 20 s., RSI(2) 74.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Resistances reelles au-dessus : 2.71-2.77 (B, 3.44 %) ; 3.1-3.14 (A, 18.24 %) ; 3.18-3.24 (B, 21.22 %) ; 3.37-3.41 (A, 28.78 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (19.01 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **8.002 pt plus bas** dans le cas TYPIQUE (médiane), 12.323 au p90, **13.403 au pire**
   - perte réelle **27.012 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 19.01 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0126 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0259** [0.0094 ; 0.058] _(largeur 4.9 pt, n_eff 173.1)_
   - swing : **0.3041** [0.2574 ; 0.3541] _(largeur 9.7 pt, n_eff 345.8)_
   - deep : **0.286** [0.2403 ; 0.3353] _(largeur 9.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.8 %** | CVaR **-8.97 %** | vol 3.6 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 6.06 % contre 3.61 % aujourd'hui, rapport 1.68)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1142** (β de hausse 0.9329, asymétrie 1.1944) vs GDAXI — 598 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.454 sur atr_grid (1.0 ATR, 6.336 %) — p(stop avant cible) 0.5382 [0.49 ; 0.59], R/R 3.811, perte reelle 7.284 % (gap inclus), CVaR 15.77 %, EV -1.3005 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2392 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.538, borne haute 0.590 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 15.77 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.504 %) — p(stop avant cible) 0.3508 [0.30 ; 0.40], R/R 2.5, perte reelle 11.101 % (gap inclus), EV -1.8228 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 2.2 % x 27.76 % + P(rien) 62.7 % x 2.32 % ne couvrent pas P(stop) 35.1 % x 11.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.49 ATR (stop 12.679 %) — p(stop avant cible) 0.2474 [0.20 ; 0.29], R/R 1.935, perte reelle 14.342 % (gap inclus), EV -2.2094 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 2.3 % x 27.76 % + P(rien) 73.0 % x 0.97 % ne couvrent pas P(stop) 24.7 % x 14.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.584 %) — p(stop avant cible) 0.8671 [0.83 ; 0.90], R/R 14.886, perte reelle 1.865 % (gap inclus), EV -0.4045 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 14.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.867, borne haute 0.900 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 0.9 % x 27.76 % + P(rien) 12.4 % x 7.77 % ne couvrent pas P(stop) 86.7 % x 1.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.168 %) — p(stop avant cible) 0.7359 [0.69 ; 0.78], R/R 7.777, perte reelle 3.569 % (gap inclus), EV -0.598 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 7.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.736, borne haute 0.780 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 1.7 % x 27.76 % + P(rien) 24.7 % x 6.26 % ne couvrent pas P(stop) 73.6 % x 3.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.752 %) — p(stop avant cible) 0.6485 [0.60 ; 0.70], R/R 5.065, perte reelle 5.48 % (gap inclus), EV -1.0083 % — **REFUSE**
      - refuse : cible atteinte seulement 2.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.648, borne haute 0.697 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 13.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 2.0 % x 27.76 % + P(rien) 33.2 % x 6.02 % ne couvrent pas P(stop) 64.8 % x 5.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.336 %) — p(stop avant cible) 0.5382 [0.49 ; 0.59], R/R 3.811, perte reelle 7.284 % (gap inclus), EV -1.3005 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.538, borne haute 0.590 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 2.2 % x 27.76 % + P(rien) 44.0 % x 4.56 % ne couvrent pas P(stop) 53.8 % x 7.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.49 ATR (stop 11.336 %) — p(stop avant cible) 0.301 [0.25 ; 0.35], R/R 2.157, perte reelle 12.869 % (gap inclus), EV -2.116 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 2.2 % x 27.76 % + P(rien) 67.7 % x 1.69 % ne couvrent pas P(stop) 30.1 % x 12.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 14.256 %) — p(stop avant cible) 0.1829 [0.14 ; 0.23], R/R 1.712, perte reelle 16.213 % (gap inclus), EV -2.2219 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 2.3 % x 27.76 % + P(rien) 79.4 % x 0.14 % ne couvrent pas P(stop) 18.3 % x 16.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 15.84 %) — p(stop avant cible) 0.1489 [0.11 ; 0.19], R/R 1.551, perte reelle 17.893 % (gap inclus), EV -2.2561 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 2.3 % x 27.76 % + P(rien) 82.8 % x -0.27 % ne couvrent pas P(stop) 14.9 % x 17.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 17.424 %) — p(stop avant cible) 0.1235 [0.09 ; 0.16], R/R 1.427, perte reelle 19.445 % (gap inclus), EV -2.2452 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 2.3 % x 27.76 % + P(rien) 85.3 % x -0.57 % ne couvrent pas P(stop) 12.3 % x 19.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 19.008 %) — p(stop avant cible) 0.1085 [0.08 ; 0.14], R/R 1.339, perte reelle 20.727 % (gap inclus), EV -2.2694 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.27 %) : P(cible) 2.3 % x 27.76 % + P(rien) 86.8 % x -0.77 % ne couvrent pas P(stop) 10.8 % x 20.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 22.176 %) — p(stop avant cible) 0.0826 [0.06 ; 0.12], R/R 1.2, perte reelle 23.128 % (gap inclus), EV -2.3435 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 2.3 % x 27.76 % + P(rien) 89.4 % x -1.20 % ne couvrent pas P(stop) 8.3 % x 23.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 25.344 %) — p(stop avant cible) 0.0683 [0.05 ; 0.10], R/R 1.083, perte reelle 25.617 % (gap inclus), EV -2.4663 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 2.3 % x 27.76 % + P(rien) 90.8 % x -1.50 % ne couvrent pas P(stop) 6.8 % x 25.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 28.511 %) — p(stop avant cible) 0.0484 [0.03 ; 0.07], R/R 0.966, perte reelle 28.731 % (gap inclus), EV -2.5862 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.59 %) : P(cible) 2.3 % x 27.76 % + P(rien) 92.8 % x -1.98 % ne couvrent pas P(stop) 4.8 % x 28.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 31.679 %) — p(stop avant cible) 0.0395 [0.02 ; 0.06], R/R 0.873, perte reelle 31.801 % (gap inclus), EV -2.6729 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.67 %) : P(cible) 2.3 % x 27.76 % + P(rien) 93.7 % x -2.20 % ne couvrent pas P(stop) 4.0 % x 31.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 34.847 %) — p(stop avant cible) 0.0393 [0.02 ; 0.06], R/R 0.796, perte reelle 34.856 % (gap inclus), EV -2.7924 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.79 %) : P(cible) 2.3 % x 27.76 % + P(rien) 93.8 % x -2.20 % ne couvrent pas P(stop) 3.9 % x 34.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 38.015 %) — p(stop avant cible) 0.0138 [0.01 ; 0.03], R/R 0.73, perte reelle 38.015 % (gap inclus), EV -2.6924 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.69 %) : P(cible) 2.3 % x 27.76 % + P(rien) 96.3 % x -2.92 % ne couvrent pas P(stop) 1.4 % x 38.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 41.183 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.674, perte reelle 41.183 % (gap inclus), EV -2.6296 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.63 %) : P(cible) 2.3 % x 27.76 % + P(rien) 97.6 % x -3.30 % ne couvrent pas P(stop) 0.1 % x 41.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 44.351 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.626, perte reelle 44.351 % (gap inclus), EV -2.6222 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.62 %) : P(cible) 2.3 % x 27.76 % + P(rien) 97.7 % x -3.34 % ne couvrent pas P(stop) 0.0 % x 44.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 47.519 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.584, perte reelle 47.519 % (gap inclus), EV -2.6222 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.62 %) : P(cible) 2.3 % x 27.76 % + P(rien) 97.7 % x -3.34 % ne couvrent pas P(stop) 0.0 % x 47.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 50.687 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.548, perte reelle 50.687 % (gap inclus), EV -2.6222 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.62 %) : P(cible) 2.3 % x 27.76 % + P(rien) 97.7 % x -3.34 % ne couvrent pas P(stop) 0.0 % x 50.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.62, ATR14 0.166 (6.336 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 2.325 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.317 % | 2.6117 | 88.95 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.634 % | 2.6034 | 81.36 % | 86.67 % | 89.62 % | 92.67 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.95 % | 2.5951 | 75.25 % | 82.82 % | 86.56 % | 89.9 % | 93.83 % | 96.08 % |
| 0.2 ATR | 1.267 % | 2.5868 | 69.03 % | 78.97 % | 83.4 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.584 % | 2.5785 | 63.21 % | 75.62 % | 80.24 % | 84.85 % | 90.05 % | 93.57 % |
| 0.35 ATR | 2.218 % | 2.5619 | 51.87 % | 67.52 % | 73.81 % | 80.0 % | 86.17 % | 91.56 % |
| 0.5 ATR | 3.168 % | 2.537 | 35.6 % | 54.99 % | 63.04 % | 71.19 % | 80.4 % | 88.34 % |
| 0.75 ATR | 4.752 % | 2.4955 | 19.13 % | 37.71 % | 47.53 % | 59.7 % | 71.94 % | 82.11 % |
| 1.0 ATR | 6.336 % | 2.454 | 10.06 % | 25.07 % | 36.07 % | 47.82 % | 62.59 % | 75.68 % |
| 1.25 ATR | 7.92 % | 2.4125 | 4.83 % | 17.37 % | 27.57 % | 39.9 % | 56.12 % | 70.65 % |
| 1.5 ATR | 9.504 % | 2.371 | 3.06 % | 11.45 % | 19.86 % | 31.88 % | 48.96 % | 65.63 % |
| 2.0 ATR | 12.672 % | 2.288 | 1.38 % | 5.13 % | 9.68 % | 19.8 % | 35.52 % | 53.97 % |
| 2.5 ATR | 15.84 % | 2.205 | 0.49 % | 2.86 % | 5.93 % | 12.57 % | 28.16 % | 46.33 % |
| 3.0 ATR | 19.008 % | 2.122 | 0.39 % | 1.68 % | 3.85 % | 8.91 % | 21.29 % | 39.5 % |
| 4.0 ATR | 25.344 % | 1.956 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 12.04 % | 25.53 % |
| 6.0 ATR | 38.015 % | 1.624 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.50 ATR | 1.98 ATR | 2.72 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.09 ATR | 1.47 ATR | 1.78 ATR | 1.99 ATR | 2.85 ATR | 3.82 ATR |
| **10 s.** | 0.66 ATR | 1.46 ATR | 1.65 ATR | 2.17 ATR | 2.73 ATR | 3.14 ATR | 4.59 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.26 ATR | 2.60 ATR | 3.46 ATR | 4.09 ATR | 4.93 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.752 %, prix 2.4955), p(touche) 37.71 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.336 %, prix 2.454), p(touche) 36.07 % (en stress 96.08 %)  ✅ optimum identifie (69.1 % des re-echantillons)
- **5 seance(s)** : plage utile 1.089–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.92 %, prix 2.4125), p(touche) 39.9 % (en stress 94.06 %)  ✅ optimum identifie (79.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.647–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.672 %, prix 2.288), p(touche) 35.52 % (en stress 98.02 %)  ✅ optimum identifie (76.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.597–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (85.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : €-0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 77.2 | bear 6.0 | side 16.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→65% · +2.0%→42% · +3.0%→23% · +5.0%→10% · +8.0%→2%
- Range intraday médian 3.96% (p90 6.52%) · excursion haute méd. +1.57% / basse méd. −1.88%
- Profil de vol intra : ouverture 2.571% vs midi 1.19% vs clôture 1.188% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.152)_ ; drift intra méd. -0.511% ; recovery-V 19%
- **σ réalisé intraday** 3.126% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 2.9518 (VA 2.9403–2.9711 ; dernier close 2.918)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 25% · rebond 70% · **stop −1.87%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.81 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 37% (gap-down >1% 7% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −2.18%) · haut méd +0.41% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.66%) · haut méd +0.54% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −3.17%) · haut méd +0.67% · range méd 2.04%
- Excursion ouverture 60min (n=160) : bas méd −1.06% (p90 −3.37%) · haut méd +0.84% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 81% (129/159) · gap 20% · délai 0.4min · rebond 64% (86/129) (MFE +1.48%)
   - −1.0% : fill 30min 38% · séance 67% (111/159) · gap 7% · délai 9.3min · rebond 62% (74/111) (MFE +1.42%)
   - −1.5% : fill 30min 26% · séance 55% (92/159) · gap 3% · délai 31.6min · rebond 60% (58/92) (MFE +1.25%)
   - −2.0% : fill 30min 16% · séance 46% (77/159) · gap 3% · délai 67.4min · rebond 54% (43/77) (MFE +1.17%)
   - −3.0% : fill 30min 7% · séance 25% (45/159) · gap 2% · délai 86.4min · rebond 70% (32/45) (MFE +1.52%)
   - −4.0% : fill 30min 3% · séance 10% (24/159) · gap 1% · délai 359.9min · rebond 38% (13/24) (MFE +0.64%)
   - −5.0% : fill 30min 2% · séance 4% (13/159) · gap 1% · délai 33.7min · rebond 33% (7/13) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −2.16%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −1.65%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.06% (p90 −1.83%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=811 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~9.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 74% (46/55) · rebond 63% (31/46)
      · −2.0% : fill 52% (35/55) · rebond 49% (19/35)
      · −3.0% : fill 26% (22/55) · rebond 62% (15/22)
      · −4.0% : fill 15% (15/55) · rebond 34% (8/15)
      · −5.0% : fill 10% (10/55) · rebond 33% (5/10)
   - **flat** (30 séances) :
      · −1.0% : fill 74% (23/30) · rebond 58% (14/23)
      · −2.0% : fill 50% (17/30) · rebond 49% (8/17)
      · −3.0% : fill 29% (10/30) · rebond 83% (8/10)
      · −4.0% : fill 10% (4/30) · rebond 14% (1/4)
      · −5.0% : fill 6% (2/30) · rebond 23% (1/2)
   - **gap-up** (74 séances) :
      · −1.0% : fill 61% (42/74) · rebond 64% (29/42)
      · −2.0% : fill 41% (25/74) · rebond 60% (16/25)
      · −3.0% : fill 22% (13/74) · rebond 68% (9/13)
      · −4.0% : fill 8% (5/74) · rebond 55% (4/5)
      · −5.0% : fill 0% (1/74) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 60% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **12min** → P(séance verte=clôture>ouverture) 58% si début vert vs 28% si rouge (base 43% · écart 30 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **58%** · continue >prix actuel 38% ; creux résiduel méd -1.71% (q20 -2.8%) → **SL/trailing à −2.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +2.35% → **scale +1.68% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **28%** (continue à baisser 59%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.09%** (au-delà de la MAE q10 -4.09%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +3.3%] · haut q95 +3.68% · bas q05 -3.73%
   - 60min (n=160) : retour [-3.03% .. +4.12%] · haut q95 +4.72% · bas q05 -3.81%
   - 2h (n=160) : retour [-3.2% .. +3.32%] · haut q95 +5.18% · bas q05 -4.3%
   - 4h (n=160) : retour [-3.24% .. +4.34%] · haut q95 +5.21% · bas q05 -4.31%
   - 6h (n=160) : retour [-3.57% .. +5.54%] · haut q95 +5.95% · bas q05 -4.33%
   - session (n=160) : retour [-4.49% .. +4.05%] · haut q95 +6.33% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.04 · part idiosyncratique 0.96
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 36.5  _(momentum baissier)_
- **ADX** : 24.5  _(pas de tendance nette)_
- **MACD** : hist -0.012  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 27.3%
- **ATR** : 0.17 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.262  _(distribution)_
- **Vol ratio** : 0.39  _(volume atone)_
- **Choppiness** : 43.7  _(transition)_
- **MA** : MA20 2.78 · MA50 3.05 · MA200 4.53  _(prix < MA20)_
- **Dist MA** : MA20 -5.9% · MA50 -14.1% · MA200 -42.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (754417 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
