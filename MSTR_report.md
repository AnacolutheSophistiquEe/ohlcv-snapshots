# MSTR

**Generated** : 2026-11-20T01:24:39.610844+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $86.15  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (19 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $86.15 (+1.3% vs entrée) · entrée $85.06 · stop $82.58 · T1 $89.47 · R/R 1.78  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +18.5 % ≠ (strike 107.0 − spot 86.15)/spot = +24.2 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 494 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-19 : 86.15 · ATR Wilder 8.57 (9.94 %)_
- **Swing** : plage **75.3 → 67.75** (-12.6 % a -21.36 % sous la cloture, 0.88 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 54.56 (-19.46 % sous le bas ; sous le support 58.85-61.41 (- 0,5 ATR)).
- **Deep** : plage **67.75 → 48.24** (-21.36 % a -44.0 % sous la cloture, 2.28 ATR) — touchee 47 % → 15 % du temps en 20 seances ; supports reels dans la plage : 58.85-61.41 (C) ; 48.73-52.79 (A). stop INDICATIF 39.59 (-17.93 % sous le bas ; sous le support 43.87-48.11 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 7.71 ATR sous le plus haut 20 s., RSI(2) 0.2. Limite **81.87** (seance suivante), stop catastrophe 47.61, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 80.68-81.81 (A, -5.04 %) ; 58.85-61.41 (C, -28.72 %) ; 48.73-52.79 (A, -38.72 %) ; 43.87-48.11 (A, -44.16 %)
- Resistances reelles au-dessus : 89.21-91.67 (A, 3.55 %) ; 100.05-104.17 (A, 16.13 %) ; 104.6-105.5 (A, 21.42 %) ; 113.2-116.4 (A, 31.4 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=11.01 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.4 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **14.178 pt plus bas** dans le cas TYPIQUE (médiane), 14.813 au p90, **14.972 au pire**
   - perte réelle **22.94 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 12.4 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0252 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.584 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3718** [0.3024 ; 0.4454] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.3078** [0.2609 ; 0.3579] _(largeur 9.7 pt, n_eff 345.7)_
   - deep : **0.2568** [0.2129 ; 0.3047] _(largeur 9.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.35 %** | CVaR **-9.26 %** | vol 5.03 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.31 % contre 5.40 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.42 % vs -18.02 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3792** (β de hausse 1.8255, asymétrie 1.3033) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 77.8536 sur atr_grid (1.0 ATR, 9.63 %) — p(stop avant cible) 0.4834 [0.43 ; 0.54], R/R 3.419, perte reelle 9.766 % (gap inclus), CVaR 10.891 %, EV -0.2773 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6867 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.52 ATR (stop 8.312 %) — p(stop avant cible) 0.5531 [0.50 ; 0.60], R/R 3.909, perte reelle 8.54 % (gap inclus), EV -0.226 % — **REFUSE**
      - refuse : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.553, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.451 ; 0.512] sur 1246 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 4.7 % x 33.38 % + P(rien) 40.0 % x 7.35 % ne couvrent pas P(stop) 55.3 % x 8.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 14.445 %) — p(stop avant cible) 0.2943 [0.25 ; 0.34], R/R 2.278, perte reelle 14.657 % (gap inclus), EV -0.4755 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 4.9 % x 33.38 % + P(rien) 65.7 % x 3.37 % ne couvrent pas P(stop) 29.4 % x 14.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.408 %) — p(stop avant cible) 0.8869 [0.85 ; 0.92], R/R 12.966, perte reelle 2.575 % (gap inclus), EV -0.7358 % — **REFUSE**
      - refuse : cible atteinte seulement 1.9 % du temps (< 15 %) meme a 10 seances : le R/R de 12.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.887, borne haute 0.917 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 1.9 % x 33.38 % + P(rien) 9.4 % x 9.72 % ne couvrent pas P(stop) 88.7 % x 2.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 9.63 %) — p(stop avant cible) 0.4834 [0.43 ; 0.54], R/R 3.419, perte reelle 9.766 % (gap inclus), EV -0.2773 % — **REFUSE**
      - refuse : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 4.7 % x 33.38 % + P(rien) 47.0 % x 6.12 % ne couvrent pas P(stop) 48.3 % x 9.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 12.038 %) — p(stop avant cible) 0.3841 [0.33 ; 0.44], R/R 2.742, perte reelle 12.173 % (gap inclus), EV -0.3074 % — **REFUSE**
      - refuse : cible atteinte seulement 4.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 4.8 % x 33.38 % + P(rien) 56.8 % x 4.88 % ne couvrent pas P(stop) 38.4 % x 12.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 16.853 %) — p(stop avant cible) 0.2042 [0.16 ; 0.25], R/R 1.954, perte reelle 17.089 % (gap inclus), EV -0.5692 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 4.9 % x 33.38 % + P(rien) 74.7 % x 1.73 % ne couvrent pas P(stop) 20.4 % x 17.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 19.26 %) — p(stop avant cible) 0.1503 [0.12 ; 0.19], R/R 1.703, perte reelle 19.602 % (gap inclus), EV -0.7208 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 4.9 % x 33.38 % + P(rien) 80.1 % x 0.75 % ne couvrent pas P(stop) 15.0 % x 19.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 21.668 %) — p(stop avant cible) 0.1247 [0.09 ; 0.16], R/R 1.51, perte reelle 22.112 % (gap inclus), EV -0.8003 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 4.9 % x 33.38 % + P(rien) 82.7 % x 0.40 % ne couvrent pas P(stop) 12.5 % x 22.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 24.076 %) — p(stop avant cible) 0.0919 [0.06 ; 0.13], R/R 1.363, perte reelle 24.5 % (gap inclus), EV -0.8516 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 4.9 % x 33.38 % + P(rien) 85.9 % x -0.26 % ne couvrent pas P(stop) 9.2 % x 24.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 26.483 %) — p(stop avant cible) 0.0693 [0.05 ; 0.10], R/R 1.246, perte reelle 26.802 % (gap inclus), EV -0.8573 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 4.9 % x 33.38 % + P(rien) 88.2 % x -0.71 % ne couvrent pas P(stop) 6.9 % x 26.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 28.891 %) — p(stop avant cible) 0.0566 [0.04 ; 0.08], R/R 1.14, perte reelle 29.284 % (gap inclus), EV -0.9396 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 4.9 % x 33.38 % + P(rien) 89.5 % x -1.01 % ne couvrent pas P(stop) 5.7 % x 29.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 33.706 %) — p(stop avant cible) 0.0221 [0.01 ; 0.04], R/R 0.98, perte reelle 34.056 % (gap inclus), EV -0.8491 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 4.9 % x 33.38 % + P(rien) 92.9 % x -1.85 % ne couvrent pas P(stop) 2.2 % x 34.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 38.521 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.859, perte reelle 38.858 % (gap inclus), EV -0.7607 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 4.9 % x 33.38 % + P(rien) 94.7 % x -2.33 % ne couvrent pas P(stop) 0.5 % x 38.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 43.336 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.769, perte reelle 43.407 % (gap inclus), EV -0.717 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.45 % ne couvrent pas P(stop) 0.0 % x 43.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 48.151 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.687, perte reelle 48.619 % (gap inclus), EV -0.7165 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.46 % ne couvrent pas P(stop) 0.0 % x 48.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 52.966 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.625, perte reelle 53.435 % (gap inclus), EV -0.7176 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.46 % ne couvrent pas P(stop) 0.0 % x 53.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 57.781 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.578, perte reelle 57.803 % (gap inclus), EV -0.7125 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.46 % ne couvrent pas P(stop) 0.0 % x 57.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 62.596 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.533, perte reelle 62.596 % (gap inclus), EV -0.7139 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.46 % ne couvrent pas P(stop) 0.0 % x 62.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 67.412 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.495, perte reelle 67.412 % (gap inclus), EV -0.7147 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.46 % ne couvrent pas P(stop) 0.0 % x 67.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 72.227 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.462, perte reelle 72.227 % (gap inclus), EV -0.7147 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.46 % ne couvrent pas P(stop) 0.0 % x 72.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 77.042 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.433, perte reelle 77.042 % (gap inclus), EV -0.7147 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 4.9 % x 33.38 % + P(rien) 95.1 % x -2.46 % ne couvrent pas P(stop) 0.0 % x 77.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 86.15, ATR14 8.2964 (9.63 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.39 ATR = 3.756 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.482 % | 85.7352 | 93.96 % | 96.47 % | 97.07 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.963 % | 85.3204 | 88.22 % | 92.04 % | 93.74 % | 94.94 % | 96.75 % | 97.33 % |
| 0.15 ATR | 1.445 % | 84.9055 | 81.57 % | 87.5 % | 90.21 % | 92.11 % | 94.51 % | 95.59 % |
| 0.2 ATR | 1.926 % | 84.4907 | 74.02 % | 82.16 % | 85.57 % | 88.78 % | 92.07 % | 93.63 % |
| 0.25 ATR | 2.408 % | 84.0759 | 67.67 % | 78.43 % | 82.74 % | 86.65 % | 89.63 % | 91.89 % |
| 0.35 ATR | 3.371 % | 83.2463 | 54.58 % | 69.25 % | 75.88 % | 81.6 % | 86.28 % | 89.22 % |
| 0.5 ATR | 4.815 % | 82.0018 | 37.56 % | 55.54 % | 63.98 % | 72.3 % | 79.27 % | 84.5 % |
| 0.75 ATR | 7.223 % | 79.9277 | 19.44 % | 38.21 % | 48.13 % | 59.45 % | 69.51 % | 77.0 % |
| 1.0 ATR | 9.63 % | 77.8536 | 9.57 % | 25.71 % | 35.72 % | 47.22 % | 60.37 % | 69.92 % |
| 1.25 ATR | 12.038 % | 75.7795 | 4.13 % | 14.92 % | 25.43 % | 36.5 % | 51.22 % | 62.53 % |
| 1.5 ATR | 14.445 % | 73.7054 | 2.11 % | 8.67 % | 17.56 % | 29.73 % | 44.21 % | 56.88 % |
| 2.0 ATR | 19.26 % | 69.5571 | 0.1 % | 2.92 % | 7.16 % | 16.18 % | 31.5 % | 47.02 % |
| 2.5 ATR | 24.076 % | 65.4089 | 0.1 % | 0.71 % | 2.12 % | 8.39 % | 20.93 % | 37.47 % |
| 3.0 ATR | 28.891 % | 61.2607 | 0.1 % | 0.3 % | 0.71 % | 4.04 % | 14.02 % | 27.72 % |
| 4.0 ATR | 38.521 % | 52.9643 | 0.0 % | 0.0 % | 0.2 % | 0.61 % | 5.59 % | 16.84 % |
| 6.0 ATR | 57.781 % | 36.3714 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.41 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.43 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.58 ATR | 0.65 ATR | 0.85 ATR | 1.02 ATR | 1.13 ATR | 1.45 ATR | 1.82 ATR |
| **3 s.** | 0.36 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.42 ATR | 1.86 ATR | 2.21 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.05 ATR | 1.38 ATR | 1.68 ATR | 1.86 ATR | 2.40 ATR | 2.89 ATR |
| **10 s.** | 0.61 ATR | 1.29 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.57 ATR | 3.48 ATR | 4.23 ATR |
| **20 s.** | 0.82 ATR | 1.85 ATR | 2.11 ATR | 2.73 ATR | 3.25 ATR | 3.71 ATR | 5.06 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.434–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.815 %, prix 82.0019), p(touche) 37.56 % (en stress 85.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.652–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (7.223 %, prix 79.9274), p(touche) 38.21 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.813–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (9.63 %, prix 77.8538), p(touche) 35.72 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.052–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (12.038 %, prix 75.7793), p(touche) 36.5 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.472–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (14.445 %, prix 73.7056), p(touche) 44.21 % (en stress 100.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (63.4 % des re-echantillons)
- **20 seance(s)** : plage utile VIDE (borne basse 2.106 ATR au-dessus du haut de la grille, 2.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 71.6 | side 23.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.261% → cible +5.179% / stop −2.926%, p_fill 73%, n_eff≈79.8) : P(cible|rempli) **14%** · **EV/risk +0.018** (×p_fill ; si rempli +0.07% du capital)
  - **swing** (entrée dip −2.77% → cible +11.074% / stop −9.905%, p_fill 63%, n_eff≈74.8) : P(cible|rempli) **27%** · **EV/risk +0.027** (×p_fill ; si rempli +0.42% du capital)
  - **deep** (entrée dip −4.285% → cible +15.908% / stop −15.091%, p_fill 61%, n_eff≈69.0) : P(cible|rempli) **28%** · **EV/risk -0.044** (×p_fill ; si rempli -1.08% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→58% · +3.0%→40% · +5.0%→19% · +8.0%→10%
- Range intraday médian 5.35% (p90 9.82%) · excursion haute méd. +2.51% / basse méd. −2.26%
- Profil de vol intra : ouverture 3.268% vs midi 1.123% vs clôture 1.265% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 17% · trend ↑2%/↓0% ; spike-down 69% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. 0.468% ; recovery-V 35%
- **σ réalisé intraday** 3.406% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 59% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 148.5395 (VA 146.6095–150.0835 ; dernier close 146.04)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 73% · **stop −3.89%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 38% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −1.81%) · haut méd +0.88% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.68%) · haut méd +1.24% · range méd 2.55%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.06%) · haut méd +1.47% · range méd 2.95%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −3.47%) · haut méd +1.83% · range méd 3.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 76% (121/159) · gap 46% · délai 0.0min · rebond 44% (57/121) (MFE +0.7%)
   - −1.0% : fill 30min 55% · séance 67% (112/159) · gap 38% · délai 0.0min · rebond 48% (59/112) (MFE +0.91%)
   - −1.5% : fill 30min 45% · séance 61% (103/159) · gap 31% · délai 0.0min · rebond 53% (57/103) (MFE +1.16%)
   - −2.0% : fill 30min 38% · séance 54% (91/159) · gap 25% · délai 0.0min · rebond 60% (54/91) (MFE +1.25%)
   - −3.0% : fill 30min 28% · séance 41% (71/159) · gap 17% · délai 0.7min · rebond 52% (38/71) (MFE +1.5%)
   - −4.0% : fill 30min 21% · séance 32% (56/159) · gap 6% · délai 3.2min · rebond 72% (37/56) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 25% (41/159) · gap 4% · délai 12.9min · rebond 73% (29/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.65% (p90 −2.12%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.8% (p90 −2.19%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −2.14%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=888 jambes) : jambe baissière méd −1.12% (p90 −2.6%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 97% (74/75) · rebond 49% (34/74)
      · −2.0% : fill 86% (66/75) · rebond 58% (37/66)
      · −3.0% : fill 71% (57/75) · rebond 49% (30/57)
      · −4.0% : fill 60% (48/75) · rebond 72% (32/48)
      · −5.0% : fill 49% (37/75) · rebond 74% (27/37)
   - **flat** (18 séances) :
      · −1.0% : fill 74% (14/18) · rebond 55% (10/14)
      · −2.0% : fill 46% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 38% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 17% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 30% (24/66) · rebond 41% (15/24)
      · −2.0% : fill 19% (16/66) · rebond 70% (12/16)
      · −3.0% : fill 7% (7/66) · rebond 67% (4/7)
      · −4.0% : fill 3% (4/66) · rebond 58% (2/4)
      · −5.0% : fill 2% (2/66) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 56% si les 15 1res min sont vertes (88 cas) · 32% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 71% si début vert vs 7% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=90) : tient le vert **71%** · continue >prix actuel 43% ; creux résiduel méd -1.55% (q20 -2.88%) → **SL/trailing à −2.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +2.85% → **scale +1.62% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **7%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.18%** (au-delà de la MAE q10 -5.18%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +3.69%] · haut q95 +3.94% · bas q05 -3.62%
   - 60min (n=160) : retour [-3.45% .. +5.63%] · haut q95 +6.12% · bas q05 -4.56%
   - 2h (n=160) : retour [-4.42% .. +7.83%] · haut q95 +8.96% · bas q05 -5.49%
   - 4h (n=160) : retour [-5.2% .. +8.2%] · haut q95 +10.02% · bas q05 -6.02%
   - 6h (n=160) : retour [-5.31% .. +8.86%] · haut q95 +10.13% · bas q05 -6.26%
   - session (n=160) : retour [-5.14% .. +8.51%] · haut q95 +10.13% · bas q05 -6.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0.6% / strong 6.9%) · base = 12 séances trend-up (n_eff 8.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **47%**. Lecture précoce 30 min : signature présente → 17% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.9% (p75 1.29% / p90 2.02%) · ~4.0 replis/séance, durée méd 30.47 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 20.0 min, n=46)
   - −1.0% → **74%** (reprise méd 17.06 min, n=20)
   - −1.5% → **58%** (reprise méd 13.97 min, n=11)
   - −2.0% → **46%** (reprise méd 31.23 min, n=8)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.02%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +8.69% (q75 +10.68% / q95 +13.17%), MFE méd +10.02% / q90 +13.15%
   - Échelle scale-out : +10.02% (33%) / +12.77% (33%) / +13.15% (34%)
- **DÉSARMER** : repli > **−2.02%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 157.2 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.15% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.81%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.82 · part idiosyncratique 0.17
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 18.8  _(survente)_
- **ADX** : 27.9  _(tendance etablie)_
- **MACD** : hist -4.425  _(pas de croisement recent)_
- **BB** : %B -0.02 · largeur 59.3%
- **ATR** : 8.3 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.211  _(distribution)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 25.0  _(marche directionnel)_
- **MA** : MA20 124.14 · MA50 139.97 · MA200 131.91  _(prix < MA20)_
- **Dist MA** : MA20 -30.6% · MA50 -38.5% · MA200 -34.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (696101 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
