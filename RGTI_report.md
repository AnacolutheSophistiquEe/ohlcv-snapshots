# RGTI

**Generated** : 2026-10-26T01:25:44.636681+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $11.52  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $11.52 (+0.9% vs entrée) · entrée $11.42 · stop $11.18 · T1 $11.81 · R/R 1.63  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.095 _(réel 5 s)_ (GBM 0.037) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.08% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -50 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 11.52 · ATR Wilder 0.8125 (7.05 %)_
- **Swing** : plage **10.53 → 10.12** (-8.55 % a -12.11 % sous la cloture, 0.51 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 10.05-10.31 (A). stop INDICATIF 9.09 (-10.18 % sous le bas ; sous le support 9.5-9.74 (- 0,5 ATR)).
- **Deep** : plage **10.12 → 9.12** (-12.11 % a -20.8 % sous la cloture, 1.23 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 10.05-10.31 (A) ; 9.5-9.74 (C) ; 8.92-9.14 (A). stop INDICATIF 7.94 (-12.94 % sous le bas ; sous le support 8.35-8.45 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.38 ATR sous le plus haut 20 s., RSI(2) 31.4. Limite **11.11** (seance suivante), stop catastrophe 7.86, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 10.71-11.11 (A, -3.56 %) ; 10.05-10.31 (A, -10.5 %) ; 9.5-9.74 (C, -15.45 %) ; 8.92-9.14 (A, -20.66 %) ; 8.35-8.45 (B, -26.65 %) ; 6.86-7.03 (B, -39.02 %)
- Resistances reelles au-dessus : 11.87-12.08 (B, 3.04 %) ; 12.34-12.53 (A, 7.12 %) ; 12.75-13.13 (A, 10.68 %) ; 13.41-13.61 (A, 16.41 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.69 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.82 %)** : le gap seul le franchit 1.116 % des séances (14 fois sur 1254).
   - exécution **2.867 pt plus bas** dans le cas TYPIQUE (médiane), 8.119 au p90, **22.393 au pire**
   - perte réelle **13.376 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 8.82 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0509 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 14 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.118 % | p01 -8.97 % | pire -31.213 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5117** [0.4376 ; 0.5855] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5496** [0.4969 ; 0.6015] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5366** [0.4839 ; 0.5887] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.84 %** | CVaR **-11.15 %** | vol 6.79 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.34 % contre 6.23 % aujourd'hui, rapport 3.10)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.75 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8364** (β de hausse 2.0059, asymétrie 0.9155) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.451× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 10.5317 sur atr_grid (1.25 ATR, 8.579 %) — p(stop avant cible) 0.6566 [0.61 ; 0.71], R/R 3.249, perte reelle 8.76 % (gap inclus), CVaR 10.85 %, EV -1.045 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4982 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.657, borne haute 0.705 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.52 ATR (stop 7.169 %) — p(stop avant cible) 0.7001 [0.65 ; 0.75], R/R 3.908, perte reelle 7.282 % (gap inclus), EV -0.77 % — **REFUSE**
      - refuse : cible atteinte seulement 11.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.700, borne haute 0.747 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 11.1 % x 28.46 % + P(rien) 18.9 % x 6.20 % ne couvrent pas P(stop) 70.0 % x 7.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 10.295 %) — p(stop avant cible) 0.6192 [0.57 ; 0.67], R/R 2.72, perte reelle 10.463 % (gap inclus), EV -1.6976 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.619, borne haute 0.669 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.70 %) : P(cible) 12.3 % x 28.46 % + P(rien) 25.8 % x 4.97 % ne couvrent pas P(stop) 61.9 % x 10.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.716 %) — p(stop avant cible) 0.9227 [0.89 ; 0.95], R/R 15.722, perte reelle 1.81 % (gap inclus), EV -0.0685 % — **REFUSE**
      - refuse : cible atteinte seulement 4.6 % du temps (< 15 %) meme a 10 seances : le R/R de 15.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.923, borne haute 0.947 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 4.6 % x 28.46 % + P(rien) 3.1 % x 9.26 % ne couvrent pas P(stop) 92.3 % x 1.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.52 ATR (stop 5.618 %) — p(stop avant cible) 0.7688 [0.72 ; 0.81], R/R 4.961, perte reelle 5.736 % (gap inclus), EV -0.7678 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 9.3 % x 28.46 % + P(rien) 13.8 % x 7.12 % ne couvrent pas P(stop) 76.9 % x 5.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 8.579 %) — p(stop avant cible) 0.6566 [0.61 ; 0.71], R/R 3.249, perte reelle 8.76 % (gap inclus), EV -1.045 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.657, borne haute 0.705 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 11.8 % x 28.46 % + P(rien) 22.6 % x 6.02 % ne couvrent pas P(stop) 65.7 % x 8.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 12.011 %) — p(stop avant cible) 0.5409 [0.49 ; 0.59], R/R 2.329, perte reelle 12.222 % (gap inclus), EV -1.6046 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.541, borne haute 0.593 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 13.1 % x 28.46 % + P(rien) 32.8 % x 3.90 % ne couvrent pas P(stop) 54.1 % x 12.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 13.726 %) — p(stop avant cible) 0.4494 [0.40 ; 0.50], R/R 2.042, perte reelle 13.938 % (gap inclus), EV -1.258 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 13.7 % x 28.46 % + P(rien) 41.4 % x 2.70 % ne couvrent pas P(stop) 44.9 % x 13.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 15.442 %) — p(stop avant cible) 0.3848 [0.33 ; 0.44], R/R 1.817, perte reelle 15.666 % (gap inclus), EV -1.217 % — **REFUSE**
      - refuse : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 14.2 % x 28.46 % + P(rien) 47.3 % x 1.63 % ne couvrent pas P(stop) 38.5 % x 15.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 17.158 %) — p(stop avant cible) 0.3132 [0.27 ; 0.36], R/R 1.629, perte reelle 17.472 % (gap inclus), EV -1.2608 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 14.6 % x 28.46 % + P(rien) 54.1 % x 0.12 % ne couvrent pas P(stop) 31.3 % x 17.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 18.874 %) — p(stop avant cible) 0.2726 [0.23 ; 0.32], R/R 1.488, perte reelle 19.128 % (gap inclus), EV -1.1308 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 15.0 % x 28.46 % + P(rien) 57.7 % x -0.34 % ne couvrent pas P(stop) 27.3 % x 19.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 20.59 %) — p(stop avant cible) 0.2135 [0.17 ; 0.26], R/R 1.353, perte reelle 21.042 % (gap inclus), EV -1.0166 % — **REFUSE**
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 15.4 % x 28.46 % + P(rien) 63.2 % x -1.45 % ne couvrent pas P(stop) 21.3 % x 21.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 24.021 %) — p(stop avant cible) 0.1348 [0.10 ; 0.17], R/R 1.174, perte reelle 24.237 % (gap inclus), EV -0.9367 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 15.5 % x 28.46 % + P(rien) 71.0 % x -2.93 % ne couvrent pas P(stop) 13.5 % x 24.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 27.453 %) — p(stop avant cible) 0.0735 [0.05 ; 0.10], R/R 1.028, perte reelle 27.688 % (gap inclus), EV -0.8216 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 15.9 % x 28.46 % + P(rien) 76.8 % x -4.31 % ne couvrent pas P(stop) 7.3 % x 27.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 30.884 %) — p(stop avant cible) 0.0438 [0.03 ; 0.07], R/R 0.917, perte reelle 31.048 % (gap inclus), EV -0.734 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 15.9 % x 28.46 % + P(rien) 79.7 % x -4.90 % ne couvrent pas P(stop) 4.4 % x 31.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 34.316 %) — p(stop avant cible) 0.0236 [0.01 ; 0.04], R/R 0.815, perte reelle 34.919 % (gap inclus), EV -0.6588 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 16.0 % x 28.46 % + P(rien) 81.7 % x -5.36 % ne couvrent pas P(stop) 2.4 % x 34.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 37.748 %) — p(stop avant cible) 0.0149 [0.01 ; 0.03], R/R 0.748, perte reelle 38.061 % (gap inclus), EV -0.656 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 16.0 % x 28.46 % + P(rien) 82.5 % x -5.61 % ne couvrent pas P(stop) 1.5 % x 38.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 41.179 %) — p(stop avant cible) 0.007 [0.00 ; 0.02], R/R 0.69, perte reelle 41.262 % (gap inclus), EV -0.5864 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 16.1 % x 28.46 % + P(rien) 83.2 % x -5.85 % ne couvrent pas P(stop) 0.7 % x 41.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 44.611 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.628, perte reelle 45.299 % (gap inclus), EV -0.5922 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 16.1 % x 28.46 % + P(rien) 83.5 % x -5.93 % ne couvrent pas P(stop) 0.5 % x 45.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 48.043 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.592, perte reelle 48.043 % (gap inclus), EV -0.5947 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 16.1 % x 28.46 % + P(rien) 83.7 % x -6.01 % ne couvrent pas P(stop) 0.3 % x 48.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 51.474 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.545, perte reelle 52.262 % (gap inclus), EV -0.6054 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 16.1 % x 28.46 % + P(rien) 83.7 % x -6.01 % ne couvrent pas P(stop) 0.3 % x 52.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 54.906 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.5, perte reelle 56.967 % (gap inclus), EV -0.5863 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 16.1 % x 28.46 % + P(rien) 83.7 % x -6.01 % ne couvrent pas P(stop) 0.2 % x 56.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 11.52, ATR14 0.7906 (6.863 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.408 ATR = 2.8 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.343 % | 11.4805 | 92.05 % | 94.36 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.686 % | 11.4409 | 86.32 % | 90.94 % | 92.44 % | 94.95 % | 95.94 % | 97.44 % |
| 0.15 ATR | 1.029 % | 11.4014 | 80.89 % | 87.21 % | 89.01 % | 92.02 % | 94.01 % | 96.1 % |
| 0.2 ATR | 1.373 % | 11.3619 | 74.14 % | 82.58 % | 85.38 % | 88.69 % | 91.47 % | 94.46 % |
| 0.25 ATR | 1.716 % | 11.3223 | 68.11 % | 78.35 % | 81.45 % | 85.66 % | 88.93 % | 92.51 % |
| 0.35 ATR | 2.402 % | 11.2433 | 55.53 % | 68.58 % | 73.89 % | 79.6 % | 84.57 % | 89.64 % |
| 0.5 ATR | 3.432 % | 11.1247 | 41.25 % | 57.1 % | 64.92 % | 71.82 % | 79.19 % | 85.33 % |
| 0.75 ATR | 5.147 % | 10.927 | 21.83 % | 39.17 % | 50.2 % | 59.19 % | 70.86 % | 78.97 % |
| 1.0 ATR | 6.863 % | 10.7294 | 9.76 % | 24.27 % | 33.87 % | 46.97 % | 62.03 % | 72.51 % |
| 1.25 ATR | 8.579 % | 10.5317 | 4.12 % | 14.8 % | 23.89 % | 37.17 % | 52.89 % | 65.03 % |
| 1.5 ATR | 10.295 % | 10.334 | 1.81 % | 7.35 % | 13.81 % | 25.66 % | 43.15 % | 56.92 % |
| 2.0 ATR | 13.726 % | 9.9387 | 0.4 % | 1.81 % | 4.23 % | 11.01 % | 25.48 % | 40.62 % |
| 2.5 ATR | 17.158 % | 9.5434 | 0.1 % | 0.4 % | 1.31 % | 4.65 % | 14.72 % | 28.31 % |
| 3.0 ATR | 20.59 % | 9.1481 | 0.0 % | 0.2 % | 0.5 % | 1.72 % | 7.41 % | 16.62 % |
| 4.0 ATR | 27.453 % | 8.3574 | 0.0 % | 0.1 % | 0.2 % | 0.51 % | 1.93 % | 4.0 % |
| 6.0 ATR | 41.179 % | 6.7761 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.61 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.75 ATR | 0.83 ATR | 1.02 ATR | 1.22 ATR | 1.35 ATR | 1.70 ATR | 1.96 ATR |
| **5 s.** | 0.44 ATR | 0.94 ATR | 1.05 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.08 ATR | 2.47 ATR |
| **10 s.** | 0.63 ATR | 1.32 ATR | 1.45 ATR | 1.79 ATR | 2.02 ATR | 2.25 ATR | 2.82 ATR | 3.44 ATR |
| **20 s.** | 0.90 ATR | 1.71 ATR | 1.87 ATR | 2.31 ATR | 2.64 ATR | 2.85 ATR | 3.52 ATR | 3.92 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.461–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.432 %, prix 11.1246), p(touche) 41.25 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (64.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.669–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.147 %, prix 10.9271), p(touche) 39.17 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.83–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.863 %, prix 10.7294), p(touche) 33.87 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.05–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.579 %, prix 10.5317), p(touche) 37.17 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.453–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.295 %, prix 10.334), p(touche) 43.15 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (71.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.866–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.726 %, prix 9.9388), p(touche) 40.62 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : $0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 — | T3 —
- Kelly (position) : f* 0.053 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 61.0 | side 34.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.891% → cible +3.462% / stop −2.078%, p_fill 78%, n_eff≈84.1) : P(cible|rempli) **20%** · **EV/risk -0.095** (×p_fill ; si rempli -0.25% du capital)
  - **swing** (entrée dip −1.957% → cible +10.239% / stop −7.0%, p_fill 77%, n_eff≈90.1) : P(cible|rempli) **26%** · **EV/risk -0.168** (×p_fill ; si rempli -1.52% du capital)
  - **deep** (entrée dip −3.025% → cible +11.452% / stop −10.616%, p_fill 76%, n_eff≈84.7) : P(cible|rempli) **28%** · **EV/risk -0.279** (×p_fill ; si rempli -3.90% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→74% · +2.0%→62% · +3.0%→45% · +5.0%→30% · +8.0%→10%
- Range intraday médian 6.39% (p90 11.03%) · excursion haute méd. +2.64% / basse méd. −2.45%
- Profil de vol intra : ouverture 4.544% vs midi 1.307% vs clôture 1.583% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.493% ; recovery-V 29%
- **σ réalisé intraday** 3.543% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 69% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 11.4051 (VA 11.2514–11.4461 ; dernier close 11.515)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 64% · **stop −4.84%** sous le fill (sous le bruit) · cible +1.64% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 58% (gap-down >1% 42% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.72%) · haut méd +1.04% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.23% (p90 −3.5%) · haut méd +1.39% · range méd 3.07%
- Excursion ouverture 30min (n=160) : bas méd −1.46% (p90 −4.21%) · haut méd +1.57% · range méd 3.46%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −4.91%) · haut méd +1.85% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 11.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 83% (132/159) · gap 49% · délai 0.0min · rebond 56% (80/132) (MFE +1.37%)
   - −1.0% : fill 30min 65% · séance 76% (121/159) · gap 42% · délai 0.0min · rebond 62% (76/121) (MFE +1.41%)
   - −1.5% : fill 30min 60% · séance 68% (112/159) · gap 31% · délai 0.0min · rebond 64% (71/112) (MFE +1.58%)
   - −2.0% : fill 30min 54% · séance 62% (102/159) · gap 28% · délai 0.0min · rebond 64% (65/102) (MFE +1.78%)
   - −3.0% : fill 30min 37% · séance 49% (88/159) · gap 11% · délai 2.6min · rebond 64% (61/88) (MFE +1.71%)
   - −4.0% : fill 30min 26% · séance 39% (67/159) · gap 6% · délai 11.9min · rebond 66% (48/67) (MFE +1.75%)
   - −5.0% : fill 30min 10% · séance 28% (53/159) · gap 1% · délai 37.8min · rebond 64% (35/53) (MFE +1.64%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.69%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.55% (p90 −2.09%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −2.13%) → stop au-delà de −1.42% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1023 jambes) : jambe baissière méd −1.27% (p90 −2.97%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (82 séances) :
      · −1.0% : fill 94% (78/82) · rebond 57% (45/78)
      · −2.0% : fill 87% (72/82) · rebond 62% (44/72)
      · −3.0% : fill 73% (65/82) · rebond 62% (43/65)
      · −4.0% : fill 63% (52/82) · rebond 61% (36/52)
      · −5.0% : fill 45% (42/82) · rebond 60% (26/42)
   - **flat** (16 séances) :
      · −1.0% : fill 86% (14/16) · rebond 83% (12/14)
      · −2.0% : fill 55% (10/16) · rebond 92% (9/10)
      · −3.0% : fill 21% (5/16) · rebond 92% (4/5)
      · −4.0% : fill 14% (4/16) · rebond 87% (3/4)
      · −5.0% : fill 8% (3/16) · rebond 100% (3/3)
   - **gap-up** (61 séances) :
      · −1.0% : fill 47% (29/61) · rebond 65% (19/29)
      · −2.0% : fill 29% (20/61) · rebond 60% (12/20)
      · −3.0% : fill 24% (18/61) · rebond 65% (14/18)
      · −4.0% : fill 13% (11/61) · rebond 91% (9/11)
      · −5.0% : fill 9% (8/61) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (83 cas) · 22% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 7% si rouge (base 44% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 47% ; creux résiduel méd -1.47% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.76% / q75 +3.11% → **scale +1.76% / runner +3.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.99% .. +4.08%] · haut q95 +5.52% · bas q05 -5.26%
   - 60min (n=160) : retour [-5.24% .. +5.35%] · haut q95 +6.4% · bas q05 -6.73%
   - 2h (n=160) : retour [-6.01% .. +6.03%] · haut q95 +6.9% · bas q05 -7.02%
   - 4h (n=160) : retour [-6.03% .. +6.35%] · haut q95 +7.93% · bas q05 -7.32%
   - 6h (n=160) : retour [-6.11% .. +7.73%] · haut q95 +9.19% · bas q05 -7.59%
   - session (n=160) : retour [-6.43% .. +7.31%] · haut q95 +9.61% · bas q05 -7.79%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 6.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.16% (p75 1.63% / p90 2.44%) · ~5.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 15.0 min, n=48)
   - −1.0% → **87%** (reprise méd 35.0 min, n=29)
   - −1.5% → **86%** (reprise méd 48.4 min, n=17)
   - −2.0% → **90%** (reprise méd 15.0 min, n=9)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.44%** (p90, défaut prudent ; serré/agressif −1.63%) ; extension open→close méd +9.37% (q75 +10.69% / q95 +12.08%), MFE méd +10.33% / q90 +12.7%
   - Échelle scale-out : +10.33% (33%) / +12.07% (33%) / +12.7% (34%)
- **DÉSARMER** : repli > **−2.44%** depuis le plus-haut = décay → P(retournement) **13%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.7% : P(retournement après) 0% (mèche méd None%)
- **CONTEXTE** : la dernière heure tient les gains 76% du temps (retour médian dernière heure +0.7%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 21.8  _(survente)_
- **ADX** : 28.8  _(tendance etablie)_
- **MACD** : hist -0.177  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 50.1%
- **ATR** : 0.79 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.366  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 32.8  _(marche directionnel)_
- **MA** : MA20 13.59 · MA50 15.12 · MA200 17.51  _(prix < MA20)_
- **Dist MA** : MA20 -15.3% · MA50 -23.8% · MA200 -34.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (789352 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
