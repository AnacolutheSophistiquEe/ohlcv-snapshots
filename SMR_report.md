# SMR

**Generated** : 2026-10-22T00:27:29.306027+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $5.50  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 12/125 fenêtres (p_fill pondéré 7 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $5.50 (+9.6% vs entrée) · entrée $5.02 · stop $4.87 · T1 $5.26 · R/R 1.6  
> ↳ ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.9% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +7.5 % ≠ (strike 6.0 − spot 5.50)/spot = +9.1 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.45). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-21 : 5.5 · ATR Wilder 0.518 (9.42 %)_
- **Swing** : plage **4.89 → 4.56** (-11.08 % a -17.13 % sous la cloture, 0.64 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 4.61-4.69 (C). stop INDICATIF 4.04 (-11.36 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **4.56 → 3.71** (-17.13 % a -32.58 % sous la cloture, 1.64 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 3.76-3.79 (A). stop INDICATIF 3.22 (-13.14 % sous le bas ; sous le support 3.48-3.65 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.14 ATR sous le plus haut 20 s., RSI(2) 7.8. Limite **5.24** (seance suivante), stop catastrophe 3.17, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 4.61-4.69 (C, -14.73 %) ; 3.76-3.79 (A, -31.09 %) ; 3.48-3.65 (B, -33.64 %) ; 3.18-3.22 (B, -41.45 %) ; 2.8-3.01 (B, -45.27 %) ; 2.45-2.55 (B, -53.62 %)
- Resistances reelles au-dessus : 6.35-6.36 (B, 15.45 %) ; 6.88-6.88 (C, 25.09 %) ; 7.21-7.37 (A, 31.09 %) ; 7.81-8.05 (A, 42.0 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.70 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (26.43 %)** : le gap seul le franchit 0.086 % des séances (1 fois sur 1165).
   - exécution **3.893 pt plus bas** dans le cas TYPIQUE (médiane), 3.893 au p90, **3.893 au pire**
   - perte réelle **30.323 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 26.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0033 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.582 % | p01 -6.957 % | pire -30.323 % _(sur 1165 séances)_
- **P(stop avant cible)** _(source : daily, 1166 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5121** [0.438 ; 0.5858] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3761** [0.3262 ; 0.428] _(largeur 10.2 pt, n_eff 345.4)_
   - deep : **0.3066** [0.2597 ; 0.3567] _(largeur 9.7 pt, n_eff 345.4)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.03 %** | vol 6.83 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.26 % contre 5.65 % aujourd'hui, rapport 1.99)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.22 % vs -18.74 % si l'on extrapolait par √5 _(rapport 1.026 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6054** (β de hausse 1.3893, asymétrie 1.1555) vs IWM — 556 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.027× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 5.2577 sur atr_grid (0.5 ATR, 4.406 %) — p(stop avant cible) 0.7654 [0.72 ; 0.81], R/R 2.622, perte reelle 4.552 % (gap inclus), CVaR 6.527 %, EV -0.8793 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5948 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.765, borne haute 0.808 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 13.218 %) — p(stop avant cible) 0.4365 [0.38 ; 0.49], R/R 0.895, perte reelle 13.338 % (gap inclus), EV -1.2515 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 41.7 % x 11.93 % + P(rien) 14.6 % x -2.78 % ne couvrent pas P(stop) 43.6 % x 13.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.203 %) — p(stop avant cible) 0.8676 [0.83 ; 0.90], R/R 5.218, perte reelle 2.287 % (gap inclus), EV -0.4919 % — **REFUSE**
      - refuse : cible atteinte seulement 12.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.868, borne haute 0.900 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 12.5 % x 11.93 % + P(rien) 0.8 % x 0.37 % ne couvrent pas P(stop) 86.8 % x 2.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 4.406 %) — p(stop avant cible) 0.7654 [0.72 ; 0.81], R/R 2.622, perte reelle 4.552 % (gap inclus), EV -0.8793 % — **REFUSE**
      - refuse : p_stop_first 0.765, borne haute 0.808 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 21.6 % x 11.93 % + P(rien) 1.9 % x 1.62 % ne couvrent pas P(stop) 76.5 % x 4.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 6.609 %) — p(stop avant cible) 0.6721 [0.62 ; 0.72], R/R 1.76, perte reelle 6.781 % (gap inclus), EV -1.0383 % — **REFUSE**
      - refuse : p_stop_first 0.672, borne haute 0.720 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 29.0 % x 11.93 % + P(rien) 3.8 % x 1.50 % ne couvrent pas P(stop) 67.2 % x 6.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 8.812 %) — p(stop avant cible) 0.587 [0.53 ; 0.64], R/R 1.332, perte reelle 8.96 % (gap inclus), EV -1.1098 % — **REFUSE**
      - refuse : p_stop_first 0.587, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 34.7 % x 11.93 % + P(rien) 6.6 % x 0.10 % ne couvrent pas P(stop) 58.7 % x 8.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 11.015 %) — p(stop avant cible) 0.4966 [0.44 ; 0.55], R/R 1.073, perte reelle 11.118 % (gap inclus), EV -1.1679 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 38.8 % x 11.93 % + P(rien) 11.6 % x -2.34 % ne couvrent pas P(stop) 49.7 % x 11.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 15.42 %) — p(stop avant cible) 0.3473 [0.30 ; 0.40], R/R 0.768, perte reelle 15.537 % (gap inclus), EV -1.2754 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 43.1 % x 11.93 % + P(rien) 22.1 % x -4.65 % ne couvrent pas P(stop) 34.7 % x 15.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 17.623 %) — p(stop avant cible) 0.2833 [0.24 ; 0.33], R/R 0.67, perte reelle 17.815 % (gap inclus), EV -1.2805 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 44.1 % x 11.93 % + P(rien) 27.6 % x -5.41 % ne couvrent pas P(stop) 28.3 % x 17.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 19.826 %) — p(stop avant cible) 0.2062 [0.17 ; 0.25], R/R 0.594, perte reelle 20.092 % (gap inclus), EV -1.168 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 44.3 % x 11.93 % + P(rien) 35.0 % x -6.61 % ne couvrent pas P(stop) 20.6 % x 20.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 22.029 %) — p(stop avant cible) 0.1728 [0.14 ; 0.22], R/R 0.539, perte reelle 22.138 % (gap inclus), EV -1.2282 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 44.4 % x 11.93 % + P(rien) 38.3 % x -7.05 % ne couvrent pas P(stop) 17.3 % x 22.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 24.232 %) — p(stop avant cible) 0.139 [0.11 ; 0.18], R/R 0.487, perte reelle 24.49 % (gap inclus), EV -1.2831 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 44.6 % x 11.93 % + P(rien) 41.5 % x -7.72 % ne couvrent pas P(stop) 13.9 % x 24.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 26.435 %) — p(stop avant cible) 0.0974 [0.07 ; 0.13], R/R 0.442, perte reelle 27.0 % (gap inclus), EV -1.1599 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 44.7 % x 11.93 % + P(rien) 45.6 % x -8.47 % ne couvrent pas P(stop) 9.7 % x 27.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 30.841 %) — p(stop avant cible) 0.0582 [0.04 ; 0.09], R/R 0.384, perte reelle 31.071 % (gap inclus), EV -1.2517 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 44.7 % x 11.93 % + P(rien) 49.5 % x -9.64 % ne couvrent pas P(stop) 5.8 % x 31.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 35.247 %) — p(stop avant cible) 0.0243 [0.01 ; 0.04], R/R 0.338, perte reelle 35.31 % (gap inclus), EV -1.1493 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 44.7 % x 11.93 % + P(rien) 52.9 % x -10.63 % ne couvrent pas P(stop) 2.4 % x 35.31 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 39.653 %) — p(stop avant cible) 0.0152 [0.01 ; 0.03], R/R 0.3, perte reelle 39.802 % (gap inclus), EV -1.2061 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 44.7 % x 11.93 % + P(rien) 53.8 % x -11.03 % ne couvrent pas P(stop) 1.5 % x 39.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 44.058 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 0.27, perte reelle 44.12 % (gap inclus), EV -1.1898 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 44.7 % x 11.93 % + P(rien) 54.3 % x -11.18 % ne couvrent pas P(stop) 1.0 % x 44.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 48.464 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.241, perte reelle 49.574 % (gap inclus), EV -1.1988 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 44.7 % x 11.93 % + P(rien) 55.1 % x -11.67 % ne couvrent pas P(stop) 0.2 % x 49.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 52.87 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.226, perte reelle 52.87 % (gap inclus), EV -1.1916 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 44.7 % x 11.93 % + P(rien) 55.3 % x -11.79 % ne couvrent pas P(stop) 0.0 % x 52.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 57.276 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.208, perte reelle 57.276 % (gap inclus), EV -1.1919 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 44.7 % x 11.93 % + P(rien) 55.3 % x -11.79 % ne couvrent pas P(stop) 0.0 % x 57.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 61.682 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.193, perte reelle 61.682 % (gap inclus), EV -1.1919 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 44.7 % x 11.93 % + P(rien) 55.3 % x -11.79 % ne couvrent pas P(stop) 0.0 % x 61.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 66.088 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.181, perte reelle 66.088 % (gap inclus), EV -1.1919 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 44.7 % x 11.93 % + P(rien) 55.3 % x -11.79 % ne couvrent pas P(stop) 0.0 % x 66.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 70.493 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.169, perte reelle 70.493 % (gap inclus), EV -1.1919 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 44.7 % x 11.93 % + P(rien) 55.3 % x -11.79 % ne couvrent pas P(stop) 0.0 % x 70.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 5.5, ATR14 0.4846 (8.812 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.426 ATR = 3.754 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.441 % | 5.4758 | 92.6 % | 95.13 % | 96.35 % | 97.11 % | 97.99 % | 98.42 % |
| 0.1 ATR | 0.881 % | 5.4515 | 86.96 % | 91.37 % | 93.36 % | 94.78 % | 96.32 % | 97.52 % |
| 0.15 ATR | 1.322 % | 5.4273 | 80.88 % | 87.17 % | 89.81 % | 91.9 % | 94.08 % | 96.16 % |
| 0.2 ATR | 1.762 % | 5.4031 | 75.14 % | 82.85 % | 86.6 % | 89.46 % | 92.52 % | 95.15 % |
| 0.25 ATR | 2.203 % | 5.3788 | 69.94 % | 79.76 % | 84.05 % | 87.35 % | 90.85 % | 94.02 % |
| 0.35 ATR | 3.084 % | 5.3304 | 58.12 % | 72.23 % | 77.63 % | 83.02 % | 87.83 % | 91.65 % |
| 0.5 ATR | 4.406 % | 5.2577 | 42.1 % | 59.18 % | 67.33 % | 74.36 % | 83.48 % | 88.71 % |
| 0.75 ATR | 6.609 % | 5.1365 | 20.66 % | 37.61 % | 47.84 % | 60.16 % | 72.77 % | 81.38 % |
| 1.0 ATR | 8.812 % | 5.0154 | 11.27 % | 26.11 % | 36.1 % | 49.83 % | 65.07 % | 75.62 % |
| 1.25 ATR | 11.015 % | 4.8942 | 4.64 % | 16.26 % | 25.47 % | 38.85 % | 55.36 % | 69.3 % |
| 1.5 ATR | 13.218 % | 4.773 | 2.21 % | 9.96 % | 16.61 % | 28.75 % | 46.09 % | 62.64 % |
| 2.0 ATR | 17.623 % | 4.5307 | 0.33 % | 3.21 % | 6.76 % | 15.09 % | 31.58 % | 49.55 % |
| 2.5 ATR | 22.029 % | 4.2884 | 0.11 % | 1.33 % | 3.1 % | 7.44 % | 20.87 % | 38.71 % |
| 3.0 ATR | 26.435 % | 4.0461 | 0.11 % | 0.55 % | 1.88 % | 4.11 % | 12.17 % | 29.01 % |
| 4.0 ATR | 35.247 % | 3.5614 | 0.0 % | 0.22 % | 0.33 % | 1.22 % | 5.02 % | 14.0 % |
| 6.0 ATR | 52.87 % | 2.5921 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.33 % | 1.58 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.61 ATR | 0.66 ATR | 0.85 ATR | 1.03 ATR | 1.16 ATR | 1.50 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.84 ATR | 2.24 ATR |
| **5 s.** | 0.49 ATR | 1.00 ATR | 1.11 ATR | 1.40 ATR | 1.64 ATR | 1.82 ATR | 2.33 ATR | 2.87 ATR |
| **10 s.** | 0.70 ATR | 1.40 ATR | 1.54 ATR | 1.95 ATR | 2.31 ATR | 2.55 ATR | 3.30 ATR | 4.01 ATR |
| **20 s.** | 1.02 ATR | 1.98 ATR | 2.21 ATR | 2.79 ATR | 3.27 ATR | 3.60 ATR | 4.64 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.473–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.406 %, prix 5.2577), p(touche) 42.1 % (en stress 82.42 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.664–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.609 %, prix 5.1365), p(touche) 37.61 % (en stress 89.01 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (73.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.81–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.812 %, prix 5.0153), p(touche) 36.1 % (en stress 90.11 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.11–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (11.015 %, prix 4.8942), p(touche) 38.85 % (en stress 95.6 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.538–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.21–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.005 | EV/share : $0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 — | T3 —
- Kelly (position) : f* 0.008 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 26.8 | bear 58.8 | side 14.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=10))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→62% · +3.0%→54% · +5.0%→34% · +8.0%→14%
- Range intraday médian 7.02% (p90 12.09%) · excursion haute méd. +3.23% / basse méd. −3.1%
- Profil de vol intra : ouverture 4.766% vs midi 1.404% vs clôture 1.695% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.568% ; recovery-V 32%
- **σ réalisé intraday** 4.046% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 62% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 7.8201 (VA 7.7996–7.8714 ; dernier close 7.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 45% · rebond 75% · **stop −4.75%** sous le fill (sous le bruit) · cible +2.64% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.3% · baisse 53% (gap-down >1% 35% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.94%) · haut méd +1.32% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −4.33%) · haut méd +1.53% · range méd 3.57%
- Excursion ouverture 30min (n=160) : bas méd −1.69% (p90 −4.84%) · haut méd +1.7% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −2.12% (p90 −5.34%) · haut méd +2.25% · range méd 4.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (127/159) · gap 48% · délai 0.0min · rebond 60% (77/127) (MFE +1.63%)
   - −1.0% : fill 30min 63% · séance 75% (121/159) · gap 36% · délai 0.0min · rebond 62% (75/121) (MFE +1.79%)
   - −1.5% : fill 30min 60% · séance 72% (115/159) · gap 26% · délai 0.1min · rebond 67% (80/115) (MFE +1.81%)
   - −2.0% : fill 30min 52% · séance 64% (105/159) · gap 22% · délai 1.0min · rebond 61% (69/105) (MFE +1.75%)
   - −3.0% : fill 30min 40% · séance 52% (90/159) · gap 10% · délai 4.8min · rebond 74% (69/90) (MFE +1.92%)
   - −4.0% : fill 30min 31% · séance 45% (79/159) · gap 4% · délai 7.8min · rebond 75% (60/79) (MFE +2.64%)
   - −5.0% : fill 30min 19% · séance 34% (60/159) · gap 2% · délai 23.4min · rebond 76% (44/60) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.48%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.29%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.99% (p90 −2.71%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1089 jambes) : jambe baissière méd −1.28% (p90 −3.12%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 96% (83/86) · rebond 59% (51/83)
      · −2.0% : fill 89% (78/86) · rebond 68% (56/78)
      · −3.0% : fill 83% (73/86) · rebond 79% (59/73)
      · −4.0% : fill 70% (63/86) · rebond 82% (51/63)
      · −5.0% : fill 53% (47/86) · rebond 80% (37/47)
   - **flat** (11 séances) :
      · −1.0% : fill 94% (9/11) · rebond 66% (5/9)
      · −2.0% : fill 52% (6/11) · rebond 39% (2/6)
      · −3.0% : fill 52% (6/11) · rebond 50% (3/6)
      · −4.0% : fill 52% (6/11) · rebond 62% (4/6)
      · −5.0% : fill 39% (4/11) · rebond 78% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 49% (29/62) · rebond 70% (19/29)
      · −2.0% : fill 36% (21/62) · rebond 46% (11/21)
      · −3.0% : fill 15% (11/62) · rebond 49% (7/11)
      · −4.0% : fill 14% (10/62) · rebond 41% (5/10)
      · −5.0% : fill 11% (9/62) · rebond 49% (4/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 72% si les 15 1res min sont vertes (73 cas) · 29% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 84% si début vert vs 19% si rouge (base 47% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 222min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **84%** · continue >prix actuel 59% ; creux résiduel méd -1.71% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.66% / q75 +4.53% → **scale +2.66% / runner +4.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **19%** (continue à baisser 53%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.68% .. +4.36%] · haut q95 +6.14% · bas q05 -5.36%
   - 60min (n=160) : retour [-5.02% .. +4.72%] · haut q95 +6.47% · bas q05 -5.85%
   - 2h (n=160) : retour [-7.52% .. +5.37%] · haut q95 +7.8% · bas q05 -7.94%
   - 4h (n=160) : retour [-7.67% .. +6.92%] · haut q95 +8.32% · bas q05 -9.19%
   - 6h (n=160) : retour [-6.72% .. +8.0%] · haut q95 +9.66% · bas q05 -9.21%
   - session (n=160) : retour [-7.99% .. +8.0%] · haut q95 +10.29% · bas q05 -9.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.36 · part idiosyncratique 0.64
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 18.3  _(survente)_
- **ADX** : 32.0  _(tendance etablie)_
- **MACD** : hist -0.144  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 57.0%
- **ATR** : 0.48 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.348  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 30.4  _(marche directionnel)_
- **MA** : MA20 7.08 · MA50 8.41 · MA200 11.34  _(prix < MA20)_
- **Dist MA** : MA20 -22.3% · MA50 -34.6% · MA200 -51.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (769035 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
