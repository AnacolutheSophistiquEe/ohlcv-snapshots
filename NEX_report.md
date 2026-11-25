# NEX

**Generated** : 2026-11-25T01:10:20.247049+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €118.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot €118.80 (+4.4% vs entrée) · entrée €113.83 · stop €104.73 · T1 €116.32 · R/R 0.27  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 118.8 · ATR Wilder 5.06 (4.26 %)_
- **Swing** : plage **111.89 → 107.76** (-5.82 % a -9.29 % sous la cloture, 0.82 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 110.28-111.7 (B) ; 107.17-109.69 (A). stop INDICATIF 101.96 (-5.38 % sous le bas ; sous le support 104.49-106.6 (- 0,5 ATR)).
- **Deep** : plage **107.76 → 95.88** (-9.29 % a -19.3 % sous la cloture, 2.35 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 107.17-109.69 (A) ; 104.49-106.6 (B) ; 101.91-102.92 (A) ; 99.23-101.52 (B) ; 96.36-98.46 (B) ; 93.34-97.27 (A). stop INDICATIF 88.21 (-8.0 % sous le bas ; sous le support 90.74-93.0 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.02 ATR sous le plus haut 20 s., RSI(2) 24.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 112.93-114.01 (B, -4.03 %) ; 110.28-111.7 (B, -5.98 %) ; 107.17-109.69 (A, -7.67 %) ; 104.49-106.6 (B, -10.27 %) ; 101.91-102.92 (A, -13.37 %) ; 99.23-101.52 (B, -14.54 %)
- Resistances reelles au-dessus : 121.91-124.33 (A, 2.61 %) ; 124.7-126.98 (A, 4.97 %) ; 127.74-130.22 (A, 7.53 %) ; 130.61-131.89 (A, 9.94 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.55 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.55 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.572 % | p01 -3.604 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0023** [0.0001 ; 0.0198] _(largeur 2.0 pt, n_eff 173.1)_
   - swing : **0.3442** [0.2956 ; 0.3954] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.2843** [0.2387 ; 0.3335] _(largeur 9.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.66 %** | CVaR **-5.41 %** | vol 2.34 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.6 % vs -8.19 % si l'on extrapolait par √5 _(rapport 0.928 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0054** (β de hausse 1.0916, asymétrie 0.921) vs FCHI — 622 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 105.1384 sur atr_grid (2.75 ATR, 11.5 %) — p(stop avant cible) 0.0919 [0.06 ; 0.13], R/R 3.209, perte reelle 11.688 % (gap inclus), CVaR 11.845 %, EV 0.0089 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.74 ATR (stop 4.957 %) — p(stop avant cible) 0.5075 [0.45 ; 0.56], R/R 7.325, perte reelle 5.121 % (gap inclus), EV -0.5054 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.507, borne haute 0.560 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.0 % x 37.51 % + P(rien) 49.2 % x 4.25 % ne couvrent pas P(stop) 50.7 % x 5.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 6.273 %) — p(stop avant cible) 0.3863 [0.34 ; 0.44], R/R 5.85, perte reelle 6.412 % (gap inclus), EV -0.4277 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 0.0 % x 37.51 % + P(rien) 61.4 % x 3.34 % ne couvrent pas P(stop) 38.6 % x 6.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.045 %) — p(stop avant cible) 0.909 [0.88 ; 0.94], R/R 34.703, perte reelle 1.081 % (gap inclus), EV -0.2204 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 34.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 0.0 % x 37.51 % + P(rien) 9.1 % x 8.38 % ne couvrent pas P(stop) 90.9 % x 1.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.74 ATR (stop 4.364 %) — p(stop avant cible) 0.5635 [0.51 ; 0.62], R/R 8.276, perte reelle 4.532 % (gap inclus), EV -0.4949 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.564, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 0.0 % x 37.51 % + P(rien) 43.6 % x 4.72 % ne couvrent pas P(stop) 56.4 % x 4.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 7.318 %) — p(stop avant cible) 0.2712 [0.23 ; 0.32], R/R 5.024, perte reelle 7.466 % (gap inclus), EV -0.0393 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.0 % x 37.51 % + P(rien) 72.9 % x 2.72 % ne couvrent pas P(stop) 27.1 % x 7.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 8.363 %) — p(stop avant cible) 0.218 [0.18 ; 0.26], R/R 4.429, perte reelle 8.469 % (gap inclus), EV -0.0312 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.0 % x 37.51 % + P(rien) 78.2 % x 2.32 % ne couvrent pas P(stop) 21.8 % x 8.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 9.409 %) — p(stop avant cible) 0.1623 [0.13 ; 0.20], R/R 3.93, perte reelle 9.545 % (gap inclus), EV -0.0161 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.0 % x 37.51 % + P(rien) 83.8 % x 1.83 % ne couvrent pas P(stop) 16.2 % x 9.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 10.454 %) — p(stop avant cible) 0.1263 [0.09 ; 0.16], R/R 3.552, perte reelle 10.56 % (gap inclus), EV -0.0449 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.0 % x 37.51 % + P(rien) 87.4 % x 1.48 % ne couvrent pas P(stop) 12.6 % x 10.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 11.5 %) — p(stop avant cible) 0.0919 [0.06 ; 0.13], R/R 3.209, perte reelle 11.688 % (gap inclus), EV 0.0089 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 3.0 ATR (stop 12.545 %) — p(stop avant cible) 0.0697 [0.05 ; 0.10], R/R 2.934, perte reelle 12.785 % (gap inclus), EV -0.0278 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.0 % x 37.51 % + P(rien) 93.0 % x 0.93 % ne couvrent pas P(stop) 7.0 % x 12.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+37.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 14.636 %) — p(stop avant cible) 0.0292 [0.02 ; 0.05], R/R 2.511, perte reelle 14.938 % (gap inclus), EV 0.0753 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.53 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 16.727 %) — p(stop avant cible) 0.0099 [0.00 ; 0.02], R/R 2.172, perte reelle 17.269 % (gap inclus), EV 0.117 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.99 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 18.818 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 1.904, perte reelle 19.7 % (gap inclus), EV 0.1501 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.68 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 20.908 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 1.653, perte reelle 22.693 % (gap inclus), EV 0.1582 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.53 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.999 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.567, perte reelle 23.94 % (gap inclus), EV 0.162 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.49 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 25.09 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 1.495, perte reelle 25.09 % (gap inclus), EV 0.1641 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.44 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 27.181 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.38, perte reelle 27.181 % (gap inclus), EV 0.167 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.37 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 29.272 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.281, perte reelle 29.272 % (gap inclus), EV 0.167 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.37 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 31.363 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.196, perte reelle 31.363 % (gap inclus), EV 0.167 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.37 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 33.454 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.121, perte reelle 33.454 % (gap inclus), EV 0.167 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.37 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 118.8, ATR14 4.9679 (4.182 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 1.455 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.209 % | 118.5516 | 87.75 % | 91.56 % | 93.32 % | 95.18 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.418 % | 118.3032 | 81.86 % | 87.83 % | 90.47 % | 93.21 % | 95.55 % | 96.9 % |
| 0.15 ATR | 0.627 % | 118.0548 | 75.29 % | 83.61 % | 87.03 % | 90.26 % | 94.07 % | 95.6 % |
| 0.2 ATR | 0.836 % | 117.8064 | 68.33 % | 78.02 % | 82.91 % | 88.09 % | 92.68 % | 94.91 % |
| 0.25 ATR | 1.045 % | 117.558 | 61.96 % | 73.6 % | 78.88 % | 85.14 % | 90.7 % | 93.71 % |
| 0.35 ATR | 1.464 % | 117.0613 | 49.71 % | 64.28 % | 71.71 % | 79.04 % | 86.94 % | 91.61 % |
| 0.5 ATR | 2.091 % | 116.3161 | 34.61 % | 52.7 % | 61.3 % | 71.16 % | 80.32 % | 87.51 % |
| 0.75 ATR | 3.136 % | 115.0741 | 20.69 % | 36.41 % | 47.54 % | 58.96 % | 70.23 % | 81.12 % |
| 1.0 ATR | 4.182 % | 113.8321 | 10.88 % | 24.44 % | 34.77 % | 48.23 % | 61.33 % | 74.33 % |
| 1.25 ATR | 5.227 % | 112.5902 | 4.71 % | 16.49 % | 25.44 % | 39.67 % | 54.6 % | 67.83 % |
| 1.5 ATR | 6.273 % | 111.3482 | 2.45 % | 11.48 % | 19.16 % | 30.91 % | 47.28 % | 60.64 % |
| 2.0 ATR | 8.363 % | 108.8643 | 0.78 % | 5.5 % | 10.22 % | 19.49 % | 35.31 % | 50.65 % |
| 2.5 ATR | 10.454 % | 106.3804 | 0.49 % | 2.45 % | 5.4 % | 11.32 % | 24.53 % | 39.06 % |
| 3.0 ATR | 12.545 % | 103.8964 | 0.2 % | 1.57 % | 3.14 % | 7.19 % | 17.51 % | 30.87 % |
| 4.0 ATR | 16.727 % | 98.9286 | 0.1 % | 0.49 % | 0.88 % | 1.97 % | 7.52 % | 18.78 % |
| 6.0 ATR | 25.09 % | 88.9929 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.5 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.77 ATR | 1.04 ATR | 1.24 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.62 ATR | 2.08 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.80 ATR | 1.05 ATR | 1.27 ATR | 1.47 ATR | 2.02 ATR | 2.59 ATR |
| **5 s.** | 0.43 ATR | 0.96 ATR | 1.09 ATR | 1.44 ATR | 1.76 ATR | 1.98 ATR | 2.66 ATR | 3.42 ATR |
| **10 s.** | 0.63 ATR | 1.41 ATR | 1.59 ATR | 2.11 ATR | 2.48 ATR | 2.82 ATR | 3.75 ATR | 4.81 ATR |
| **20 s.** | 0.97 ATR | 2.03 ATR | 2.24 ATR | 2.87 ATR | 3.49 ATR | 3.90 ATR | 5.23 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.397 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (77.8 % des re-echantillons)
- **2 seance(s)** : plage utile 0.618–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.136 %, prix 115.0744), p(touche) 36.41 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.8–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.182 %, prix 113.8318), p(touche) 34.77 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.094–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.227 %, prix 112.5903), p(touche) 39.67 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.595–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.363 %, prix 108.8648), p(touche) 35.31 % (en stress 98.04 %)  ✅ optimum identifie (68.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.244–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.454 %, prix 106.3807), p(touche) 39.06 % (en stress 98.02 %)  ✅ optimum identifie (63.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.066 | EV/share : €-0.605 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 1 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.6 | bear 16.6 | side 71.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→65% · +1.0%→52% · +2.0%→22% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.94% (p90 4.66%) · excursion haute méd. +1.05% / basse méd. −1.41%
- Profil de vol intra : ouverture 1.742% vs midi 0.526% vs clôture 0.695% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.944% ; recovery-V 13%
- **σ réalisé intraday** 2.228% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 71% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 113.2062 (VA 112.9812–114.2188 ; dernier close 113.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 52% · **stop −2.11%** sous le fill (sous le bruit) · cible +1.29% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 28% (gap-down >1% 9% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −1.83%) · haut méd +0.2% · range méd 1.01%
- Excursion ouverture 15min (n=160) : bas méd −0.77% (p90 −2.19%) · haut méd +0.36% · range méd 1.31%
- Excursion ouverture 30min (n=160) : bas méd −0.78% (p90 −2.35%) · haut méd +0.37% · range méd 1.59%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.75%) · haut méd +0.57% · range méd 1.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 113.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 63% (90/159) · gap 13% · délai 0.8min · rebond 38% (37/90) (MFE +0.64%)
   - −1.0% : fill 30min 29% · séance 54% (74/159) · gap 9% · délai 21.4min · rebond 31% (27/74) (MFE +0.58%)
   - −1.5% : fill 30min 22% · séance 43% (59/159) · gap 0% · délai 27.4min · rebond 30% (19/59) (MFE +0.58%)
   - −2.0% : fill 30min 14% · séance 34% (43/159) · gap 0% · délai 56.6min · rebond 26% (14/43) (MFE +0.54%)
   - −3.0% : fill 30min 8% · séance 20% (26/159) · gap 0% · délai 101.3min · rebond 52% (13/26) (MFE +1.29%)
   - −4.0% : fill 30min 4% · séance 12% (12/159) · gap 0% · délai 107.9min · rebond 28% (2/12) (MFE +0.49%)
   - −5.0% : fill 30min 0% · séance 4% (4/159) · gap 0% · délai 119.3min · rebond 58% (2/4) (MFE +1.2%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.16% (p90 −1.31%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.79%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.78%) → stop au-delà de −0.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=328 jambes) : jambe baissière méd −1.12% (p90 −2.37%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (25 séances) :
      · −1.0% : fill 88% (21/25) · rebond 23% (7/21)
      · −2.0% : fill 69% (15/25) · rebond 19% (3/15)
      · −3.0% : fill 51% (11/25) · rebond 43% (4/11)
      · −4.0% : fill 41% (8/25) · rebond 46% (2/8)
      · −5.0% : fill 11% (3/25) · rebond 20% (1/3)
   - **flat** (35 séances) :
      · −1.0% : fill 57% (20/35) · rebond 23% (6/20)
      · −2.0% : fill 30% (12/35) · rebond 24% (4/12)
      · −3.0% : fill 22% (8/35) · rebond 22% (3/8)
      · −4.0% : fill 12% (3/35) · rebond 0% (0/3)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (99 séances) :
      · −1.0% : fill 43% (33/99) · rebond 39% (14/33)
      · −2.0% : fill 24% (16/99) · rebond 35% (7/16)
      · −3.0% : fill 10% (7/99) · rebond 92% (6/7)
      · −4.0% : fill 3% (1/99) · rebond 0% (0/1)
      · −5.0% : fill 3% (1/99) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 61% si les 15 1res min sont vertes (82 cas) · 20% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **19min** → P(séance verte=clôture>ouverture) 71% si début vert vs 14% si rouge (base 40% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 299min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **71%** · continue >prix actuel 61% ; creux résiduel méd -0.98% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.09% / q75 +1.87% → **scale +1.09% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **14%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.11%** (au-delà de la MAE q10 -3.11%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.81% .. +1.6%] · haut q95 +2.12% · bas q05 -3.19%
   - 60min (n=160) : retour [-2.91% .. +2.05%] · haut q95 +2.46% · bas q05 -3.43%
   - 2h (n=160) : retour [-3.54% .. +2.1%] · haut q95 +2.53% · bas q05 -3.73%
   - 4h (n=160) : retour [-3.23% .. +2.19%] · haut q95 +2.93% · bas q05 -3.86%
   - 6h (n=160) : retour [-3.81% .. +3.34%] · haut q95 +3.4% · bas q05 -4.16%
   - session (n=160) : retour [-3.59% .. +2.46%] · haut q95 +3.6% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.4  _(neutre)_
- **ADX** : 13.3  _(pas de tendance nette)_
- **MACD** : hist -0.317  _(bearish_recent)_
- **BB** : %B 0.17 · largeur 14.3%
- **ATR** : 4.97 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.099  _(distribution)_
- **Vol ratio** : 0.27  _(volume atone)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 124.67 · MA50 127.95 · MA200 135.09  _(prix < MA20)_
- **Dist MA** : MA20 -4.7% · MA50 -7.2% · MA200 -12.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (506271 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
