# RHM

**Generated** : 2026-11-19T01:04:16.131467+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 0/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €743.70  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 4/125 fenêtres (p_fill pondéré 2 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €743.70 (+7.4% vs entrée) · entrée €692.73 · stop €677.44 · T1 €718.21 · R/R 1.67  
> ↳ ¼-Kelly 0.001 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.21% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.56). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 0/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-18 : 743.7 · ATR Wilder 43.68 (5.87 %)_
- **Swing** : plage **680.35 → 643.26** (-8.52 % a -13.51 % sous la cloture, 0.85 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 677.76-695.89 (A). stop INDICATIF 595.63 (-7.4 % sous le bas ; sous le support 617.47-627.13 (- 0,5 ATR)).
- **Deep** : plage **643.26 → 538.0** (-13.51 % a -27.66 % sous la cloture, 2.41 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 617.47-627.13 (C) ; 584.17-592.25 (A) ; 557.13-560.53 (C) ; 525.86-543.49 (B). stop INDICATIF 477.81 (-11.19 % sous le bas ; sous le support 499.65-520.14 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 7.25 ATR sous le plus haut 20 s., RSI(2) 5.2. Limite **721.86** (seance suivante), stop catastrophe 547.13, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 677.76-695.89 (A, -6.43 %) ; 617.47-627.13 (C, -15.67 %) ; 584.17-592.25 (A, -20.36 %) ; 557.13-560.53 (C, -24.63 %) ; 525.86-543.49 (B, -26.92 %) ; 499.65-520.14 (B, -30.06 %)
- Resistances reelles au-dessus : 909.0-928.8 (A, 22.23 %) ; 936.2-953.59 (A, 25.88 %) ; 976.0-987.1 (A, 31.24 %) ; 1006.4-1006.4 (B, 35.32 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.80 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (20.56 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **1.869 pt plus bas** dans le cas TYPIQUE (médiane), 1.869 au p90, **1.869 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 20.56 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0015 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.62 % | p01 -3.886 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3319** [0.265 ; 0.4044] _(largeur 13.9 pt, n_eff 173.1)_
   - swing : **0.2217** [0.1804 ; 0.2677] _(largeur 8.7 pt, n_eff 345.8)_
   - deep : **0.1914** [0.1526 ; 0.2353] _(largeur 8.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.76 %** | CVaR **-6.99 %** | vol 3.0 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 2.06 % contre 3.29 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.44 % vs -9.03 % si l'on extrapolait par √5 _(rapport 0.935 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5221** (β de hausse 0.5695, asymétrie 0.9168) vs GDAXI — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.134× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 692.7286 sur atr_grid (1.0 ATR, 6.854 %) — p(stop avant cible) 0.4738 [0.42 ; 0.53], R/R 6.272, perte reelle 7.659 % (gap inclus), CVaR 12.593 %, EV -1.1764 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0454 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 12.59 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.281 %) — p(stop avant cible) 0.2876 [0.24 ; 0.34], R/R 4.387, perte reelle 10.95 % (gap inclus), EV -1.3858 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 0.1 % x 48.04 % + P(rien) 71.2 % x 2.44 % ne couvrent pas P(stop) 28.8 % x 10.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.713 %) — p(stop avant cible) 0.8653 [0.83 ; 0.90], R/R 26.854, perte reelle 1.789 % (gap inclus), EV -0.13 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 26.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.865, borne haute 0.898 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.0 % x 48.04 % + P(rien) 13.5 % x 10.53 % ne couvrent pas P(stop) 86.5 % x 1.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 3.427 %) — p(stop avant cible) 0.7274 [0.68 ; 0.77], R/R 12.947, perte reelle 3.711 % (gap inclus), EV -0.5889 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.727, borne haute 0.772 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.0 % x 48.04 % + P(rien) 27.3 % x 7.74 % ne couvrent pas P(stop) 72.7 % x 3.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 5.14 %) — p(stop avant cible) 0.6173 [0.57 ; 0.67], R/R 8.451, perte reelle 5.685 % (gap inclus), EV -1.0454 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.0 % x 48.04 % + P(rien) 38.3 % x 6.44 % ne couvrent pas P(stop) 61.7 % x 5.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 6.854 %) — p(stop avant cible) 0.4738 [0.42 ; 0.53], R/R 6.272, perte reelle 7.659 % (gap inclus), EV -1.1764 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.1 % x 48.04 % + P(rien) 52.6 % x 4.61 % ne couvrent pas P(stop) 47.4 % x 7.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 8.567 %) — p(stop avant cible) 0.382 [0.33 ; 0.43], R/R 5.109, perte reelle 9.403 % (gap inclus), EV -1.3508 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 0.1 % x 48.04 % + P(rien) 61.7 % x 3.58 % ne couvrent pas P(stop) 38.2 % x 9.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 11.994 %) — p(stop avant cible) 0.2166 [0.18 ; 0.26], R/R 3.847, perte reelle 12.487 % (gap inclus), EV -1.3584 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 0.1 % x 48.04 % + P(rien) 78.3 % x 1.68 % ne couvrent pas P(stop) 21.7 % x 12.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 13.708 %) — p(stop avant cible) 0.1728 [0.14 ; 0.22], R/R 3.387, perte reelle 14.182 % (gap inclus), EV -1.4489 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 0.1 % x 48.04 % + P(rien) 82.7 % x 1.18 % ne couvrent pas P(stop) 17.3 % x 14.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 15.421 %) — p(stop avant cible) 0.1505 [0.12 ; 0.19], R/R 3.036, perte reelle 15.821 % (gap inclus), EV -1.5995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 0.1 % x 48.04 % + P(rien) 84.9 % x 0.89 % ne couvrent pas P(stop) 15.0 % x 15.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 17.134 %) — p(stop avant cible) 0.1176 [0.09 ; 0.15], R/R 2.745, perte reelle 17.501 % (gap inclus), EV -1.6571 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 0.1 % x 48.04 % + P(rien) 88.2 % x 0.42 % ne couvrent pas P(stop) 11.8 % x 17.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 18.848 %) — p(stop avant cible) 0.097 [0.07 ; 0.13], R/R 2.506, perte reelle 19.17 % (gap inclus), EV -1.7397 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 0.1 % x 48.04 % + P(rien) 90.2 % x 0.10 % ne couvrent pas P(stop) 9.7 % x 19.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 20.561 %) — p(stop avant cible) 0.0783 [0.05 ; 0.11], R/R 2.304, perte reelle 20.851 % (gap inclus), EV -1.8217 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 0.1 % x 48.04 % + P(rien) 92.1 % x -0.24 % ne couvrent pas P(stop) 7.8 % x 20.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 23.988 %) — p(stop avant cible) 0.031 [0.02 ; 0.05], R/R 1.976, perte reelle 24.316 % (gap inclus), EV -1.6787 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 0.1 % x 48.04 % + P(rien) 96.8 % x -0.98 % ne couvrent pas P(stop) 3.1 % x 24.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 27.415 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 1.752, perte reelle 27.415 % (gap inclus), EV -1.662 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.0 % x -1.44 % ne couvrent pas P(stop) 1.0 % x 27.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 30.842 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.558, perte reelle 30.842 % (gap inclus), EV -1.5803 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.8 % x -1.58 % ne couvrent pas P(stop) 0.1 % x 30.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 34.269 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.402, perte reelle 34.269 % (gap inclus), EV -1.536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.9 % x -1.57 % ne couvrent pas P(stop) 0.0 % x 34.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 37.696 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.274, perte reelle 37.696 % (gap inclus), EV -1.536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.9 % x -1.57 % ne couvrent pas P(stop) 0.0 % x 37.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 41.123 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.168, perte reelle 41.123 % (gap inclus), EV -1.536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.9 % x -1.57 % ne couvrent pas P(stop) 0.0 % x 41.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 44.549 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.078, perte reelle 44.549 % (gap inclus), EV -1.536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.9 % x -1.57 % ne couvrent pas P(stop) 0.0 % x 44.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 47.976 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.001, perte reelle 47.976 % (gap inclus), EV -1.536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.9 % x -1.57 % ne couvrent pas P(stop) 0.0 % x 47.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 51.403 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.935, perte reelle 51.403 % (gap inclus), EV -1.536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.9 % x -1.57 % ne couvrent pas P(stop) 0.0 % x 51.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 54.83 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.876, perte reelle 54.83 % (gap inclus), EV -1.536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 48.04 % + P(rien) 99.9 % x -1.57 % ne couvrent pas P(stop) 0.0 % x 54.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 743.7, ATR14 50.9714 (6.854 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.392 ATR = 2.687 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.343 % | 741.1514 | 89.64 % | 92.6 % | 93.77 % | 94.95 % | 97.31 % | 97.99 % |
| 0.1 ATR | 0.685 % | 738.6029 | 83.93 % | 88.55 % | 90.42 % | 91.98 % | 95.62 % | 96.68 % |
| 0.15 ATR | 1.028 % | 736.0543 | 76.73 % | 83.42 % | 86.26 % | 88.71 % | 93.33 % | 95.28 % |
| 0.2 ATR | 1.371 % | 733.5057 | 70.02 % | 78.87 % | 82.02 % | 85.54 % | 91.24 % | 93.67 % |
| 0.25 ATR | 1.713 % | 730.9572 | 62.43 % | 73.05 % | 76.88 % | 81.39 % | 88.66 % | 91.86 % |
| 0.35 ATR | 2.399 % | 725.86 | 53.55 % | 65.75 % | 71.05 % | 76.83 % | 85.97 % | 89.85 % |
| 0.5 ATR | 3.427 % | 718.2143 | 40.73 % | 55.18 % | 61.76 % | 69.6 % | 80.8 % | 84.82 % |
| 0.75 ATR | 5.14 % | 705.4714 | 23.57 % | 39.19 % | 47.63 % | 58.32 % | 71.34 % | 78.59 % |
| 1.0 ATR | 6.854 % | 692.7286 | 13.21 % | 27.15 % | 37.06 % | 49.21 % | 63.48 % | 72.36 % |
| 1.25 ATR | 8.567 % | 679.9857 | 7.69 % | 18.46 % | 26.98 % | 40.0 % | 55.52 % | 66.33 % |
| 1.5 ATR | 10.281 % | 667.2429 | 3.94 % | 13.43 % | 21.25 % | 32.38 % | 47.36 % | 59.3 % |
| 2.0 ATR | 13.708 % | 641.7571 | 1.78 % | 7.31 % | 12.75 % | 21.98 % | 35.82 % | 49.95 % |
| 2.5 ATR | 17.134 % | 616.2714 | 0.49 % | 3.46 % | 6.62 % | 12.97 % | 26.07 % | 40.3 % |
| 3.0 ATR | 20.561 % | 590.7857 | 0.1 % | 1.48 % | 4.05 % | 8.12 % | 18.31 % | 33.77 % |
| 4.0 ATR | 27.415 % | 539.8143 | 0.0 % | 0.39 % | 1.48 % | 3.66 % | 9.55 % | 21.41 % |
| 6.0 ATR | 41.123 % | 437.8714 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.39 % | 3.92 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.15 ATR | 1.43 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.88 ATR | 1.06 ATR | 1.21 ATR | 1.78 ATR | 2.30 ATR |
| **3 s.** | 0.28 ATR | 0.71 ATR | 0.81 ATR | 1.10 ATR | 1.34 ATR | 1.57 ATR | 2.22 ATR | 2.81 ATR |
| **5 s.** | 0.39 ATR | 0.98 ATR | 1.11 ATR | 1.48 ATR | 1.85 ATR | 2.11 ATR | 2.81 ATR | 3.70 ATR |
| **10 s.** | 0.65 ATR | 1.42 ATR | 1.60 ATR | 2.15 ATR | 2.57 ATR | 2.89 ATR | 3.95 ATR | 5.12 ATR |
| **20 s.** | 0.89 ATR | 2.00 ATR | 2.26 ATR | 3.06 ATR | 3.71 ATR | 4.16 ATR | 5.30 ATR | 5.88 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.45 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.659–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.14 %, prix 705.4738), p(touche) 39.19 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.812–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.854 %, prix 692.7268), p(touche) 37.06 % (en stress 96.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.114–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.567 %, prix 679.9872), p(touche) 40.0 % (en stress 97.03 %)  ✅ optimum identifie (77.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.602–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.708 %, prix 641.7536), p(touche) 35.82 % (en stress 95.05 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.256–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.134 %, prix 616.2745), p(touche) 40.3 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.001 | EV/share : €0.021 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 17 % | T2 — | T3 —
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.7 | bear 71.8 | side 22.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=5))
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.23 · part idiosyncratique 0.77
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 12.3  _(survente)_
- **ADX** : 32.5  _(tendance etablie)_
- **MACD** : hist -18.498  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 52.3%
- **ATR** : 50.97 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.211  _(distribution)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 31.3  _(marche directionnel)_
- **MA** : MA20 907.94 · MA50 957.99 · MA200 1204.07  _(prix < MA20)_
- **Dist MA** : MA20 -18.1% · MA50 -22.4% · MA200 -38.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (698547 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
