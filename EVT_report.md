# EVT

**Generated** : 2026-10-20T21:42:10.880922+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.72  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (12 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €2.72 (+0.4% vs entrée) · entrée €2.71 · stop €2.50 · T1 €2.79 · R/R 0.38  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 268 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-20 : 2.72 · ATR Wilder 0.1515 (5.57 %)_
- **Swing** : plage **2.52 → 2.37** (-7.44 % a -12.86 % sous la cloture, 0.97 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.22 (-6.39 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **2.37 → 1.74** (-12.86 % a -35.97 % sous la cloture, 4.15 ATR) — touchee 48 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 1.59 (-8.69 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.76 ATR sous le plus haut 20 s., RSI(2) 89.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Resistances reelles au-dessus : 3.1-3.14 (A, 13.81 %) ; 3.18-3.24 (B, 16.68 %) ; 3.37-3.41 (A, 23.95 %) ; 3.88-3.88 (C, 42.54 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.58 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **5.278 pt plus bas** dans le cas TYPIQUE (médiane), 19.352 au p90, **25.833 au pire**
   - perte réelle **14.861 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 6.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0455 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0256** [0.0092 ; 0.0575] _(largeur 4.8 pt, n_eff 173.1)_
   - swing : **0.3793** [0.3293 ; 0.4313] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.382** [0.3319 ; 0.434] _(largeur 10.2 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.8 %** | CVaR **-8.97 %** | vol 3.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 6.16 % contre 3.63 % aujourd'hui, rapport 1.70)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1172** (β de hausse 0.9328, asymétrie 1.1977) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.6006 sur atr_grid (0.75 ATR, 4.46 %) — p(stop avant cible) 0.6684 [0.62 ; 0.72], R/R 8.806, perte reelle 4.969 % (gap inclus), CVaR 10.715 %, EV -0.9632 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.298 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.668, borne haute 0.717 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.07 ATR (stop 3.564 %) — p(stop avant cible) 0.7197 [0.67 ; 0.77], R/R 10.829, perte reelle 4.041 % (gap inclus), EV -0.8133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.720, borne haute 0.765 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.07 ATR du spot — compartiment <1, mesure a 48.2 % de casse (IC clusterise [0.448 ; 0.516] sur 1122 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.0 % x 43.76 % + P(rien) 28.0 % x 7.42 % ne couvrent pas P(stop) 72.0 % x 4.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 8.92 %) — p(stop avant cible) 0.3826 [0.33 ; 0.43], R/R 4.194, perte reelle 10.435 % (gap inclus), EV -1.84 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 0.1 % x 43.76 % + P(rien) 61.6 % x 3.41 % ne couvrent pas P(stop) 38.3 % x 10.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 1.95 ATR (stop 14.732 %) — p(stop avant cible) 0.1791 [0.14 ; 0.22], R/R 2.625, perte reelle 16.668 % (gap inclus), EV -2.3711 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.37 %) : P(cible) 0.1 % x 43.76 % + P(rien) 82.0 % x 0.69 % ne couvrent pas P(stop) 17.9 % x 16.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.07 ATR (stop 2.225 %) — p(stop avant cible) 0.8382 [0.80 ; 0.87], R/R 16.857, perte reelle 2.596 % (gap inclus), EV -0.7327 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 16.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.838, borne haute 0.874 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 0.0 % x 43.76 % + P(rien) 16.2 % x 8.83 % ne couvrent pas P(stop) 83.8 % x 2.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 4.46 %) — p(stop avant cible) 0.6684 [0.62 ; 0.72], R/R 8.806, perte reelle 4.969 % (gap inclus), EV -0.9632 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.668, borne haute 0.717 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 0.1 % x 43.76 % + P(rien) 33.1 % x 7.03 % ne couvrent pas P(stop) 66.8 % x 4.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 5.946 %) — p(stop avant cible) 0.5569 [0.50 ; 0.61], R/R 6.413, perte reelle 6.823 % (gap inclus), EV -1.193 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.557, borne haute 0.609 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.1 % x 43.76 % + P(rien) 44.2 % x 5.79 % ne couvrent pas P(stop) 55.7 % x 6.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.433 %) — p(stop avant cible) 0.454 [0.40 ; 0.51], R/R 4.928, perte reelle 8.88 % (gap inclus), EV -1.6055 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.61 %) : P(cible) 0.1 % x 43.76 % + P(rien) 54.5 % x 4.36 % ne couvrent pas P(stop) 45.4 % x 8.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 1.95 ATR (stop 13.393 %) — p(stop avant cible) 0.2091 [0.17 ; 0.25], R/R 2.878, perte reelle 15.206 % (gap inclus), EV -2.2867 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.29 %) : P(cible) 0.1 % x 43.76 % + P(rien) 79.0 % x 1.07 % ne couvrent pas P(stop) 20.9 % x 15.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 16.352 %) — p(stop avant cible) 0.1429 [0.11 ; 0.18], R/R 2.387, perte reelle 18.332 % (gap inclus), EV -2.3596 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.36 %) : P(cible) 0.1 % x 43.76 % + P(rien) 85.6 % x 0.25 % ne couvrent pas P(stop) 14.3 % x 18.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 17.839 %) — p(stop avant cible) 0.1229 [0.09 ; 0.16], R/R 2.215, perte reelle 19.758 % (gap inclus), EV -2.3562 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.36 %) : P(cible) 0.1 % x 43.76 % + P(rien) 87.6 % x 0.03 % ne couvrent pas P(stop) 12.3 % x 19.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 20.812 %) — p(stop avant cible) 0.0959 [0.07 ; 0.13], R/R 1.986, perte reelle 22.039 % (gap inclus), EV -2.4137 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.41 %) : P(cible) 0.1 % x 43.76 % + P(rien) 90.3 % x -0.39 % ne couvrent pas P(stop) 9.6 % x 22.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 23.785 %) — p(stop avant cible) 0.077 [0.05 ; 0.11], R/R 1.793, perte reelle 24.411 % (gap inclus), EV -2.499 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.50 %) : P(cible) 0.1 % x 43.76 % + P(rien) 92.2 % x -0.72 % ne couvrent pas P(stop) 7.7 % x 24.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 26.758 %) — p(stop avant cible) 0.0624 [0.04 ; 0.09], R/R 1.62, perte reelle 27.017 % (gap inclus), EV -2.6132 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.1 % x 43.76 % + P(rien) 93.7 % x -1.04 % ne couvrent pas P(stop) 6.2 % x 27.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 29.731 %) — p(stop avant cible) 0.0393 [0.02 ; 0.06], R/R 1.462, perte reelle 29.941 % (gap inclus), EV -2.679 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 0.1 % x 43.76 % + P(rien) 96.0 % x -1.62 % ne couvrent pas P(stop) 3.9 % x 29.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 32.704 %) — p(stop avant cible) 0.0393 [0.02 ; 0.06], R/R 1.335, perte reelle 32.787 % (gap inclus), EV -2.7908 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.79 %) : P(cible) 0.1 % x 43.76 % + P(rien) 96.0 % x -1.62 % ne couvrent pas P(stop) 3.9 % x 32.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 35.678 %) — p(stop avant cible) 0.0304 [0.02 ; 0.05], R/R 1.227, perte reelle 35.678 % (gap inclus), EV -2.8471 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.85 %) : P(cible) 0.1 % x 43.76 % + P(rien) 96.9 % x -1.87 % ne couvrent pas P(stop) 3.0 % x 35.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 38.651 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 1.132, perte reelle 38.651 % (gap inclus), EV -2.7295 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.73 %) : P(cible) 0.1 % x 43.76 % + P(rien) 99.3 % x -2.58 % ne couvrent pas P(stop) 0.6 % x 38.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 41.624 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 1.051, perte reelle 41.624 % (gap inclus), EV -2.705 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.70 %) : P(cible) 0.1 % x 43.76 % + P(rien) 99.8 % x -2.73 % ne couvrent pas P(stop) 0.1 % x 41.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 44.597 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.981, perte reelle 44.597 % (gap inclus), EV -2.7008 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.70 %) : P(cible) 0.1 % x 43.76 % + P(rien) 99.9 % x -2.75 % ne couvrent pas P(stop) 0.0 % x 44.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 47.57 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.92, perte reelle 47.57 % (gap inclus), EV -2.7008 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.70 %) : P(cible) 0.1 % x 43.76 % + P(rien) 99.9 % x -2.75 % ne couvrent pas P(stop) 0.0 % x 47.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.722, ATR14 0.1619 (5.946 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 2.182 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.297 % | 2.7139 | 88.95 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.595 % | 2.7058 | 81.36 % | 86.67 % | 89.62 % | 92.67 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.892 % | 2.6977 | 75.35 % | 82.92 % | 86.66 % | 90.0 % | 93.93 % | 96.08 % |
| 0.2 ATR | 1.189 % | 2.6896 | 69.13 % | 79.07 % | 83.5 % | 87.33 % | 92.04 % | 94.77 % |
| 0.25 ATR | 1.487 % | 2.6815 | 63.21 % | 75.72 % | 80.34 % | 84.85 % | 90.15 % | 93.57 % |
| 0.35 ATR | 2.081 % | 2.6653 | 51.87 % | 67.52 % | 73.91 % | 80.0 % | 86.27 % | 91.56 % |
| 0.5 ATR | 2.973 % | 2.6411 | 35.6 % | 54.99 % | 63.04 % | 71.19 % | 80.5 % | 88.34 % |
| 0.75 ATR | 4.46 % | 2.6006 | 19.13 % | 37.71 % | 47.53 % | 59.7 % | 72.04 % | 82.11 % |
| 1.0 ATR | 5.946 % | 2.5601 | 10.06 % | 25.07 % | 36.07 % | 47.82 % | 62.69 % | 75.68 % |
| 1.25 ATR | 7.433 % | 2.5197 | 4.83 % | 17.37 % | 27.57 % | 39.9 % | 56.22 % | 70.65 % |
| 1.5 ATR | 8.919 % | 2.4792 | 3.06 % | 11.45 % | 19.86 % | 31.88 % | 49.05 % | 65.63 % |
| 2.0 ATR | 11.893 % | 2.3983 | 1.38 % | 5.13 % | 9.68 % | 19.8 % | 35.62 % | 53.97 % |
| 2.5 ATR | 14.866 % | 2.3174 | 0.49 % | 2.86 % | 5.93 % | 12.57 % | 28.26 % | 46.43 % |
| 3.0 ATR | 17.839 % | 2.2364 | 0.39 % | 1.68 % | 3.85 % | 8.91 % | 21.39 % | 39.5 % |
| 4.0 ATR | 23.785 % | 2.0746 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 12.14 % | 25.53 % |
| 6.0 ATR | 35.678 % | 1.7509 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.50 ATR | 1.98 ATR | 2.72 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.09 ATR | 1.47 ATR | 1.78 ATR | 1.99 ATR | 2.85 ATR | 3.82 ATR |
| **10 s.** | 0.66 ATR | 1.47 ATR | 1.65 ATR | 2.18 ATR | 2.74 ATR | 3.15 ATR | 4.61 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.26 ATR | 2.60 ATR | 3.46 ATR | 4.09 ATR | 4.93 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (61.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.46 %, prix 2.6006), p(touche) 37.71 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (68.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.946 %, prix 2.5601), p(touche) 36.07 % (en stress 96.08 %)  ✅ optimum identifie (69.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.089–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.433 %, prix 2.5197), p(touche) 39.9 % (en stress 94.06 %)  ✅ optimum identifie (78.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.651–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.893 %, prix 2.3983), p(touche) 35.62 % (en stress 98.02 %)  ✅ optimum identifie (76.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.603–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (17.839 %, prix 2.2364), p(touche) 39.5 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 76.6 | bear 6.0 | side 17.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.368% → cible +2.983% / stop −8.001%, p_fill 84%, n_eff≈92.1) : P(cible|rempli) **14%** · **EV/risk -0.083** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −0.632% → cible +6.692% / stop −5.986%, p_fill 88%, n_eff≈101.0) : P(cible|rempli) **26%** · **EV/risk -0.172** (×p_fill ; si rempli -1.18% du capital)
  - **deep** (entrée dip −0.87% → cible +15.177% / stop −8.999%, p_fill 85%, n_eff≈94.3) : P(cible|rempli) **1%** · **EV/risk -0.375** (×p_fill ; si rempli -3.96% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.07 · part idiosyncratique 0.93
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 34.0  _(momentum baissier)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist 0.002  _(bullish_recent)_
- **BB** : %B 0.42 · largeur 27.3%
- **ATR** : 0.16 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.208  _(distribution)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 42.7  _(transition)_
- **MA** : MA20 2.78 · MA50 3.03 · MA200 4.51  _(prix < MA20)_
- **Dist MA** : MA20 -2.1% · MA50 -10.2% · MA200 -39.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (784322 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
