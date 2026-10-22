# NEX

**Generated** : 2026-10-22T00:09:52.757557+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €121.60  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 11/125 fenêtres (p_fill pondéré 9 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €121.60 (+3.9% vs entrée) · entrée €117.01 · stop €115.26 · T1 €119.31 · R/R 1.31  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-21 : 121.6 · ATR Wilder 4.44 (3.65 %)_
- **Swing** : plage **115.93 → 112.32** (-4.67 % a -7.63 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 115.59-117.16 (B) ; 112.93-114.01 (B). stop INDICATIF 107.44 (-4.35 % sous le bas ; sous le support 109.66-110.28 (- 0,5 ATR)).
- **Deep** : plage **112.32 → 102.42** (-7.63 % a -15.77 % sous la cloture, 2.23 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 109.66-110.28 (A) ; 107.17-109.18 (A) ; 104.49-106.6 (B) ; 102.03-102.92 (A). stop INDICATIF 97.58 (-4.72 % sous le bas ; sous le support 99.8-101.93 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.37 ATR sous le plus haut 20 s., RSI(2) 48.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 117.84-119.71 (B, -1.55 %) ; 115.59-117.16 (B, -3.65 %) ; 112.93-114.01 (B, -6.24 %) ; 109.66-110.28 (A, -9.31 %) ; 107.17-109.18 (A, -10.21 %) ; 104.49-106.6 (B, -12.34 %)
- Resistances reelles au-dessus : 123.8-125.7 (A, 1.81 %) ; 126.88-128.6 (A, 4.34 %) ; 129.73-131.89 (A, 6.68 %) ; 133.87-135.9 (A, 10.09 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.31 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.535 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4286** [0.3566 ; 0.503] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.3834** [0.3333 ; 0.4354] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3447** [0.2961 ; 0.3959] _(largeur 10.0 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.62 %** | CVaR **-5.29 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.6 % vs -7.9 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 0.9994** (β de hausse 1.0886, asymétrie 0.9181) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 108.9893 sur atr_grid (2.75 ATR, 10.371 %) — p(stop avant cible) 0.1042 [0.08 ; 0.14], R/R 3.272, perte reelle 10.527 % (gap inclus), CVaR 10.696 %, EV -0.0127 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.657 %) — p(stop avant cible) 0.4262 [0.37 ; 0.48], R/R 5.886, perte reelle 5.851 % (gap inclus), EV -0.4274 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 0.0 % x 34.44 % + P(rien) 57.4 % x 3.60 % ne couvrent pas P(stop) 42.6 % x 5.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 0.943 %) — p(stop avant cible) 0.9176 [0.89 ; 0.94], R/R 35.115, perte reelle 0.981 % (gap inclus), EV -0.2344 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 35.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.918, borne haute 0.943 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.0 % x 34.44 % + P(rien) 8.2 % x 8.08 % ne couvrent pas P(stop) 91.8 % x 0.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.886 %) — p(stop avant cible) 0.7895 [0.74 ; 0.83], R/R 17.55, perte reelle 1.962 % (gap inclus), EV -0.3365 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 17.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.789, borne haute 0.830 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.0 % x 34.44 % + P(rien) 21.1 % x 5.76 % ne couvrent pas P(stop) 79.0 % x 1.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 2.828 %) — p(stop avant cible) 0.7033 [0.65 ; 0.75], R/R 11.806, perte reelle 2.917 % (gap inclus), EV -0.3676 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.703, borne haute 0.750 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.0 % x 34.44 % + P(rien) 29.7 % x 5.68 % ne couvrent pas P(stop) 70.3 % x 2.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 3.771 %) — p(stop avant cible) 0.6096 [0.56 ; 0.66], R/R 8.761, perte reelle 3.931 % (gap inclus), EV -0.4531 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.610, borne haute 0.660 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.0 % x 34.44 % + P(rien) 39.0 % x 4.98 % ne couvrent pas P(stop) 61.0 % x 3.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 4.714 %) — p(stop avant cible) 0.5123 [0.46 ; 0.56], R/R 7.049, perte reelle 4.886 % (gap inclus), EV -0.4439 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.512, borne haute 0.565 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 0.0 % x 34.44 % + P(rien) 48.8 % x 4.22 % ne couvrent pas P(stop) 51.2 % x 4.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 6.6 %) — p(stop avant cible) 0.3397 [0.29 ; 0.39], R/R 5.101, perte reelle 6.751 % (gap inclus), EV -0.3244 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 34.44 % + P(rien) 66.0 % x 2.98 % ne couvrent pas P(stop) 34.0 % x 6.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 7.542 %) — p(stop avant cible) 0.2563 [0.21 ; 0.30], R/R 4.47, perte reelle 7.705 % (gap inclus), EV -0.1364 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.0 % x 34.44 % + P(rien) 74.4 % x 2.47 % ne couvrent pas P(stop) 25.6 % x 7.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 8.485 %) — p(stop avant cible) 0.2023 [0.16 ; 0.25], R/R 4.001, perte reelle 8.609 % (gap inclus), EV -0.0723 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.0 % x 34.44 % + P(rien) 79.8 % x 2.09 % ne couvrent pas P(stop) 20.2 % x 8.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 9.428 %) — p(stop avant cible) 0.1449 [0.11 ; 0.18], R/R 3.6, perte reelle 9.566 % (gap inclus), EV -0.0225 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.0 % x 34.44 % + P(rien) 85.5 % x 1.59 % ne couvrent pas P(stop) 14.5 % x 9.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 10.371 %) — p(stop avant cible) 0.1042 [0.08 ; 0.14], R/R 3.272, perte reelle 10.527 % (gap inclus), EV -0.0127 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 0.0 % x 34.44 % + P(rien) 89.6 % x 1.21 % ne couvrent pas P(stop) 10.4 % x 10.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 11.313 %) — p(stop avant cible) 0.0779 [0.05 ; 0.11], R/R 2.991, perte reelle 11.514 % (gap inclus), EV 0.0038 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 13.199 %) — p(stop avant cible) 0.0411 [0.02 ; 0.07], R/R 2.504, perte reelle 13.755 % (gap inclus), EV -0.017 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.0 % x 34.44 % + P(rien) 95.9 % x 0.57 % ne couvrent pas P(stop) 4.1 % x 13.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.4 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 15.085 %) — p(stop avant cible) 0.0177 [0.01 ; 0.04], R/R 2.183, perte reelle 15.775 % (gap inclus), EV 0.036 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.97 %) — p(stop avant cible) 0.0085 [0.00 ; 0.02], R/R 1.962, perte reelle 17.553 % (gap inclus), EV 0.0514 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.73 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.856 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 1.746, perte reelle 19.721 % (gap inclus), EV 0.0794 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.48 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.741 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 1.553, perte reelle 22.174 % (gap inclus), EV 0.084 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.43 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.627 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.45, perte reelle 23.755 % (gap inclus), EV 0.0916 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.512 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.384, perte reelle 24.876 % (gap inclus), EV 0.0946 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.21 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.398 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.305, perte reelle 26.398 % (gap inclus), EV 0.0937 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.284 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.218, perte reelle 28.284 % (gap inclus), EV 0.0984 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.13 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.169 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.142, perte reelle 30.169 % (gap inclus), EV 0.0984 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.13 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 121.6, ATR14 4.5857 (3.771 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 1.316 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 121.3707 | 87.84 % | 91.56 % | 93.32 % | 95.18 % | 97.03 % | 97.9 % |
| 0.1 ATR | 0.377 % | 121.1414 | 82.06 % | 87.93 % | 90.47 % | 93.21 % | 95.65 % | 97.0 % |
| 0.15 ATR | 0.566 % | 120.9121 | 75.49 % | 83.71 % | 87.03 % | 90.26 % | 94.16 % | 95.7 % |
| 0.2 ATR | 0.754 % | 120.6829 | 69.02 % | 78.51 % | 83.3 % | 88.29 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.943 % | 120.4536 | 62.35 % | 73.7 % | 79.17 % | 85.14 % | 90.7 % | 93.81 % |
| 0.35 ATR | 1.32 % | 119.995 | 49.9 % | 64.18 % | 71.81 % | 78.84 % | 86.65 % | 91.61 % |
| 0.5 ATR | 1.886 % | 119.3071 | 35.0 % | 52.5 % | 61.39 % | 70.87 % | 80.22 % | 87.41 % |
| 0.75 ATR | 2.828 % | 118.1607 | 20.69 % | 36.41 % | 47.15 % | 58.76 % | 70.23 % | 80.92 % |
| 1.0 ATR | 3.771 % | 117.0143 | 10.78 % | 24.53 % | 34.77 % | 48.43 % | 61.62 % | 74.23 % |
| 1.25 ATR | 4.714 % | 115.8679 | 4.8 % | 16.49 % | 25.25 % | 39.76 % | 54.6 % | 67.83 % |
| 1.5 ATR | 5.657 % | 114.7214 | 2.45 % | 11.58 % | 19.06 % | 31.1 % | 47.18 % | 60.34 % |
| 2.0 ATR | 7.542 % | 112.4286 | 0.88 % | 5.59 % | 10.51 % | 20.08 % | 35.61 % | 50.35 % |
| 2.5 ATR | 9.428 % | 110.1357 | 0.49 % | 2.75 % | 5.89 % | 11.81 % | 24.83 % | 38.46 % |
| 3.0 ATR | 11.313 % | 107.8429 | 0.2 % | 1.67 % | 3.24 % | 7.28 % | 17.61 % | 29.87 % |
| 4.0 ATR | 15.085 % | 103.2571 | 0.1 % | 0.49 % | 0.88 % | 1.97 % | 7.42 % | 17.58 % |
| 6.0 ATR | 22.627 % | 94.0857 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.77 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.63 ATR | 2.10 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.05 ATR | 1.26 ATR | 1.46 ATR | 2.06 ATR | 2.67 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.10 ATR | 1.45 ATR | 1.78 ATR | 2.00 ATR | 2.70 ATR | 3.43 ATR |
| **10 s.** | 0.63 ATR | 1.41 ATR | 1.59 ATR | 2.12 ATR | 2.49 ATR | 2.83 ATR | 3.75 ATR | 4.80 ATR |
| **20 s.** | 0.97 ATR | 2.02 ATR | 2.23 ATR | 2.82 ATR | 3.40 ATR | 3.80 ATR | 5.15 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.617–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.828 %, prix 118.1612), p(touche) 36.41 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.793–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.771 %, prix 117.0145), p(touche) 34.77 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.099–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.714 %, prix 115.8678), p(touche) 39.76 % (en stress 94.12 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.594–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.542 %, prix 112.4289), p(touche) 35.61 % (en stress 99.02 %)  ✅ optimum identifie (70.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.225–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.428 %, prix 110.1356), p(touche) 38.46 % (en stress 98.02 %)  ✅ optimum identifie (68.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 61.2 | bear 5.1 | side 33.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=10))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→57% · +2.0%→28% · +3.0%→12% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.73% (p90 4.75%) · excursion haute méd. +1.13% / basse méd. −1.13%
- Profil de vol intra : ouverture 1.673% vs midi 0.529% vs clôture 0.71% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -0.332% ; recovery-V 10%
- **σ réalisé intraday** 1.991% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 71% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 136.2225 (VA 135.7475–137.0775 ; dernier close 136.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 25% · rebond 31% · **stop −2.1%** sous le fill (sous le bruit) · cible +0.53% · R/R 0.25 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 25% (gap-down >1% 3% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.34% (p90 −1.71%) · haut méd +0.28% · range méd 0.92%
- Excursion ouverture 15min (n=160) : bas méd −0.45% (p90 −1.95%) · haut méd +0.44% · range méd 1.27%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.08%) · haut méd +0.6% · range méd 1.4%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.28%) · haut méd +0.64% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 38% · séance 57% (88/159) · gap 9% · délai 3.9min · rebond 41% (38/88) (MFE +0.64%)
   - −1.0% : fill 30min 20% · séance 46% (69/159) · gap 3% · délai 51.9min · rebond 35% (27/69) (MFE +0.58%)
   - −1.5% : fill 30min 12% · séance 36% (54/159) · gap 0% · délai 62.0min · rebond 31% (19/54) (MFE +0.58%)
   - −2.0% : fill 30min 7% · séance 25% (39/159) · gap 0% · délai 111.9min · rebond 31% (15/39) (MFE +0.53%)
   - −3.0% : fill 30min 4% · séance 14% (23/159) · gap 0% · délai 268.3min · rebond 37% (10/23) (MFE +0.59%)
   - −4.0% : fill 30min 2% · séance 5% (10/159) · gap 0% · délai 161.7min · rebond 8% (3/10) (MFE +0.38%)
   - −5.0% : fill 30min 0% · séance 3% (4/159) · gap 0% · délai 260.4min · rebond 24% (2/4) (MFE +0.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.99%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.81%) → stop au-delà de −0.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.78%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.01% (p90 −2.27%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 77% (17/22) · rebond 27% (6/17)
      · −2.0% : fill 61% (12/22) · rebond 12% (2/12)
      · −3.0% : fill 43% (9/22) · rebond 15% (3/9)
      · −4.0% : fill 26% (6/22) · rebond 4% (1/6)
      · −5.0% : fill 20% (3/22) · rebond 20% (1/3)
   - **flat** (36 séances) :
      · −1.0% : fill 54% (21/36) · rebond 27% (7/21)
      · −2.0% : fill 25% (12/36) · rebond 33% (5/12)
      · −3.0% : fill 16% (8/36) · rebond 32% (3/8)
      · −4.0% : fill 5% (3/36) · rebond 8% (1/3)
      · −5.0% : fill 0% (1/36) · rebond 100% (1/1)
   - **gap-up** (101 séances) :
      · −1.0% : fill 35% (31/101) · rebond 44% (14/31)
      · −2.0% : fill 18% (15/101) · rebond 45% (8/15)
      · −3.0% : fill 6% (6/101) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/101) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/101) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 65% si les 15 1res min sont vertes (85 cas) · 22% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **20min** → P(séance verte=clôture>ouverture) 69% si début vert vs 23% si rouge (base 46% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 242min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **69%** · continue >prix actuel 58% ; creux résiduel méd -0.98% (q20 -1.84%) → **SL/trailing à −1.84%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.1% / q75 +1.84% → **scale +1.1% / runner +1.84%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **23%** (continue à baisser 63%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.05%** (au-delà de la MAE q10 -3.05%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.96% .. +1.64%] · haut q95 +2.01% · bas q05 -2.58%
   - 60min (n=160) : retour [-2.59% .. +2.13%] · haut q95 +2.44% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.07% .. +2.15%] · haut q95 +2.67% · bas q05 -3.66%
   - 4h (n=160) : retour [-2.91% .. +2.47%] · haut q95 +3.05% · bas q05 -3.75%
   - 6h (n=160) : retour [-3.6% .. +3.4%] · haut q95 +3.53% · bas q05 -4.13%
   - session (n=160) : retour [-3.38% .. +2.74%] · haut q95 +3.86% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.4  _(momentum baissier)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -1.029  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 15.2%
- **ATR** : 4.59 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.227  _(distribution)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 42.7  _(transition)_
- **MA** : MA20 129.92 · MA50 135.49 · MA200 135.72  _(prix < MA20)_
- **Dist MA** : MA20 -6.4% · MA50 -10.2% · MA200 -10.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (770036 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
