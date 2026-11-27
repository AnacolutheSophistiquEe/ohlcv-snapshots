# ENR

**Generated** : 2026-11-27T01:08:28.793926+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €117.46  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (24 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €117.46 (+0.7% vs entrée) · entrée €116.62 · stop €113.12 · T1 €123.61 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-26 : 117.46 · ATR Wilder 7.05 (6.01 %)_
- **Swing** : plage **108.69 → 103.01** (-7.47 % a -12.31 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 103.21-104.4 (B). stop INDICATIF 95.03 (-7.74 % sous le bas ; sous le support 98.56-100.32 (- 0,5 ATR)).
- **Deep** : plage **103.01 → 91.63** (-12.31 % a -21.99 % sous la cloture, 1.61 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 98.56-100.32 (A) ; 94.0-95.27 (A) ; 89.3-92.68 (A). stop INDICATIF 82.19 (-10.3 % sous le bas ; sous le support 85.71-89.14 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.5 ATR sous le plus haut 20 s., RSI(2) 52.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 109.88-110.92 (A, -5.57 %) ; 103.21-104.4 (B, -11.11 %) ; 98.56-100.32 (A, -14.59 %) ; 94.0-95.27 (A, -18.89 %) ; 89.3-92.68 (A, -21.09 %) ; 85.71-89.14 (A, -24.11 %)
- Resistances reelles au-dessus : 122.83-124.46 (A, 4.57 %) ; 130.89-133.85 (A, 11.44 %) ; 135.1-138.15 (A, 15.02 %) ; 138.68-140.18 (A, 18.07 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.83 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.62 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1274).
   - exécution **7.283 pt plus bas** dans le cas TYPIQUE (médiane), 22.261 au p90, **28.137 au pire**
   - perte réelle **18.578 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 7.62 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0344 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.407 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2465** [0.1869 ; 0.3145] _(largeur 12.8 pt, n_eff 173.1)_
   - swing : **0.3792** [0.3292 ; 0.4312] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3666** [0.3171 ; 0.4183] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 960 séances)** : VaR **-4.65 %** | CVaR **-7.9 %** | vol 3.57 %/j
   - _fenêtre arrêtée : rupture de regime a 1020 seances en arriere (volatilite 2.02 % contre 3.41 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.17 % vs -10.3 % si l'on extrapolait par √5 _(rapport 0.89 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3645** (β de hausse 1.0728, asymétrie 1.2719) vs GDAXI — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 108.7917 sur grid_snapped (0.92 ATR, 7.38 %) — p(stop avant cible) 0.4671 [0.41 ; 0.52], R/R 4.465, perte reelle 7.999 % (gap inclus), CVaR 12.66 %, EV -1.2984 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0477 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 12.66 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.57 ATR (stop 6.172 %) — p(stop avant cible) 0.5597 [0.51 ; 0.61], R/R 5.466, perte reelle 6.533 % (gap inclus), EV -1.2586 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.560, borne haute 0.611 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.1 % x 35.71 % + P(rien) 43.9 % x 5.37 % ne couvrent pas P(stop) 56.0 % x 6.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 0.92 ATR (stop 8.268 %) — p(stop avant cible) 0.4227 [0.37 ; 0.48], R/R 3.991, perte reelle 8.947 % (gap inclus), EV -1.3797 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.17 % > budget 12.00 %
      - ⚠ support DETECTE a 0.47 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.449 ; 0.511] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 0.1 % x 35.71 % + P(rien) 57.6 % x 4.10 % ne couvrent pas P(stop) 42.3 % x 8.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.51 %) — p(stop avant cible) 0.8883 [0.85 ; 0.92], R/R 22.645, perte reelle 1.577 % (gap inclus), EV -0.3632 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 22.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.0 % x 35.71 % + P(rien) 11.1 % x 9.20 % ne couvrent pas P(stop) 88.8 % x 1.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+35.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.57 ATR (stop 5.284 %) — p(stop avant cible) 0.6263 [0.57 ; 0.68], R/R 6.491, perte reelle 5.501 % (gap inclus), EV -1.1262 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.626, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 0.1 % x 35.71 % + P(rien) 37.3 % x 6.12 % ne couvrent pas P(stop) 62.6 % x 5.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.92 ATR (stop 7.38 %) — p(stop avant cible) 0.4671 [0.41 ; 0.52], R/R 4.465, perte reelle 7.999 % (gap inclus), EV -1.2984 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 0.1 % x 35.71 % + P(rien) 53.2 % x 4.51 % ne couvrent pas P(stop) 46.7 % x 8.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 9.06 %) — p(stop avant cible) 0.3765 [0.33 ; 0.43], R/R 3.679, perte reelle 9.705 % (gap inclus), EV -1.3221 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.1 % x 35.71 % + P(rien) 62.3 % x 3.68 % ne couvrent pas P(stop) 37.6 % x 9.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 10.57 %) — p(stop avant cible) 0.2952 [0.25 ; 0.34], R/R 3.215, perte reelle 11.108 % (gap inclus), EV -1.257 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.1 % x 35.71 % + P(rien) 70.4 % x 2.82 % ne couvrent pas P(stop) 29.5 % x 11.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 12.079 %) — p(stop avant cible) 0.1978 [0.16 ; 0.24], R/R 2.83, perte reelle 12.618 % (gap inclus), EV -0.828 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 0.1 % x 35.71 % + P(rien) 80.1 % x 2.03 % ne couvrent pas P(stop) 19.8 % x 12.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 13.589 %) — p(stop avant cible) 0.1386 [0.11 ; 0.18], R/R 2.527, perte reelle 14.132 % (gap inclus), EV -0.4909 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 0.1 % x 35.71 % + P(rien) 86.0 % x 1.66 % ne couvrent pas P(stop) 13.9 % x 14.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 15.099 %) — p(stop avant cible) 0.0761 [0.05 ; 0.11], R/R 2.258, perte reelle 15.816 % (gap inclus), EV -0.1204 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.1 % x 35.71 % + P(rien) 92.3 % x 1.13 % ne couvrent pas P(stop) 7.6 % x 15.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 16.609 %) — p(stop avant cible) 0.0408 [0.02 ; 0.07], R/R 2.031, perte reelle 17.582 % (gap inclus), EV 0.1326 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.92 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 18.119 %) — p(stop avant cible) 0.0356 [0.02 ; 0.06], R/R 1.895, perte reelle 18.846 % (gap inclus), EV 0.1378 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.32 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.139 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 1.452, perte reelle 24.586 % (gap inclus), EV 0.2602 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.90 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 24.159 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 1.316, perte reelle 27.143 % (gap inclus), EV 0.2994 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.62 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 27.179 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.229, perte reelle 29.05 % (gap inclus), EV 0.3206 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.39 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.199 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 1.148, perte reelle 31.095 % (gap inclus), EV 0.3268 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.31 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.219 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.05, perte reelle 34.005 % (gap inclus), EV 0.337 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.07 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.238 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.982, perte reelle 36.362 % (gap inclus), EV 0.3378 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.09 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.258 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.91, perte reelle 39.258 % (gap inclus), EV 0.334 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 42.278 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.845, perte reelle 42.278 % (gap inclus), EV 0.3408 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.02 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 45.298 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.788, perte reelle 45.298 % (gap inclus), EV 0.3428 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.93 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 48.318 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.739, perte reelle 48.318 % (gap inclus), EV 0.3446 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.93 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 117.46, ATR14 7.0943 (6.04 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.369 ATR = 2.229 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.302 % | 117.1053 | 91.62 % | 94.37 % | 95.95 % | 96.53 % | 97.61 % | 98.29 % |
| 0.1 ATR | 0.604 % | 116.7506 | 83.93 % | 88.55 % | 91.01 % | 93.07 % | 95.12 % | 96.18 % |
| 0.15 ATR | 0.906 % | 116.3959 | 76.53 % | 82.72 % | 86.36 % | 89.11 % | 91.84 % | 93.97 % |
| 0.2 ATR | 1.208 % | 116.0411 | 70.51 % | 79.37 % | 83.3 % | 87.03 % | 90.05 % | 92.66 % |
| 0.25 ATR | 1.51 % | 115.6864 | 63.61 % | 74.93 % | 79.55 % | 83.76 % | 88.06 % | 91.36 % |
| 0.35 ATR | 2.114 % | 114.977 | 51.97 % | 65.35 % | 70.85 % | 76.53 % | 82.99 % | 87.64 % |
| 0.5 ATR | 3.02 % | 113.9129 | 36.59 % | 52.22 % | 60.18 % | 67.52 % | 75.72 % | 81.91 % |
| 0.75 ATR | 4.53 % | 112.1393 | 19.82 % | 36.03 % | 45.75 % | 55.35 % | 66.77 % | 75.28 % |
| 1.0 ATR | 6.04 % | 110.3657 | 11.34 % | 26.26 % | 35.38 % | 45.64 % | 58.91 % | 68.04 % |
| 1.25 ATR | 7.55 % | 108.5921 | 6.31 % | 17.67 % | 25.79 % | 36.83 % | 50.35 % | 60.6 % |
| 1.5 ATR | 9.06 % | 106.8186 | 2.96 % | 11.55 % | 18.58 % | 29.01 % | 43.08 % | 54.27 % |
| 2.0 ATR | 12.079 % | 103.2714 | 0.79 % | 4.44 % | 9.19 % | 17.43 % | 30.05 % | 43.02 % |
| 2.5 ATR | 15.099 % | 99.7243 | 0.3 % | 2.07 % | 4.25 % | 10.3 % | 20.8 % | 33.07 % |
| 3.0 ATR | 18.119 % | 96.1771 | 0.1 % | 0.89 % | 2.08 % | 5.35 % | 13.43 % | 25.13 % |
| 4.0 ATR | 24.159 % | 89.0829 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 7.06 % | 14.17 % |
| 6.0 ATR | 36.238 % | 74.8943 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.93 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.07 ATR | 1.35 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.83 ATR | 1.04 ATR | 1.18 ATR | 1.61 ATR | 1.96 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.77 ATR | 1.06 ATR | 1.28 ATR | 1.45 ATR | 1.96 ATR | 2.42 ATR |
| **5 s.** | 0.38 ATR | 0.89 ATR | 1.02 ATR | 1.37 ATR | 1.67 ATR | 1.89 ATR | 2.53 ATR | 3.12 ATR |
| **10 s.** | 0.52 ATR | 1.26 ATR | 1.43 ATR | 1.89 ATR | 2.27 ATR | 2.55 ATR | 3.54 ATR | 4.85 ATR |
| **20 s.** | 0.76 ATR | 1.69 ATR | 1.91 ATR | 2.50 ATR | 3.01 ATR | 3.47 ATR | 5.01 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.418 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.53 %, prix 112.1391), p(touche) 36.03 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.768–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.04 %, prix 110.3654), p(touche) 35.38 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (86.1 % des re-echantillons)
- **5 seance(s)** : plage utile 1.018–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.55 %, prix 108.5918), p(touche) 36.83 % (en stress 96.04 %)  ✅ optimum identifie (90.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.434–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.06 %, prix 106.8181), p(touche) 43.08 % (en stress 99.01 %)  ✅ optimum identifie (92.6 % des re-echantillons)
- **20 seance(s)** : plage utile 1.912–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.079 %, prix 103.272), p(touche) 43.02 % (en stress 99.0 %)  ✅ optimum identifie (88.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 78.5 | bear 16.4 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.713% → cible +5.996% / stop −2.998%, p_fill 79%, n_eff≈83.7) : P(cible|rempli) **2%** · **EV/risk -0.179** (×p_fill ; si rempli -0.68% du capital)
  - **swing** (entrée dip −1.58% → cible +6.923% / stop −6.137%, p_fill 72%, n_eff≈84.4) : P(cible|rempli) **15%** · **EV/risk -0.160** (×p_fill ; si rempli -1.36% du capital)
  - **deep** (entrée dip −2.441% → cible +18.403% / stop −9.286%, p_fill 73%, n_eff≈83.9) : P(cible|rempli) **2%** · **EV/risk -0.194** (×p_fill ; si rempli -2.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→34% · +3.0%→15% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.62% (p90 6.06%) · excursion haute méd. +1.37% / basse méd. −1.89%
- Profil de vol intra : ouverture 1.961% vs midi 0.824% vs clôture 1.048% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.864% ; recovery-V 25%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 83% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 121.5065 (VA 120.2185–123.5995 ; dernier close 118.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 57% · **stop −4.86%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.22 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.69%) · haut méd +0.49% · range méd 1.14%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.05%) · haut méd +0.58% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.19%) · haut méd +0.62% · range méd 1.69%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.35%) · haut méd +0.68% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 70% (115/159) · gap 30% · délai 0.2min · rebond 48% (59/115) (MFE +0.88%)
   - −1.0% : fill 30min 40% · séance 66% (107/159) · gap 20% · délai 8.6min · rebond 51% (59/107) (MFE +1.04%)
   - −1.5% : fill 30min 29% · séance 53% (88/159) · gap 13% · délai 12.6min · rebond 55% (48/88) (MFE +1.28%)
   - −2.0% : fill 30min 23% · séance 44% (73/159) · gap 9% · délai 20.7min · rebond 50% (41/73) (MFE +1.0%)
   - −3.0% : fill 30min 10% · séance 29% (48/159) · gap 3% · délai 251.6min · rebond 40% (24/48) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 200.1min · rebond 57% (20/32) (MFE +1.05%)
   - −5.0% : fill 30min 4% · séance 13% (24/159) · gap 0% · délai 397.7min · rebond 38% (11/24) (MFE +0.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.66%) → stop au-delà de −0.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=526 jambes) : jambe baissière méd −1.04% (p90 −2.31%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 41% (26/53)
      · −2.0% : fill 84% (41/54) · rebond 49% (20/41)
      · −3.0% : fill 59% (30/54) · rebond 40% (14/30)
      · −4.0% : fill 39% (22/54) · rebond 75% (16/22)
      · −5.0% : fill 30% (18/54) · rebond 47% (10/18)
   - **flat** (18 séances) :
      · −1.0% : fill 59% (13/18) · rebond 64% (9/13)
      · −2.0% : fill 33% (8/18) · rebond 68% (6/8)
      · −3.0% : fill 20% (5/18) · rebond 48% (3/5)
      · −4.0% : fill 6% (3/18) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 46% (41/87) · rebond 61% (24/41)
      · −2.0% : fill 23% (24/87) · rebond 46% (15/24)
      · −3.0% : fill 13% (13/87) · rebond 36% (7/13)
      · −4.0% : fill 9% (7/87) · rebond 11% (2/7)
      · −5.0% : fill 5% (4/87) · rebond 12% (1/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 61% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.18% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.1% → **scale +1.08% / runner +2.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.96%** (au-delà de la MAE q10 -4.96%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +1.62%] · haut q95 +2.08% · bas q05 -2.65%
   - 60min (n=160) : retour [-2.5% .. +1.42%] · haut q95 +2.41% · bas q05 -3.07%
   - 2h (n=160) : retour [-2.53% .. +2.22%] · haut q95 +2.56% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.61% .. +2.42%] · haut q95 +3.02% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.22% .. +3.06%] · haut q95 +3.68% · bas q05 -4.31%
   - session (n=160) : retour [-5.78% .. +2.83%] · haut q95 +4.66% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.58 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.5  _(neutre)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -0.644  _(bearish_recent)_
- **BB** : %B 0.24 · largeur 20.3%
- **ATR** : 7.09 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.251  _(distribution)_
- **Vol ratio** : 0.25  _(volume atone)_
- **Choppiness** : 54.3  _(transition)_
- **MA** : MA20 123.93 · MA50 132.61 · MA200 151.94  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -11.4% · MA200 -22.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (687863 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
