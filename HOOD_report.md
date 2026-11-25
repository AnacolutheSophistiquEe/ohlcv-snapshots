# HOOD

**Generated** : 2026-11-25T01:30:38.647599+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $65.67  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot $65.67 (+0.8% vs entrée) · entrée $65.13 · stop $63.17 · T1 $67.84 · R/R 1.38  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.4 % ≠ (strike 69.0 − spot 65.67)/spot = +5.1 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 65.67 · ATR Wilder 5.31 (8.08 %)_
- **Swing** : plage **59.53 → 54.68** (-9.34 % a -16.72 % sous la cloture, 0.91 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 52.65-54.84 (B). stop INDICATIF 47.23 (-13.64 % sous le bas ; sous le support 49.88-52.06 (- 0,5 ATR)).
- **Deep** : plage **54.68 → 43.89** (-16.72 % a -33.16 % sous la cloture, 2.03 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 52.65-54.84 (B) ; 49.88-52.06 (B) ; 45.56-48.08 (A) ; 42.76-44.02 (B). stop INDICATIF 37.09 (-15.5 % sous le bas ; sous le support 39.74-40.47 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.08 ATR sous le plus haut 20 s., RSI(2) 41.9. Limite **63.01** (seance suivante), stop catastrophe 41.78, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 62.63-63.51 (B, -3.27 %) ; 52.65-54.84 (B, -16.49 %) ; 49.88-52.06 (B, -20.72 %) ; 45.56-48.08 (A, -26.78 %) ; 42.76-44.02 (B, -32.96 %) ; 39.74-40.47 (C, -38.38 %)
- Resistances reelles au-dessus : 69.93-72.25 (A, 6.5 %) ; 72.79-74.59 (A, 10.86 %) ; 75.51-77.87 (A, 14.99 %) ; 78.93-79.57 (A, 20.2 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.42 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.06 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **1.451 pt plus bas** dans le cas TYPIQUE (médiane), 5.895 au p90, **7.725 au pire**
   - perte réelle **12.711 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 10.06 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0127 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.514 % | p01 -6.925 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3206** [0.2545 ; 0.3927] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.3683** [0.3187 ; 0.4201] _(largeur 10.1 pt, n_eff 345.7)_
   - deep : **0.3466** [0.2979 ; 0.3979] _(largeur 10.0 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.39 %** | CVaR **-9.19 %** | vol 4.36 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.04 % contre 4.43 % aujourd'hui, rapport 0.46)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.41 % vs -14.72 % si l'on extrapolait par √5 _(rapport 0.979 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8507** (β de hausse 1.6459, asymétrie 1.1244) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 60.244 sur atr_grid (1.0 ATR, 8.256 %) — p(stop avant cible) 0.5571 [0.50 ; 0.61], R/R 4.523, perte reelle 8.755 % (gap inclus), CVaR 11.764 %, EV -0.5708 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0896 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.557, borne haute 0.609 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.4 ATR (stop 6.808 %) — p(stop avant cible) 0.6361 [0.58 ; 0.69], R/R 5.436, perte reelle 7.285 % (gap inclus), EV -0.6864 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.636, borne haute 0.685 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.40 ATR du spot — compartiment <1, mesure a 49.2 % de casse (IC clusterise [0.458 ; 0.523] sur 1200 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 0.3 % x 39.60 % + P(rien) 36.1 % x 10.64 % ne couvrent pas P(stop) 63.6 % x 7.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 12.383 %) — p(stop avant cible) 0.353 [0.30 ; 0.40], R/R 3.052, perte reelle 12.974 % (gap inclus), EV -0.3988 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 0.3 % x 39.60 % + P(rien) 64.4 % x 6.33 % ne couvrent pas P(stop) 35.3 % x 12.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.4 ATR (stop 5.751 %) — p(stop avant cible) 0.6796 [0.63 ; 0.73], R/R 6.479, perte reelle 6.113 % (gap inclus), EV -0.481 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 6.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.680, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 0.3 % x 39.60 % + P(rien) 31.8 % x 11.23 % ne couvrent pas P(stop) 68.0 % x 6.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 8.256 %) — p(stop avant cible) 0.5571 [0.50 ; 0.61], R/R 4.523, perte reelle 8.755 % (gap inclus), EV -0.5708 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.557, borne haute 0.609 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 0.3 % x 39.60 % + P(rien) 44.0 % x 9.55 % ne couvrent pas P(stop) 55.7 % x 8.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 10.32 %) — p(stop avant cible) 0.4556 [0.40 ; 0.51], R/R 3.659, perte reelle 10.823 % (gap inclus), EV -0.4681 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 0.3 % x 39.60 % + P(rien) 54.2 % x 8.05 % ne couvrent pas P(stop) 45.6 % x 10.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 14.447 %) — p(stop avant cible) 0.2673 [0.22 ; 0.32], R/R 2.665, perte reelle 14.862 % (gap inclus), EV -0.4442 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 0.3 % x 39.60 % + P(rien) 73.0 % x 4.69 % ne couvrent pas P(stop) 26.7 % x 14.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 16.511 %) — p(stop avant cible) 0.1917 [0.15 ; 0.24], R/R 2.356, perte reelle 16.812 % (gap inclus), EV -0.3675 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.3 % x 39.60 % + P(rien) 80.6 % x 3.42 % ne couvrent pas P(stop) 19.2 % x 16.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 18.575 %) — p(stop avant cible) 0.132 [0.10 ; 0.17], R/R 2.106, perte reelle 18.806 % (gap inclus), EV -0.3486 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.3 % x 39.60 % + P(rien) 86.5 % x 2.35 % ne couvrent pas P(stop) 13.2 % x 18.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 20.639 %) — p(stop avant cible) 0.0863 [0.06 ; 0.12], R/R 1.898, perte reelle 20.868 % (gap inclus), EV -0.25 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.3 % x 39.60 % + P(rien) 91.1 % x 1.59 % ne couvrent pas P(stop) 8.6 % x 20.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 22.703 %) — p(stop avant cible) 0.0544 [0.03 ; 0.08], R/R 1.722, perte reelle 22.999 % (gap inclus), EV -0.2056 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.3 % x 39.60 % + P(rien) 94.3 % x 1.00 % ne couvrent pas P(stop) 5.4 % x 23.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 24.767 %) — p(stop avant cible) 0.0265 [0.01 ; 0.05], R/R 1.563, perte reelle 25.333 % (gap inclus), EV -0.148 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.3 % x 39.60 % + P(rien) 97.1 % x 0.43 % ne couvrent pas P(stop) 2.6 % x 25.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 28.895 %) — p(stop avant cible) 0.019 [0.01 ; 0.04], R/R 1.355, perte reelle 29.217 % (gap inclus), EV -0.1626 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.3 % x 39.60 % + P(rien) 97.8 % x 0.30 % ne couvrent pas P(stop) 1.9 % x 29.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 33.022 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 1.19, perte reelle 33.266 % (gap inclus), EV -0.0832 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.2 % x -0.02 % ne couvrent pas P(stop) 0.5 % x 33.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 37.15 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.066, perte reelle 37.15 % (gap inclus), EV -0.0429 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.6 % x -0.09 % ne couvrent pas P(stop) 0.1 % x 37.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 41.278 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.959, perte reelle 41.278 % (gap inclus), EV -0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.7 % x -0.13 % ne couvrent pas P(stop) 0.0 % x 41.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 45.406 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.872, perte reelle 45.406 % (gap inclus), EV -0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.7 % x -0.13 % ne couvrent pas P(stop) 0.0 % x 45.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 49.534 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.799, perte reelle 49.534 % (gap inclus), EV -0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.7 % x -0.13 % ne couvrent pas P(stop) 0.0 % x 49.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 53.662 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.738, perte reelle 53.662 % (gap inclus), EV -0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.7 % x -0.13 % ne couvrent pas P(stop) 0.0 % x 53.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 57.789 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.685, perte reelle 57.789 % (gap inclus), EV -0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.7 % x -0.13 % ne couvrent pas P(stop) 0.0 % x 57.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 61.917 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.64, perte reelle 61.917 % (gap inclus), EV -0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.7 % x -0.13 % ne couvrent pas P(stop) 0.0 % x 61.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 66.045 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.6, perte reelle 66.045 % (gap inclus), EV -0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.3 % x 39.60 % + P(rien) 99.7 % x -0.13 % ne couvrent pas P(stop) 0.0 % x 66.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 65.665, ATR14 5.421 (8.256 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 3.096 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.413 % | 65.3939 | 93.05 % | 95.36 % | 96.27 % | 96.76 % | 97.26 % | 98.05 % |
| 0.1 ATR | 0.826 % | 65.1229 | 85.6 % | 90.83 % | 92.53 % | 94.03 % | 94.92 % | 96.41 % |
| 0.15 ATR | 1.238 % | 64.8518 | 77.95 % | 85.89 % | 88.6 % | 90.9 % | 92.89 % | 95.07 % |
| 0.2 ATR | 1.651 % | 64.5808 | 71.5 % | 80.65 % | 84.36 % | 87.66 % | 90.65 % | 93.22 % |
| 0.25 ATR | 2.064 % | 64.3097 | 64.55 % | 75.0 % | 79.82 % | 84.23 % | 88.01 % | 90.86 % |
| 0.35 ATR | 2.889 % | 63.7676 | 52.57 % | 66.13 % | 72.86 % | 78.87 % | 84.35 % | 87.99 % |
| 0.5 ATR | 4.128 % | 62.9545 | 37.16 % | 54.03 % | 62.06 % | 69.87 % | 77.54 % | 82.34 % |
| 0.75 ATR | 6.192 % | 61.5992 | 19.54 % | 36.59 % | 46.82 % | 57.03 % | 66.77 % | 73.2 % |
| 1.0 ATR | 8.256 % | 60.244 | 9.37 % | 23.79 % | 34.01 % | 45.5 % | 56.4 % | 65.81 % |
| 1.25 ATR | 10.32 % | 58.8887 | 4.83 % | 15.02 % | 23.51 % | 35.49 % | 48.88 % | 59.65 % |
| 1.5 ATR | 12.383 % | 57.5334 | 2.52 % | 10.28 % | 16.85 % | 28.41 % | 42.17 % | 54.0 % |
| 2.0 ATR | 16.511 % | 54.8229 | 0.4 % | 3.83 % | 7.37 % | 15.98 % | 31.3 % | 44.35 % |
| 2.5 ATR | 20.639 % | 52.1124 | 0.0 % | 1.41 % | 3.73 % | 8.39 % | 22.66 % | 35.42 % |
| 3.0 ATR | 24.767 % | 49.4019 | 0.0 % | 0.5 % | 2.12 % | 4.95 % | 15.65 % | 27.41 % |
| 4.0 ATR | 33.022 % | 43.9808 | 0.0 % | 0.3 % | 0.61 % | 1.82 % | 6.0 % | 15.91 % |
| 6.0 ATR | 49.534 % | 33.1387 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 5.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.63 ATR | 0.82 ATR | 0.98 ATR | 1.11 ATR | 1.52 ATR | 1.91 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.86 ATR | 2.33 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.01 ATR | 1.34 ATR | 1.64 ATR | 1.84 ATR | 2.39 ATR | 2.99 ATR |
| **10 s.** | 0.56 ATR | 1.21 ATR | 1.40 ATR | 1.92 ATR | 2.37 ATR | 2.69 ATR | 3.58 ATR | 4.43 ATR |
| **20 s.** | 0.70 ATR | 1.71 ATR | 1.97 ATR | 2.65 ATR | 3.21 ATR | 3.64 ATR | 5.12 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.424 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.629–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.192 %, prix 61.599), p(touche) 36.59 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.786–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.256 %, prix 60.2437), p(touche) 34.01 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.012–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.32 %, prix 58.8884), p(touche) 35.49 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.395–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (12.383 %, prix 57.5337), p(touche) 42.17 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.966–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.511 %, prix 54.8231), p(touche) 44.35 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : $-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.8 | bear 83.2 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.814% → cible +4.162% / stop −3.0%, p_fill 74%, n_eff≈79.6) : P(cible|rempli) **12%** · **EV/risk -0.122** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −1.805% → cible +10.716% / stop −8.407%, p_fill 75%, n_eff≈85.7) : P(cible|rempli) **27%** · **EV/risk +0.025** (×p_fill ; si rempli +0.28% du capital)
  - **deep** (entrée dip −2.787% → cible +13.427% / stop −12.738%, p_fill 70%, n_eff≈77.2) : P(cible|rempli) **43%** · **EV/risk +0.060** (×p_fill ; si rempli +1.09% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→52% · +3.0%→34% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.75% (p90 8.94%) · excursion haute méd. +2.07% / basse méd. −2.15%
- Profil de vol intra : ouverture 3.568% vs midi 0.948% vs clôture 1.079% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.057)_ ; drift intra méd. -0.413% ; recovery-V 19%
- **σ réalisé intraday** 3.025% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 60% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 96.1559 (VA 95.5739–96.6651 ; dernier close 95.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 27% · rebond 71% · **stop −3.99%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. -0.16% · baisse 53% (gap-down >1% 34% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.34%) · haut méd +0.88% · range méd 2.06%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −2.96%) · haut méd +1.23% · range méd 2.63%
- Excursion ouverture 30min (n=160) : bas méd −1.41% (p90 −3.35%) · haut méd +1.36% · range méd 3.2%
- Excursion ouverture 60min (n=160) : bas méd −1.78% (p90 −3.71%) · haut méd +1.53% · range méd 3.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.07 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (122/159) · gap 41% · délai 0.0min · rebond 60% (70/122) (MFE +1.4%)
   - −1.0% : fill 30min 58% · séance 70% (107/159) · gap 34% · délai 0.0min · rebond 65% (66/107) (MFE +1.62%)
   - −1.5% : fill 30min 46% · séance 62% (97/159) · gap 25% · délai 1.1min · rebond 55% (54/97) (MFE +1.31%)
   - −2.0% : fill 30min 36% · séance 50% (84/159) · gap 19% · délai 1.6min · rebond 63% (55/84) (MFE +1.3%)
   - −3.0% : fill 30min 24% · séance 35% (61/159) · gap 10% · délai 7.4min · rebond 74% (44/61) (MFE +1.88%)
   - −4.0% : fill 30min 15% · séance 27% (45/159) · gap 3% · délai 11.1min · rebond 71% (32/45) (MFE +2.53%)
   - −5.0% : fill 30min 7% · séance 17% (28/159) · gap 1% · délai 55.8min · rebond 47% (18/28) (MFE +1.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.47%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.3%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.41%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=725 jambes) : jambe baissière méd −1.14% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 91% (68/72) · rebond 57% (36/68)
      · −2.0% : fill 73% (58/72) · rebond 64% (37/58)
      · −3.0% : fill 59% (47/72) · rebond 82% (35/47)
      · −4.0% : fill 47% (36/72) · rebond 78% (28/36)
      · −5.0% : fill 31% (24/72) · rebond 47% (15/24)
   - **flat** (17 séances) :
      · −1.0% : fill 72% (11/17) · rebond 79% (8/11)
      · −2.0% : fill 38% (8/17) · rebond 55% (5/8)
      · −3.0% : fill 15% (3/17) · rebond 0% (0/3)
      · −4.0% : fill 15% (3/17) · rebond 0% (0/3)
      · −5.0% : fill 13% (2/17) · rebond 15% (1/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 45% (28/70) · rebond 78% (22/28)
      · −2.0% : fill 29% (18/70) · rebond 63% (13/18)
      · −3.0% : fill 13% (11/70) · rebond 56% (9/11)
      · −4.0% : fill 7% (6/70) · rebond 63% (4/6)
      · −5.0% : fill 2% (2/70) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 58% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 65% si début vert vs 18% si rouge (base 42% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **65%** · continue >prix actuel 43% ; creux résiduel méd -1.45% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +2.53% → **scale +1.32% / runner +2.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 63%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.8%** (au-delà de la MAE q10 -3.8%), cible rebond +1.47% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.48% .. +3.77%] · haut q95 +4.35% · bas q05 -4.82%
   - 60min (n=160) : retour [-3.67% .. +4.97%] · haut q95 +5.48% · bas q05 -4.85%
   - 2h (n=160) : retour [-4.63% .. +4.96%] · haut q95 +6.62% · bas q05 -5.1%
   - 4h (n=160) : retour [-4.82% .. +5.74%] · haut q95 +7.31% · bas q05 -6.0%
   - 6h (n=160) : retour [-5.77% .. +6.28%] · haut q95 +7.31% · bas q05 -7.11%
   - session (n=160) : retour [-5.56% .. +6.85%] · haut q95 +7.46% · bas q05 -7.12%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.88% (p75 1.28% / p90 2.57%) · ~3.72 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=50)
   - −1.0% → **68%** (reprise méd 26.42 min, n=21)
   - −1.5% → **64%** (reprise méd 29.02 min, n=10)
   - −2.0% → **53%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.57%** (p90, défaut prudent ; serré/agressif −1.28%) ; extension open→close méd +6.81% (q75 +7.91% / q95 +11.09%), MFE méd +7.28% / q90 +11.48%
   - Échelle scale-out : +7.28% (33%) / +8.78% (33%) / +11.48% (34%)
- **DÉSARMER** : repli > **−2.57%** depuis le plus-haut = décay → P(retournement) **39%** (préavis méd 256.98 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.48% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +0.47%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.71 · part idiosyncratique 0.29
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.6  _(survente)_
- **ADX** : 34.3  _(tendance etablie)_
- **MACD** : hist -0.749  _(pas de croisement recent)_
- **BB** : %B 0.14 · largeur 45.2%
- **ATR** : 5.42 (54.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.078  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 42.1  _(transition)_
- **MA** : MA20 78.35 · MA50 96.63 · MA200 90.78  _(prix < MA20)_
- **Dist MA** : MA20 -16.2% · MA50 -32.0% · MA200 -27.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (526394 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
