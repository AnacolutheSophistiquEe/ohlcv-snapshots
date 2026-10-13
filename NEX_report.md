# NEX

**Generated** : 2026-10-13T21:46:21.487035+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €131.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €131.10 (+0.5% vs entrée) · entrée €130.40 · stop €128.45 · T1 €132.43 · R/R 1.04  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-13 : 131.1 · ATR Wilder 4.15 (3.16 %)_
- **Swing** : plage **125.92 → 122.57** (-3.95 % a -6.51 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 123.8-125.7 (A). stop INDICATIF 118.42 (-3.38 % sous le bas ; sous le support 120.5-122.56 (- 0,5 ATR)).
- **Deep** : plage **122.57 → 113.3** (-6.51 % a -13.58 % sous la cloture, 2.24 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 120.5-122.56 (B) ; 117.84-120.59 (B) ; 115.59-117.16 (B) ; 112.93-114.01 (B). stop INDICATIF 106.93 (-5.62 % sous le bas ; sous le support 109.01-110.28 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.18 ATR sous le plus haut 20 s., RSI(2) 59.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 126.88-128.6 (B, -1.9 %) ; 123.8-125.7 (A, -4.12 %) ; 120.5-122.56 (B, -6.52 %) ; 117.84-120.59 (B, -8.01 %) ; 115.59-117.16 (B, -10.64 %) ; 112.93-114.01 (B, -13.03 %)
- Resistances reelles au-dessus : 134.34-136.3 (A, 2.47 %) ; 137.58-139.35 (A, 4.94 %) ; 140.66-142.7 (A, 7.29 %) ; 143.2-145.2 (A, 9.23 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.26 %)** : le gap seul le franchit 0.781 % des séances (10 fois sur 1280).
   - exécution **2.969 pt plus bas** dans le cas TYPIQUE (médiane), 4.217 au p90, **5.336 au pire**
   - perte réelle **6.706 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 4.26 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0191 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3899** [0.3196 ; 0.4639] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.465** [0.4129 ; 0.5177] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4392** [0.3876 ; 0.4918] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.53 %** | CVaR **-5.29 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.88 % si l'on extrapolait par √5 _(rapport 0.953 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0022** (β de hausse 1.0876, asymétrie 0.9215) vs FCHI — 620 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 121.1216 sur swing_based (1.78 ATR, 7.611 %) — p(stop avant cible) 0.2389 [0.20 ; 0.29], R/R 3.184, perte reelle 7.794 % (gap inclus), CVaR 8.487 %, EV 0.0869 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9593 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.79 ATR (stop 4.544 %) — p(stop avant cible) 0.5238 [0.47 ; 0.58], R/R 5.268, perte reelle 4.711 % (gap inclus), EV -0.3072 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.524, borne haute 0.576 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.6 % x 24.82 % + P(rien) 47.0 % x 4.27 % ne couvrent pas P(stop) 52.4 % x 4.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.78 ATR (stop 7.611 %) — p(stop avant cible) 0.2389 [0.20 ; 0.29], R/R 3.184, perte reelle 7.794 % (gap inclus), EV 0.0869 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🔴 support a 5.76 ATR (stop 19.938 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 1.197, perte reelle 20.737 % (gap inclus), EV 0.3239 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.43 % > budget 12.00 %
      - ⚠ support DETECTE a 0.69 ATR du spot — compartiment <1, mesure a 46.6 % de casse (IC clusterise [0.434 ; 0.497] sur 1119 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.774 %) — p(stop avant cible) 0.9204 [0.89 ; 0.95], R/R 30.668, perte reelle 0.809 % (gap inclus), EV -0.1021 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 30.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.920, borne haute 0.946 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.3 % x 24.82 % + P(rien) 7.7 % x 7.42 % ne couvrent pas P(stop) 92.0 % x 0.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.547 %) — p(stop avant cible) 0.8185 [0.78 ; 0.86], R/R 15.36, perte reelle 1.616 % (gap inclus), EV -0.155 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 15.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.819, borne haute 0.856 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.6 % x 24.82 % + P(rien) 17.5 % x 5.79 % ne couvrent pas P(stop) 81.8 % x 1.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.79 ATR (stop 3.362 %) — p(stop avant cible) 0.6328 [0.58 ; 0.68], R/R 7.157, perte reelle 3.468 % (gap inclus), EV -0.231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 7.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.633, borne haute 0.682 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.6 % x 24.82 % + P(rien) 36.1 % x 5.02 % ne couvrent pas P(stop) 63.3 % x 3.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 3.868 %) — p(stop avant cible) 0.5831 [0.53 ; 0.63], R/R 6.163, perte reelle 4.027 % (gap inclus), EV -0.2903 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.583, borne haute 0.634 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 0.6 % x 24.82 % + P(rien) 41.1 % x 4.64 % ne couvrent pas P(stop) 58.3 % x 4.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.78 ATR (stop 6.429 %) — p(stop avant cible) 0.3317 [0.28 ; 0.38], R/R 3.761, perte reelle 6.6 % (gap inclus), EV -0.1224 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.6 % x 24.82 % + P(rien) 66.2 % x 2.89 % ne couvrent pas P(stop) 33.2 % x 6.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 6.963 %) — p(stop avant cible) 0.2857 [0.24 ; 0.34], R/R 3.477, perte reelle 7.138 % (gap inclus), EV -0.0303 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.6 % x 24.82 % + P(rien) 70.8 % x 2.62 % ne couvrent pas P(stop) 28.6 % x 7.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 8.51 %) — p(stop avant cible) 0.1876 [0.15 ; 0.23], R/R 2.87, perte reelle 8.646 % (gap inclus), EV 0.1606 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.284 %) — p(stop avant cible) 0.1323 [0.10 ; 0.17], R/R 2.628, perte reelle 9.445 % (gap inclus), EV 0.24 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 10.831 %) — p(stop avant cible) 0.0849 [0.06 ; 0.12], R/R 2.252, perte reelle 11.019 % (gap inclus), EV 0.2478 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 12.379 %) — p(stop avant cible) 0.0602 [0.04 ; 0.09], R/R 1.948, perte reelle 12.744 % (gap inclus), EV 0.2097 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.82 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 13.926 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 1.729, perte reelle 14.351 % (gap inclus), EV 0.2357 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.41 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.473 %) — p(stop avant cible) 0.0166 [0.01 ; 0.03], R/R 1.542, perte reelle 16.092 % (gap inclus), EV 0.2769 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.90 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.021 %) — p(stop avant cible) 0.0088 [0.00 ; 0.02], R/R 1.412, perte reelle 17.576 % (gap inclus), EV 0.2865 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.82 % > budget 12.00 %
   - 🔴 grid_snapped a 5.76 ATR (stop 18.755 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 1.262, perte reelle 19.666 % (gap inclus), EV 0.3168 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.56 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.663 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 1.082, perte reelle 22.946 % (gap inclus), EV 0.3247 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 23.21 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.032, perte reelle 24.046 % (gap inclus), EV 0.3291 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.34 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.758 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.998, perte reelle 24.876 % (gap inclus), EV 0.3321 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.28 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 131.1, ATR14 4.0571 (3.095 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 1.08 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.155 % | 130.8971 | 87.84 % | 91.56 % | 93.32 % | 95.18 % | 97.03 % | 97.9 % |
| 0.1 ATR | 0.309 % | 130.6943 | 82.06 % | 87.93 % | 90.47 % | 93.21 % | 95.65 % | 97.0 % |
| 0.15 ATR | 0.464 % | 130.4914 | 75.49 % | 83.71 % | 87.03 % | 90.26 % | 94.16 % | 95.7 % |
| 0.2 ATR | 0.619 % | 130.2886 | 68.92 % | 78.51 % | 83.3 % | 88.29 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.774 % | 130.0857 | 62.25 % | 73.7 % | 79.17 % | 85.14 % | 90.7 % | 93.81 % |
| 0.35 ATR | 1.083 % | 129.68 | 49.9 % | 64.28 % | 71.81 % | 78.84 % | 86.65 % | 91.61 % |
| 0.5 ATR | 1.547 % | 129.0714 | 34.61 % | 52.4 % | 61.39 % | 70.77 % | 80.22 % | 87.41 % |
| 0.75 ATR | 2.321 % | 128.0571 | 20.49 % | 36.21 % | 46.95 % | 58.56 % | 70.23 % | 80.92 % |
| 1.0 ATR | 3.095 % | 127.0429 | 10.69 % | 24.24 % | 34.48 % | 48.23 % | 61.62 % | 74.23 % |
| 1.25 ATR | 3.868 % | 126.0286 | 4.8 % | 16.19 % | 24.95 % | 39.37 % | 54.5 % | 67.73 % |
| 1.5 ATR | 4.642 % | 125.0143 | 2.45 % | 11.29 % | 18.76 % | 30.81 % | 47.08 % | 60.34 % |
| 2.0 ATR | 6.189 % | 122.9857 | 0.88 % | 5.3 % | 10.22 % | 19.69 % | 35.41 % | 50.45 % |
| 2.5 ATR | 7.737 % | 120.9571 | 0.49 % | 2.65 % | 5.7 % | 11.71 % | 24.63 % | 38.56 % |
| 3.0 ATR | 9.284 % | 118.9286 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.51 % | 30.07 % |
| 4.0 ATR | 12.379 % | 114.8714 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.78 % |
| 6.0 ATR | 18.568 % | 106.7572 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.3 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.61 ATR | 2.06 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.45 ATR | 2.02 ATR | 2.64 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.09 ATR | 1.44 ATR | 1.76 ATR | 1.99 ATR | 2.69 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.59 ATR | 2.11 ATR | 2.48 ATR | 2.83 ATR | 3.75 ATR | 4.81 ATR |
| **20 s.** | 0.97 ATR | 2.02 ATR | 2.23 ATR | 2.83 ATR | 3.41 ATR | 3.82 ATR | 5.15 ATR | 5.90 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (71.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.321 %, prix 128.0572), p(touche) 36.21 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.789–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.095 %, prix 127.0425), p(touche) 34.48 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.091–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.868 %, prix 126.0291), p(touche) 39.37 % (en stress 93.14 %)  ✅ optimum identifie (62.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.589–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.189 %, prix 122.9862), p(touche) 35.41 % (en stress 98.04 %)  ✅ optimum identifie (70.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.229–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.737 %, prix 120.9568), p(touche) 38.56 % (en stress 98.02 %)  ✅ optimum identifie (68.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.127 | EV/share : €-0.248 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 10 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.7 | bear 12.4 | side 72.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 131.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.528% → cible +1.556% / stop −1.5%, p_fill 73%, n_eff≈76.1) : P(cible|rempli) **24%** · **EV/risk -0.219** (×p_fill ; si rempli -0.45% du capital)
  - **swing** (entrée dip −1.165% → cible +3.501% / stop −3.131%, p_fill 65%, n_eff≈75.4) : P(cible|rempli) **30%** · **EV/risk -0.125** (×p_fill ; si rempli -0.60% du capital)
  - **deep** (entrée dip −1.808% → cible +4.983% / stop −4.727%, p_fill 64%, n_eff≈72.8) : P(cible|rempli) **35%** · **EV/risk -0.102** (×p_fill ; si rempli -0.75% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→57% · +2.0%→28% · +3.0%→12% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.73% (p90 4.75%) · excursion haute méd. +1.13% / basse méd. −1.13%
- Profil de vol intra : ouverture 1.673% vs midi 0.529% vs clôture 0.71% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -0.332% ; recovery-V 10%
- **σ réalisé intraday** 1.991% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 71% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 136.2225 (VA 135.7475–137.0775 ; dernier close 136.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 25% · rebond 31% · **stop −2.1%** sous le fill (sous le bruit) · cible +0.53% · R/R 0.25 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 25% (gap-down >1% 3% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.34% (p90 −1.71%) · haut méd +0.28% · range méd 0.92%
- Excursion ouverture 15min (n=160) : bas méd −0.45% (p90 −1.95%) · haut méd +0.44% · range méd 1.27%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.08%) · haut méd +0.6% · range méd 1.4%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.28%) · haut méd +0.64% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 38% · séance 57% (88/159) · gap 9% · délai 3.9min · rebond 41% (38/88) (MFE +0.64%)
   - −1.0% : fill 30min 20% · séance 46% (69/159) · gap 3% · délai 51.9min · rebond 35% (27/69) (MFE +0.58%)
   - −1.5% : fill 30min 12% · séance 36% (54/159) · gap 0% · délai 62.0min · rebond 31% (19/54) (MFE +0.58%)
   - −2.0% : fill 30min 7% · séance 25% (39/159) · gap 0% · délai 111.9min · rebond 31% (15/39) (MFE +0.53%)
   - −3.0% : fill 30min 4% · séance 14% (23/159) · gap 0% · délai 268.3min · rebond 37% (10/23) (MFE +0.59%)
   - −4.0% : fill 30min 2% · séance 5% (10/159) · gap 0% · délai 161.7min · rebond 8% (3/10) (MFE +0.38%)
   - −5.0% : fill 30min 0% · séance 3% (4/159) · gap 0% · délai 260.4min · rebond 24% (2/4) (MFE +0.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.99%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.81%) → stop au-delà de −0.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.78%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.01% (p90 −2.27%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 77% (17/22) · rebond 27% (6/17)
      · −2.0% : fill 61% (12/22) · rebond 12% (2/12)
      · −3.0% : fill 43% (9/22) · rebond 15% (3/9)
      · −4.0% : fill 26% (6/22) · rebond 4% (1/6)
      · −5.0% : fill 20% (3/22) · rebond 20% (1/3)
   - **flat** (36 séances) :
      · −1.0% : fill 54% (21/36) · rebond 27% (7/21)
      · −2.0% : fill 25% (12/36) · rebond 33% (5/12)
      · −3.0% : fill 16% (8/36) · rebond 32% (3/8)
      · −4.0% : fill 5% (3/36) · rebond 8% (1/3)
      · −5.0% : fill 0% (1/36) · rebond 100% (1/1)
   - **gap-up** (101 séances) :
      · −1.0% : fill 35% (31/101) · rebond 44% (14/31)
      · −2.0% : fill 18% (15/101) · rebond 45% (8/15)
      · −3.0% : fill 6% (6/101) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/101) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/101) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 65% si les 15 1res min sont vertes (85 cas) · 22% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **20min** → P(séance verte=clôture>ouverture) 69% si début vert vs 23% si rouge (base 46% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 242min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **69%** · continue >prix actuel 58% ; creux résiduel méd -0.98% (q20 -1.84%) → **SL/trailing à −1.84%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.1% / q75 +1.84% → **scale +1.1% / runner +1.84%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **23%** (continue à baisser 63%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.05%** (au-delà de la MAE q10 -3.05%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.96% .. +1.64%] · haut q95 +2.01% · bas q05 -2.58%
   - 60min (n=160) : retour [-2.59% .. +2.13%] · haut q95 +2.44% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.07% .. +2.15%] · haut q95 +2.67% · bas q05 -3.66%
   - 4h (n=160) : retour [-2.91% .. +2.47%] · haut q95 +3.05% · bas q05 -3.75%
   - 6h (n=160) : retour [-3.6% .. +3.4%] · haut q95 +3.53% · bas q05 -4.13%
   - session (n=160) : retour [-3.38% .. +2.74%] · haut q95 +3.86% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.5  _(momentum baissier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist -0.367  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 12.9%
- **ATR** : 4.06 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.167  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 47.3  _(transition)_
- **MA** : MA20 134.5 · MA50 137.37 · MA200 135.77  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 -4.6% · MA200 -3.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (939152 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
