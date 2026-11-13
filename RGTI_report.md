# RGTI

**Generated** : 2026-11-13T01:26:04.889768+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $10.34  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $10.34 (+2.9% vs entrée) · entrée $10.05 · stop $9.58 · T1 $11.00 · R/R 2.02  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +8.0 % ≠ (strike 12.0 − spot 10.34)/spot = +16.1 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 10.34 · ATR Wilder 1.06 (10.22 %)_
- **Swing** : plage **9.05 → 8.5** (-12.48 % a -17.82 % sous la cloture, 0.52 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 8.92-9.19 (A). stop INDICATIF 7.82 (-7.95 % sous le bas ; sous le support 8.35-8.45 (- 0,5 ATR)).
- **Deep** : plage **8.5 → 7.09** (-17.82 % a -31.39 % sous la cloture, 1.33 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 8.35-8.45 (B). stop INDICATIF 6.33 (-10.76 % sous le bas ; sous le support 6.86-7.03 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.73 ATR sous le plus haut 20 s., RSI(2) 15.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 9.5-9.74 (C, -5.8 %) ; 8.92-9.19 (A, -11.11 %) ; 8.35-8.45 (B, -18.28 %) ; 6.86-7.03 (B, -32.06 %) ; 5.95-5.95 (C, -42.46 %) ; 1.83-2.21 (B, -78.63 %)
- Resistances reelles au-dessus : 10.71-11.12 (A, 3.58 %) ; 11.4-11.87 (A, 10.25 %) ; 12.08-12.59 (A, 16.83 %) ; 12.75-13.23 (A, 23.31 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.89 %)** : le gap seul le franchit 0.16 % des séances (2 fois sur 1253).
   - exécution **7.675 pt plus bas** dans le cas TYPIQUE (médiane), 12.993 au p90, **14.323 au pire**
   - perte réelle **24.565 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 16.89 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0123 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.144 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2801** [0.2173 ; 0.3502] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.3604** [0.3111 ; 0.412] _(largeur 10.1 pt, n_eff 345.7)_
   - deep : **0.2998** [0.2533 ; 0.3496] _(largeur 9.6 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (28.1 pt), deep (26.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.71 %** | CVaR **-10.67 %** | vol 6.79 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 16.17 % contre 5.58 % aujourd'hui, rapport 2.90)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.29 % si l'on extrapolait par √5 _(rapport 0.976 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8562** (β de hausse 2.0439, asymétrie 0.9081) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.389× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 9.5043 sur atr_grid (0.75 ATR, 8.082 %) — p(stop avant cible) 0.6898 [0.64 ; 0.74], R/R 3.695, perte reelle 8.245 % (gap inclus), CVaR 10.22 %, EV -1.3636 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.7043 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.03 ATR (stop 14.711 %) — p(stop avant cible) 0.4223 [0.37 ; 0.47], R/R 2.036, perte reelle 14.963 % (gap inclus), EV -1.8965 % — **REFUSE**
      - refuse : cible atteinte seulement 11.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 11.3 % x 30.46 % + P(rien) 46.5 % x 2.13 % ne couvrent pas P(stop) 42.2 % x 14.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.694 %) — p(stop avant cible) 0.8909 [0.85 ; 0.92], R/R 10.954, perte reelle 2.781 % (gap inclus), EV -0.3145 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 10.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 5.1 % x 30.46 % + P(rien) 5.8 % x 10.34 % ne couvrent pas P(stop) 89.1 % x 2.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 5.388 %) — p(stop avant cible) 0.7869 [0.74 ; 0.83], R/R 5.488, perte reelle 5.551 % (gap inclus), EV -0.9789 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.787, borne haute 0.828 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 7.4 % x 30.46 % + P(rien) 13.9 % x 8.14 % ne couvrent pas P(stop) 78.7 % x 5.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 8.082 %) — p(stop avant cible) 0.6898 [0.64 ; 0.74], R/R 3.695, perte reelle 8.245 % (gap inclus), EV -1.3636 % — **REFUSE**
      - refuse : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 9.5 % x 30.46 % + P(rien) 21.5 % x 6.61 % ne couvrent pas P(stop) 69.0 % x 8.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 16.164 %) — p(stop avant cible) 0.3585 [0.31 ; 0.41], R/R 1.86, perte reelle 16.377 % (gap inclus), EV -1.6646 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 12.0 % x 30.46 % + P(rien) 52.2 % x 1.07 % ne couvrent pas P(stop) 35.9 % x 16.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 18.858 %) — p(stop avant cible) 0.2797 [0.23 ; 0.33], R/R 1.596, perte reelle 19.089 % (gap inclus), EV -1.6767 % — **REFUSE**
      - refuse : cible atteinte seulement 12.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 12.4 % x 30.46 % + P(rien) 59.6 % x -0.21 % ne couvrent pas P(stop) 28.0 % x 19.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 21.552 %) — p(stop avant cible) 0.1899 [0.15 ; 0.23], R/R 1.395, perte reelle 21.837 % (gap inclus), EV -1.303 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 12.8 % x 30.46 % + P(rien) 68.2 % x -1.56 % ne couvrent pas P(stop) 19.0 % x 21.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 24.245 %) — p(stop avant cible) 0.1356 [0.10 ; 0.17], R/R 1.246, perte reelle 24.446 % (gap inclus), EV -1.2673 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 12.9 % x 30.46 % + P(rien) 73.6 % x -2.54 % ne couvrent pas P(stop) 13.6 % x 24.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 26.939 %) — p(stop avant cible) 0.079 [0.05 ; 0.11], R/R 1.123, perte reelle 27.118 % (gap inclus), EV -0.9487 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 13.2 % x 30.46 % + P(rien) 78.9 % x -3.58 % ne couvrent pas P(stop) 7.9 % x 27.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 29.633 %) — p(stop avant cible) 0.0572 [0.04 ; 0.09], R/R 1.021, perte reelle 29.823 % (gap inclus), EV -0.9196 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 13.2 % x 30.46 % + P(rien) 81.0 % x -4.00 % ne couvrent pas P(stop) 5.7 % x 29.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 32.327 %) — p(stop avant cible) 0.0356 [0.02 ; 0.06], R/R 0.937, perte reelle 32.525 % (gap inclus), EV -0.8701 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 13.3 % x 30.46 % + P(rien) 83.2 % x -4.51 % ne couvrent pas P(stop) 3.6 % x 32.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 37.715 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.801, perte reelle 38.033 % (gap inclus), EV -0.7643 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 13.3 % x 30.46 % + P(rien) 85.3 % x -5.03 % ne couvrent pas P(stop) 1.4 % x 38.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 43.103 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.707, perte reelle 43.103 % (gap inclus), EV -0.7007 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.2 % x -5.32 % ne couvrent pas P(stop) 0.4 % x 43.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 48.491 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.628, perte reelle 48.491 % (gap inclus), EV -0.7083 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.4 % x -5.39 % ne couvrent pas P(stop) 0.3 % x 48.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 53.879 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.552, perte reelle 55.212 % (gap inclus), EV -0.7014 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.4 % x -5.39 % ne couvrent pas P(stop) 0.2 % x 55.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 59.267 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.502, perte reelle 60.674 % (gap inclus), EV -0.7137 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.4 % x -5.40 % ne couvrent pas P(stop) 0.2 % x 60.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 64.655 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.471, perte reelle 64.655 % (gap inclus), EV -0.722 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.4 % x -5.40 % ne couvrent pas P(stop) 0.2 % x 64.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 70.042 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.435, perte reelle 70.042 % (gap inclus), EV -0.6703 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.6 % x -5.48 % ne couvrent pas P(stop) 0.0 % x 70.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 75.43 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.404, perte reelle 75.43 % (gap inclus), EV -0.6703 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.6 % x -5.48 % ne couvrent pas P(stop) 0.0 % x 75.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 80.818 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.377, perte reelle 80.818 % (gap inclus), EV -0.6703 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.6 % x -5.48 % ne couvrent pas P(stop) 0.0 % x 80.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 86.206 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.353, perte reelle 86.206 % (gap inclus), EV -0.6703 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 13.4 % x 30.46 % + P(rien) 86.6 % x -5.48 % ne couvrent pas P(stop) 0.0 % x 86.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 10.34, ATR14 1.1142 (10.776 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.409 ATR = 4.407 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.539 % | 10.2843 | 92.04 % | 94.35 % | 95.66 % | 97.07 % | 97.56 % | 98.56 % |
| 0.1 ATR | 1.078 % | 10.2286 | 86.2 % | 90.83 % | 92.43 % | 95.05 % | 96.04 % | 97.43 % |
| 0.15 ATR | 1.616 % | 10.1729 | 80.87 % | 87.2 % | 89.1 % | 92.21 % | 94.21 % | 96.1 % |
| 0.2 ATR | 2.155 % | 10.1172 | 73.82 % | 82.36 % | 85.37 % | 88.88 % | 91.57 % | 94.46 % |
| 0.25 ATR | 2.694 % | 10.0614 | 67.88 % | 78.23 % | 81.53 % | 85.84 % | 89.02 % | 92.51 % |
| 0.35 ATR | 3.772 % | 9.95 | 55.59 % | 68.65 % | 74.07 % | 79.78 % | 84.65 % | 89.63 % |
| 0.5 ATR | 5.388 % | 9.7829 | 41.29 % | 57.16 % | 65.09 % | 72.09 % | 79.47 % | 85.32 % |
| 0.75 ATR | 8.082 % | 9.5043 | 21.75 % | 39.31 % | 50.55 % | 59.66 % | 71.34 % | 79.06 % |
| 1.0 ATR | 10.776 % | 9.2258 | 9.57 % | 24.19 % | 33.91 % | 47.42 % | 62.5 % | 72.59 % |
| 1.25 ATR | 13.47 % | 8.9472 | 4.23 % | 14.82 % | 24.02 % | 37.61 % | 53.25 % | 65.3 % |
| 1.5 ATR | 16.164 % | 8.6687 | 1.91 % | 7.46 % | 13.93 % | 25.88 % | 43.5 % | 57.29 % |
| 2.0 ATR | 21.552 % | 8.1116 | 0.3 % | 1.71 % | 4.34 % | 11.22 % | 25.61 % | 41.27 % |
| 2.5 ATR | 26.939 % | 7.5545 | 0.0 % | 0.3 % | 1.11 % | 4.55 % | 14.84 % | 28.95 % |
| 3.0 ATR | 32.327 % | 6.9974 | 0.0 % | 0.1 % | 0.3 % | 1.42 % | 7.52 % | 17.35 % |
| 4.0 ATR | 43.103 % | 5.8831 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.73 % | 5.03 % |
| 6.0 ATR | 64.655 % | 3.6547 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.72 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.61 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.76 ATR | 0.83 ATR | 1.02 ATR | 1.23 ATR | 1.35 ATR | 1.71 ATR | 1.97 ATR |
| **5 s.** | 0.44 ATR | 0.95 ATR | 1.06 ATR | 1.35 ATR | 1.53 ATR | 1.70 ATR | 2.09 ATR | 2.47 ATR |
| **10 s.** | 0.64 ATR | 1.33 ATR | 1.46 ATR | 1.79 ATR | 2.03 ATR | 2.26 ATR | 2.83 ATR | 3.44 ATR |
| **20 s.** | 0.91 ATR | 1.73 ATR | 1.88 ATR | 2.34 ATR | 2.67 ATR | 2.89 ATR | 3.60 ATR | 4.01 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.461–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (5.388 %, prix 9.7829), p(touche) 41.29 % (en stress 85.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.67–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (8.082 %, prix 9.5043), p(touche) 39.31 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.833 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.062–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (13.47 %, prix 8.9472), p(touche) 37.61 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.462–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (16.164 %, prix 8.6686), p(touche) 43.5 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (74.6 % des re-echantillons)
- **20 seance(s)** : plage utile VIDE (borne basse 1.884 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 38.9 | bear 56.1 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.775% → cible +9.408% / stop −4.705%, p_fill 44%, n_eff≈48.4) : P(cible|rempli) **2%** · **EV/risk -0.090** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −6.114% → cible +13.293% / stop −11.478%, p_fill 38%, n_eff≈44.9) : P(cible|rempli) **19%** · **EV/risk -0.015** (×p_fill ; si rempli -0.46% du capital)
  - **deep** (entrée dip −9.446% → cible +32.95% / stop −17.85%, p_fill 36%, n_eff≈40.4) : P(cible|rempli) **12%** · **EV/risk -0.021** (×p_fill ; si rempli -1.04% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 44.4  _(momentum baissier)_
- **ADX** : 29.8  _(tendance etablie)_
- **MACD** : hist 0.091  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 25.5%
- **ATR** : 1.11 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.124  _(distribution)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 11.55 · MA50 13.67 · MA200 16.61  _(prix < MA20)_
- **Dist MA** : MA20 -10.4% · MA50 -24.4% · MA200 -37.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (714575 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
