# RGTI

**Generated** : 2026-10-20T00:25:34.290568+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $11.66  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 19/125 fenêtres (p_fill pondéré 13 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $11.66 (+7.5% vs entrée) · entrée $10.85 · stop $10.60 · T1 $11.26 · R/R 1.64  
> ↳ ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.26% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +5.9 % ≠ (strike 12.5 − spot 11.66)/spot = +7.2 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -42 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-19 : 11.66 · ATR Wilder 0.8907 (7.64 %)_
- **Swing** : plage **10.59 → 10.14** (-9.22 % a -13.04 % sous la cloture, 0.5 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 10.05-10.31 (A). stop INDICATIF 9.05 (-10.74 % sous le bas ; sous le support 9.5-9.74 (- 0,5 ATR)).
- **Deep** : plage **10.14 → 9.05** (-13.04 % a -22.4 % sous la cloture, 1.23 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 10.05-10.31 (A) ; 9.5-9.74 (C) ; 8.92-9.14 (A). stop INDICATIF 7.9 (-12.68 % sous le bas ; sous le support 8.35-8.45 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.73 ATR sous le plus haut 20 s., RSI(2) 24.1. Limite **11.22** (seance suivante), stop catastrophe 7.66, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 10.71-10.92 (A, -6.39 %) ; 10.05-10.31 (A, -11.62 %) ; 9.5-9.74 (C, -16.5 %) ; 8.92-9.14 (A, -21.65 %) ; 8.35-8.45 (B, -27.56 %) ; 6.86-7.03 (B, -39.78 %)
- Resistances reelles au-dessus : 12.34-12.75 (A, 5.79 %) ; 13.13-13.56 (A, 12.56 %) ; 13.61-13.82 (B, 16.67 %) ; 14.24-14.6 (A, 22.07 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.62 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (21.03 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **10.183 pt plus bas** dans le cas TYPIQUE (médiane), 10.183 au p90, **10.183 au pire**
   - perte réelle **31.213 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 21.03 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0081 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.503** [0.429 ; 0.5769] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4835** [0.4311 ; 0.5361] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4383** [0.3867 ; 0.4909] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.94 %** | CVaR **-11.24 %** | vol 6.82 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.26 % contre 6.26 % aujourd'hui, rapport 3.08)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8358** (β de hausse 2.0051, asymétrie 0.9155) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.438× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 10.6429 sur atr_grid (1.25 ATR, 8.762 %) — p(stop avant cible) 0.6436 [0.59 ; 0.69], R/R 3.001, perte reelle 8.927 % (gap inclus), CVaR 10.88 %, EV -0.933 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3215 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.644, borne haute 0.693 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.515 %) — p(stop avant cible) 0.5927 [0.54 ; 0.64], R/R 2.514, perte reelle 10.659 % (gap inclus), EV -1.3885 % — **REFUSE**
      - refuse : p_stop_first 0.593, borne haute 0.643 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 15.1 % x 26.79 % + P(rien) 25.7 % x 3.48 % ne couvrent pas P(stop) 59.3 % x 10.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.752 %) — p(stop avant cible) 0.9149 [0.88 ; 0.94], R/R 14.511, perte reelle 1.847 % (gap inclus), EV 0.1133 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 14.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.915, borne haute 0.941 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.505 %) — p(stop avant cible) 0.8345 [0.79 ; 0.87], R/R 7.418, perte reelle 3.612 % (gap inclus), EV -0.1414 % — **REFUSE**
      - refuse : cible atteinte seulement 8.7 % du temps (< 15 %) meme a 10 seances : le R/R de 7.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.835, borne haute 0.871 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 8.7 % x 26.79 % + P(rien) 7.8 % x 6.90 % ne couvrent pas P(stop) 83.5 % x 3.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 5.257 %) — p(stop avant cible) 0.7761 [0.73 ; 0.82], R/R 5.002, perte reelle 5.357 % (gap inclus), EV -0.6384 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.776, borne haute 0.818 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 10.3 % x 26.79 % + P(rien) 12.1 % x 6.28 % ne couvrent pas P(stop) 77.6 % x 5.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 7.01 %) — p(stop avant cible) 0.7028 [0.65 ; 0.75], R/R 3.753, perte reelle 7.139 % (gap inclus), EV -0.7086 % — **REFUSE**
      - refuse : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.703, borne haute 0.749 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 12.7 % x 26.79 % + P(rien) 17.1 % x 5.36 % ne couvrent pas P(stop) 70.3 % x 7.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 8.762 %) — p(stop avant cible) 0.6436 [0.59 ; 0.69], R/R 3.001, perte reelle 8.927 % (gap inclus), EV -0.933 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.644, borne haute 0.693 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 14.1 % x 26.79 % + P(rien) 21.6 % x 4.84 % ne couvrent pas P(stop) 64.4 % x 8.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 12.267 %) — p(stop avant cible) 0.5179 [0.47 ; 0.57], R/R 2.149, perte reelle 12.465 % (gap inclus), EV -1.3399 % — **REFUSE**
      - refuse : p_stop_first 0.518, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 15.7 % x 26.79 % + P(rien) 32.5 % x 2.79 % ne couvrent pas P(stop) 51.8 % x 12.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 14.02 %) — p(stop avant cible) 0.4301 [0.38 ; 0.48], R/R 1.887, perte reelle 14.196 % (gap inclus), EV -1.0275 % — **REFUSE**
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 16.3 % x 26.79 % + P(rien) 40.7 % x 1.76 % ne couvrent pas P(stop) 43.0 % x 14.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 15.772 %) — p(stop avant cible) 0.3542 [0.31 ; 0.41], R/R 1.677, perte reelle 15.976 % (gap inclus), EV -0.9035 % — **REFUSE**
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 16.9 % x 26.79 % + P(rien) 47.7 % x 0.50 % ne couvrent pas P(stop) 35.4 % x 15.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 17.525 %) — p(stop avant cible) 0.2784 [0.23 ; 0.33], R/R 1.506, perte reelle 17.789 % (gap inclus), EV -0.7336 % — **REFUSE**
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 17.5 % x 26.79 % + P(rien) 54.6 % x -0.88 % ne couvrent pas P(stop) 27.8 % x 17.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 19.277 %) — p(stop avant cible) 0.2326 [0.19 ; 0.28], R/R 1.365, perte reelle 19.623 % (gap inclus), EV -0.6381 % — **REFUSE**
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 18.0 % x 26.79 % + P(rien) 58.7 % x -1.54 % ne couvrent pas P(stop) 23.3 % x 19.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 21.03 %) — p(stop avant cible) 0.1854 [0.15 ; 0.23], R/R 1.251, perte reelle 21.416 % (gap inclus), EV -0.5759 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 18.1 % x 26.79 % + P(rien) 63.4 % x -2.29 % ne couvrent pas P(stop) 18.5 % x 21.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 24.535 %) — p(stop avant cible) 0.1254 [0.09 ; 0.16], R/R 1.076, perte reelle 24.89 % (gap inclus), EV -0.5847 % — **REFUSE**
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 18.1 % x 26.79 % + P(rien) 69.3 % x -3.35 % ne couvrent pas P(stop) 12.5 % x 24.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 28.04 %) — p(stop avant cible) 0.0705 [0.05 ; 0.10], R/R 0.949, perte reelle 28.238 % (gap inclus), EV -0.3951 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 18.5 % x 26.79 % + P(rien) 74.4 % x -4.53 % ne couvrent pas P(stop) 7.0 % x 28.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 31.545 %) — p(stop avant cible) 0.0396 [0.02 ; 0.06], R/R 0.846, perte reelle 31.684 % (gap inclus), EV -0.3312 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 18.6 % x 26.79 % + P(rien) 77.5 % x -5.23 % ne couvrent pas P(stop) 4.0 % x 31.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 35.05 %) — p(stop avant cible) 0.0237 [0.01 ; 0.04], R/R 0.756, perte reelle 35.444 % (gap inclus), EV -0.261 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 18.6 % x 26.79 % + P(rien) 79.0 % x -5.59 % ne couvrent pas P(stop) 2.4 % x 35.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 38.555 %) — p(stop avant cible) 0.0118 [0.00 ; 0.03], R/R 0.688, perte reelle 38.923 % (gap inclus), EV -0.2271 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 18.6 % x 26.79 % + P(rien) 80.2 % x -5.93 % ne couvrent pas P(stop) 1.2 % x 38.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 42.06 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.637, perte reelle 42.06 % (gap inclus), EV -0.171 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 18.7 % x 26.79 % + P(rien) 80.8 % x -6.18 % ne couvrent pas P(stop) 0.5 % x 42.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 45.565 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.583, perte reelle 45.985 % (gap inclus), EV -0.1827 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 18.7 % x 26.79 % + P(rien) 80.9 % x -6.18 % ne couvrent pas P(stop) 0.4 % x 45.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 49.07 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.546, perte reelle 49.07 % (gap inclus), EV -0.1831 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 18.7 % x 26.79 % + P(rien) 81.0 % x -6.26 % ne couvrent pas P(stop) 0.2 % x 49.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 52.575 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.5, perte reelle 53.605 % (gap inclus), EV -0.1909 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 18.7 % x 26.79 % + P(rien) 81.0 % x -6.27 % ne couvrent pas P(stop) 0.2 % x 53.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 56.08 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.454, perte reelle 58.973 % (gap inclus), EV -0.1703 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 18.7 % x 26.79 % + P(rien) 81.1 % x -6.26 % ne couvrent pas P(stop) 0.2 % x 58.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 11.665, ATR14 0.8177 (7.01 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.41 ATR = 2.874 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.35 % | 11.6241 | 92.04 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.701 % | 11.5832 | 86.4 % | 91.03 % | 92.43 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 1.051 % | 11.5423 | 80.97 % | 87.3 % | 89.1 % | 92.01 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.402 % | 11.5015 | 74.32 % | 82.66 % | 85.57 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.752 % | 11.4606 | 68.28 % | 78.43 % | 81.63 % | 85.74 % | 88.92 % | 92.51 % |
| 0.35 ATR | 2.453 % | 11.3788 | 55.79 % | 68.65 % | 74.07 % | 79.68 % | 84.55 % | 89.63 % |
| 0.5 ATR | 3.505 % | 11.2561 | 41.29 % | 57.16 % | 65.09 % | 71.89 % | 79.17 % | 85.32 % |
| 0.75 ATR | 5.257 % | 11.0517 | 21.85 % | 39.21 % | 50.35 % | 59.25 % | 70.83 % | 78.95 % |
| 1.0 ATR | 7.01 % | 10.8473 | 9.87 % | 24.29 % | 34.01 % | 47.02 % | 61.99 % | 72.48 % |
| 1.25 ATR | 8.762 % | 10.6429 | 4.13 % | 14.92 % | 24.02 % | 37.21 % | 52.85 % | 64.99 % |
| 1.5 ATR | 10.515 % | 10.4384 | 1.81 % | 7.36 % | 13.93 % | 25.78 % | 43.09 % | 56.88 % |
| 2.0 ATR | 14.02 % | 10.0296 | 0.4 % | 1.81 % | 4.24 % | 11.12 % | 25.41 % | 40.55 % |
| 2.5 ATR | 17.525 % | 9.6207 | 0.1 % | 0.4 % | 1.31 % | 4.75 % | 14.63 % | 28.23 % |
| 3.0 ATR | 21.03 % | 9.2119 | 0.0 % | 0.2 % | 0.5 % | 1.82 % | 7.32 % | 16.53 % |
| 4.0 ATR | 28.04 % | 8.3941 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 3.9 % |
| 6.0 ATR | 42.06 % | 6.7587 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.61 ATR | 0.71 ATR | 0.79 ATR | 1.00 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.76 ATR | 0.83 ATR | 1.02 ATR | 1.23 ATR | 1.35 ATR | 1.70 ATR | 1.96 ATR |
| **5 s.** | 0.44 ATR | 0.94 ATR | 1.05 ATR | 1.34 ATR | 1.53 ATR | 1.70 ATR | 2.09 ATR | 2.48 ATR |
| **10 s.** | 0.62 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.02 ATR | 2.25 ATR | 2.82 ATR | 3.43 ATR |
| **20 s.** | 0.90 ATR | 1.71 ATR | 1.86 ATR | 2.31 ATR | 2.64 ATR | 2.85 ATR | 3.52 ATR | 3.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.462–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.505 %, prix 11.2561), p(touche) 41.29 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.669–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.257 %, prix 11.0518), p(touche) 39.21 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.832–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.01 %, prix 10.8473), p(touche) 34.01 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.051–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.762 %, prix 10.6429), p(touche) 37.21 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.515 %, prix 10.4384), p(touche) 43.09 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (71.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.864–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.02 %, prix 10.0296), p(touche) 40.55 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.048 | EV/share : $0.012 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 — | T3 —
- Kelly (position) : f* 0.067 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 49.8 | side 45.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −7.007% → cible +3.769% / stop −2.261%, p_fill 13%, n_eff≈16.3) : P(cible|rempli) **36%** · **EV/risk +0.062** (×p_fill ; si rempli +1.06% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→77% · +2.0%→64% · +3.0%→46% · +5.0%→31% · +8.0%→10%
- Range intraday médian 6.8% (p90 11.03%) · excursion haute méd. +2.76% / basse méd. −2.46%
- Profil de vol intra : ouverture 4.714% vs midi 1.402% vs clôture 1.624% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.001)_ ; drift intra méd. -0.541% ; recovery-V 20%
- **σ réalisé intraday** 3.707% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 15.5684 (VA 15.2377–15.7574 ; dernier close 15.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 37% · rebond 75% · **stop −5.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 55% (gap-down >1% 36% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.87%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.58%) · haut méd +1.56% · range méd 3.3%
- Excursion ouverture 30min (n=160) : bas méd −1.45% (p90 −4.44%) · haut méd +1.84% · range méd 3.8%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −5.46%) · haut méd +2.09% · range méd 4.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (130/159) · gap 44% · délai 0.0min · rebond 63% (83/130) (MFE +1.59%)
   - −1.0% : fill 30min 60% · séance 71% (119/159) · gap 36% · délai 0.0min · rebond 70% (78/119) (MFE +1.68%)
   - −1.5% : fill 30min 54% · séance 63% (111/159) · gap 27% · délai 0.0min · rebond 68% (74/111) (MFE +1.92%)
   - −2.0% : fill 30min 48% · séance 57% (102/159) · gap 22% · délai 0.2min · rebond 67% (68/102) (MFE +2.13%)
   - −3.0% : fill 30min 33% · séance 48% (89/159) · gap 8% · délai 8.9min · rebond 65% (63/89) (MFE +1.87%)
   - −4.0% : fill 30min 24% · séance 37% (67/159) · gap 5% · délai 15.3min · rebond 75% (50/67) (MFE +2.24%)
   - −5.0% : fill 30min 12% · séance 26% (54/159) · gap 1% · délai 32.8min · rebond 57% (35/54) (MFE +1.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.86%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.28%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.38%) → stop au-delà de −1.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1068 jambes) : jambe baissière méd −1.27% (p90 −3.0%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 92% (79/83) · rebond 66% (48/79)
      · −2.0% : fill 82% (73/83) · rebond 68% (48/73)
      · −3.0% : fill 70% (66/83) · rebond 62% (45/66)
      · −4.0% : fill 60% (52/83) · rebond 70% (38/52)
      · −5.0% : fill 43% (43/83) · rebond 50% (26/43)
   - **flat** (16 séances) :
      · −1.0% : fill 84% (14/16) · rebond 98% (13/14)
      · −2.0% : fill 48% (10/16) · rebond 90% (9/10)
      · −3.0% : fill 24% (5/16) · rebond 92% (4/5)
      · −4.0% : fill 16% (4/16) · rebond 87% (3/4)
      · −5.0% : fill 10% (3/16) · rebond 100% (3/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (26/60) · rebond 64% (17/26)
      · −2.0% : fill 30% (19/60) · rebond 53% (11/19)
      · −3.0% : fill 29% (18/60) · rebond 65% (14/18)
      · −4.0% : fill 15% (11/60) · rebond 91% (9/11)
      · −5.0% : fill 10% (8/60) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 70% si les 15 1res min sont vertes (86 cas) · 21% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 47% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **86%** · continue >prix actuel 47% ; creux résiduel méd -1.49% (q20 -2.51%) → **SL/trailing à −2.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +3.2% → **scale +1.67% / runner +3.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.18%** (au-delà de la MAE q10 -4.18%), cible rebond +1.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.03% .. +4.37%] · haut q95 +5.8% · bas q05 -6.04%
   - 60min (n=160) : retour [-6.1% .. +5.82%] · haut q95 +6.56% · bas q05 -7.0%
   - 2h (n=160) : retour [-6.68% .. +5.93%] · haut q95 +6.77% · bas q05 -7.24%
   - 4h (n=160) : retour [-6.76% .. +6.25%] · haut q95 +7.97% · bas q05 -7.75%
   - 6h (n=160) : retour [-6.74% .. +6.96%] · haut q95 +9.18% · bas q05 -8.44%
   - session (n=160) : retour [-7.06% .. +7.17%] · haut q95 +9.19% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.66% / p90 2.43%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.0 min, n=43)
   - −1.0% → **83%** (reprise méd 35.0 min, n=27)
   - −1.5% → **83%** (reprise méd 93.49 min, n=16)
   - −2.0% → **84%** (reprise méd 44.98 min, n=8)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.43%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.12% (q75 +9.53% / q95 +9.89%), MFE méd +9.52% / q90 +11.18%
   - Échelle scale-out : +9.52% (33%) / +10.45% (33%) / +11.18% (34%)
- **DÉSARMER** : repli > **−2.43%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.18% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.45
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 16.1  _(survente)_
- **ADX** : 21.4  _(pas de tendance nette)_
- **MACD** : hist -0.337  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 46.6%
- **ATR** : 0.82 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.354  _(distribution)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 28.3  _(marche directionnel)_
- **MA** : MA20 14.54 · MA50 15.64 · MA200 17.77  _(prix < MA20)_
- **Dist MA** : MA20 -19.8% · MA50 -25.4% · MA200 -34.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760720 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
