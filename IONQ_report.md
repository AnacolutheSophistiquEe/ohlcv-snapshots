# IONQ

**Generated** : 2026-11-13T01:24:58.630669+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $30.84  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $30.84 (+1.6% vs entrée) · entrée $30.35 · stop $27.50 · T1 $33.29 · R/R 1.03  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -3.1 % ≠ (strike 33.0 − spot 30.84)/spot = +7.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 30.84 · ATR Wilder 2.8 (9.07 %)_
- **Swing** : plage **27.34 → 25.13** (-11.34 % a -18.51 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 24.92-25.92 (A). stop INDICATIF 20.87 (-16.96 % sous le bas ; sous le support 22.27-23.49 (- 0,5 ATR)).
- **Deep** : plage **25.13 → 20.28** (-18.51 % a -34.23 % sous la cloture, 1.73 ATR) — touchee 48 % → 15 % du temps en 20 seances ; supports reels dans la plage : 24.92-25.92 (A) ; 22.27-23.49 (B) ; 20.61-21.5 (B). stop INDICATIF 16.48 (-18.75 % sous le bas ; sous le support 17.88-18.81 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.97 ATR sous le plus haut 20 s., RSI(2) 16.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 27.83-28.32 (B, -8.17 %) ; 24.92-25.92 (A, -15.94 %) ; 22.27-23.49 (B, -23.85 %) ; 20.61-21.5 (B, -30.29 %) ; 17.88-18.81 (A, -39.01 %) ; 13.38-14.15 (A, -54.12 %)
- Resistances reelles au-dessus : 31.81-31.85 (A, 3.15 %) ; 33.29-34.18 (A, 7.94 %) ; 34.77-36.03 (A, 12.74 %) ; 36.35-37.28 (A, 17.87 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.34 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.84 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **1.106 pt plus bas** dans le cas TYPIQUE (médiane), 9.037 au p90, **11.019 au pire**
   - perte réelle **15.082 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0102 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.148 % | p01 -6.504 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3161** [0.2503 ; 0.388] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.4091** [0.3582 ; 0.4615] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3908** [0.3404 ; 0.443] _(largeur 10.3 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.61 %** | CVaR **-10.12 %** | vol 6.16 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.22 % contre 5.58 % aujourd'hui, rapport 1.83)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.92 % vs -20.01 % si l'on extrapolait par √5 _(rapport 0.896 ; < 1 = le √5 surestime)_
- **β de baisse : 2.1674** (β de hausse 2.0107, asymétrie 1.0779) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 27.2718 sur atr_grid (1.25 ATR, 11.57 %) — p(stop avant cible) 0.5085 [0.46 ; 0.56], R/R 2.621, perte reelle 11.7 % (gap inclus), CVaR 12.889 %, EV -0.6175 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4508 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.508, borne haute 0.561 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.89 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.3 ATR (stop 5.848 %) — p(stop avant cible) 0.7691 [0.72 ; 0.81], R/R 5.166, perte reelle 5.937 % (gap inclus), EV -0.3701 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.27 ATR du spot — compartiment <1, mesure a 50.7 % de casse (IC clusterise [0.471 ; 0.542] sur 1138 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 9.9 % x 30.67 % + P(rien) 13.2 % x 8.82 % ne couvrent pas P(stop) 76.9 % x 5.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 13.884 %) — p(stop avant cible) 0.4059 [0.36 ; 0.46], R/R 2.191, perte reelle 13.999 % (gap inclus), EV -0.7919 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.79 %) : P(cible) 11.9 % x 30.67 % + P(rien) 47.5 % x 2.60 % ne couvrent pas P(stop) 40.6 % x 14.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.08 ATR (stop 22.304 %) — p(stop avant cible) 0.168 [0.13 ; 0.21], R/R 1.363, perte reelle 22.508 % (gap inclus), EV -0.4374 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 12.9 % x 30.67 % + P(rien) 70.3 % x -0.86 % ne couvrent pas P(stop) 16.8 % x 22.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 9.256 %) — p(stop avant cible) 0.6343 [0.58 ; 0.68], R/R 3.277, perte reelle 9.359 % (gap inclus), EV -0.526 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.634, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 10.9 % x 30.67 % + P(rien) 25.7 % x 8.02 % ne couvrent pas P(stop) 63.4 % x 9.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 11.57 %) — p(stop avant cible) 0.5085 [0.46 ; 0.56], R/R 2.621, perte reelle 11.7 % (gap inclus), EV -0.6175 % — **REFUSE**
      - refuse : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.508, borne haute 0.561 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 11.5 % x 30.67 % + P(rien) 37.6 % x 4.77 % ne couvrent pas P(stop) 50.8 % x 11.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 16.198 %) — p(stop avant cible) 0.3251 [0.28 ; 0.38], R/R 1.884, perte reelle 16.277 % (gap inclus), EV -1.0054 % — **REFUSE**
      - refuse : cible atteinte seulement 12.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 12.1 % x 30.67 % + P(rien) 55.4 % x 1.04 % ne couvrent pas P(stop) 32.5 % x 16.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 25.454 %) — p(stop avant cible) 0.1058 [0.08 ; 0.14], R/R 1.201, perte reelle 25.529 % (gap inclus), EV -0.314 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 12.9 % x 30.67 % + P(rien) 76.5 % x -2.04 % ne couvrent pas P(stop) 10.6 % x 25.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 27.768 %) — p(stop avant cible) 0.0856 [0.06 ; 0.12], R/R 1.102, perte reelle 27.825 % (gap inclus), EV -0.4476 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 12.9 % x 30.67 % + P(rien) 78.6 % x -2.56 % ne couvrent pas P(stop) 8.6 % x 27.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 32.396 %) — p(stop avant cible) 0.0285 [0.01 ; 0.05], R/R 0.945, perte reelle 32.455 % (gap inclus), EV -0.4734 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 12.9 % x 30.67 % + P(rien) 84.3 % x -4.15 % ne couvrent pas P(stop) 2.9 % x 32.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 37.024 %) — p(stop avant cible) 0.0106 [0.00 ; 0.03], R/R 0.824, perte reelle 37.235 % (gap inclus), EV -0.3834 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 12.9 % x 30.67 % + P(rien) 86.1 % x -4.57 % ne couvrent pas P(stop) 1.1 % x 37.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 41.652 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.736, perte reelle 41.652 % (gap inclus), EV -0.3649 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 12.9 % x 30.67 % + P(rien) 86.8 % x -4.80 % ne couvrent pas P(stop) 0.4 % x 41.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 46.28 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.663, perte reelle 46.28 % (gap inclus), EV -0.3483 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 12.9 % x 30.67 % + P(rien) 87.1 % x -4.89 % ne couvrent pas P(stop) 0.1 % x 46.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 50.908 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.602, perte reelle 50.908 % (gap inclus), EV -0.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 12.9 % x 30.67 % + P(rien) 87.1 % x -4.89 % ne couvrent pas P(stop) 0.0 % x 50.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 55.536 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.552, perte reelle 55.536 % (gap inclus), EV -0.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 12.9 % x 30.67 % + P(rien) 87.1 % x -4.89 % ne couvrent pas P(stop) 0.0 % x 55.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 60.164 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.51, perte reelle 60.164 % (gap inclus), EV -0.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 12.9 % x 30.67 % + P(rien) 87.1 % x -4.89 % ne couvrent pas P(stop) 0.0 % x 60.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 64.792 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.473, perte reelle 64.792 % (gap inclus), EV -0.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 12.9 % x 30.67 % + P(rien) 87.1 % x -4.89 % ne couvrent pas P(stop) 0.0 % x 64.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 69.421 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.442, perte reelle 69.421 % (gap inclus), EV -0.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 12.9 % x 30.67 % + P(rien) 87.1 % x -4.89 % ne couvrent pas P(stop) 0.0 % x 69.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 74.049 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.414, perte reelle 74.049 % (gap inclus), EV -0.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 12.9 % x 30.67 % + P(rien) 87.1 % x -4.89 % ne couvrent pas P(stop) 0.0 % x 74.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 30.84, ATR14 2.8546 (9.256 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.378 ATR = 3.499 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.463 % | 30.6973 | 93.86 % | 95.46 % | 96.27 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.926 % | 30.5545 | 86.1 % | 91.23 % | 92.33 % | 94.74 % | 95.83 % | 96.82 % |
| 0.15 ATR | 1.388 % | 30.4118 | 78.85 % | 86.39 % | 88.4 % | 91.61 % | 93.6 % | 95.59 % |
| 0.2 ATR | 1.851 % | 30.2691 | 71.0 % | 80.44 % | 84.16 % | 88.37 % | 90.85 % | 93.43 % |
| 0.25 ATR | 2.314 % | 30.1264 | 64.95 % | 76.21 % | 80.73 % | 85.84 % | 88.72 % | 91.89 % |
| 0.35 ATR | 3.24 % | 29.8409 | 52.77 % | 67.24 % | 74.17 % | 79.58 % | 84.04 % | 88.3 % |
| 0.5 ATR | 4.628 % | 29.4127 | 38.07 % | 54.44 % | 62.16 % | 71.28 % | 78.56 % | 84.39 % |
| 0.75 ATR | 6.942 % | 28.6991 | 22.26 % | 39.42 % | 48.64 % | 59.25 % | 69.41 % | 76.8 % |
| 1.0 ATR | 9.256 % | 27.9854 | 9.97 % | 24.8 % | 34.91 % | 46.31 % | 58.54 % | 68.17 % |
| 1.25 ATR | 11.57 % | 27.2718 | 3.93 % | 14.42 % | 24.12 % | 35.09 % | 50.51 % | 61.81 % |
| 1.5 ATR | 13.884 % | 26.5581 | 1.21 % | 7.16 % | 15.94 % | 25.68 % | 41.46 % | 56.16 % |
| 2.0 ATR | 18.512 % | 25.1309 | 0.1 % | 1.92 % | 5.15 % | 14.46 % | 28.86 % | 45.48 % |
| 2.5 ATR | 23.14 % | 23.7036 | 0.0 % | 0.2 % | 1.31 % | 6.07 % | 18.9 % | 34.91 % |
| 3.0 ATR | 27.768 % | 22.2763 | 0.0 % | 0.1 % | 0.4 % | 2.83 % | 12.09 % | 26.8 % |
| 4.0 ATR | 37.024 % | 19.4217 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 3.46 % | 12.22 % |
| 6.0 ATR | 55.536 % | 13.7126 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.21 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.66 ATR | 0.86 ATR | 1.00 ATR | 1.12 ATR | 1.40 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.82 ATR | 1.04 ATR | 1.23 ATR | 1.38 ATR | 1.77 ATR | 2.02 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.03 ATR | 1.31 ATR | 1.53 ATR | 1.75 ATR | 2.27 ATR | 2.67 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.84 ATR | 2.19 ATR | 2.44 ATR | 3.24 ATR | 3.82 ATR |
| **20 s.** | 0.80 ATR | 1.79 ATR | 2.02 ATR | 2.62 ATR | 3.12 ATR | 3.47 ATR | 4.41 ATR | 5.33 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.429 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.657–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.942 %, prix 28.6991), p(touche) 39.42 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.816–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (9.256 %, prix 27.9854), p(touche) 34.91 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.029–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (11.57 %, prix 27.2718), p(touche) 35.09 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.402–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (13.884 %, prix 26.5582), p(touche) 41.46 % (en stress 97.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.023 ATR au-dessus du haut de la grille, 2.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (73.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.111 | EV/share : $-0.317 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 9 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.3 | bear 38.9 | side 27.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.711% → cible +8.72% / stop −4.36%, p_fill 85%, n_eff≈90.4) : P(cible|rempli) **7%** · **EV/risk -0.090** (×p_fill ; si rempli -0.46% du capital)
  - **swing** (entrée dip −1.585% → cible +9.676% / stop −9.404%, p_fill 81%, n_eff≈95.1) : P(cible|rempli) **34%** · **EV/risk -0.125** (×p_fill ; si rempli -1.45% du capital)
  - **deep** (entrée dip −2.316% → cible +23.173% / stop −14.213%, p_fill 82%, n_eff≈92.6) : P(cible|rempli) **18%** · **EV/risk -0.237** (×p_fill ; si rempli -4.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→77% · +2.0%→62% · +3.0%→52% · +5.0%→26% · +8.0%→12%
- Range intraday médian 6.97% (p90 11.38%) · excursion haute méd. +3.18% / basse méd. −2.5%
- Profil de vol intra : ouverture 4.647% vs midi 1.288% vs clôture 1.495% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 25% · trend ↑0%/↓0% ; spike-down 64% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; neutre — autocorr -0.018)_ ; drift intra méd. -0.489% ; recovery-V 23%
- **σ réalisé intraday** 3.806% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 60% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 31.1144 (VA 30.5681–31.2294 ; dernier close 31.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 66% · **stop −5.21%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.25 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 53% (gap-down >1% 38% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.04% (p90 −2.65%) · haut méd +0.99% · range méd 2.55%
- Excursion ouverture 15min (n=160) : bas méd −1.23% (p90 −3.55%) · haut méd +1.33% · range méd 3.12%
- Excursion ouverture 30min (n=160) : bas méd −1.67% (p90 −4.61%) · haut méd +1.77% · range méd 3.97%
- Excursion ouverture 60min (n=160) : bas méd −1.74% (p90 −5.6%) · haut méd +1.78% · range méd 4.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 31.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 78% (126/159) · gap 47% · délai 0.0min · rebond 55% (80/126) (MFE +1.5%)
   - −1.0% : fill 30min 67% · séance 74% (119/159) · gap 38% · délai 0.0min · rebond 64% (83/119) (MFE +1.62%)
   - −1.5% : fill 30min 60% · séance 69% (112/159) · gap 34% · délai 0.0min · rebond 65% (76/112) (MFE +1.95%)
   - −2.0% : fill 30min 51% · séance 59% (100/159) · gap 25% · délai 0.0min · rebond 67% (68/100) (MFE +1.87%)
   - −3.0% : fill 30min 39% · séance 48% (82/159) · gap 12% · délai 2.9min · rebond 63% (57/82) (MFE +2.28%)
   - −4.0% : fill 30min 26% · séance 38% (63/159) · gap 6% · délai 9.0min · rebond 62% (44/63) (MFE +1.9%)
   - −5.0% : fill 30min 13% · séance 26% (47/159) · gap 1% · délai 31.4min · rebond 66% (35/47) (MFE +1.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.44%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −2.35%) → stop au-delà de −1.58% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −1.85%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1013 jambes) : jambe baissière méd −1.23% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 62% (54/79)
      · −2.0% : fill 87% (71/79) · rebond 68% (50/71)
      · −3.0% : fill 73% (59/79) · rebond 63% (40/59)
      · −4.0% : fill 60% (45/79) · rebond 58% (29/45)
      · −5.0% : fill 39% (33/79) · rebond 61% (22/33)
   - **flat** (16 séances) :
      · −1.0% : fill 67% (11/16) · rebond 88% (10/11)
      · −2.0% : fill 51% (9/16) · rebond 92% (7/9)
      · −3.0% : fill 37% (6/16) · rebond 78% (5/6)
      · −4.0% : fill 19% (4/16) · rebond 57% (3/4)
      · −5.0% : fill 14% (3/16) · rebond 100% (3/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 44% (29/64) · rebond 58% (19/29)
      · −2.0% : fill 25% (20/64) · rebond 52% (11/20)
      · −3.0% : fill 20% (17/64) · rebond 57% (12/17)
      · −4.0% : fill 15% (14/64) · rebond 88% (12/14)
      · −5.0% : fill 14% (11/64) · rebond 72% (10/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 56% si les 15 1res min sont vertes (90 cas) · 27% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 68% si début vert vs 16% si rouge (base 43% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **68%** · continue >prix actuel 42% ; creux résiduel méd -1.91% (q20 -3.16%) → **SL/trailing à −3.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.85% → **scale +1.5% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.1%** (au-delà de la MAE q10 -4.1%), cible rebond +1.66% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.02% .. +5.03%] · haut q95 +5.67% · bas q05 -5.45%
   - 60min (n=160) : retour [-5.78% .. +5.37%] · haut q95 +6.95% · bas q05 -6.77%
   - 2h (n=160) : retour [-6.38% .. +6.14%] · haut q95 +7.8% · bas q05 -7.08%
   - 4h (n=160) : retour [-6.7% .. +6.96%] · haut q95 +8.6% · bas q05 -7.66%
   - 6h (n=160) : retour [-6.45% .. +7.44%] · haut q95 +9.93% · bas q05 -7.51%
   - session (n=160) : retour [-6.41% .. +8.2%] · haut q95 +9.95% · bas q05 -7.51%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 13% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 2.14% / p90 2.83%) · ~4.0 replis/séance, durée méd 55.01 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 29.17 min, n=54)
   - −1.0% → **82%** (reprise méd 31.37 min, n=38)
   - −1.5% → **76%** (reprise méd 44.94 min, n=20)
   - −2.0% → **68%** (reprise méd 38.95 min, n=14)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.83%** (p90, défaut prudent ; serré/agressif −2.14%) ; extension open→close méd +8.26% (q75 +11.05% / q95 +12.73%), MFE méd +10.06% / q90 +12.75%
   - Échelle scale-out : +10.06% (33%) / +12.25% (33%) / +12.75% (34%)
- **DÉSARMER** : repli > **−2.83%** depuis le plus-haut = décay → P(retournement) **16%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.75% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 76% du temps (retour médian dernière heure +0.3%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.4 · part idiosyncratique 0.6
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 49.2  _(neutre)_
- **ADX** : 26.4  _(tendance etablie)_
- **MACD** : hist 0.621  _(pas de croisement recent)_
- **BB** : %B 0.43 · largeur 26.9%
- **ATR** : 2.85 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.043  _(neutre)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 31.4 · MA50 36.55 · MA200 41.31  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 -15.6% · MA200 -25.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (707909 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
