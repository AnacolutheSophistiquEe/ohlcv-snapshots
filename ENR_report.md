# ENR

**Generated** : 2026-10-16T21:43:46.114989+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €134.98  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (10 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €134.98 (+0.8% vs entrée) · entrée €133.94 · stop €123.23 · T1 €136.70 · R/R 0.26  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 134.98 · ATR Wilder 5.47 (4.05 %)_
- **Swing** : plage **128.87 → 124.29** (-4.53 % a -7.92 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 122.83-124.32 (A). stop INDICATIF 118.81 (-4.4 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **124.29 → 116.65** (-7.92 % a -13.58 % sous la cloture, 1.4 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 122.83-124.32 (A). stop INDICATIF 110.73 (-5.08 % sous le bas ; sous le support 113.47-114.51 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.93 ATR sous le plus haut 20 s., RSI(2) 41.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 130.89-133.3 (A, -1.24 %) ; 122.83-124.32 (A, -7.9 %) ; 113.47-114.51 (A, -15.16 %) ; 109.88-110.08 (C, -18.45 %) ; 103.21-104.4 (B, -22.65 %) ; 98.56-100.32 (A, -25.68 %)
- Resistances reelles au-dessus : 137.46-140.18 (A, 1.84 %) ; 143.38-146.08 (B, 6.22 %) ; 146.98-148.4 (B, 8.89 %) ; 150.58-151.76 (A, 11.56 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.67 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.78 %)** : le gap seul le franchit 0.785 % des séances (10 fois sur 1274).
   - exécution **1.301 pt plus bas** dans le cas TYPIQUE (médiane), 12.348 au p90, **29.977 au pire**
   - perte réelle **11.393 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 5.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0441 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.368 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0067** [0.0008 ; 0.0283] _(largeur 2.8 pt, n_eff 173.1)_
   - swing : **0.4605** [0.4085 ; 0.5132] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4422** [0.3905 ; 0.4948] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 80.2 observations effectives », dont la borne haute a 95 % vaut environ 3.7 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.65 %** | CVaR **-6.61 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.00 % contre 2.92 % aujourd'hui, rapport 2.06)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.76 % si l'on extrapolait par √5 _(rapport 0.903 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3422** (β de hausse 1.1058, asymétrie 1.2138) vs GDAXI — 598 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.302× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 121.1943 sur atr_grid (2.5 ATR, 10.213 %) — p(stop avant cible) 0.2486 [0.21 ; 0.30], R/R 3.689, perte reelle 10.572 % (gap inclus), CVaR 11.997 %, EV -0.1475 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.996 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.85 ATR (stop 6.266 %) — p(stop avant cible) 0.4929 [0.44 ; 0.55], R/R 5.937, perte reelle 6.569 % (gap inclus), EV -0.5329 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.1 % x 39.00 % + P(rien) 50.6 % x 5.30 % ne couvrent pas P(stop) 49.3 % x 6.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 support a 3.9 ATR (stop 18.721 %) — p(stop avant cible) 0.0241 [0.01 ; 0.04], R/R 1.974, perte reelle 19.762 % (gap inclus), EV 0.9213 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.79 % > budget 12.00 %
      - ⚠ support DETECTE a 0.75 ATR du spot — compartiment <1, mesure a 50.3 % de casse (IC clusterise [0.469 ; 0.537] sur 1152 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 6.37 ATR (stop 28.79 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 1.296, perte reelle 30.085 % (gap inclus), EV 1.0923 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.06 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.021 %) — p(stop avant cible) 0.9173 [0.88 ; 0.94], R/R 36.066, perte reelle 1.081 % (gap inclus), EV -0.172 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 36.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.917, borne haute 0.943 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 39.00 % + P(rien) 8.3 % x 9.92 % ne couvrent pas P(stop) 91.7 % x 1.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.043 %) — p(stop avant cible) 0.8276 [0.79 ; 0.86], R/R 18.205, perte reelle 2.142 % (gap inclus), EV -0.3145 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 18.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.828, borne haute 0.865 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.0 % x 39.00 % + P(rien) 17.2 % x 8.46 % ne couvrent pas P(stop) 82.8 % x 2.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.85 ATR (stop 4.71 %) — p(stop avant cible) 0.602 [0.55 ; 0.65], R/R 8.029, perte reelle 4.858 % (gap inclus), EV -0.3025 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.602, borne haute 0.653 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.1 % x 39.00 % + P(rien) 39.7 % x 6.54 % ne couvrent pas P(stop) 60.2 % x 4.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 7.149 %) — p(stop avant cible) 0.4401 [0.39 ; 0.49], R/R 5.247, perte reelle 7.434 % (gap inclus), EV -0.5399 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.1 % x 39.00 % + P(rien) 55.9 % x 4.84 % ne couvrent pas P(stop) 44.0 % x 7.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 8.171 %) — p(stop avant cible) 0.3639 [0.31 ; 0.42], R/R 4.587, perte reelle 8.503 % (gap inclus), EV -0.3897 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.1 % x 39.00 % + P(rien) 63.5 % x 4.22 % ne couvrent pas P(stop) 36.4 % x 8.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 9.192 %) — p(stop avant cible) 0.2973 [0.25 ; 0.35], R/R 4.1, perte reelle 9.513 % (gap inclus), EV -0.2064 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.1 % x 39.00 % + P(rien) 70.2 % x 3.70 % ne couvrent pas P(stop) 29.7 % x 9.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 10.213 %) — p(stop avant cible) 0.2486 [0.21 ; 0.30], R/R 3.689, perte reelle 10.572 % (gap inclus), EV -0.1475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.1 % x 39.00 % + P(rien) 75.1 % x 3.27 % ne couvrent pas P(stop) 24.9 % x 10.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 11.234 %) — p(stop avant cible) 0.1841 [0.15 ; 0.23], R/R 3.322, perte reelle 11.743 % (gap inclus), EV 0.0574 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.11 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 12.256 %) — p(stop avant cible) 0.1294 [0.10 ; 0.17], R/R 3.034, perte reelle 12.855 % (gap inclus), EV 0.3519 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.81 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 14.298 %) — p(stop avant cible) 0.0687 [0.05 ; 0.10], R/R 2.517, perte reelle 15.499 % (gap inclus), EV 0.6682 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.95 % > budget 12.00 %
   - 🔴 grid_snapped a 3.9 ATR (stop 17.164 %) — p(stop avant cible) 0.0303 [0.02 ; 0.05], R/R 2.12, perte reelle 18.397 % (gap inclus), EV 0.8888 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.98 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 20.426 %) — p(stop avant cible) 0.0113 [0.00 ; 0.03], R/R 1.746, perte reelle 22.34 % (gap inclus), EV 1.0077 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.469 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 1.535, perte reelle 25.411 % (gap inclus), EV 1.0275 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.78 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 24.512 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 1.431, perte reelle 27.258 % (gap inclus), EV 1.0571 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.51 % > budget 12.00 %
   - 🟢 grid_snapped a 6.37 ATR (stop 27.234 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.341, perte reelle 29.075 % (gap inclus), EV 1.0857 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 30.639 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 1.229, perte reelle 31.743 % (gap inclus), EV 1.0958 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.98 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 32.682 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.159, perte reelle 33.655 % (gap inclus), EV 1.103 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.82 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 134.98, ATR14 5.5143 (4.085 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.499 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.204 % | 134.7043 | 91.42 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.409 % | 134.4286 | 83.73 % | 88.25 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.613 % | 134.1529 | 76.43 % | 82.33 % | 85.87 % | 88.61 % | 91.14 % | 93.27 % |
| 0.2 ATR | 0.817 % | 133.8771 | 70.41 % | 78.97 % | 82.91 % | 86.53 % | 89.35 % | 91.86 % |
| 0.25 ATR | 1.021 % | 133.6014 | 63.81 % | 74.63 % | 79.25 % | 83.37 % | 87.36 % | 90.55 % |
| 0.35 ATR | 1.43 % | 133.05 | 51.78 % | 64.76 % | 70.16 % | 75.84 % | 81.99 % | 86.43 % |
| 0.5 ATR | 2.043 % | 132.2229 | 36.49 % | 51.83 % | 59.39 % | 66.44 % | 74.33 % | 80.3 % |
| 0.75 ATR | 3.064 % | 130.8443 | 19.63 % | 35.74 % | 45.06 % | 54.26 % | 65.07 % | 73.37 % |
| 1.0 ATR | 4.085 % | 129.4657 | 11.05 % | 25.47 % | 34.19 % | 44.06 % | 56.62 % | 65.33 % |
| 1.25 ATR | 5.107 % | 128.0871 | 6.11 % | 17.28 % | 24.8 % | 35.35 % | 47.96 % | 57.79 % |
| 1.5 ATR | 6.128 % | 126.7086 | 2.86 % | 11.06 % | 17.79 % | 27.52 % | 40.8 % | 51.46 % |
| 2.0 ATR | 8.171 % | 123.9514 | 0.79 % | 4.15 % | 8.7 % | 16.04 % | 27.86 % | 40.2 % |
| 2.5 ATR | 10.213 % | 121.1943 | 0.3 % | 2.07 % | 4.05 % | 9.31 % | 19.2 % | 30.45 % |
| 3.0 ATR | 12.256 % | 118.4371 | 0.1 % | 0.89 % | 1.98 % | 4.95 % | 12.24 % | 22.61 % |
| 4.0 ATR | 16.341 % | 112.9229 | 0.1 % | 0.39 % | 1.19 % | 2.28 % | 6.37 % | 12.46 % |
| 6.0 ATR | 24.512 % | 101.8943 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.58 ATR | 1.94 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.93 ATR | 2.40 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.98 ATR | 1.32 ATR | 1.61 ATR | 1.83 ATR | 2.45 ATR | 2.99 ATR |
| **10 s.** | 0.49 ATR | 1.19 ATR | 1.35 ATR | 1.80 ATR | 2.17 ATR | 2.45 ATR | 3.38 ATR | 4.66 ATR |
| **20 s.** | 0.69 ATR | 1.56 ATR | 1.79 ATR | 2.37 ATR | 2.85 ATR | 3.26 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.417–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.064 %, prix 130.8442), p(touche) 35.74 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.751–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.085 %, prix 129.4661), p(touche) 34.19 % (en stress 91.18 %)  ✅ optimum identifie (84.2 % des re-echantillons)
- **5 seance(s)** : plage utile 0.977–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.085 %, prix 129.4661), p(touche) 44.06 % (en stress 99.01 %)  ✅ optimum identifie (88.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.353–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.128 %, prix 126.7084), p(touche) 40.8 % (en stress 100.0 %)  ✅ optimum identifie (91.0 % des re-echantillons)
- **20 seance(s)** : plage utile 1.787–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.171 %, prix 123.9508), p(touche) 40.2 % (en stress 99.0 %)  ✅ optimum identifie (88.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 60.2 | side 34.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.772% → cible +2.058% / stop −8.0%, p_fill 76%, n_eff≈80.2) : P(cible|rempli) **27%** · **EV/risk -0.049** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −1.695% → cible +4.646% / stop −4.156%, p_fill 68%, n_eff≈80.0) : P(cible|rempli) **26%** · **EV/risk -0.229** (×p_fill ; si rempli -1.40% du capital)
  - **deep** (entrée dip −2.612% → cible +6.633% / stop −6.292%, p_fill 68%, n_eff≈76.6) : P(cible|rempli) **34%** · **EV/risk -0.136** (×p_fill ; si rempli -1.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→38% · +3.0%→18% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.7% (p90 6.11%) · excursion haute méd. +1.52% / basse méd. −1.74%
- Profil de vol intra : ouverture 1.958% vs midi 0.866% vs clôture 1.062% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.357% ; recovery-V 20%
- **σ réalisé intraday** 2.187% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 146.1558 (VA 145.4312–146.3972 ; dernier close 145.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 49% · rebond 59% · **stop −3.83%** sous le fill (sous le bruit) · cible +1.48% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 33% (gap-down >1% 15% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.67%) · haut méd +0.44% · range méd 1.12%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.17%) · haut méd +0.59% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.23%) · haut méd +0.62% · range méd 1.68%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.44%) · haut méd +0.73% · range méd 1.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 145.42 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 69% (116/159) · gap 24% · délai 0.5min · rebond 58% (62/116) (MFE +1.2%)
   - −1.0% : fill 30min 38% · séance 64% (108/159) · gap 15% · délai 10.3min · rebond 61% (62/108) (MFE +1.36%)
   - −1.5% : fill 30min 25% · séance 49% (88/159) · gap 11% · délai 22.9min · rebond 59% (50/88) (MFE +1.48%)
   - −2.0% : fill 30min 17% · séance 40% (73/159) · gap 8% · délai 62.1min · rebond 54% (44/73) (MFE +1.08%)
   - −3.0% : fill 30min 9% · séance 22% (46/159) · gap 2% · délai 189.8min · rebond 44% (26/46) (MFE +0.86%)
   - −4.0% : fill 30min 6% · séance 14% (33/159) · gap 1% · délai 76.7min · rebond 58% (22/33) (MFE +1.12%)
   - −5.0% : fill 30min 2% · séance 11% (24/159) · gap 0% · délai 388.5min · rebond 43% (12/24) (MFE +0.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.72%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.33% (p90 −1.32%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −0.95%) → stop au-delà de −0.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=521 jambes) : jambe baissière méd −1.02% (p90 −2.33%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (52/53) · rebond 55% (28/52)
      · −2.0% : fill 75% (39/53) · rebond 44% (20/39)
      · −3.0% : fill 45% (27/53) · rebond 33% (14/27)
      · −4.0% : fill 37% (22/53) · rebond 60% (16/22)
      · −5.0% : fill 31% (18/53) · rebond 49% (11/18)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 65% (10/14)
      · −2.0% : fill 44% (9/17) · rebond 67% (6/9)
      · −3.0% : fill 27% (6/17) · rebond 46% (3/6)
      · −4.0% : fill 9% (4/17) · rebond 52% (2/4)
      · −5.0% : fill 7% (3/17) · rebond 0% (0/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 43% (42/89) · rebond 66% (24/42)
      · −2.0% : fill 21% (25/89) · rebond 65% (18/25)
      · −3.0% : fill 8% (13/89) · rebond 72% (9/13)
      · −4.0% : fill 4% (7/89) · rebond 47% (4/7)
      · −5.0% : fill 2% (3/89) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (75 cas) · 24% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 219min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -1.07% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.24% / q75 +2.25% → **scale +1.24% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.65%** (au-delà de la MAE q10 -3.65%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.93% .. +1.69%] · haut q95 +2.36% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.46% .. +1.94%] · haut q95 +2.55% · bas q05 -2.86%
   - 2h (n=160) : retour [-2.78% .. +2.36%] · haut q95 +2.76% · bas q05 -3.56%
   - 4h (n=160) : retour [-3.15% .. +2.63%] · haut q95 +3.22% · bas q05 -3.93%
   - 6h (n=160) : retour [-3.69% .. +3.35%] · haut q95 +4.15% · bas q05 -4.56%
   - session (n=160) : retour [-4.9% .. +3.08%] · haut q95 +4.77% · bas q05 -6.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 42.5  _(momentum baissier)_
- **ADX** : 11.7  _(pas de tendance nette)_
- **MACD** : hist -0.934  _(bearish_recent)_
- **BB** : %B 0.03 · largeur 11.3%
- **ATR** : 5.51 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.054  _(accumulation)_
- **Vol ratio** : 1.38  _(volume normal)_
- **Choppiness** : 40.5  _(transition)_
- **MA** : MA20 142.62 · MA50 146.17 · MA200 154.3  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 -7.7% · MA200 -12.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (810674 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
