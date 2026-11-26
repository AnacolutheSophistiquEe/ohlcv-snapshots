# RHM

**Generated** : 2026-11-26T21:39:34.469230+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · €765.70  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 11/125 fenêtres (p_fill pondéré 7 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €765.70 (+5.0% vs entrée) · entrée €729.46 · stop €714.88 · T1 €747.58 · R/R 1.24  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-26 : 765.7 · ATR Wilder 38.47 (5.02 %)_
- **Swing** : plage **709.49 → 676.04** (-7.34 % a -11.71 % sous la cloture, 0.87 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 677.76-695.89 (A). stop INDICATIF 637.57 (-5.69 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **676.04 → 581.67** (-11.71 % a -24.03 % sous la cloture, 2.45 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 617.47-627.13 (C) ; 584.17-592.25 (A). stop INDICATIF 519.63 (-10.67 % sous le bas ; sous le support 538.86-557.13 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 7.43 ATR sous le plus haut 20 s., RSI(2) 92.5. Limite **746.47** (seance suivante), stop catastrophe 592.59, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 677.76-695.89 (A, -9.12 %) ; 617.47-627.13 (C, -18.1 %) ; 584.17-592.25 (A, -22.65 %) ; 538.86-557.13 (C, -27.24 %) ; 519.16-536.48 (B, -29.94 %) ; 499.65-514.63 (B, -32.79 %)
- Resistances reelles au-dessus : 909.0-919.11 (B, 18.71 %) ; 928.8-940.0 (A, 21.3 %) ; 976.0-987.1 (A, 27.47 %) ; 1006.4-1006.4 (B, 31.44 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.80 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.2 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **8.229 pt plus bas** dans le cas TYPIQUE (médiane), 8.229 au p90, **8.229 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 14.2 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0065 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.62 % | p01 -3.886 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3667** [0.2976 ; 0.4402] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4041** [0.3534 ; 0.4564] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3976** [0.347 ; 0.4499] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.76 %** | CVaR **-7.12 %** | vol 3.09 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 2.04 % contre 3.36 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.5 % vs -9.03 % si l'on extrapolait par √5 _(rapport 0.942 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5198** (β de hausse 0.588, asymétrie 0.884) vs GDAXI — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.294× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 711.3464 sur atr_based (1.5 ATR, 7.099 %) — p(stop avant cible) 0.4789 [0.43 ; 0.53], R/R 5.669, perte reelle 7.826 % (gap inclus), CVaR 12.49 %, EV -1.3994 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0368 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 12.49 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.099 %) — p(stop avant cible) 0.4789 [0.43 ; 0.53], R/R 5.669, perte reelle 7.826 % (gap inclus), EV -1.3994 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 0.1 % x 44.36 % + P(rien) 52.0 % x 4.46 % ne couvrent pas P(stop) 47.9 % x 7.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ swing_based a 2.23 ATR (stop 12.601 %) — p(stop avant cible) 0.2237 [0.18 ; 0.27], R/R 3.41, perte reelle 13.011 % (gap inclus), EV -1.7939 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.79 %) : P(cible) 0.1 % x 44.36 % + P(rien) 77.6 % x 1.41 % ne couvrent pas P(stop) 22.4 % x 13.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.183 %) — p(stop avant cible) 0.895 [0.86 ; 0.92], R/R 35.839, perte reelle 1.238 % (gap inclus), EV -0.0145 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 35.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.895, borne haute 0.924 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 0.0 % x 44.36 % + P(rien) 10.5 % x 10.41 % ne couvrent pas P(stop) 89.5 % x 1.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.366 %) — p(stop avant cible) 0.8272 [0.78 ; 0.86], R/R 17.723, perte reelle 2.503 % (gap inclus), EV -0.3524 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 17.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.827, borne haute 0.864 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.0 % x 44.36 % + P(rien) 17.3 % x 9.94 % ne couvrent pas P(stop) 82.7 % x 2.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 3.549 %) — p(stop avant cible) 0.7308 [0.68 ; 0.78], R/R 11.592, perte reelle 3.827 % (gap inclus), EV -0.7356 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.731, borne haute 0.775 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 0.0 % x 44.36 % + P(rien) 26.9 % x 7.66 % ne couvrent pas P(stop) 73.1 % x 3.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 4.732 %) — p(stop avant cible) 0.6508 [0.60 ; 0.70], R/R 8.572, perte reelle 5.175 % (gap inclus), EV -0.995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.651, borne haute 0.700 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 0.0 % x 44.36 % + P(rien) 34.9 % x 6.80 % ne couvrent pas P(stop) 65.1 % x 5.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 5.915 %) — p(stop avant cible) 0.5709 [0.52 ; 0.62], R/R 6.746, perte reelle 6.576 % (gap inclus), EV -1.3302 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.571, borne haute 0.622 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.33 %) : P(cible) 0.1 % x 44.36 % + P(rien) 42.9 % x 5.60 % ne couvrent pas P(stop) 57.1 % x 6.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 8.282 %) — p(stop avant cible) 0.41 [0.36 ; 0.46], R/R 4.901, perte reelle 9.052 % (gap inclus), EV -1.5542 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.55 %) : P(cible) 0.1 % x 44.36 % + P(rien) 58.9 % x 3.62 % ne couvrent pas P(stop) 41.0 % x 9.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 2.23 ATR (stop 11.952 %) — p(stop avant cible) 0.2377 [0.20 ; 0.28], R/R 3.577, perte reelle 12.403 % (gap inclus), EV -1.7127 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 0.1 % x 44.36 % + P(rien) 76.2 % x 1.59 % ne couvrent pas P(stop) 23.8 % x 12.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 14.197 %) — p(stop avant cible) 0.1717 [0.13 ; 0.21], R/R 3.04, perte reelle 14.594 % (gap inclus), EV -1.8431 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 0.1 % x 44.36 % + P(rien) 82.8 % x 0.77 % ne couvrent pas P(stop) 17.2 % x 14.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 16.563 %) — p(stop avant cible) 0.1411 [0.11 ; 0.18], R/R 2.615, perte reelle 16.963 % (gap inclus), EV -2.0804 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 0.1 % x 44.36 % + P(rien) 85.8 % x 0.33 % ne couvrent pas P(stop) 14.1 % x 16.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 18.929 %) — p(stop avant cible) 0.102 [0.07 ; 0.14], R/R 2.308, perte reelle 19.221 % (gap inclus), EV -2.1754 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 0.1 % x 44.36 % + P(rien) 89.7 % x -0.27 % ne couvrent pas P(stop) 10.2 % x 19.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 21.296 %) — p(stop avant cible) 0.0693 [0.05 ; 0.10], R/R 2.058, perte reelle 21.562 % (gap inclus), EV -2.1864 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.19 %) : P(cible) 0.1 % x 44.36 % + P(rien) 93.0 % x -0.77 % ne couvrent pas P(stop) 6.9 % x 21.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 23.662 %) — p(stop avant cible) 0.0299 [0.02 ; 0.05], R/R 1.837, perte reelle 24.151 % (gap inclus), EV -2.0739 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 0.1 % x 44.36 % + P(rien) 97.0 % x -1.42 % ne couvrent pas P(stop) 3.0 % x 24.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 26.028 %) — p(stop avant cible) 0.0158 [0.01 ; 0.03], R/R 1.7, perte reelle 26.096 % (gap inclus), EV -2.0909 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 0.1 % x 44.36 % + P(rien) 98.4 % x -1.73 % ne couvrent pas P(stop) 1.6 % x 26.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 28.394 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 1.562, perte reelle 28.394 % (gap inclus), EV -2.0587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 0.1 % x 44.36 % + P(rien) 99.6 % x -1.99 % ne couvrent pas P(stop) 0.4 % x 28.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 30.76 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.442, perte reelle 30.76 % (gap inclus), EV -1.9859 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 0.1 % x 44.36 % + P(rien) 99.8 % x -1.98 % ne couvrent pas P(stop) 0.1 % x 30.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 33.127 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.339, perte reelle 33.127 % (gap inclus), EV -1.9421 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 0.1 % x 44.36 % + P(rien) 99.9 % x -1.97 % ne couvrent pas P(stop) 0.0 % x 33.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 35.493 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.25, perte reelle 35.493 % (gap inclus), EV -1.9421 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 0.1 % x 44.36 % + P(rien) 99.9 % x -1.97 % ne couvrent pas P(stop) 0.0 % x 35.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 37.859 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.172, perte reelle 37.859 % (gap inclus), EV -1.9421 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 0.1 % x 44.36 % + P(rien) 99.9 % x -1.97 % ne couvrent pas P(stop) 0.0 % x 37.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 765.7, ATR14 36.2357 (4.732 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.39 ATR = 1.846 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.237 % | 763.8882 | 89.55 % | 92.5 % | 93.68 % | 94.95 % | 97.31 % | 97.99 % |
| 0.1 ATR | 0.473 % | 762.0764 | 83.63 % | 88.35 % | 90.32 % | 91.98 % | 95.62 % | 96.68 % |
| 0.15 ATR | 0.71 % | 760.2647 | 76.53 % | 83.32 % | 86.26 % | 88.81 % | 93.43 % | 95.28 % |
| 0.2 ATR | 0.946 % | 758.4529 | 69.82 % | 78.78 % | 82.02 % | 85.64 % | 91.34 % | 93.67 % |
| 0.25 ATR | 1.183 % | 756.6411 | 62.43 % | 73.05 % | 76.98 % | 81.49 % | 88.76 % | 91.86 % |
| 0.35 ATR | 1.656 % | 753.0175 | 53.45 % | 65.65 % | 71.05 % | 76.93 % | 86.07 % | 89.85 % |
| 0.5 ATR | 2.366 % | 747.5822 | 40.53 % | 55.08 % | 61.76 % | 69.7 % | 80.9 % | 84.82 % |
| 0.75 ATR | 3.549 % | 738.5232 | 23.57 % | 39.19 % | 47.73 % | 58.51 % | 71.64 % | 78.59 % |
| 1.0 ATR | 4.732 % | 729.4643 | 13.21 % | 27.25 % | 37.15 % | 49.6 % | 63.88 % | 72.36 % |
| 1.25 ATR | 5.915 % | 720.4054 | 7.69 % | 18.46 % | 27.08 % | 40.4 % | 56.12 % | 66.33 % |
| 1.5 ATR | 7.099 % | 711.3464 | 3.94 % | 13.43 % | 21.25 % | 32.38 % | 47.96 % | 59.3 % |
| 2.0 ATR | 9.465 % | 693.2286 | 1.78 % | 7.31 % | 12.75 % | 21.98 % | 36.42 % | 50.15 % |
| 2.5 ATR | 11.831 % | 675.1107 | 0.49 % | 3.46 % | 6.62 % | 12.97 % | 26.37 % | 40.8 % |
| 3.0 ATR | 14.197 % | 656.9929 | 0.1 % | 1.48 % | 4.05 % | 8.12 % | 18.61 % | 34.37 % |
| 4.0 ATR | 18.929 % | 620.7571 | 0.0 % | 0.39 % | 1.48 % | 3.66 % | 9.55 % | 22.01 % |
| 6.0 ATR | 28.394 % | 548.2857 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.39 % | 4.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.15 ATR | 1.43 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.88 ATR | 1.06 ATR | 1.21 ATR | 1.78 ATR | 2.30 ATR |
| **3 s.** | 0.28 ATR | 0.71 ATR | 0.81 ATR | 1.10 ATR | 1.34 ATR | 1.57 ATR | 2.22 ATR | 2.81 ATR |
| **5 s.** | 0.39 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.85 ATR | 2.11 ATR | 2.81 ATR | 3.70 ATR |
| **10 s.** | 0.66 ATR | 1.44 ATR | 1.63 ATR | 2.17 ATR | 2.59 ATR | 2.91 ATR | 3.95 ATR | 5.12 ATR |
| **20 s.** | 0.89 ATR | 2.01 ATR | 2.27 ATR | 3.11 ATR | 3.76 ATR | 4.23 ATR | 5.37 ATR | 5.95 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.448 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.659–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.549 %, prix 738.5253), p(touche) 39.19 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.815–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.732 %, prix 729.4671), p(touche) 37.15 % (en stress 95.1 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.125–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.915 %, prix 720.4089), p(touche) 40.4 % (en stress 97.03 %)  ✅ optimum identifie (72.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.628–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.465 %, prix 693.2265), p(touche) 36.42 % (en stress 95.05 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (95.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.275–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (11.831 %, prix 675.11), p(touche) 40.8 % (en stress 98.0 %)  ✅ optimum identifie (97.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : €-0.324 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 3 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 41.5 | bear 51.8 | side 6.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→43% · +3.0%→26% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.92% (p90 6.37%) · excursion haute méd. +1.54% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.386% vs midi 0.887% vs clôture 1.007% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. 0.01% ; recovery-V 14%
- **σ réalisé intraday** 2.348% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 65% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1019.35 (VA 1013.75–1023.55 ; dernier close 1015.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 52% · rebond 59% · **stop −2.85%** sous le fill (sous le bruit) · cible +1.34% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 39% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.73%) · haut méd +0.46% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.14%) · haut méd +0.6% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.31%) · haut méd +0.75% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −2.38%) · haut méd +0.88% · range méd 2.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1019.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 75% (112/159) · gap 18% · délai 0.4min · rebond 57% (62/112) (MFE +1.08%)
   - −1.0% : fill 30min 42% · séance 64% (98/159) · gap 7% · délai 6.3min · rebond 59% (58/98) (MFE +1.26%)
   - −1.5% : fill 30min 26% · séance 52% (80/159) · gap 4% · délai 29.9min · rebond 59% (47/80) (MFE +1.34%)
   - −2.0% : fill 30min 16% · séance 40% (66/159) · gap 2% · délai 88.0min · rebond 52% (38/66) (MFE +1.2%)
   - −3.0% : fill 30min 6% · séance 25% (38/159) · gap 2% · délai 141.2min · rebond 42% (18/38) (MFE +0.97%)
   - −4.0% : fill 30min 2% · séance 12% (21/159) · gap 1% · délai 153.2min · rebond 60% (12/21) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 5% (11/159) · gap 0% · délai 103.2min · rebond 94% (10/11) (MFE +2.81%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.37%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.44%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.48%) → stop au-delà de −0.96% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=544 jambes) : jambe baissière méd −0.97% (p90 −2.4%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 98% (36/37) · rebond 69% (25/36)
      · −2.0% : fill 65% (28/37) · rebond 46% (16/28)
      · −3.0% : fill 46% (16/37) · rebond 33% (7/16)
      · −4.0% : fill 34% (12/37) · rebond 58% (7/12)
      · −5.0% : fill 15% (6/37) · rebond 100% (6/6)
   - **flat** (29 séances) :
      · −1.0% : fill 74% (21/29) · rebond 60% (14/21)
      · −2.0% : fill 41% (11/29) · rebond 75% (8/11)
      · −3.0% : fill 21% (6/29) · rebond 67% (3/6)
      · −4.0% : fill 3% (2/29) · rebond 62% (1/2)
      · −5.0% : fill 3% (2/29) · rebond 62% (1/2)
   - **gap-up** (93 séances) :
      · −1.0% : fill 41% (41/93) · rebond 46% (19/41)
      · −2.0% : fill 27% (27/93) · rebond 44% (14/27)
      · −3.0% : fill 15% (16/93) · rebond 41% (8/16)
      · −4.0% : fill 4% (7/93) · rebond 70% (4/7)
      · −5.0% : fill 1% (3/93) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 57% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **45min** → P(séance verte=clôture>ouverture) 65% si début vert vs 20% si rouge (base 43% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **65%** · continue >prix actuel 48% ; creux résiduel méd -1.21% (q20 -2.27%) → **SL/trailing à −2.27%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.5% → **scale +1.5% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 58%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.6%** (au-delà de la MAE q10 -3.6%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.04% .. +2.68%] · haut q95 +2.92% · bas q05 -2.8%
   - 60min (n=160) : retour [-2.51% .. +3.12%] · haut q95 +3.43% · bas q05 -3.45%
   - 2h (n=160) : retour [-3.37% .. +2.76%] · haut q95 +3.79% · bas q05 -3.97%
   - 4h (n=160) : retour [-3.21% .. +2.84%] · haut q95 +4.17% · bas q05 -4.74%
   - 6h (n=160) : retour [-3.6% .. +3.07%] · haut q95 +4.55% · bas q05 -5.07%
   - session (n=160) : retour [-4.05% .. +3.96%] · haut q95 +4.97% · bas q05 -5.07%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.29 · part idiosyncratique 0.71
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.6  _(momentum baissier)_
- **ADX** : 34.1  _(tendance etablie)_
- **MACD** : hist -0.425  _(pas de croisement recent)_
- **BB** : %B 0.38 · largeur 52.4%
- **ATR** : 36.24 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.251  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 36.8  _(marche directionnel)_
- **MA** : MA20 819.3 · MA50 924.38 · MA200 1178.06  _(prix < MA20)_
- **Dist MA** : MA20 -6.5% · MA50 -17.2% · MA200 -35.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (695330 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
