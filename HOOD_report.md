# HOOD

**Generated** : 2026-11-19T01:31:35.093945+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $69.16  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (18 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $69.16 (+2.1% vs entrée) · entrée $67.75 · stop $65.72 · T1 $70.34 · R/R 1.28  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-18 : 69.16 · ATR Wilder 5.06 (7.32 %)_
- **Swing** : plage **63.34 → 58.79** (-8.42 % a -14.99 % sous la cloture, 0.9 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 62.63-63.51 (B). stop INDICATIF 50.12 (-14.75 % sous le bas ; sous le support 52.65-54.84 (- 0,5 ATR)).
- **Deep** : plage **58.79 → 49.03** (-14.99 % a -29.11 % sous la cloture, 1.93 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 52.65-54.84 (B) ; 49.88-52.06 (B). stop INDICATIF 43.03 (-12.24 % sous le bas ; sous le support 45.56-48.08 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.36 ATR sous le plus haut 20 s., RSI(2) 3.6. Limite **66.63** (seance suivante), stop catastrophe 46.38, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 62.63-63.51 (B, -8.16 %) ; 52.65-54.84 (B, -20.71 %) ; 49.88-52.06 (B, -24.73 %) ; 45.56-48.08 (A, -30.48 %) ; 42.76-44.02 (B, -36.35 %) ; 39.21-40.47 (A, -41.49 %)
- Resistances reelles au-dessus : 72.79-74.59 (A, 5.26 %) ; 75.51-77.87 (A, 9.18 %) ; 78.93-79.57 (A, 14.13 %) ; 81.93-83.68 (A, 18.46 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.50 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.98 %)** : le gap seul le franchit 0.16 % des séances (2 fois sur 1253).
   - exécution **3.975 pt plus bas** dans le cas TYPIQUE (médiane), 5.439 au p90, **5.805 au pire**
   - perte réelle **15.955 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 11.98 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0063 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.514 % | p01 -6.925 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3001** [0.2356 ; 0.3713] _(largeur 13.6 pt, n_eff 173.1)_
   - swing : **0.3856** [0.3354 ; 0.4377] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3491** [0.3003 ; 0.4004] _(largeur 10.0 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (29.9 pt), deep (30.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.21 %** | CVaR **-9.11 %** | vol 4.34 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.03 % contre 4.36 % aujourd'hui, rapport 0.46)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.33 % vs -14.64 % si l'on extrapolait par √5 _(rapport 0.978 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8002** (β de hausse 1.6317, asymétrie 1.1033) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 61.7901 sur support (1.09 ATR, 10.656 %) — p(stop avant cible) 0.4247 [0.37 ; 0.48], R/R 4.09, perte reelle 11.158 % (gap inclus), CVaR 14.417 %, EV -0.2281 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1974 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 14.42 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.09 ATR (stop 10.656 %) — p(stop avant cible) 0.4247 [0.37 ; 0.48], R/R 4.09, perte reelle 11.158 % (gap inclus), EV -0.2281 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.1 % x 45.64 % + P(rien) 57.5 % x 7.80 % ne couvrent pas P(stop) 42.5 % x 11.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.872 %) — p(stop avant cible) 0.8975 [0.86 ; 0.93], R/R 21.925, perte reelle 2.082 % (gap inclus), EV -0.48 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 21.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.897, borne haute 0.926 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 0.0 % x 45.64 % + P(rien) 10.2 % x 13.54 % ne couvrent pas P(stop) 89.8 % x 2.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 3.745 %) — p(stop avant cible) 0.7614 [0.71 ; 0.80], R/R 11.472, perte reelle 3.978 % (gap inclus), EV -0.0651 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.761, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.1 % x 45.64 % + P(rien) 23.8 % x 12.34 % ne couvrent pas P(stop) 76.1 % x 3.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 5.617 %) — p(stop avant cible) 0.678 [0.63 ; 0.73], R/R 7.682, perte reelle 5.941 % (gap inclus), EV -0.3417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.678, borne haute 0.726 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.1 % x 45.64 % + P(rien) 32.1 % x 11.38 % ne couvrent pas P(stop) 67.8 % x 5.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 13.107 %) — p(stop avant cible) 0.3151 [0.27 ; 0.37], R/R 3.336, perte reelle 13.68 % (gap inclus), EV -0.2025 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.1 % x 45.64 % + P(rien) 68.4 % x 5.96 % ne couvrent pas P(stop) 31.5 % x 13.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 14.98 %) — p(stop avant cible) 0.2395 [0.20 ; 0.29], R/R 2.968, perte reelle 15.379 % (gap inclus), EV -0.1806 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.1 % x 45.64 % + P(rien) 76.0 % x 4.57 % ne couvrent pas P(stop) 23.9 % x 15.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 16.852 %) — p(stop avant cible) 0.1582 [0.12 ; 0.20], R/R 2.655, perte reelle 17.19 % (gap inclus), EV 0.0498 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.92 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 18.724 %) — p(stop avant cible) 0.1089 [0.08 ; 0.14], R/R 2.404, perte reelle 18.984 % (gap inclus), EV 0.1481 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.29 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 20.597 %) — p(stop avant cible) 0.0708 [0.05 ; 0.10], R/R 2.185, perte reelle 20.888 % (gap inclus), EV 0.187 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.01 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 22.469 %) — p(stop avant cible) 0.0439 [0.03 ; 0.07], R/R 1.996, perte reelle 22.87 % (gap inclus), EV 0.2568 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.46 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 26.214 %) — p(stop avant cible) 0.0255 [0.01 ; 0.05], R/R 1.711, perte reelle 26.675 % (gap inclus), EV 0.2629 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.23 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 29.959 %) — p(stop avant cible) 0.0183 [0.01 ; 0.04], R/R 1.512, perte reelle 30.177 % (gap inclus), EV 0.2685 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.78 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 33.704 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 1.341, perte reelle 34.026 % (gap inclus), EV 0.3701 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.09 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 37.449 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.219, perte reelle 37.449 % (gap inclus), EV 0.384 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 41.194 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.108, perte reelle 41.194 % (gap inclus), EV 0.3979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 44.939 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.016, perte reelle 44.939 % (gap inclus), EV 0.3979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 48.684 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.937, perte reelle 48.684 % (gap inclus), EV 0.3979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 52.428 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.871, perte reelle 52.428 % (gap inclus), EV 0.3979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 56.173 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.812, perte reelle 56.173 % (gap inclus), EV 0.3979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 59.918 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.762, perte reelle 59.918 % (gap inclus), EV 0.3979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 69.16, ATR14 5.1799 (7.49 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.374 ATR = 2.801 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.374 % | 68.901 | 93.05 % | 95.36 % | 96.27 % | 96.76 % | 97.26 % | 98.05 % |
| 0.1 ATR | 0.749 % | 68.642 | 85.6 % | 90.83 % | 92.53 % | 94.03 % | 94.92 % | 96.41 % |
| 0.15 ATR | 1.123 % | 68.383 | 77.95 % | 85.89 % | 88.6 % | 90.9 % | 92.89 % | 95.07 % |
| 0.2 ATR | 1.498 % | 68.124 | 71.4 % | 80.54 % | 84.36 % | 87.66 % | 90.65 % | 93.22 % |
| 0.25 ATR | 1.872 % | 67.865 | 64.35 % | 74.8 % | 79.72 % | 84.13 % | 88.01 % | 90.86 % |
| 0.35 ATR | 2.621 % | 67.347 | 52.47 % | 66.03 % | 72.75 % | 78.77 % | 84.35 % | 87.99 % |
| 0.5 ATR | 3.745 % | 66.57 | 37.06 % | 53.93 % | 61.96 % | 69.77 % | 77.54 % | 82.34 % |
| 0.75 ATR | 5.617 % | 65.2751 | 19.44 % | 36.49 % | 46.72 % | 56.93 % | 66.77 % | 73.2 % |
| 1.0 ATR | 7.49 % | 63.9801 | 9.26 % | 23.69 % | 33.91 % | 45.3 % | 56.4 % | 65.81 % |
| 1.25 ATR | 9.362 % | 62.6851 | 4.83 % | 15.02 % | 23.31 % | 35.19 % | 48.88 % | 59.65 % |
| 1.5 ATR | 11.235 % | 61.3901 | 2.52 % | 10.18 % | 16.85 % | 28.11 % | 42.17 % | 54.0 % |
| 2.0 ATR | 14.98 % | 58.8001 | 0.4 % | 3.73 % | 7.27 % | 15.67 % | 31.2 % | 44.35 % |
| 2.5 ATR | 18.724 % | 56.2102 | 0.0 % | 1.41 % | 3.73 % | 8.29 % | 22.66 % | 35.42 % |
| 3.0 ATR | 22.469 % | 53.6202 | 0.0 % | 0.5 % | 2.12 % | 4.95 % | 15.55 % | 27.41 % |
| 4.0 ATR | 29.959 % | 48.4403 | 0.0 % | 0.3 % | 0.61 % | 1.82 % | 6.0 % | 15.71 % |
| 6.0 ATR | 44.939 % | 38.0804 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 5.13 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.63 ATR | 0.82 ATR | 0.97 ATR | 1.11 ATR | 1.51 ATR | 1.90 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.02 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.01 ATR | 1.33 ATR | 1.62 ATR | 1.83 ATR | 2.38 ATR | 2.99 ATR |
| **10 s.** | 0.56 ATR | 1.21 ATR | 1.40 ATR | 1.92 ATR | 2.36 ATR | 2.69 ATR | 3.58 ATR | 4.43 ATR |
| **20 s.** | 0.70 ATR | 1.71 ATR | 1.97 ATR | 2.65 ATR | 3.21 ATR | 3.63 ATR | 5.08 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.423 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.628–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.617 %, prix 65.2753), p(touche) 36.49 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.784–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.49 %, prix 63.9799), p(touche) 33.91 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.007–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.362 %, prix 62.6852), p(touche) 35.19 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.395–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.235 %, prix 61.3899), p(touche) 42.17 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.966–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.98 %, prix 58.7998), p(touche) 44.35 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.007 | EV/share : $-0.013 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 73.7 | side 21.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.041% → cible +3.823% / stop −3.0%, p_fill 54%, n_eff≈58.5) : P(cible|rempli) **19%** · **EV/risk +0.009** (×p_fill ; si rempli +0.05% du capital)
  - **swing** (entrée dip −4.49% → cible +8.767% / stop −7.842%, p_fill 35%, n_eff≈40.4) : P(cible|rempli) **28%** · **EV/risk -0.003** (×p_fill ; si rempli -0.07% du capital)
  - **deep** (entrée dip −6.935% → cible +18.739% / stop −12.072%, p_fill 35%, n_eff≈37.9) : P(cible|rempli) **39%** · **EV/risk +0.155** (×p_fill ; si rempli +5.27% du capital)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.73 · part idiosyncratique 0.27
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.6  _(survente)_
- **ADX** : 32.8  _(tendance etablie)_
- **MACD** : hist -0.966  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 38.9%
- **ATR** : 5.18 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.044  _(neutre)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 46.0  _(transition)_
- **MA** : MA20 84.11 · MA50 100.37 · MA200 91.08  _(prix < MA20)_
- **Dist MA** : MA20 -17.8% · MA50 -31.1% · MA200 -24.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (689687 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
