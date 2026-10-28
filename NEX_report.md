# NEX

**Generated** : 2026-10-28T21:48:07.941168+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €124.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €124.10 (+4.0% vs entrée) · entrée €119.36 · stop €109.82 · T1 €121.73 · R/R 0.25  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-28 : 124.1 · ATR Wilder 4.55 (3.67 %)_
- **Swing** : plage **118.1 → 114.41** (-4.83 % a -7.81 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 115.59-117.84 (B). stop INDICATIF 110.66 (-3.28 % sous le bas ; sous le support 112.93-114.01 (- 0,5 ATR)).
- **Deep** : plage **114.41 → 104.2** (-7.81 % a -16.03 % sous la cloture, 2.24 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 112.93-114.01 (B) ; 109.66-111.7 (A) ; 107.17-109.18 (A) ; 104.59-106.6 (B) ; 102.23-104.49 (A). stop INDICATIF 97.53 (-6.41 % sous le bas ; sous le support 99.8-102.03 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.97 ATR sous le plus haut 20 s., RSI(2) 88.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 121.04-122.56 (B, -1.24 %) ; 118.73-120.99 (B, -2.51 %) ; 115.59-117.84 (B, -5.04 %) ; 112.93-114.01 (B, -8.13 %) ; 109.66-111.7 (A, -9.99 %) ; 107.17-109.18 (A, -12.02 %)
- Resistances reelles au-dessus : 126.88-128.6 (A, 2.24 %) ; 129.73-131.89 (A, 4.53 %) ; 133.87-135.9 (A, 7.87 %) ; 136.3-137.6 (A, 9.83 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.45 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.45 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.535 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0028** [0.0001 ; 0.0209] _(largeur 2.1 pt, n_eff 173.1)_
   - swing : **0.3913** [0.3409 ; 0.4435] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.358** [0.3088 ; 0.4095] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.62 %** | CVaR **-5.31 %** | vol 2.32 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.8 % vs -8.09 % si l'on extrapolait par √5 _(rapport 0.964 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0093** (β de hausse 1.0886, asymétrie 0.9272) vs FCHI — 620 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 112.2607 sur atr_grid (2.5 ATR, 9.54 %) — p(stop avant cible) 0.163 [0.13 ; 0.20], R/R 3.274, perte reelle 9.681 % (gap inclus), CVaR 9.998 %, EV -0.2778 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.724 %) — p(stop avant cible) 0.4328 [0.38 ; 0.49], R/R 5.372, perte reelle 5.9 % (gap inclus), EV -0.5543 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 0.0 % x 31.70 % + P(rien) 56.7 % x 3.52 % ne couvrent pas P(stop) 43.3 % x 5.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ swing_based a 2.82 ATR (stop 13.258 %) — p(stop avant cible) 0.0571 [0.04 ; 0.09], R/R 2.325, perte reelle 13.631 % (gap inclus), EV -0.3271 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.0 % x 31.70 % + P(rien) 94.3 % x 0.48 % ne couvrent pas P(stop) 5.7 % x 13.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 0.954 %) — p(stop avant cible) 0.9199 [0.89 ; 0.94], R/R 31.991, perte reelle 0.991 % (gap inclus), EV -0.2645 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 31.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.920, borne haute 0.945 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 0.0 % x 31.70 % + P(rien) 8.0 % x 8.08 % ne couvrent pas P(stop) 92.0 % x 0.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.908 %) — p(stop avant cible) 0.7853 [0.74 ; 0.83], R/R 15.891, perte reelle 1.995 % (gap inclus), EV -0.3737 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 15.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.785, borne haute 0.826 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.0 % x 31.70 % + P(rien) 21.5 % x 5.55 % ne couvrent pas P(stop) 78.5 % x 1.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 2.862 %) — p(stop avant cible) 0.7042 [0.65 ; 0.75], R/R 10.738, perte reelle 2.952 % (gap inclus), EV -0.4522 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.704, borne haute 0.750 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.0 % x 31.70 % + P(rien) 29.6 % x 5.50 % ne couvrent pas P(stop) 70.4 % x 2.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 3.816 %) — p(stop avant cible) 0.6158 [0.56 ; 0.67], R/R 7.928, perte reelle 3.998 % (gap inclus), EV -0.5351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.616, borne haute 0.666 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.0 % x 31.70 % + P(rien) 38.4 % x 5.02 % ne couvrent pas P(stop) 61.6 % x 4.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 4.77 %) — p(stop avant cible) 0.5159 [0.46 ; 0.57], R/R 6.394, perte reelle 4.957 % (gap inclus), EV -0.5359 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.516, borne haute 0.568 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.0 % x 31.70 % + P(rien) 48.4 % x 4.18 % ne couvrent pas P(stop) 51.6 % x 4.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 6.678 %) — p(stop avant cible) 0.3497 [0.30 ; 0.40], R/R 4.652, perte reelle 6.813 % (gap inclus), EV -0.478 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 0.0 % x 31.70 % + P(rien) 65.0 % x 2.93 % ne couvrent pas P(stop) 35.0 % x 6.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 7.632 %) — p(stop avant cible) 0.2692 [0.22 ; 0.32], R/R 4.069, perte reelle 7.79 % (gap inclus), EV -0.3374 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.0 % x 31.70 % + P(rien) 73.1 % x 2.41 % ne couvrent pas P(stop) 26.9 % x 7.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 8.586 %) — p(stop avant cible) 0.2132 [0.17 ; 0.26], R/R 3.639, perte reelle 8.71 % (gap inclus), EV -0.2905 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 0.0 % x 31.70 % + P(rien) 78.7 % x 1.99 % ne couvrent pas P(stop) 21.3 % x 8.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 9.54 %) — p(stop avant cible) 0.163 [0.13 ; 0.20], R/R 3.274, perte reelle 9.681 % (gap inclus), EV -0.2778 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.0 % x 31.70 % + P(rien) 83.7 % x 1.55 % ne couvrent pas P(stop) 16.3 % x 9.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 2.82 ATR (stop 11.9 %) — p(stop avant cible) 0.0875 [0.06 ; 0.12], R/R 2.605, perte reelle 12.167 % (gap inclus), EV -0.3018 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.0 % x 31.70 % + P(rien) 91.2 % x 0.84 % ne couvrent pas P(stop) 8.8 % x 12.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 15.264 %) — p(stop avant cible) 0.0274 [0.01 ; 0.05], R/R 2.024, perte reelle 15.66 % (gap inclus), EV -0.2706 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 0.0 % x 31.70 % + P(rien) 97.3 % x 0.16 % ne couvrent pas P(stop) 2.7 % x 15.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 17.172 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 1.795, perte reelle 17.654 % (gap inclus), EV -0.2201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 0.0 % x 31.70 % + P(rien) 99.2 % x -0.08 % ne couvrent pas P(stop) 0.8 % x 17.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 19.08 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.597, perte reelle 19.845 % (gap inclus), EV -0.1929 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.0 % x 31.70 % + P(rien) 99.6 % x -0.12 % ne couvrent pas P(stop) 0.4 % x 19.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 20.988 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 1.395, perte reelle 22.72 % (gap inclus), EV -0.1836 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.0 % x 31.70 % + P(rien) 99.8 % x -0.14 % ne couvrent pas P(stop) 0.2 % x 22.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 22.896 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.327, perte reelle 23.889 % (gap inclus), EV -0.1811 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.0 % x 31.70 % + P(rien) 99.9 % x -0.15 % ne couvrent pas P(stop) 0.1 % x 23.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 24.804 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.274, perte reelle 24.876 % (gap inclus), EV -0.1776 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.0 % x 31.70 % + P(rien) 99.9 % x -0.16 % ne couvrent pas P(stop) 0.1 % x 24.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 26.712 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.187, perte reelle 26.712 % (gap inclus), EV -0.1735 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 31.70 % + P(rien) 100.0 % x -0.17 % ne couvrent pas P(stop) 0.0 % x 26.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 28.62 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.107, perte reelle 28.62 % (gap inclus), EV -0.1735 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 31.70 % + P(rien) 100.0 % x -0.17 % ne couvrent pas P(stop) 0.0 % x 28.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 30.528 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.038, perte reelle 30.528 % (gap inclus), EV -0.1735 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 31.70 % + P(rien) 100.0 % x -0.17 % ne couvrent pas P(stop) 0.0 % x 30.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+31.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 124.1, ATR14 4.7357 (3.816 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 1.328 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.191 % | 123.8632 | 87.65 % | 91.46 % | 93.32 % | 95.18 % | 97.03 % | 97.9 % |
| 0.1 ATR | 0.382 % | 123.6264 | 81.86 % | 87.83 % | 90.47 % | 93.21 % | 95.65 % | 97.0 % |
| 0.15 ATR | 0.572 % | 123.3896 | 75.29 % | 83.61 % | 87.03 % | 90.26 % | 94.16 % | 95.7 % |
| 0.2 ATR | 0.763 % | 123.1529 | 68.73 % | 78.41 % | 83.3 % | 88.29 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.954 % | 122.9161 | 62.16 % | 73.7 % | 79.17 % | 85.14 % | 90.7 % | 93.81 % |
| 0.35 ATR | 1.336 % | 122.4425 | 49.8 % | 64.18 % | 71.81 % | 78.84 % | 86.65 % | 91.61 % |
| 0.5 ATR | 1.908 % | 121.7321 | 34.9 % | 52.5 % | 61.39 % | 70.87 % | 80.22 % | 87.41 % |
| 0.75 ATR | 2.862 % | 120.5482 | 20.69 % | 36.41 % | 47.35 % | 58.76 % | 70.23 % | 80.92 % |
| 1.0 ATR | 3.816 % | 119.3643 | 10.78 % | 24.53 % | 34.97 % | 48.43 % | 61.62 % | 74.23 % |
| 1.25 ATR | 4.77 % | 118.1804 | 4.8 % | 16.58 % | 25.44 % | 39.76 % | 54.6 % | 67.73 % |
| 1.5 ATR | 5.724 % | 116.9964 | 2.55 % | 11.58 % | 19.25 % | 31.1 % | 47.18 % | 60.34 % |
| 2.0 ATR | 7.632 % | 114.6286 | 0.88 % | 5.59 % | 10.51 % | 19.78 % | 35.61 % | 50.35 % |
| 2.5 ATR | 9.54 % | 112.2607 | 0.49 % | 2.65 % | 5.7 % | 11.71 % | 24.73 % | 38.46 % |
| 3.0 ATR | 11.448 % | 109.8929 | 0.2 % | 1.67 % | 3.24 % | 7.38 % | 17.51 % | 29.87 % |
| 4.0 ATR | 15.264 % | 105.1571 | 0.1 % | 0.49 % | 0.88 % | 1.97 % | 7.42 % | 17.78 % |
| 6.0 ATR | 22.896 % | 95.6857 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.77 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.63 ATR | 2.10 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.80 ATR | 1.05 ATR | 1.27 ATR | 1.47 ATR | 2.05 ATR | 2.64 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.10 ATR | 1.45 ATR | 1.77 ATR | 1.99 ATR | 2.70 ATR | 3.44 ATR |
| **10 s.** | 0.63 ATR | 1.41 ATR | 1.59 ATR | 2.12 ATR | 2.49 ATR | 2.83 ATR | 3.74 ATR | 4.80 ATR |
| **20 s.** | 0.97 ATR | 2.02 ATR | 2.23 ATR | 2.82 ATR | 3.40 ATR | 3.82 ATR | 5.16 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (80.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.617–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.862 %, prix 120.5483), p(touche) 36.41 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.816 %, prix 119.3643), p(touche) 34.97 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.099–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.77 %, prix 118.1804), p(touche) 39.76 % (en stress 94.12 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.594–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.632 %, prix 114.6287), p(touche) 35.61 % (en stress 99.02 %)  ✅ optimum identifie (66.1 % des re-echantillons)
- **20 seance(s)** : plage utile 2.225–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.54 %, prix 112.2609), p(touche) 38.46 % (en stress 98.02 %)  ✅ optimum identifie (67.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 76.0 | bear 5.0 | side 19.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=11))
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.2  _(neutre)_
- **ADX** : 22.6  _(pas de tendance nette)_
- **MACD** : hist -0.179  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 20.7%
- **ATR** : 4.74 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.028  _(neutre)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 41.5  _(transition)_
- **MA** : MA20 126.05 · MA50 133.35 · MA200 135.63  _(prix < MA20)_
- **Dist MA** : MA20 -1.6% · MA50 -6.9% · MA200 -8.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (792646 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
