# CEG

**Generated** : 2026-11-27T01:28:57.550188+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $235.28  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 5/125 fenêtres (p_fill pondéré 4 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $235.28 (+6.3% vs entrée) · entrée $221.30 · stop $203.60 · T1 $228.29 · R/R 0.39  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-25 : 235.28 · ATR Wilder 13.51 (5.74 %)_
- **Swing** : plage **216.45 → 206.43** (-8.0 % a -12.26 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 215.8-227.93 (B) ; 200.47-206.48 (B). stop INDICATIF 186.54 (-9.64 % sous le bas ; sous le support 193.3-196.52 (- 0,5 ATR)).
- **Deep** : plage **206.43 → 182.0** (-12.26 % a -22.65 % sous la cloture, 1.81 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 200.47-206.48 (B) ; 193.3-196.52 (B) ; 186.2-192.79 (A) ; 178.45-182.19 (B). stop INDICATIF 162.06 (-10.96 % sous le bas ; sous le support 168.81-175.42 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.65 ATR sous le plus haut 20 s., RSI(2) 18.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 224.39-230.95 (A, -1.84 %) ; 215.8-227.93 (B, -3.12 %) ; 200.47-206.48 (B, -12.24 %) ; 193.3-196.52 (B, -16.48 %) ; 186.2-192.79 (A, -18.06 %) ; 178.45-182.19 (B, -22.57 %)
- Resistances reelles au-dessus : 239.77-245.81 (A, 1.91 %) ; 246.82-250.17 (A, 4.91 %) ; 255.32-259.88 (A, 8.52 %) ; 263.52-268.31 (A, 12.0 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.05 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (17.82 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 17.82 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.871 % | p01 -4.442 % | pire -15.824 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0064** [0.0008 ; 0.0278] _(largeur 2.7 pt, n_eff 173.1)_
   - swing : **0.3149** [0.2676 ; 0.3653] _(largeur 9.8 pt, n_eff 345.6)_
   - deep : **0.2713** [0.2265 ; 0.3199] _(largeur 9.3 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.75 %** | CVaR **-6.94 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 5.70 % contre 3.04 % aujourd'hui, rapport 1.88)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.19 % vs -9.84 % si l'on extrapolait par √5 _(rapport 1.036 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1584** (β de hausse 1.197, asymétrie 0.9678) vs SPY — 567 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.782× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 217.8068 sur atr_grid (1.25 ATR, 7.427 %) — p(stop avant cible) 0.4423 [0.39 ; 0.49], R/R 7.733, perte reelle 7.58 % (gap inclus), CVaR 8.78 %, EV -0.6583 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.51 ATR (stop 5.685 %) — p(stop avant cible) 0.5607 [0.51 ; 0.61], R/R 10.034, perte reelle 5.842 % (gap inclus), EV -0.5832 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.561, borne haute 0.612 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 0.0 % x 58.62 % + P(rien) 43.9 % x 6.13 % ne couvrent pas P(stop) 56.1 % x 5.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 8.912 %) — p(stop avant cible) 0.3888 [0.34 ; 0.44], R/R 6.514, perte reelle 8.998 % (gap inclus), EV -0.921 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 0.0 % x 58.62 % + P(rien) 61.1 % x 4.22 % ne couvrent pas P(stop) 38.9 % x 9.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.485 %) — p(stop avant cible) 0.8807 [0.84 ; 0.91], R/R 35.942, perte reelle 1.631 % (gap inclus), EV -0.3833 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 35.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.881, borne haute 0.912 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.0 % x 58.62 % + P(rien) 11.9 % x 8.83 % ne couvrent pas P(stop) 88.1 % x 1.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.51 ATR (stop 4.812 %) — p(stop avant cible) 0.6357 [0.58 ; 0.69], R/R 11.816, perte reelle 4.961 % (gap inclus), EV -0.8655 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.636, borne haute 0.685 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 0.0 % x 58.62 % + P(rien) 36.4 % x 6.28 % ne couvrent pas P(stop) 63.6 % x 4.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 7.427 %) — p(stop avant cible) 0.4423 [0.39 ; 0.49], R/R 7.733, perte reelle 7.58 % (gap inclus), EV -0.6583 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 0.0 % x 58.62 % + P(rien) 55.8 % x 4.83 % ne couvrent pas P(stop) 44.2 % x 7.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 10.397 %) — p(stop avant cible) 0.2901 [0.24 ; 0.34], R/R 5.592, perte reelle 10.482 % (gap inclus), EV -0.7986 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 0.0 % x 58.62 % + P(rien) 71.0 % x 3.16 % ne couvrent pas P(stop) 29.0 % x 10.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 11.882 %) — p(stop avant cible) 0.2173 [0.18 ; 0.26], R/R 4.9, perte reelle 11.962 % (gap inclus), EV -0.496 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 0.0 % x 58.62 % + P(rien) 78.3 % x 2.69 % ne couvrent pas P(stop) 21.7 % x 11.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 13.368 %) — p(stop avant cible) 0.166 [0.13 ; 0.21], R/R 4.364, perte reelle 13.431 % (gap inclus), EV -0.4308 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 0.0 % x 58.62 % + P(rien) 83.4 % x 2.16 % ne couvrent pas P(stop) 16.6 % x 13.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 14.853 %) — p(stop avant cible) 0.1096 [0.08 ; 0.15], R/R 3.939, perte reelle 14.883 % (gap inclus), EV -0.3286 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.0 % x 58.62 % + P(rien) 89.0 % x 1.46 % ne couvrent pas P(stop) 11.0 % x 14.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 16.338 %) — p(stop avant cible) 0.0605 [0.04 ; 0.09], R/R 3.579, perte reelle 16.378 % (gap inclus), EV -0.2371 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.0 % x 58.62 % + P(rien) 94.0 % x 0.80 % ne couvrent pas P(stop) 6.0 % x 16.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 17.824 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 3.256, perte reelle 18.002 % (gap inclus), EV -0.2181 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 0.0 % x 58.62 % + P(rien) 96.3 % x 0.47 % ne couvrent pas P(stop) 3.7 % x 18.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 20.794 %) — p(stop avant cible) 0.0102 [0.00 ; 0.03], R/R 2.812, perte reelle 20.847 % (gap inclus), EV -0.1033 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.0 % x 58.62 % + P(rien) 99.0 % x 0.11 % ne couvrent pas P(stop) 1.0 % x 20.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 23.765 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 2.462, perte reelle 23.811 % (gap inclus), EV -0.0942 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.0 % x 58.62 % + P(rien) 99.4 % x 0.06 % ne couvrent pas P(stop) 0.6 % x 23.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 26.736 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 2.182, perte reelle 26.862 % (gap inclus), EV -0.0881 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.0 % x 58.62 % + P(rien) 99.5 % x 0.04 % ne couvrent pas P(stop) 0.5 % x 26.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 29.706 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 1.973, perte reelle 29.715 % (gap inclus), EV -0.0823 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 58.62 % + P(rien) 99.8 % x -0.03 % ne couvrent pas P(stop) 0.2 % x 29.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 32.677 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 1.794, perte reelle 32.677 % (gap inclus), EV -0.0812 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 58.62 % + P(rien) 100.0 % x -0.06 % ne couvrent pas P(stop) 0.1 % x 32.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 35.647 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.644, perte reelle 35.647 % (gap inclus), EV -0.0804 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 58.62 % + P(rien) 100.0 % x -0.08 % ne couvrent pas P(stop) 0.0 % x 35.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 38.618 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.518, perte reelle 38.618 % (gap inclus), EV -0.0804 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 58.62 % + P(rien) 100.0 % x -0.08 % ne couvrent pas P(stop) 0.0 % x 38.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 41.589 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.409, perte reelle 41.589 % (gap inclus), EV -0.0804 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 58.62 % + P(rien) 100.0 % x -0.08 % ne couvrent pas P(stop) 0.0 % x 41.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 44.559 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.315, perte reelle 44.559 % (gap inclus), EV -0.0804 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 58.62 % + P(rien) 100.0 % x -0.08 % ne couvrent pas P(stop) 0.0 % x 44.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 47.53 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.233, perte reelle 47.53 % (gap inclus), EV -0.0804 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 58.62 % + P(rien) 100.0 % x -0.08 % ne couvrent pas P(stop) 0.0 % x 47.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 235.28, ATR14 13.9785 (5.941 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.391 ATR = 2.323 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.297 % | 234.5811 | 91.86 % | 94.78 % | 95.71 % | 96.75 % | 97.68 % | 98.08 % |
| 0.1 ATR | 0.594 % | 233.8821 | 85.8 % | 90.7 % | 92.68 % | 94.23 % | 95.79 % | 96.91 % |
| 0.15 ATR | 0.891 % | 233.1832 | 79.23 % | 86.52 % | 88.7 % | 90.88 % | 93.99 % | 95.63 % |
| 0.2 ATR | 1.188 % | 232.4843 | 72.23 % | 81.19 % | 84.41 % | 87.11 % | 91.57 % | 94.36 % |
| 0.25 ATR | 1.485 % | 231.7854 | 65.34 % | 75.55 % | 79.5 % | 83.33 % | 88.83 % | 92.44 % |
| 0.35 ATR | 2.079 % | 230.3875 | 54.18 % | 66.35 % | 71.86 % | 77.25 % | 84.51 % | 89.03 % |
| 0.5 ATR | 2.971 % | 228.2907 | 39.04 % | 53.29 % | 59.83 % | 66.77 % | 77.56 % | 83.49 % |
| 0.75 ATR | 4.456 % | 224.7961 | 20.46 % | 37.1 % | 45.71 % | 53.98 % | 67.54 % | 76.78 % |
| 1.0 ATR | 5.941 % | 221.3015 | 11.06 % | 24.14 % | 33.68 % | 43.92 % | 58.59 % | 70.61 % |
| 1.25 ATR | 7.427 % | 217.8068 | 5.64 % | 16.2 % | 24.58 % | 36.16 % | 52.37 % | 64.54 % |
| 1.5 ATR | 8.912 % | 214.3122 | 2.71 % | 10.76 % | 17.57 % | 29.35 % | 45.42 % | 58.36 % |
| 2.0 ATR | 11.882 % | 207.323 | 0.84 % | 4.39 % | 9.31 % | 18.13 % | 31.72 % | 46.43 % |
| 2.5 ATR | 14.853 % | 200.3337 | 0.42 % | 2.19 % | 4.71 % | 11.11 % | 21.5 % | 36.63 % |
| 3.0 ATR | 17.824 % | 193.3444 | 0.0 % | 1.04 % | 2.72 % | 6.71 % | 15.17 % | 28.54 % |
| 4.0 ATR | 23.765 % | 179.3659 | 0.0 % | 0.21 % | 0.84 % | 2.62 % | 6.85 % | 14.06 % |
| 6.0 ATR | 35.647 % | 151.4089 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.74 % | 2.66 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.30 ATR |
| **2 s.** | 0.26 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.98 ATR | 1.13 ATR | 1.56 ATR | 1.95 ATR |
| **3 s.** | 0.31 ATR | 0.67 ATR | 0.77 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.96 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.85 ATR | 0.97 ATR | 1.37 ATR | 1.69 ATR | 1.92 ATR | 2.63 ATR | 3.42 ATR |
| **10 s.** | 0.56 ATR | 1.33 ATR | 1.51 ATR | 1.95 ATR | 2.33 ATR | 2.62 ATR | 3.62 ATR | 4.61 ATR |
| **20 s.** | 0.82 ATR | 1.85 ATR | 2.07 ATR | 2.72 ATR | 3.24 ATR | 3.59 ATR | 4.71 ATR | 5.59 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.441 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.628–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.456 %, prix 224.7959), p(touche) 37.1 % (en stress 88.54 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.765–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.941 %, prix 221.302), p(touche) 33.68 % (en stress 95.83 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.941 %, prix 221.302), p(touche) 43.92 % (en stress 96.88 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.515–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.882 %, prix 207.324), p(touche) 31.72 % (en stress 96.84 %)  ✅ optimum identifie (75.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.073–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.853 %, prix 200.3339), p(touche) 36.63 % (en stress 95.74 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (88.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : $-0.768 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.7 | bear 74.1 | side 6.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→62% · +2.0%→34% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.36% (p90 5.65%) · excursion haute méd. +1.38% / basse méd. −1.56%
- Profil de vol intra : ouverture 2.53% vs midi 0.658% vs clôture 0.771% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr 0.005)_ ; drift intra méd. -0.554% ; recovery-V 16%
- **σ réalisé intraday** 2.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 59% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 253.5534 (VA 252.1149–254.9919 ; dernier close 253.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 34% · **stop −2.58%** sous le fill (sous le bruit) · cible +0.8% · R/R 0.31 (high win-rate)
- Gaps overnight (n=159) : méd. 0.54% · baisse 37% (gap-down >1% 11% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.8%) · haut méd +0.66% · range méd 1.52%
- Excursion ouverture 15min (n=160) : bas méd −0.97% (p90 −2.69%) · haut méd +0.84% · range méd 2.02%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −3.19%) · haut méd +0.92% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.18% (p90 −3.97%) · haut méd +1.01% · range méd 2.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 253.0638 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 66% (98/159) · gap 26% · délai 0.0min · rebond 43% (44/98) (MFE +0.93%)
   - −1.0% : fill 30min 45% · séance 56% (83/159) · gap 11% · délai 2.1min · rebond 53% (38/83) (MFE +1.02%)
   - −1.5% : fill 30min 37% · séance 50% (71/159) · gap 6% · délai 5.1min · rebond 47% (33/71) (MFE +0.95%)
   - −2.0% : fill 30min 25% · séance 38% (56/159) · gap 4% · délai 11.6min · rebond 53% (29/56) (MFE +1.04%)
   - −3.0% : fill 30min 13% · séance 21% (30/159) · gap 2% · délai 15.6min · rebond 44% (12/30) (MFE +0.9%)
   - −4.0% : fill 30min 9% · séance 15% (21/159) · gap 0% · délai 21.7min · rebond 34% (9/21) (MFE +0.8%)
   - −5.0% : fill 30min 3% · séance 9% (12/159) · gap 0% · délai 61.7min · rebond 24% (5/12) (MFE +0.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.42%) → stop au-delà de −0.98% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −1.41%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.48%) → stop au-delà de −1.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=471 jambes) : jambe baissière méd −1.09% (p90 −2.58%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (41 séances) :
      · −1.0% : fill 95% (38/41) · rebond 54% (19/38)
      · −2.0% : fill 72% (29/41) · rebond 52% (16/29)
      · −3.0% : fill 45% (18/41) · rebond 28% (5/18)
      · −4.0% : fill 44% (17/41) · rebond 34% (7/17)
      · −5.0% : fill 26% (10/41) · rebond 25% (4/10)
   - **flat** (20 séances) :
      · −1.0% : fill 52% (12/20) · rebond 68% (5/12)
      · −2.0% : fill 40% (11/20) · rebond 59% (6/11)
      · −3.0% : fill 12% (4/20) · rebond 51% (2/4)
      · −4.0% : fill 6% (2/20) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/20) · rebond 0% (0/1)
   - **gap-up** (98 séances) :
      · −1.0% : fill 34% (33/98) · rebond 47% (14/33)
      · −2.0% : fill 18% (16/98) · rebond 52% (7/16)
      · −3.0% : fill 9% (8/98) · rebond 88% (5/8)
      · −4.0% : fill 1% (2/98) · rebond 100% (2/2)
      · −5.0% : fill 0% (1/98) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 62% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 80% si début vert vs 16% si rouge (base 42% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **80%** · continue >prix actuel 46% ; creux résiduel méd -1.18% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +2.04% → **scale +1.2% / runner +2.04%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **16%** (continue à baisser 56%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.3%** (au-delà de la MAE q10 -2.3%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.44% .. +2.01%] · haut q95 +3.41% · bas q05 -3.51%
   - 60min (n=160) : retour [-3.66% .. +2.94%] · haut q95 +3.74% · bas q05 -4.68%
   - 2h (n=160) : retour [-3.81% .. +3.8%] · haut q95 +4.14% · bas q05 -5.27%
   - 4h (n=160) : retour [-4.48% .. +3.64%] · haut q95 +4.31% · bas q05 -5.39%
   - 6h (n=160) : retour [-4.7% .. +3.8%] · haut q95 +4.82% · bas q05 -5.75%
   - session (n=160) : retour [-4.6% .. +3.49%] · haut q95 +4.82% · bas q05 -5.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **32%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.11% (p75 1.79% / p90 2.39%) · ~1.0 replis/séance, durée méd 169.74 min. P(nouveau plus-haut après repli) :
   - −0.5% → **68%** (reprise méd 29.55 min, n=17)
   - −1.0% → **67%** (reprise méd 182.65 min, n=9)
   - −1.5% → **45%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.39%** (p90, défaut prudent ; serré/agressif −1.79%) ; extension open→close méd +3.62% (q75 +4.52% / q95 +6.21%), MFE méd +4.59% / q90 +5.86%
   - Échelle scale-out : +4.59% (33%) / +5.3% (33%) / +5.86% (34%)
- **DÉSARMER** : repli > **−2.39%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.86% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.49%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.5  _(neutre)_
- **ADX** : 15.3  _(pas de tendance nette)_
- **MACD** : hist -2.95  _(bearish_recent)_
- **BB** : %B 0.09 · largeur 22.5%
- **ATR** : 13.98 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.003  _(neutre)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 48.8  _(transition)_
- **MA** : MA20 259.46 · MA50 264.83 · MA200 277.07  _(prix < MA20)_
- **Dist MA** : MA20 -9.3% · MA50 -11.2% · MA200 -15.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (688691 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
