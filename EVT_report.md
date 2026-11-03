# EVT

**Generated** : 2026-11-03T21:43:35.470190+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.86  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)  
> ↳ spot €2.86 (+1.4% vs entrée) · entrée €2.82 · stop €2.71 · T1 €2.88 · R/R 0.55  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-03 : 2.86 · ATR Wilder 0.1304 (4.56 %)_
- **Swing** : plage **2.68 → 2.56** (-6.14 % a -10.66 % sous la cloture, 0.99 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.34 (-8.39 % sous le bas ; sous le support 2.41-2.41 (- 0,5 ATR)).
- **Deep** : plage **2.56 → 2.02** (-10.66 % a -29.46 % sous la cloture, 4.13 ATR) — touchee 49 % → 15 % du temps en 20 seances ; supports reels dans la plage : 2.41-2.41 (C). stop INDICATIF 1.89 (-6.46 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (1.01 ATR sous le plus haut 20 s., RSI(2) 61.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 2.71-2.77 (C, -3.29 %) ; 2.41-2.41 (C, -15.87 %)
- Resistances reelles au-dessus : 3.1-3.14 (A, 8.32 %) ; 3.18-3.24 (B, 11.05 %) ; 3.37-3.41 (A, 17.97 %) ; 3.88-3.88 (C, 35.66 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.73 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **5.094 pt plus bas** dans le cas TYPIQUE (médiane), 19.362 au p90, **23.683 au pire**
   - perte réelle **18.001 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 8.73 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0364 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1082** [0.0685 ; 0.1609] _(largeur 9.2 pt, n_eff 173.1)_
   - swing : **0.3605** [0.3112 ; 0.4121] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.4887** [0.4363 ; 0.5413] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.5 pt), deep (25.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.8 %** | CVaR **-8.97 %** | vol 3.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 6.10 % contre 3.51 % aujourd'hui, rapport 1.74)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1169** (β de hausse 0.9252, asymétrie 1.2072) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.6747 sur grid_snapped (1.28 ATR, 6.478 %) — p(stop avant cible) 0.5218 [0.47 ; 0.57], R/R 5.062, perte reelle 7.366 % (gap inclus), CVaR 15.283 %, EV -1.0091 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2961 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 15.28 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.28 ATR (stop 7.094 %) — p(stop avant cible) 0.473 [0.42 ; 0.53], R/R 4.496, perte reelle 8.294 % (gap inclus), EV -1.1853 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.3 % x 37.29 % + P(rien) 52.4 % x 5.00 % ne couvrent pas P(stop) 47.3 % x 8.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.86 ATR (stop 17.724 %) — p(stop avant cible) 0.1161 [0.09 ; 0.15], R/R 1.894, perte reelle 19.684 % (gap inclus), EV -1.8259 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.3 % x 37.29 % + P(rien) 88.1 % x 0.39 % ne couvrent pas P(stop) 11.6 % x 19.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.028 %) — p(stop avant cible) 0.9126 [0.88 ; 0.94], R/R 31.776, perte reelle 1.173 % (gap inclus), EV -0.2253 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 31.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.913, borne haute 0.939 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.1 % x 37.29 % + P(rien) 8.6 % x 9.36 % ne couvrent pas P(stop) 91.3 % x 1.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.055 %) — p(stop avant cible) 0.834 [0.79 ; 0.87], R/R 15.404, perte reelle 2.421 % (gap inclus), EV -0.4383 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 15.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.834, borne haute 0.870 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 0.2 % x 37.29 % + P(rien) 16.4 % x 9.25 % ne couvrent pas P(stop) 83.4 % x 2.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 3.083 %) — p(stop avant cible) 0.7414 [0.69 ; 0.79], R/R 10.778, perte reelle 3.46 % (gap inclus), EV -0.4503 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 10.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.741, borne haute 0.785 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.2 % x 37.29 % + P(rien) 25.7 % x 7.96 % ne couvrent pas P(stop) 74.1 % x 3.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 4.111 %) — p(stop avant cible) 0.6725 [0.62 ; 0.72], R/R 8.126, perte reelle 4.589 % (gap inclus), EV -0.4928 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.672, borne haute 0.720 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 0.2 % x 37.29 % + P(rien) 32.6 % x 7.75 % ne couvrent pas P(stop) 67.2 % x 4.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 1.28 ATR (stop 6.478 %) — p(stop avant cible) 0.5218 [0.47 ; 0.57], R/R 5.062, perte reelle 7.366 % (gap inclus), EV -1.0091 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 0.3 % x 37.29 % + P(rien) 47.5 % x 5.71 % ne couvrent pas P(stop) 52.2 % x 7.37 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 8.222 %) — p(stop avant cible) 0.4173 [0.37 ; 0.47], R/R 3.882, perte reelle 9.605 % (gap inclus), EV -1.4379 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.44 %) : P(cible) 0.3 % x 37.29 % + P(rien) 58.0 % x 4.23 % ne couvrent pas P(stop) 41.7 % x 9.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 9.25 %) — p(stop avant cible) 0.3674 [0.32 ; 0.42], R/R 3.486, perte reelle 10.695 % (gap inclus), EV -1.5513 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.55 %) : P(cible) 0.3 % x 37.29 % + P(rien) 62.9 % x 3.59 % ne couvrent pas P(stop) 36.7 % x 10.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 10.277 %) — p(stop avant cible) 0.3401 [0.29 ; 0.39], R/R 3.193, perte reelle 11.679 % (gap inclus), EV -1.7306 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 0.3 % x 37.29 % + P(rien) 65.7 % x 3.23 % ne couvrent pas P(stop) 34.0 % x 11.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 11.305 %) — p(stop avant cible) 0.31 [0.26 ; 0.36], R/R 2.934, perte reelle 12.707 % (gap inclus), EV -1.8888 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.89 %) : P(cible) 0.3 % x 37.29 % + P(rien) 68.7 % x 2.81 % ne couvrent pas P(stop) 31.0 % x 12.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 12.333 %) — p(stop avant cible) 0.2658 [0.22 ; 0.31], R/R 2.695, perte reelle 13.835 % (gap inclus), EV -1.9865 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 0.3 % x 37.29 % + P(rien) 73.1 % x 2.15 % ne couvrent pas P(stop) 26.6 % x 13.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 14.388 %) — p(stop avant cible) 0.188 [0.15 ; 0.23], R/R 2.309, perte reelle 16.148 % (gap inclus), EV -1.928 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 0.3 % x 37.29 % + P(rien) 80.9 % x 1.22 % ne couvrent pas P(stop) 18.8 % x 16.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 3.86 ATR (stop 17.107 %) — p(stop avant cible) 0.1356 [0.10 ; 0.17], R/R 1.971, perte reelle 18.922 % (gap inclus), EV -1.9314 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 0.3 % x 37.29 % + P(rien) 86.1 % x 0.60 % ne couvrent pas P(stop) 13.6 % x 18.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 18.499 %) — p(stop avant cible) 0.1076 [0.08 ; 0.14], R/R 1.835, perte reelle 20.323 % (gap inclus), EV -1.8319 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.3 % x 37.29 % + P(rien) 88.9 % x 0.26 % ne couvrent pas P(stop) 10.8 % x 20.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 20.554 %) — p(stop avant cible) 0.0906 [0.06 ; 0.12], R/R 1.704, perte reelle 21.889 % (gap inclus), EV -1.8746 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.87 %) : P(cible) 0.3 % x 37.29 % + P(rien) 90.6 % x -0.01 % ne couvrent pas P(stop) 9.1 % x 21.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 22.61 %) — p(stop avant cible) 0.0767 [0.05 ; 0.11], R/R 1.592, perte reelle 23.421 % (gap inclus), EV -1.9154 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 0.3 % x 37.29 % + P(rien) 92.0 % x -0.26 % ne couvrent pas P(stop) 7.7 % x 23.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 24.665 %) — p(stop avant cible) 0.067 [0.04 ; 0.10], R/R 1.488, perte reelle 25.063 % (gap inclus), EV -1.9801 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.98 %) : P(cible) 0.3 % x 37.29 % + P(rien) 93.0 % x -0.45 % ne couvrent pas P(stop) 6.7 % x 25.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 26.721 %) — p(stop avant cible) 0.0589 [0.04 ; 0.09], R/R 1.382, perte reelle 26.982 % (gap inclus), EV -2.0745 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 0.3 % x 37.29 % + P(rien) 93.8 % x -0.64 % ne couvrent pas P(stop) 5.9 % x 26.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 28.776 %) — p(stop avant cible) 0.0454 [0.03 ; 0.07], R/R 1.286, perte reelle 28.985 % (gap inclus), EV -2.1365 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 0.3 % x 37.29 % + P(rien) 95.1 % x -0.99 % ne couvrent pas P(stop) 4.5 % x 28.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 30.832 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 1.203, perte reelle 30.99 % (gap inclus), EV -2.1776 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 0.3 % x 37.29 % + P(rien) 96.0 % x -1.20 % ne couvrent pas P(stop) 3.7 % x 30.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 32.887 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 1.131, perte reelle 32.963 % (gap inclus), EV -2.2508 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 0.3 % x 37.29 % + P(rien) 96.0 % x -1.20 % ne couvrent pas P(stop) 3.7 % x 32.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.86, ATR14 0.1176 (4.111 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.368 ATR = 1.513 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.206 % | 2.8541 | 88.86 % | 91.61 % | 93.48 % | 95.45 % | 97.21 % | 98.29 % |
| 0.1 ATR | 0.411 % | 2.8482 | 81.46 % | 86.77 % | 89.62 % | 92.48 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.617 % | 2.8424 | 75.44 % | 83.02 % | 86.66 % | 89.8 % | 93.93 % | 96.08 % |
| 0.2 ATR | 0.822 % | 2.8365 | 69.23 % | 79.27 % | 83.6 % | 87.23 % | 92.04 % | 94.77 % |
| 0.25 ATR | 1.028 % | 2.8306 | 63.31 % | 75.81 % | 80.34 % | 84.65 % | 89.95 % | 93.57 % |
| 0.35 ATR | 1.439 % | 2.8188 | 51.97 % | 67.52 % | 73.72 % | 79.5 % | 85.97 % | 91.56 % |
| 0.5 ATR | 2.055 % | 2.8012 | 35.6 % | 54.99 % | 62.75 % | 70.59 % | 80.1 % | 88.34 % |
| 0.75 ATR | 3.083 % | 2.7718 | 19.03 % | 37.81 % | 47.33 % | 59.11 % | 71.54 % | 82.11 % |
| 1.0 ATR | 4.111 % | 2.7424 | 9.96 % | 25.07 % | 35.77 % | 47.23 % | 62.29 % | 75.68 % |
| 1.25 ATR | 5.139 % | 2.713 | 4.73 % | 17.18 % | 27.27 % | 39.41 % | 55.82 % | 70.65 % |
| 1.5 ATR | 6.166 % | 2.6836 | 2.96 % | 11.25 % | 19.47 % | 31.39 % | 48.66 % | 65.63 % |
| 2.0 ATR | 8.222 % | 2.6249 | 1.38 % | 5.03 % | 9.49 % | 19.41 % | 35.22 % | 53.97 % |
| 2.5 ATR | 10.277 % | 2.5661 | 0.49 % | 2.86 % | 5.83 % | 12.38 % | 27.96 % | 46.53 % |
| 3.0 ATR | 12.333 % | 2.5073 | 0.39 % | 1.68 % | 3.85 % | 8.71 % | 21.09 % | 39.6 % |
| 4.0 ATR | 16.444 % | 2.3897 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 12.04 % | 25.13 % |
| 6.0 ATR | 24.665 % | 2.1546 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.73 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.01 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.08 ATR | 1.32 ATR | 1.48 ATR | 1.97 ATR | 2.71 ATR |
| **5 s.** | 0.43 ATR | 0.94 ATR | 1.07 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.82 ATR | 3.81 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.64 ATR | 2.15 ATR | 2.71 ATR | 3.12 ATR | 4.59 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.27 ATR | 2.61 ATR | 3.46 ATR | 4.02 ATR | 4.89 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.414–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (62.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.083 %, prix 2.7718), p(touche) 37.81 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (71.8 % des re-echantillons)
- **3 seance(s)** : plage utile 0.8–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.111 %, prix 2.7424), p(touche) 35.77 % (en stress 96.08 %)  ✅ optimum identifie (72.9 % des re-echantillons)
- **5 seance(s)** : plage utile 1.071–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.139 %, prix 2.713), p(touche) 39.41 % (en stress 94.06 %)  ✅ optimum identifie (77.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.636–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.222 %, prix 2.6249), p(touche) 35.22 % (en stress 98.02 %)  ✅ optimum identifie (71.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.61–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (12.333 %, prix 2.5073), p(touche) 39.6 % (en stress 98.0 %)  ✅ optimum identifie (82.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : €-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 14 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.9 | bear 5.0 | side 84.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 157.0 (= 55 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.313% → cible +2.083% / stop −4.0%, p_fill 70%, n_eff≈71.9) : P(cible|rempli) **39%** · **EV/risk +0.006** (×p_fill ; si rempli +0.03% du capital)
  - **swing** (entrée dip −2.88% → cible +12.047% / stop −6.023%, p_fill 51%, n_eff≈56.7) : P(cible|rempli) **7%** · **EV/risk -0.136** (×p_fill ; si rempli -1.61% du capital)
  - **deep** (entrée dip −4.453% → cible +13.892% / stop −6.946%, p_fill 49%, n_eff≈52.9) : P(cible|rempli) **4%** · **EV/risk -0.272** (×p_fill ; si rempli -3.88% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.12 · part idiosyncratique 0.88
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.9  _(momentum haussier)_
- **ADX** : 14.4  _(pas de tendance nette)_
- **MACD** : hist 0.028  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 23.0%
- **ATR** : 0.12 (7.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.158  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 45.5  _(transition)_
- **MA** : MA20 2.75 · MA50 2.92 · MA200 4.34  _(prix > MA20)_
- **Dist MA** : MA20 +3.9% · MA50 -1.9% · MA200 -34.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (784209 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
