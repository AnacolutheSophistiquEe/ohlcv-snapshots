# NEX

**Generated** : 2026-11-19T21:48:33.820177+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €126.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot €126.00 (+7.7% vs entrée) · entrée €117.04 · stop €111.25 · T1 €128.61 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-19 : 126.0 · ATR Wilder 4.63 (3.68 %)_
- **Swing** : plage **119.66 → 115.9** (-5.03 % a -8.02 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 118.73-120.99 (B) ; 115.59-117.84 (A). stop INDICATIF 110.62 (-4.56 % sous le bas ; sous le support 112.93-114.01 (- 0,5 ATR)).
- **Deep** : plage **115.9 → 105.02** (-8.02 % a -16.65 % sous la cloture, 2.35 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 115.59-117.84 (A) ; 112.93-114.01 (B) ; 109.66-111.7 (A) ; 107.17-109.18 (A) ; 104.59-106.6 (B). stop INDICATIF 99.91 (-4.87 % sous le bas ; sous le support 102.23-104.49 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.75 ATR sous le plus haut 20 s., RSI(2) 21.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 121.04-122.56 (B, -2.73 %) ; 118.73-120.99 (B, -3.98 %) ; 115.59-117.84 (A, -6.47 %) ; 112.93-114.01 (B, -9.51 %) ; 109.66-111.7 (A, -11.35 %) ; 107.17-109.18 (A, -13.35 %)
- Resistances reelles au-dessus : 129.5-131.79 (A, 2.78 %) ; 131.89-134.1 (A, 4.67 %) ; 134.34-136.3 (A, 6.62 %) ; 137.58-139.35 (A, 9.19 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.71 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.71 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.57 % | p01 -3.604 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0023** [0.0001 ; 0.0198] _(largeur 2.0 pt, n_eff 173.1)_
   - swing : **0.3153** [0.268 ; 0.3657] _(largeur 9.8 pt, n_eff 345.8)_
   - deep : **0.3039** [0.2572 ; 0.3539] _(largeur 9.7 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.3 observations effectives », dont la borne haute a 95 % vaut environ 20.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.62 %** | CVaR **-5.37 %** | vol 2.33 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.8 % vs -8.12 % si l'on extrapolait par √5 _(rapport 0.96 ; < 1 = le √5 surestime)_
- **β de baisse : 0.9958** (β de hausse 1.0861, asymétrie 0.9169) vs FCHI — 624 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 113.859 sur grid_snapped (2.41 ATR, 9.636 %) — p(stop avant cible) 0.1514 [0.12 ; 0.19], R/R 3.05, perte reelle 9.761 % (gap inclus), CVaR 10.013 %, EV -0.0182 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.336 %) — p(stop avant cible) 0.4643 [0.41 ; 0.52], R/R 5.395, perte reelle 5.518 % (gap inclus), EV -0.4513 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.0 % x 29.77 % + P(rien) 53.6 % x 3.94 % ne couvrent pas P(stop) 46.4 % x 5.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ swing_based a 2.41 ATR (stop 10.553 %) — p(stop avant cible) 0.1255 [0.09 ; 0.16], R/R 2.794, perte reelle 10.653 % (gap inclus), EV -0.0637 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.0 % x 29.77 % + P(rien) 87.5 % x 1.46 % ne couvrent pas P(stop) 12.6 % x 10.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 0.889 %) — p(stop avant cible) 0.9237 [0.89 ; 0.95], R/R 32.255, perte reelle 0.923 % (gap inclus), EV -0.2412 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 32.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.924, borne haute 0.948 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.0 % x 29.77 % + P(rien) 7.6 % x 8.01 % ne couvrent pas P(stop) 92.4 % x 0.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.779 %) — p(stop avant cible) 0.807 [0.76 ; 0.85], R/R 16.056, perte reelle 1.854 % (gap inclus), EV -0.3283 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 16.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.807, borne haute 0.846 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.0 % x 29.77 % + P(rien) 19.3 % x 6.05 % ne couvrent pas P(stop) 80.7 % x 1.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 2.668 %) — p(stop avant cible) 0.7178 [0.67 ; 0.76], R/R 10.846, perte reelle 2.745 % (gap inclus), EV -0.3488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.718, borne haute 0.763 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.0 % x 29.77 % + P(rien) 28.2 % x 5.75 % ne couvrent pas P(stop) 71.8 % x 2.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 3.557 %) — p(stop avant cible) 0.6469 [0.60 ; 0.70], R/R 8.042, perte reelle 3.702 % (gap inclus), EV -0.504 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.647, borne haute 0.696 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 0.0 % x 29.77 % + P(rien) 35.3 % x 5.35 % ne couvrent pas P(stop) 64.7 % x 3.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 4.447 %) — p(stop avant cible) 0.5613 [0.51 ; 0.61], R/R 6.46, perte reelle 4.609 % (gap inclus), EV -0.5076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.561, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.0 % x 29.77 % + P(rien) 43.9 % x 4.74 % ne couvrent pas P(stop) 56.1 % x 4.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 6.225 %) — p(stop avant cible) 0.3936 [0.34 ; 0.45], R/R 4.674, perte reelle 6.369 % (gap inclus), EV -0.4201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 0.0 % x 29.77 % + P(rien) 60.6 % x 3.44 % ne couvrent pas P(stop) 39.4 % x 6.37 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 7.115 %) — p(stop avant cible) 0.3039 [0.26 ; 0.35], R/R 4.105, perte reelle 7.252 % (gap inclus), EV -0.1609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.0 % x 29.77 % + P(rien) 69.6 % x 2.94 % ne couvrent pas P(stop) 30.4 % x 7.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 2.41 ATR (stop 9.636 %) — p(stop avant cible) 0.1514 [0.12 ; 0.19], R/R 3.05, perte reelle 9.761 % (gap inclus), EV -0.0182 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.0 % x 29.77 % + P(rien) 84.9 % x 1.72 % ne couvrent pas P(stop) 15.1 % x 9.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 12.45 %) — p(stop avant cible) 0.0709 [0.05 ; 0.10], R/R 2.343, perte reelle 12.704 % (gap inclus), EV -0.0335 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.0 % x 29.77 % + P(rien) 92.9 % x 0.93 % ne couvrent pas P(stop) 7.1 % x 12.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+29.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 14.229 %) — p(stop avant cible) 0.037 [0.02 ; 0.06], R/R 2.056, perte reelle 14.477 % (gap inclus), EV 0.0481 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.83 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.008 %) — p(stop avant cible) 0.0206 [0.01 ; 0.04], R/R 1.825, perte reelle 16.313 % (gap inclus), EV 0.0657 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.63 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.786 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 1.627, perte reelle 18.299 % (gap inclus), EV 0.1271 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.81 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.565 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.449, perte reelle 20.543 % (gap inclus), EV 0.1482 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.344 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 1.303, perte reelle 22.839 % (gap inclus), EV 0.1502 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.58 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.122 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.24, perte reelle 24.002 % (gap inclus), EV 0.1515 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.54 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 24.901 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 1.196, perte reelle 24.901 % (gap inclus), EV 0.1561 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.48 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.679 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.116, perte reelle 26.679 % (gap inclus), EV 0.1587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.41 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 28.458 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.046, perte reelle 28.458 % (gap inclus), EV 0.1587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.41 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 126.0, ATR14 4.4821 (3.557 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 1.234 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.178 % | 125.7759 | 87.75 % | 91.56 % | 93.32 % | 95.18 % | 96.93 % | 97.9 % |
| 0.1 ATR | 0.356 % | 125.5518 | 81.86 % | 87.83 % | 90.47 % | 93.21 % | 95.55 % | 97.0 % |
| 0.15 ATR | 0.534 % | 125.3277 | 75.29 % | 83.61 % | 87.03 % | 90.26 % | 94.07 % | 95.7 % |
| 0.2 ATR | 0.711 % | 125.1036 | 68.43 % | 78.02 % | 83.01 % | 88.09 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.889 % | 124.8795 | 61.86 % | 73.41 % | 78.88 % | 85.14 % | 90.8 % | 93.81 % |
| 0.35 ATR | 1.245 % | 124.4312 | 49.61 % | 64.08 % | 71.71 % | 79.04 % | 87.04 % | 91.71 % |
| 0.5 ATR | 1.779 % | 123.7589 | 34.51 % | 52.5 % | 61.3 % | 71.06 % | 80.42 % | 87.71 % |
| 0.75 ATR | 2.668 % | 122.6384 | 20.59 % | 36.31 % | 47.35 % | 58.76 % | 70.33 % | 81.32 % |
| 1.0 ATR | 3.557 % | 121.5179 | 10.78 % | 24.34 % | 34.58 % | 48.13 % | 61.52 % | 74.63 % |
| 1.25 ATR | 4.447 % | 120.3973 | 4.71 % | 16.39 % | 25.25 % | 39.57 % | 54.8 % | 68.13 % |
| 1.5 ATR | 5.336 % | 119.2768 | 2.45 % | 11.38 % | 18.96 % | 30.91 % | 47.48 % | 60.94 % |
| 2.0 ATR | 7.115 % | 117.0357 | 0.78 % | 5.4 % | 10.12 % | 19.59 % | 35.61 % | 50.95 % |
| 2.5 ATR | 8.893 % | 114.7946 | 0.49 % | 2.45 % | 5.4 % | 11.42 % | 24.73 % | 39.36 % |
| 3.0 ATR | 10.672 % | 112.5536 | 0.2 % | 1.57 % | 3.14 % | 7.19 % | 17.61 % | 30.97 % |
| 4.0 ATR | 14.229 % | 108.0714 | 0.1 % | 0.49 % | 0.88 % | 1.97 % | 7.52 % | 18.78 % |
| 6.0 ATR | 21.344 % | 99.1071 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.5 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.77 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.61 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.80 ATR | 1.04 ATR | 1.26 ATR | 1.46 ATR | 2.01 ATR | 2.59 ATR |
| **5 s.** | 0.43 ATR | 0.96 ATR | 1.09 ATR | 1.44 ATR | 1.76 ATR | 1.98 ATR | 2.67 ATR | 3.42 ATR |
| **10 s.** | 0.63 ATR | 1.41 ATR | 1.60 ATR | 2.12 ATR | 2.49 ATR | 2.83 ATR | 3.75 ATR | 4.81 ATR |
| **20 s.** | 0.99 ATR | 2.04 ATR | 2.26 ATR | 2.88 ATR | 3.49 ATR | 3.90 ATR | 5.23 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.396 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (79.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.616–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.668 %, prix 122.6383), p(touche) 36.31 % (en stress 90.2 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.796–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.557 %, prix 121.5182), p(touche) 34.58 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.091–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.447 %, prix 120.3968), p(touche) 39.57 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.604–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.115 %, prix 117.0351), p(touche) 35.61 % (en stress 98.04 %)  ✅ optimum identifie (67.1 % des re-echantillons)
- **20 seance(s)** : plage utile 2.257–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.893 %, prix 114.7948), p(touche) 39.36 % (en stress 98.02 %)  ✅ optimum identifie (63.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.019 | EV/share : €-0.113 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 9 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 35.3 | bear 10.1 | side 54.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 252.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.554% → cible +1.844% / stop −8.0%, p_fill 14%, n_eff≈14.3) : P(cible|rempli) **27%** · **EV/risk -0.000** (×p_fill ; si rempli -0.00% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
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

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.58 · part idiosyncratique 0.42
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 61.9  _(momentum haussier)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist 0.781  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 16.4%
- **ATR** : 4.48 (55.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.021  _(neutre)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 47.3  _(transition)_
- **MA** : MA20 124.14 · MA50 128.82 · MA200 135.35  _(prix > MA20)_
- **Dist MA** : MA20 +1.5% · MA50 -2.2% · MA200 -6.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (694407 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
