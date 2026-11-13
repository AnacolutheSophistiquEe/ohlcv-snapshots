# HOOD

**Generated** : 2026-11-13T01:29:28.333351+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $81.37  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $81.37 (+1.4% vs entrée) · entrée $80.26 · stop $77.85 · T1 $82.75 · R/R 1.03  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -3.0 % ≠ (strike 82.0 − spot 81.37)/spot = +0.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 81.37 · ATR Wilder 5.2 (6.39 %)_
- **Swing** : plage **75.49 → 70.81** (-7.23 % a -12.98 % sous la cloture, 0.9 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 72.79-74.59 (A) ; 69.93-72.25 (A). stop INDICATIF 64.31 (-9.18 % sous le bas ; sous le support 66.91-69.22 (- 0,5 ATR)).
- **Deep** : plage **70.81 → 61.08** (-12.98 % a -24.94 % sous la cloture, 1.87 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 69.93-72.25 (A) ; 66.91-69.22 (A) ; 62.63-63.51 (B). stop INDICATIF 55.87 (-8.52 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (4.43 ATR sous le plus haut 20 s., RSI(2) 34.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 78.93-79.57 (A, -2.21 %) ; 75.51-77.87 (A, -4.3 %) ; 72.79-74.59 (A, -8.33 %) ; 69.93-72.25 (A, -11.21 %) ; 66.91-69.22 (A, -14.93 %) ; 62.63-63.51 (B, -21.94 %)
- Resistances reelles au-dessus : 84.75-84.75 (C, 4.15 %) ; 88.6-90.7 (A, 8.89 %) ; 91.44-93.36 (A, 12.38 %) ; 94.4-96.59 (A, 16.01 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.42 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.12 %)** : le gap seul le franchit 0.559 % des séances (7 fois sur 1253).
   - exécution **1.999 pt plus bas** dans le cas TYPIQUE (médiane), 6.47 au p90, **8.665 au pire**
   - perte réelle **12.322 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 9.12 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0179 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.493 % | p01 -6.925 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2755** [0.2131 ; 0.3454] _(largeur 13.2 pt, n_eff 173.1)_
   - swing : **0.4837** [0.4313 ; 0.5363] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4542** [0.4023 ; 0.5069] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.19 %** | CVaR **-9.08 %** | vol 4.33 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.08 % contre 4.53 % aujourd'hui, rapport 0.46)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.4 % vs -14.64 % si l'on extrapolait par √5 _(rapport 0.983 ; < 1 = le √5 surestime)_
- **β de baisse : 1.79** (β de hausse 1.6364, asymétrie 1.0939) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.281× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 74.0212 sur sr_based (0.99 ATR, 9.031 %) — p(stop avant cible) 0.4966 [0.44 ; 0.55], R/R 3.799, perte reelle 9.544 % (gap inclus), CVaR 12.43 %, EV -0.0557 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9659 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 12.43 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.99 ATR (stop 9.031 %) — p(stop avant cible) 0.4966 [0.44 ; 0.55], R/R 3.799, perte reelle 9.544 % (gap inclus), EV -0.0557 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 1.1 % x 36.26 % + P(rien) 49.3 % x 8.73 % ne couvrent pas P(stop) 49.7 % x 9.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.38 ATR (stop 11.402 %) — p(stop avant cible) 0.3779 [0.33 ; 0.43], R/R 3.024, perte reelle 11.988 % (gap inclus), EV 0.0874 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.45 % > budget 12.00 %
   - 🔴 support a 2.44 ATR (stop 17.908 %) — p(stop avant cible) 0.1251 [0.09 ; 0.16], R/R 1.992, perte reelle 18.197 % (gap inclus), EV 0.4042 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.63 % > budget 12.00 %
      - ⚠ support DETECTE a 0.89 ATR du spot — compartiment <1, mesure a 50.7 % de casse (IC clusterise [0.471 ; 0.542] sur 1138 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 3.58 ATR (stop 24.919 %) — p(stop avant cible) 0.0278 [0.01 ; 0.05], R/R 1.424, perte reelle 25.463 % (gap inclus), EV 0.5828 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.85 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.531 %) — p(stop avant cible) 0.9188 [0.89 ; 0.94], R/R 20.989, perte reelle 1.727 % (gap inclus), EV -0.3808 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 20.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.919, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.5 % x 36.26 % + P(rien) 7.6 % x 13.33 % ne couvrent pas P(stop) 91.9 % x 1.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.062 %) — p(stop avant cible) 0.8046 [0.76 ; 0.84], R/R 10.8, perte reelle 3.357 % (gap inclus), EV -0.1213 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.805, borne haute 0.844 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 1.0 % x 36.26 % + P(rien) 18.6 % x 12.00 % ne couvrent pas P(stop) 80.5 % x 3.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.99 ATR (stop 7.892 %) — p(stop avant cible) 0.5632 [0.51 ; 0.61], R/R 4.307, perte reelle 8.418 % (gap inclus), EV -0.3018 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.563, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 1.1 % x 36.26 % + P(rien) 42.6 % x 9.52 % ne couvrent pas P(stop) 56.3 % x 8.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.38 ATR (stop 10.263 %) — p(stop avant cible) 0.4348 [0.38 ; 0.49], R/R 3.355, perte reelle 10.808 % (gap inclus), EV -0.0218 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 1.1 % x 36.26 % + P(rien) 55.5 % x 7.75 % ne couvrent pas P(stop) 43.5 % x 10.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 12.246 %) — p(stop avant cible) 0.3364 [0.29 ; 0.39], R/R 2.827, perte reelle 12.825 % (gap inclus), EV 0.2045 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.92 % > budget 12.00 %
   - 🔴 grid_snapped a 2.44 ATR (stop 16.769 %) — p(stop avant cible) 0.1626 [0.13 ; 0.20], R/R 2.12, perte reelle 17.103 % (gap inclus), EV 0.3189 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.85 % > budget 12.00 %
   - 🟢 grid_snapped a 3.58 ATR (stop 23.78 %) — p(stop avant cible) 0.0319 [0.02 ; 0.05], R/R 1.495, perte reelle 24.256 % (gap inclus), EV 0.5834 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.59 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 27.554 %) — p(stop avant cible) 0.0223 [0.01 ; 0.04], R/R 1.298, perte reelle 27.923 % (gap inclus), EV 0.587 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.48 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.615 %) — p(stop avant cible) 0.0176 [0.01 ; 0.04], R/R 1.178, perte reelle 30.782 % (gap inclus), EV 0.5888 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.90 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.677 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.066, perte reelle 34.003 % (gap inclus), EV 0.6824 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.20 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.738 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.984, perte reelle 36.862 % (gap inclus), EV 0.6962 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.95 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.8 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.911, perte reelle 39.8 % (gap inclus), EV 0.7101 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 42.862 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.846, perte reelle 42.862 % (gap inclus), EV 0.7119 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 45.923 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.789, perte reelle 45.923 % (gap inclus), EV 0.7119 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.66 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 48.985 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.74, perte reelle 48.985 % (gap inclus), EV 0.7119 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.66 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 81.37, ATR14 4.9824 (6.123 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.371 ATR = 2.272 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.306 % | 81.1209 | 93.15 % | 95.36 % | 96.27 % | 96.76 % | 97.26 % | 98.05 % |
| 0.1 ATR | 0.612 % | 80.8718 | 85.6 % | 90.73 % | 92.43 % | 94.03 % | 94.92 % | 96.41 % |
| 0.15 ATR | 0.918 % | 80.6227 | 77.95 % | 85.79 % | 88.5 % | 90.9 % | 92.89 % | 95.07 % |
| 0.2 ATR | 1.225 % | 80.3735 | 71.4 % | 80.44 % | 84.26 % | 87.66 % | 90.65 % | 93.22 % |
| 0.25 ATR | 1.531 % | 80.1244 | 64.35 % | 74.7 % | 79.62 % | 84.13 % | 88.01 % | 90.86 % |
| 0.35 ATR | 2.143 % | 79.6262 | 52.17 % | 65.62 % | 72.45 % | 78.56 % | 84.04 % | 87.99 % |
| 0.5 ATR | 3.062 % | 78.8788 | 36.76 % | 53.63 % | 61.65 % | 69.57 % | 77.24 % | 82.34 % |
| 0.75 ATR | 4.592 % | 77.6332 | 19.34 % | 36.19 % | 46.42 % | 56.62 % | 66.46 % | 73.2 % |
| 1.0 ATR | 6.123 % | 76.3877 | 9.26 % | 23.49 % | 33.6 % | 45.1 % | 56.0 % | 65.81 % |
| 1.25 ATR | 7.654 % | 75.1421 | 4.83 % | 14.82 % | 23.01 % | 34.98 % | 48.48 % | 59.65 % |
| 1.5 ATR | 9.185 % | 73.8965 | 2.52 % | 10.08 % | 16.65 % | 27.91 % | 41.77 % | 54.0 % |
| 2.0 ATR | 12.246 % | 71.4053 | 0.4 % | 3.73 % | 7.16 % | 15.47 % | 31.0 % | 44.25 % |
| 2.5 ATR | 15.308 % | 68.9141 | 0.0 % | 1.41 % | 3.73 % | 8.19 % | 22.46 % | 35.11 % |
| 3.0 ATR | 18.369 % | 66.423 | 0.0 % | 0.5 % | 2.12 % | 4.85 % | 15.45 % | 27.1 % |
| 4.0 ATR | 24.492 % | 61.4406 | 0.0 % | 0.3 % | 0.61 % | 1.82 % | 6.0 % | 15.3 % |
| 6.0 ATR | 36.738 % | 51.4759 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 5.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.97 ATR | 1.10 ATR | 1.51 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.01 ATR | 1.20 ATR | 1.37 ATR | 1.85 ATR | 2.31 ATR |
| **5 s.** | 0.41 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.62 ATR | 1.82 ATR | 2.38 ATR | 2.98 ATR |
| **10 s.** | 0.55 ATR | 1.20 ATR | 1.38 ATR | 1.91 ATR | 2.35 ATR | 2.67 ATR | 3.58 ATR | 4.43 ATR |
| **20 s.** | 0.70 ATR | 1.71 ATR | 1.96 ATR | 2.63 ATR | 3.18 ATR | 3.60 ATR | 5.03 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.42 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.592 %, prix 77.6335), p(touche) 36.19 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.778–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.123 %, prix 76.3877), p(touche) 33.6 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.002–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.654 %, prix 75.1419), p(touche) 34.98 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.38–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.185 %, prix 73.8962), p(touche) 41.77 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.962–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.246 %, prix 71.4054), p(touche) 44.25 % (en stress 97.96 %)  ✅ optimum identifie (61.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.007 | EV/share : $-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.4 | bear 70.4 | side 14.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.361% → cible +3.104% / stop −3.0%, p_fill 68%, n_eff≈73.0) : P(cible|rempli) **28%** · **EV/risk +0.003** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −2.997% → cible +7.057% / stop −6.312%, p_fill 52%, n_eff≈60.6) : P(cible|rempli) **38%** · **EV/risk +0.017** (×p_fill ; si rempli +0.20% du capital)
  - **deep** (entrée dip −4.624% → cible +19.577% / stop −9.788%, p_fill 50%, n_eff≈54.2) : P(cible|rempli) **21%** · **EV/risk +0.074** (×p_fill ; si rempli +1.45% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.75 · part idiosyncratique 0.25
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 33.3  _(momentum baissier)_
- **ADX** : 29.4  _(tendance etablie)_
- **MACD** : hist -0.126  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 31.7%
- **ATR** : 4.98 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.052  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 45.1  _(transition)_
- **MA** : MA20 89.47 · MA50 104.19 · MA200 91.53  _(prix < MA20)_
- **Dist MA** : MA20 -9.1% · MA50 -21.9% · MA200 -11.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (701180 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
