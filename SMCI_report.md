# SMCI

**Generated** : 2026-11-24T01:24:10.721421+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $24.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $24.56 (+1.2% vs entrée) · entrée $24.27 · stop $23.46 · T1 $25.61 · R/R 1.65  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.6 % ≠ (strike 22.0 − spot 24.56)/spot = -10.4 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-23 : 24.56 · ATR Wilder 2.58 (10.52 %)_
- **Swing** : plage **21.31 → 19.32** (-13.23 % a -21.35 % sous la cloture, 0.77 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 18.79-20.71 (A). stop INDICATIF 15.96 (-17.38 % sous le bas ; sous le support 17.25-17.25 (- 0,5 ATR)).
- **Deep** : plage **19.32 → 12.9** (-21.35 % a -47.48 % sous la cloture, 2.48 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 18.79-20.71 (A) ; 17.25-17.25 (C). stop INDICATIF 10.32 (-20.03 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (4.58 ATR sous le plus haut 20 s., RSI(2) 68.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 18.79-20.71 (A, -15.68 %) ; 17.25-17.25 (C, -29.76 %)
- Resistances reelles au-dessus : 27.22-28.5 (A, 10.83 %) ; 28.61-29.9 (A, 16.49 %) ; 29.94-31.19 (A, 21.91 %) ; 31.84-33.07 (A, 29.64 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.63 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1253).
   - exécution **4.597 pt plus bas** dans le cas TYPIQUE (médiane), 13.887 au p90, **15.421 au pire**
   - perte réelle **19.93 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 13.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0402 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.991 % | p01 -10.759 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4015** [0.3306 ; 0.4757] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.2419** [0.199 ; 0.2891] _(largeur 9.0 pt, n_eff 345.7)_
   - deep : **0.2565** [0.2126 ; 0.3044] _(largeur 9.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.16 %** | CVaR **-12.54 %** | vol 5.98 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.97 % contre 6.37 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.95 % vs -17.06 % si l'on extrapolait par √5 _(rapport 1.052 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5383** (β de hausse 1.2025, asymétrie 1.2792) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.678× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 22.3624 sur support (0.44 ATR, 8.948 %) — p(stop avant cible) 0.4984 [0.45 ; 0.55], R/R 3.383, perte reelle 10.115 % (gap inclus), CVaR 20.146 %, EV 0.2566 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1671 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 7.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.498, borne haute 0.551 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 20.15 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.44 ATR (stop 8.948 %) — p(stop avant cible) 0.4984 [0.45 ; 0.55], R/R 3.383, perte reelle 10.115 % (gap inclus), EV 0.2566 % — **REFUSE**
      - refuse : cible atteinte seulement 7.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.498, borne haute 0.551 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 20.15 % > budget 12.00 %
      - ⚠ support DETECTE a 0.44 ATR du spot — compartiment <1, mesure a 47.3 % de casse (IC clusterise [0.443 ; 0.504] sur 1222 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 16.486 %) — p(stop avant cible) 0.27 [0.23 ; 0.32], R/R 1.902, perte reelle 17.994 % (gap inclus), EV 0.0733 % — **REFUSE**
      - refuse : cible atteinte seulement 8.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.96 % > budget 12.00 %
   - 🟢 support a 1.88 ATR (stop 24.827 %) — p(stop avant cible) 0.124 [0.09 ; 0.16], R/R 1.334, perte reelle 25.645 % (gap inclus), EV -0.1236 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 8.2 % x 34.22 % + P(rien) 79.4 % x 0.33 % ne couvrent pas P(stop) 12.4 % x 25.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 10.991 %) — p(stop avant cible) 0.4161 [0.36 ; 0.47], R/R 2.795, perte reelle 12.243 % (gap inclus), EV 0.3189 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.89 % > budget 12.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 13.738 %) — p(stop avant cible) 0.3219 [0.27 ; 0.37], R/R 2.252, perte reelle 15.199 % (gap inclus), EV 0.2689 % — **REFUSE**
      - refuse : cible atteinte seulement 8.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.54 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 27.476 %) — p(stop avant cible) 0.0877 [0.06 ; 0.12], R/R 1.227, perte reelle 27.893 % (gap inclus), EV -0.1421 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 8.2 % x 34.22 % + P(rien) 83.1 % x -0.59 % ne couvrent pas P(stop) 8.8 % x 27.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 30.224 %) — p(stop avant cible) 0.0616 [0.04 ; 0.09], R/R 1.128, perte reelle 30.35 % (gap inclus), EV -0.1989 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 8.2 % x 34.22 % + P(rien) 85.7 % x -1.31 % ne couvrent pas P(stop) 6.2 % x 30.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 32.972 %) — p(stop avant cible) 0.0546 [0.03 ; 0.08], R/R 1.032, perte reelle 33.154 % (gap inclus), EV -0.3123 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 8.2 % x 34.22 % + P(rien) 86.4 % x -1.50 % ne couvrent pas P(stop) 5.5 % x 33.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 38.467 %) — p(stop avant cible) 0.0221 [0.01 ; 0.04], R/R 0.889, perte reelle 38.498 % (gap inclus), EV -0.274 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 8.2 % x 34.22 % + P(rien) 89.6 % x -2.48 % ne couvrent pas P(stop) 2.2 % x 38.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 43.962 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.771, perte reelle 44.361 % (gap inclus), EV -0.2127 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.6 % x -3.18 % ne couvrent pas P(stop) 0.2 % x 44.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 49.458 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.663, perte reelle 51.59 % (gap inclus), EV -0.222 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.7 % x -3.21 % ne couvrent pas P(stop) 0.1 % x 51.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 54.953 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.614, perte reelle 55.704 % (gap inclus), EV -0.225 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.7 % x -3.22 % ne couvrent pas P(stop) 0.1 % x 55.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 60.448 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.566, perte reelle 60.448 % (gap inclus), EV -0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.8 % x -3.28 % ne couvrent pas P(stop) 0.0 % x 60.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 65.943 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.519, perte reelle 65.943 % (gap inclus), EV -0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.8 % x -3.28 % ne couvrent pas P(stop) 0.0 % x 65.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 71.439 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.479, perte reelle 71.439 % (gap inclus), EV -0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.8 % x -3.28 % ne couvrent pas P(stop) 0.0 % x 71.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 76.934 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.445, perte reelle 76.934 % (gap inclus), EV -0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.8 % x -3.28 % ne couvrent pas P(stop) 0.0 % x 76.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 82.429 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.415, perte reelle 82.429 % (gap inclus), EV -0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.8 % x -3.28 % ne couvrent pas P(stop) 0.0 % x 82.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 87.925 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.389, perte reelle 87.925 % (gap inclus), EV -0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 8.2 % x 34.22 % + P(rien) 91.8 % x -3.28 % ne couvrent pas P(stop) 0.0 % x 87.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 24.56, ATR14 2.6993 (10.991 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.35 ATR = 3.847 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.55 % | 24.425 | 90.94 % | 93.75 % | 95.06 % | 95.65 % | 96.85 % | 97.95 % |
| 0.1 ATR | 1.099 % | 24.2901 | 82.48 % | 87.8 % | 89.61 % | 91.61 % | 93.39 % | 95.28 % |
| 0.15 ATR | 1.649 % | 24.1551 | 75.53 % | 82.86 % | 85.57 % | 88.78 % | 91.16 % | 94.05 % |
| 0.2 ATR | 2.198 % | 24.0201 | 68.68 % | 78.12 % | 81.23 % | 86.45 % | 89.74 % | 92.81 % |
| 0.25 ATR | 2.748 % | 23.8852 | 62.44 % | 73.49 % | 76.99 % | 83.11 % | 87.8 % | 91.27 % |
| 0.35 ATR | 3.847 % | 23.6152 | 49.95 % | 64.31 % | 70.53 % | 78.16 % | 83.74 % | 88.91 % |
| 0.5 ATR | 5.495 % | 23.2104 | 34.84 % | 50.5 % | 59.43 % | 69.77 % | 77.95 % | 84.5 % |
| 0.75 ATR | 8.243 % | 22.5355 | 17.42 % | 33.97 % | 44.2 % | 56.52 % | 67.89 % | 76.69 % |
| 1.0 ATR | 10.991 % | 21.8607 | 7.85 % | 21.88 % | 31.08 % | 44.99 % | 58.64 % | 70.12 % |
| 1.25 ATR | 13.738 % | 21.1859 | 3.73 % | 15.32 % | 22.91 % | 34.38 % | 49.49 % | 62.53 % |
| 1.5 ATR | 16.486 % | 20.5111 | 1.51 % | 9.98 % | 16.85 % | 26.79 % | 43.19 % | 56.37 % |
| 2.0 ATR | 21.981 % | 19.1614 | 0.3 % | 3.73 % | 8.88 % | 16.89 % | 31.3 % | 45.48 % |
| 2.5 ATR | 27.476 % | 17.8118 | 0.2 % | 1.51 % | 4.44 % | 10.31 % | 21.14 % | 33.78 % |
| 3.0 ATR | 32.972 % | 16.4621 | 0.2 % | 1.21 % | 2.62 % | 5.97 % | 15.04 % | 25.98 % |
| 4.0 ATR | 43.962 % | 13.7629 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.13 % | 16.12 % |
| 6.0 ATR | 65.943 % | 8.3643 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.95 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.94 ATR | 1.07 ATR | 1.50 ATR | 1.90 ATR |
| **3 s.** | 0.28 ATR | 0.66 ATR | 0.74 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.93 ATR | 2.44 ATR |
| **5 s.** | 0.41 ATR | 0.89 ATR | 1.00 ATR | 1.29 ATR | 1.59 ATR | 1.84 ATR | 2.54 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.24 ATR | 1.43 ATR | 1.93 ATR | 2.31 ATR | 2.59 ATR | 3.73 ATR | 5.03 ATR |
| **20 s.** | 0.81 ATR | 1.79 ATR | 2.02 ATR | 2.55 ATR | 3.10 ATR | 3.61 ATR | 5.20 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.399 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.583–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (8.243 %, prix 22.5355), p(touche) 33.97 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.737–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (8.243 %, prix 22.5355), p(touche) 44.2 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (10.991 %, prix 21.8606), p(touche) 44.99 % (en stress 93.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.428–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (16.486 %, prix 20.511), p(touche) 43.19 % (en stress 95.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.021 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 12.4 | bear 5.8 | side 81.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.203% → cible +5.562% / stop −3.337%, p_fill 78%, n_eff≈82.0) : P(cible|rempli) **10%** · **EV/risk -0.110** (×p_fill ; si rempli -0.47% du capital)
  - **swing** (entrée dip −2.639% → cible +12.621% / stop −11.289%, p_fill 65%, n_eff≈75.8) : P(cible|rempli) **22%** · **EV/risk -0.009** (×p_fill ; si rempli -0.16% du capital)
  - **deep** (entrée dip −4.084% → cible +18.117% / stop −17.188%, p_fill 61%, n_eff≈68.6) : P(cible|rempli) **26%** · **EV/risk +0.057** (×p_fill ; si rempli +1.60% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→57% · +3.0%→40% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.72% (p90 9.37%) · excursion haute méd. +2.42% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.884% vs midi 1.151% vs clôture 1.47% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.659% ; recovery-V 28%
- **σ réalisé intraday** 3.524% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 33.7346 (VA 33.3821–34.0871 ; dernier close 32.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 38% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −2.79%) · haut méd +0.93% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.55%) · haut méd +1.01% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.65% (p90 −3.98%) · haut méd +1.23% · range méd 3.58%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.46%) · haut méd +1.48% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (116/159) · gap 42% · délai 0.0min · rebond 49% (64/116) (MFE +0.98%)
   - −1.0% : fill 30min 58% · séance 70% (109/159) · gap 38% · délai 0.0min · rebond 51% (60/109) (MFE +1.09%)
   - −1.5% : fill 30min 52% · séance 66% (100/159) · gap 28% · délai 0.0min · rebond 56% (62/100) (MFE +1.13%)
   - −2.0% : fill 30min 47% · séance 59% (87/159) · gap 23% · délai 0.1min · rebond 56% (54/87) (MFE +1.2%)
   - −3.0% : fill 30min 34% · séance 48% (73/159) · gap 11% · délai 2.7min · rebond 62% (43/73) (MFE +1.34%)
   - −4.0% : fill 30min 21% · séance 35% (54/159) · gap 5% · délai 12.5min · rebond 72% (36/54) (MFE +1.72%)
   - −5.0% : fill 30min 15% · séance 29% (44/159) · gap 2% · délai 21.5min · rebond 74% (31/44) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −2.8%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.84%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.25%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=876 jambes) : jambe baissière méd −1.19% (p90 −2.78%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 98% (68/70) · rebond 39% (32/68)
      · −2.0% : fill 96% (64/70) · rebond 57% (37/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (33/58)
      · −4.0% : fill 64% (44/70) · rebond 70% (29/44)
      · −5.0% : fill 53% (36/70) · rebond 71% (24/36)
   - **flat** (14 séances) :
      · −1.0% : fill 90% (13/14) · rebond 84% (10/13)
      · −2.0% : fill 57% (6/14) · rebond 47% (4/6)
      · −3.0% : fill 20% (3/14) · rebond 43% (2/3)
      · −4.0% : fill 7% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 36% (28/75) · rebond 66% (18/28)
      · −2.0% : fill 21% (17/75) · rebond 58% (13/17)
      · −3.0% : fill 13% (12/75) · rebond 78% (8/12)
      · −4.0% : fill 11% (9/75) · rebond 81% (6/9)
      · −5.0% : fill 10% (8/75) · rebond 91% (7/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 67% si les 15 1res min sont vertes (78 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 43% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **83%** · continue >prix actuel 59% ; creux résiduel méd -1.33% (q20 -2.94%) → **SL/trailing à −2.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.72% → **scale +1.67% / runner +2.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.93%** (au-delà de la MAE q10 -3.93%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.1%] · haut q95 +5.04% · bas q05 -5.27%
   - 60min (n=160) : retour [-4.12% .. +4.96%] · haut q95 +6.21% · bas q05 -5.43%
   - 2h (n=160) : retour [-4.55% .. +5.52%] · haut q95 +7.12% · bas q05 -5.93%
   - 4h (n=160) : retour [-4.91% .. +6.39%] · haut q95 +7.24% · bas q05 -6.41%
   - 6h (n=160) : retour [-5.14% .. +6.41%] · haut q95 +7.8% · bas q05 -6.61%
   - session (n=160) : retour [-6.33% .. +6.37%] · haut q95 +7.95% · bas q05 -6.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.59%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.3  _(momentum baissier)_
- **ADX** : 30.6  _(tendance etablie)_
- **MACD** : hist -0.272  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 56.6%
- **ATR** : 2.7 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.241  _(distribution)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 45.8  _(transition)_
- **MA** : MA20 28.49 · MA50 34.75 · MA200 32.32  _(prix < MA20)_
- **Dist MA** : MA20 -13.8% · MA50 -29.3% · MA200 -24.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (681929 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
