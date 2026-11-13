# NEX

**Generated** : 2026-11-13T01:09:26.393910+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €131.20  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €131.20 (+1.0% vs entrée) · entrée €129.84 · stop €124.24 · T1 €141.03 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 130 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 131.2 · ATR Wilder 4.9 (3.73 %)_
- **Swing** : plage **124.5 → 120.52** (-5.11 % a -8.14 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 121.91-124.33 (B) ; 118.73-121.04 (B). stop INDICATIF 113.14 (-6.12 % sous le bas ; sous le support 115.59-117.84 (- 0,5 ATR)).
- **Deep** : plage **120.52 → 109.03** (-8.14 % a -16.9 % sous la cloture, 2.35 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 118.73-121.04 (B) ; 115.59-117.84 (A) ; 112.93-114.01 (B) ; 109.66-111.7 (A) ; 107.17-109.18 (A). stop INDICATIF 102.04 (-6.41 % sous le bas ; sous le support 104.49-106.6 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.59 ATR sous le plus haut 20 s., RSI(2) 67.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 124.7-126.98 (B, -3.22 %) ; 121.91-124.33 (B, -5.24 %) ; 118.73-121.04 (B, -7.74 %) ; 115.59-117.84 (A, -10.18 %) ; 112.93-114.01 (B, -13.1 %) ; 109.66-111.7 (A, -14.86 %)
- Resistances reelles au-dessus : 133.87-136.3 (A, 2.03 %) ; 137.58-139.35 (A, 4.86 %) ; 140.66-142.7 (A, 7.21 %) ; 143.2-145.6 (A, 9.15 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.31 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **2.76 pt plus bas** dans le cas TYPIQUE (médiane), 3.754 au p90, **4.286 au pire**
   - perte réelle **8.078 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 5.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0108 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.57 % | p01 -3.604 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0025** [0.0001 ; 0.0203] _(largeur 2.0 pt, n_eff 173.1)_
   - swing : **0.3895** [0.3392 ; 0.4416] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.4235** [0.3722 ; 0.476] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.62 %** | CVaR **-5.37 %** | vol 2.34 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.8 % vs -8.12 % si l'on extrapolait par √5 _(rapport 0.961 ; < 1 = le √5 surestime)_
- **β de baisse : 0.996** (β de hausse 1.0735, asymétrie 0.9278) vs FCHI — 622 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 121.1429 sur atr_grid (2.0 ATR, 7.666 %) — p(stop avant cible) 0.27 [0.23 ; 0.32], R/R 3.137, perte reelle 7.81 % (gap inclus), CVaR 8.441 %, EV -0.2786 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9647 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.59 ATR (stop 4.822 %) — p(stop avant cible) 0.5263 [0.47 ; 0.58], R/R 4.908, perte reelle 4.992 % (gap inclus), EV -0.622 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.526, borne haute 0.579 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 0.5 % x 24.50 % + P(rien) 46.8 % x 4.01 % ne couvrent pas P(stop) 52.6 % x 4.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 3.2 ATR (stop 14.824 %) — p(stop avant cible) 0.0303 [0.02 ; 0.05], R/R 1.604, perte reelle 15.275 % (gap inclus), EV -0.1339 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.5 % x 24.50 % + P(rien) 96.4 % x 0.21 % ne couvrent pas P(stop) 3.0 % x 15.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 4.67 ATR (stop 20.438 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.167, perte reelle 20.991 % (gap inclus), EV -0.0391 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.69 % > budget 12.00 %
      - ⚠ support DETECTE a 0.49 ATR du spot — compartiment <1, mesure a 50.7 % de casse (IC clusterise [0.471 ; 0.542] sur 1138 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.2 % x -0.12 % ne couvrent pas P(stop) 0.2 % x 20.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.958 %) — p(stop avant cible) 0.9191 [0.89 ; 0.94], R/R 24.69, perte reelle 0.992 % (gap inclus), EV -0.2496 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 24.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.919, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.3 % x 24.50 % + P(rien) 7.8 % x 7.62 % ne couvrent pas P(stop) 91.9 % x 0.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.59 ATR (stop 3.423 %) — p(stop avant cible) 0.6603 [0.61 ; 0.71], R/R 6.898, perte reelle 3.552 % (gap inclus), EV -0.5414 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.660, borne haute 0.709 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.5 % x 24.50 % + P(rien) 33.4 % x 5.01 % ne couvrent pas P(stop) 66.0 % x 3.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 5.749 %) — p(stop avant cible) 0.4399 [0.39 ; 0.49], R/R 4.135, perte reelle 5.926 % (gap inclus), EV -0.6083 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 0.5 % x 24.50 % + P(rien) 55.5 % x 3.37 % ne couvrent pas P(stop) 44.0 % x 5.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 6.707 %) — p(stop avant cible) 0.3556 [0.31 ; 0.41], R/R 3.584, perte reelle 6.837 % (gap inclus), EV -0.4519 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.5 % x 24.50 % + P(rien) 63.9 % x 2.89 % ne couvrent pas P(stop) 35.6 % x 6.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 7.666 %) — p(stop avant cible) 0.27 [0.23 ; 0.32], R/R 3.137, perte reelle 7.81 % (gap inclus), EV -0.2786 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.5 % x 24.50 % + P(rien) 72.5 % x 2.35 % ne couvrent pas P(stop) 27.0 % x 7.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 8.624 %) — p(stop avant cible) 0.2164 [0.18 ; 0.26], R/R 2.805, perte reelle 8.735 % (gap inclus), EV -0.2413 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.5 % x 24.50 % + P(rien) 77.8 % x 1.95 % ne couvrent pas P(stop) 21.6 % x 8.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 9.582 %) — p(stop avant cible) 0.1646 [0.13 ; 0.21], R/R 2.524, perte reelle 9.707 % (gap inclus), EV -0.2262 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.5 % x 24.50 % + P(rien) 83.0 % x 1.50 % ne couvrent pas P(stop) 16.5 % x 9.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 10.54 %) — p(stop avant cible) 0.1291 [0.10 ; 0.17], R/R 2.302, perte reelle 10.642 % (gap inclus), EV -0.2546 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.5 % x 24.50 % + P(rien) 86.6 % x 1.14 % ne couvrent pas P(stop) 12.9 % x 10.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 3.2 ATR (stop 13.426 %) — p(stop avant cible) 0.0549 [0.03 ; 0.08], R/R 1.782, perte reelle 13.748 % (gap inclus), EV -0.2331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.5 % x 24.50 % + P(rien) 94.0 % x 0.42 % ne couvrent pas P(stop) 5.5 % x 13.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 15.331 %) — p(stop avant cible) 0.0257 [0.01 ; 0.05], R/R 1.559, perte reelle 15.713 % (gap inclus), EV -0.1204 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.5 % x 24.50 % + P(rien) 96.9 % x 0.16 % ne couvrent pas P(stop) 2.6 % x 15.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 4.67 ATR (stop 19.039 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 1.236, perte reelle 19.823 % (gap inclus), EV -0.0452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.1 % x -0.10 % ne couvrent pas P(stop) 0.4 % x 19.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 21.08 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 1.077, perte reelle 22.75 % (gap inclus), EV -0.0357 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.3 % x -0.13 % ne couvrent pas P(stop) 0.2 % x 22.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 22.997 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.023, perte reelle 23.939 % (gap inclus), EV -0.0348 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.4 % x -0.14 % ne couvrent pas P(stop) 0.1 % x 23.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 24.913 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.983, perte reelle 24.913 % (gap inclus), EV -0.0305 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.4 % x -0.15 % ne couvrent pas P(stop) 0.1 % x 24.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 26.829 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.913, perte reelle 26.829 % (gap inclus), EV -0.0282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.5 % x -0.16 % ne couvrent pas P(stop) 0.0 % x 26.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 28.746 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.852, perte reelle 28.746 % (gap inclus), EV -0.0282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.5 % x -0.16 % ne couvrent pas P(stop) 0.0 % x 28.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 30.662 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.799, perte reelle 30.662 % (gap inclus), EV -0.0282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.5 % x 24.50 % + P(rien) 99.5 % x -0.16 % ne couvrent pas P(stop) 0.0 % x 30.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 131.2, ATR14 5.0286 (3.833 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 1.326 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.192 % | 130.9486 | 87.55 % | 91.46 % | 93.22 % | 95.08 % | 96.93 % | 97.9 % |
| 0.1 ATR | 0.383 % | 130.6971 | 81.67 % | 87.73 % | 90.37 % | 93.11 % | 95.55 % | 97.0 % |
| 0.15 ATR | 0.575 % | 130.4457 | 75.1 % | 83.51 % | 86.94 % | 90.16 % | 94.07 % | 95.7 % |
| 0.2 ATR | 0.767 % | 130.1943 | 68.33 % | 78.02 % | 83.01 % | 88.19 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.958 % | 129.9429 | 61.76 % | 73.41 % | 78.88 % | 85.14 % | 90.8 % | 93.81 % |
| 0.35 ATR | 1.341 % | 129.44 | 49.51 % | 64.08 % | 71.71 % | 79.13 % | 87.04 % | 91.71 % |
| 0.5 ATR | 1.916 % | 128.6857 | 34.71 % | 52.5 % | 61.3 % | 71.06 % | 80.61 % | 87.71 % |
| 0.75 ATR | 2.875 % | 127.4286 | 20.69 % | 36.51 % | 47.35 % | 58.86 % | 70.62 % | 81.32 % |
| 1.0 ATR | 3.833 % | 126.1714 | 10.78 % | 24.44 % | 34.77 % | 48.33 % | 61.92 % | 74.63 % |
| 1.25 ATR | 4.791 % | 124.9143 | 4.71 % | 16.39 % | 25.25 % | 39.57 % | 55.0 % | 68.23 % |
| 1.5 ATR | 5.749 % | 123.6571 | 2.45 % | 11.38 % | 18.96 % | 30.91 % | 47.48 % | 60.94 % |
| 2.0 ATR | 7.666 % | 121.1429 | 0.78 % | 5.4 % | 10.22 % | 19.69 % | 35.71 % | 50.95 % |
| 2.5 ATR | 9.582 % | 118.6286 | 0.49 % | 2.45 % | 5.4 % | 11.42 % | 24.73 % | 39.26 % |
| 3.0 ATR | 11.498 % | 116.1143 | 0.2 % | 1.57 % | 3.14 % | 7.19 % | 17.61 % | 30.77 % |
| 4.0 ATR | 15.331 % | 111.0857 | 0.1 % | 0.49 % | 0.88 % | 1.97 % | 7.52 % | 18.68 % |
| 6.0 ATR | 22.997 % | 101.0286 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.6 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.77 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.61 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.46 ATR | 2.02 ATR | 2.59 ATR |
| **5 s.** | 0.43 ATR | 0.96 ATR | 1.09 ATR | 1.44 ATR | 1.76 ATR | 1.99 ATR | 2.67 ATR | 3.42 ATR |
| **10 s.** | 0.64 ATR | 1.42 ATR | 1.60 ATR | 2.12 ATR | 2.49 ATR | 2.83 ATR | 3.75 ATR | 4.82 ATR |
| **20 s.** | 0.99 ATR | 2.04 ATR | 2.25 ATR | 2.87 ATR | 3.48 ATR | 3.89 ATR | 5.23 ATR | 5.94 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.396 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (82.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.617–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.875 %, prix 127.428), p(touche) 36.51 % (en stress 90.2 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.833 %, prix 126.1711), p(touche) 34.77 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.095–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.791 %, prix 124.9142), p(touche) 39.57 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.605–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.666 %, prix 121.1422), p(touche) 35.71 % (en stress 99.02 %)  ✅ optimum identifie (66.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.254–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.582 %, prix 118.6284), p(touche) 39.26 % (en stress 98.02 %)  ✅ optimum identifie (64.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : €-0.151 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 3 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 28.3 | bear 20.9 | side 50.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 262.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.467% → cible +1.925% / stop −8.0%, p_fill 80%, n_eff≈82.5) : P(cible|rempli) **15%** · **EV/risk -0.087** (×p_fill ; si rempli -0.87% du capital)
  - **swing** (entrée dip −1.042% → cible +8.625% / stop −4.313%, p_fill 73%, n_eff≈84.6) : P(cible|rempli) **3%** · **EV/risk -0.238** (×p_fill ; si rempli -1.41% du capital)
  - **deep** (entrée dip −1.611% → cible +9.251% / stop −5.843%, p_fill 72%, n_eff≈80.9) : P(cible|rempli) **8%** · **EV/risk -0.264** (×p_fill ; si rempli -2.14% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 68.4  _(momentum haussier)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist 1.804  _(pas de croisement recent)_
- **BB** : %B 0.92 · largeur 16.9%
- **ATR** : 5.03 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.09  _(accumulation)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 47.3  _(transition)_
- **MA** : MA20 122.45 · MA50 129.94 · MA200 135.53  _(prix > MA20)_
- **Dist MA** : MA20 +7.1% · MA50 +1.0% · MA200 -3.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (715658 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
