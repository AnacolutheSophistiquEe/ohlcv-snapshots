# CEG

**Generated** : 2026-11-23T01:28:15.017273+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $237.41  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $237.41 (+6.5% vs entrée) · entrée $222.94 · stop $205.10 · T1 $230.17 · R/R 0.41  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-20 : 237.41 · ATR Wilder 13.3 (5.6 %)_
- **Swing** : plage **218.82 → 208.96** (-7.83 % a -11.98 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 215.8-227.93 (B). stop INDICATIF 193.82 (-7.25 % sous le bas ; sous le support 200.47-206.48 (- 0,5 ATR)).
- **Deep** : plage **208.96 → 184.53** (-11.98 % a -22.28 % sous la cloture, 1.84 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 200.47-206.48 (B) ; 193.29-196.52 (B) ; 186.2-192.79 (A). stop INDICATIF 171.8 (-6.9 % sous le bas ; sous le support 178.45-182.19 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 3.54 ATR sous le plus haut 20 s., RSI(2) 1.0. Limite **230.76** (seance suivante), stop catastrophe 177.55, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 224.39-230.95 (A, -2.72 %) ; 215.8-227.93 (B, -3.99 %) ; 200.47-206.48 (B, -13.03 %) ; 193.29-196.52 (B, -17.22 %) ; 186.2-192.79 (A, -18.79 %) ; 178.45-182.19 (B, -23.26 %)
- Resistances reelles au-dessus : 246.82-250.17 (A, 3.96 %) ; 255.32-259.88 (A, 7.54 %) ; 263.52-268.31 (A, 11.0 %) ; 275.57-281.91 (A, 16.07 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.06 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (18.29 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1215).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.29 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -4.443 % | pire -15.824 % _(sur 1215 séances)_
- **P(stop avant cible)** _(source : daily, 1216 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0066** [0.0008 ; 0.0282] _(largeur 2.7 pt, n_eff 173.1)_
   - swing : **0.2906** [0.2446 ; 0.3401] _(largeur 9.5 pt, n_eff 345.6)_
   - deep : **0.2485** [0.2052 ; 0.296] _(largeur 9.1 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.75 %** | CVaR **-6.94 %** | vol 3.18 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 5.66 % contre 2.98 % aujourd'hui, rapport 1.90)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.15 % vs -9.84 % si l'on extrapolait par √5 _(rapport 1.032 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1652** (β de hausse 1.1947, asymétrie 0.9753) vs SPY — 565 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.797× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 219.3178 sur atr_grid (1.25 ATR, 7.621 %) — p(stop avant cible) 0.4169 [0.37 ; 0.47], R/R 7.354, perte reelle 7.769 % (gap inclus), CVaR 8.857 %, EV -0.5231 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.65 ATR (stop 6.813 %) — p(stop avant cible) 0.4717 [0.42 ; 0.52], R/R 8.177, perte reelle 6.987 % (gap inclus), EV -0.5443 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.0 % x 57.13 % + P(rien) 52.8 % x 5.21 % ne couvrent pas P(stop) 47.2 % x 6.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 9.145 %) — p(stop avant cible) 0.3556 [0.31 ; 0.41], R/R 6.18, perte reelle 9.245 % (gap inclus), EV -0.7231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 0.0 % x 57.13 % + P(rien) 64.4 % x 3.98 % ne couvrent pas P(stop) 35.6 % x 9.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.524 %) — p(stop avant cible) 0.8782 [0.84 ; 0.91], R/R 33.973, perte reelle 1.682 % (gap inclus), EV -0.3945 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 33.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.878, borne haute 0.909 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.0 % x 57.13 % + P(rien) 12.2 % x 8.89 % ne couvrent pas P(stop) 87.8 % x 1.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.65 ATR (stop 5.77 %) — p(stop avant cible) 0.5453 [0.49 ; 0.60], R/R 9.639, perte reelle 5.927 % (gap inclus), EV -0.5011 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 0.0 % x 57.13 % + P(rien) 45.5 % x 6.01 % ne couvrent pas P(stop) 54.5 % x 5.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 7.621 %) — p(stop avant cible) 0.4169 [0.37 ; 0.47], R/R 7.354, perte reelle 7.769 % (gap inclus), EV -0.5231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 0.0 % x 57.13 % + P(rien) 58.3 % x 4.66 % ne couvrent pas P(stop) 41.7 % x 7.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 10.669 %) — p(stop avant cible) 0.2717 [0.23 ; 0.32], R/R 5.307, perte reelle 10.764 % (gap inclus), EV -0.5918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.0 % x 57.13 % + P(rien) 72.8 % x 3.20 % ne couvrent pas P(stop) 27.2 % x 10.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 12.193 %) — p(stop avant cible) 0.2008 [0.16 ; 0.25], R/R 4.656, perte reelle 12.271 % (gap inclus), EV -0.3579 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.0 % x 57.13 % + P(rien) 79.9 % x 2.64 % ne couvrent pas P(stop) 20.1 % x 12.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 13.717 %) — p(stop avant cible) 0.1502 [0.12 ; 0.19], R/R 4.149, perte reelle 13.77 % (gap inclus), EV -0.2551 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 0.0 % x 57.13 % + P(rien) 85.0 % x 2.13 % ne couvrent pas P(stop) 15.0 % x 13.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 15.241 %) — p(stop avant cible) 0.1001 [0.07 ; 0.14], R/R 3.743, perte reelle 15.263 % (gap inclus), EV -0.1711 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 57.13 % + P(rien) 90.0 % x 1.51 % ne couvrent pas P(stop) 10.0 % x 15.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 16.765 %) — p(stop avant cible) 0.0531 [0.03 ; 0.08], R/R 3.399, perte reelle 16.81 % (gap inclus), EV -0.0702 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.0 % x 57.13 % + P(rien) 94.7 % x 0.87 % ne couvrent pas P(stop) 5.3 % x 16.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 18.29 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 3.097, perte reelle 18.448 % (gap inclus), EV -0.0811 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 57.13 % + P(rien) 96.3 % x 0.63 % ne couvrent pas P(stop) 3.7 % x 18.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+57.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 21.338 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 2.675, perte reelle 21.356 % (gap inclus), EV 0.0483 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.07 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 24.386 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 2.343, perte reelle 24.386 % (gap inclus), EV 0.0699 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.04 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 27.434 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 2.079, perte reelle 27.484 % (gap inclus), EV 0.0604 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.483 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.874, perte reelle 30.483 % (gap inclus), EV 0.0706 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.531 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 1.704, perte reelle 33.531 % (gap inclus), EV 0.0708 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.03 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.579 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.562, perte reelle 36.579 % (gap inclus), EV 0.0717 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.627 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.442, perte reelle 39.627 % (gap inclus), EV 0.0717 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 42.676 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.339, perte reelle 42.676 % (gap inclus), EV 0.0717 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 45.724 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.249, perte reelle 45.724 % (gap inclus), EV 0.0717 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 48.772 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.171, perte reelle 48.772 % (gap inclus), EV 0.0717 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 237.41, ATR14 14.4737 (6.097 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.391 ATR = 2.384 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.305 % | 236.6863 | 91.83 % | 94.76 % | 95.7 % | 96.74 % | 97.67 % | 98.08 % |
| 0.1 ATR | 0.61 % | 235.9626 | 85.76 % | 90.67 % | 92.65 % | 94.22 % | 95.77 % | 96.9 % |
| 0.15 ATR | 0.914 % | 235.2389 | 79.16 % | 86.48 % | 88.67 % | 90.85 % | 93.97 % | 95.62 % |
| 0.2 ATR | 1.219 % | 234.5153 | 72.15 % | 81.13 % | 84.37 % | 87.07 % | 91.54 % | 94.34 % |
| 0.25 ATR | 1.524 % | 233.7916 | 65.24 % | 75.47 % | 79.43 % | 83.28 % | 88.79 % | 92.41 % |
| 0.35 ATR | 2.134 % | 232.3442 | 54.14 % | 66.25 % | 71.77 % | 77.18 % | 84.46 % | 89.0 % |
| 0.5 ATR | 3.048 % | 230.1731 | 39.06 % | 53.14 % | 59.71 % | 66.67 % | 77.48 % | 83.44 % |
| 0.75 ATR | 4.572 % | 226.5547 | 20.42 % | 36.9 % | 45.54 % | 53.84 % | 67.44 % | 76.71 % |
| 1.0 ATR | 6.097 % | 222.9363 | 11.1 % | 24.11 % | 33.58 % | 43.74 % | 58.46 % | 70.51 % |
| 1.25 ATR | 7.621 % | 219.3178 | 5.65 % | 16.14 % | 24.45 % | 35.96 % | 52.22 % | 64.42 % |
| 1.5 ATR | 9.145 % | 215.6994 | 2.72 % | 10.69 % | 17.42 % | 29.13 % | 45.24 % | 58.23 % |
| 2.0 ATR | 12.193 % | 208.4625 | 0.84 % | 4.3 % | 9.13 % | 17.88 % | 31.61 % | 46.47 % |
| 2.5 ATR | 15.241 % | 201.2256 | 0.42 % | 2.2 % | 4.72 % | 10.94 % | 21.35 % | 36.65 % |
| 3.0 ATR | 18.29 % | 193.9888 | 0.0 % | 1.05 % | 2.73 % | 6.73 % | 15.22 % | 28.63 % |
| 4.0 ATR | 24.386 % | 179.515 | 0.0 % | 0.21 % | 0.84 % | 2.63 % | 6.87 % | 14.1 % |
| 6.0 ATR | 36.579 % | 150.5675 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.74 % | 2.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.30 ATR |
| **2 s.** | 0.26 ATR | 0.55 ATR | 0.62 ATR | 0.83 ATR | 0.98 ATR | 1.13 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.31 ATR | 0.67 ATR | 0.76 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.84 ATR | 0.97 ATR | 1.36 ATR | 1.68 ATR | 1.91 ATR | 2.61 ATR | 3.42 ATR |
| **10 s.** | 0.56 ATR | 1.33 ATR | 1.51 ATR | 1.95 ATR | 2.32 ATR | 2.61 ATR | 3.62 ATR | 4.61 ATR |
| **20 s.** | 0.82 ATR | 1.85 ATR | 2.08 ATR | 2.73 ATR | 3.25 ATR | 3.59 ATR | 4.72 ATR | 5.59 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.441–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.048 %, prix 230.1737), p(touche) 39.06 % (en stress 82.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.625–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.572 %, prix 226.5556), p(touche) 36.9 % (en stress 88.54 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.761–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.097 %, prix 222.9351), p(touche) 33.58 % (en stress 95.83 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.969–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.097 %, prix 222.9351), p(touche) 43.74 % (en stress 96.88 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.509–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.193 %, prix 208.4626), p(touche) 31.61 % (en stress 96.84 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (75.8 % des re-echantillons)
- **20 seance(s)** : plage utile 2.075–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.241 %, prix 201.2263), p(touche) 36.65 % (en stress 95.74 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (87.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.044 | EV/share : $-0.783 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 62.1 | bear 25.7 | side 12.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=3))
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.59 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.7  _(momentum baissier)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist -1.718  _(bearish_recent)_
- **BB** : %B 0.04 · largeur 19.8%
- **ATR** : 14.47 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.019  _(neutre)_
- **Vol ratio** : 1.4  _(volume normal)_
- **Choppiness** : 50.4  _(transition)_
- **MA** : MA20 261.29 · MA50 265.85 · MA200 277.41  _(prix < MA20)_
- **Dist MA** : MA20 -9.1% · MA50 -10.7% · MA200 -14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (685591 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
