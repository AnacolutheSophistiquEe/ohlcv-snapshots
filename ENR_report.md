# ENR

**Generated** : 2026-11-13T01:07:12.188513+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €133.20  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 33/125 fenêtres (p_fill pondéré 24 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €133.20 (+3.5% vs entrée) · entrée €128.65 · stop €118.35 · T1 €134.67 · R/R 0.58  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 133.2 · ATR Wilder 7.43 (5.57 %)_
- **Swing** : plage **123.96 → 117.99** (-6.94 % a -11.42 % sous la cloture, 0.8 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 122.83-124.46 (B). stop INDICATIF 110.8 (-6.1 % sous le bas ; sous le support 114.51-117.65 (- 0,5 ATR)).
- **Deep** : plage **117.99 → 106.75** (-11.42 % a -19.85 % sous la cloture, 1.51 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 114.51-117.65 (A) ; 109.88-113.47 (A). stop INDICATIF 99.5 (-6.8 % sous le bas ; sous le support 103.21-104.4 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.61 ATR sous le plus haut 20 s., RSI(2) 84.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 122.83-124.46 (B, -6.56 %) ; 114.51-117.65 (A, -11.68 %) ; 109.88-113.47 (A, -14.82 %) ; 103.21-104.4 (B, -21.62 %) ; 98.56-100.32 (A, -24.68 %) ; 94.0-95.27 (A, -28.47 %)
- Resistances reelles au-dessus : 135.7-139.16 (A, 1.88 %) ; 140.18-143.38 (B, 5.24 %) ; 146.08-148.4 (A, 9.67 %) ; 150.58-151.76 (A, 13.05 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.75 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (13.49 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **2.68 pt plus bas** dans le cas TYPIQUE (médiane), 18.35 au p90, **22.267 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 13.49 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0197 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.387 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0076** [0.0011 ; 0.0299] _(largeur 2.9 pt, n_eff 173.1)_
   - swing : **0.355** [0.3059 ; 0.4065] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.3143** [0.2671 ; 0.3646] _(largeur 9.8 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 26.8 observations effectives », dont la borne haute a 95 % vaut environ 11.2 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.83 %** | CVaR **-6.82 %** | vol 3.24 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.21 % contre 3.32 % aujourd'hui, rapport 1.87)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.9 % vs -10.11 % si l'on extrapolait par √5 _(rapport 0.881 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3008** (β de hausse 1.056, asymétrie 1.2319) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 123.2625 sur atr_grid (1.25 ATR, 7.461 %) — p(stop avant cible) 0.4531 [0.40 ; 0.51], R/R 4.965, perte reelle 8.119 % (gap inclus), CVaR 12.777 %, EV -1.1911 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0607 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 12.78 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.953 %) — p(stop avant cible) 0.3696 [0.32 ; 0.42], R/R 4.17, perte reelle 9.666 % (gap inclus), EV -1.2418 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 0.1 % x 40.31 % + P(rien) 63.0 % x 3.66 % ne couvrent pas P(stop) 37.0 % x 9.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ sr_based a 2.39 ATR (stop 17.176 %) — p(stop avant cible) 0.0433 [0.03 ; 0.07], R/R 2.246, perte reelle 17.945 % (gap inclus), EV 0.1279 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.44 % > budget 12.00 %
   - 🟢 support a 2.8 ATR (stop 19.627 %) — p(stop avant cible) 0.0132 [0.00 ; 0.03], R/R 1.922, perte reelle 20.976 % (gap inclus), EV 0.2595 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.19 % > budget 12.00 %
   - 🟢 support a 4.19 ATR (stop 27.883 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 1.372, perte reelle 29.372 % (gap inclus), EV 0.3449 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.492 %) — p(stop avant cible) 0.8876 [0.85 ; 0.92], R/R 25.876, perte reelle 1.558 % (gap inclus), EV -0.3513 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 25.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.0 % x 40.31 % + P(rien) 11.2 % x 9.18 % ne couvrent pas P(stop) 88.8 % x 1.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.984 %) — p(stop avant cible) 0.7764 [0.73 ; 0.82], R/R 13.05, perte reelle 3.089 % (gap inclus), EV -0.5497 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.776, borne haute 0.818 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 0.1 % x 40.31 % + P(rien) 22.3 % x 8.18 % ne couvrent pas P(stop) 77.6 % x 3.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 4.476 %) — p(stop avant cible) 0.648 [0.60 ; 0.70], R/R 8.667, perte reelle 4.651 % (gap inclus), EV -0.6664 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.648, borne haute 0.697 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 0.1 % x 40.31 % + P(rien) 35.1 % x 6.61 % ne couvrent pas P(stop) 64.8 % x 4.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 5.968 %) — p(stop avant cible) 0.5531 [0.50 ; 0.60], R/R 6.413, perte reelle 6.286 % (gap inclus), EV -1.0464 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.553, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.1 % x 40.31 % + P(rien) 44.6 % x 5.39 % ne couvrent pas P(stop) 55.3 % x 6.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 7.461 %) — p(stop avant cible) 0.4531 [0.40 ; 0.51], R/R 4.965, perte reelle 8.119 % (gap inclus), EV -1.1911 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.1 % x 40.31 % + P(rien) 54.6 % x 4.51 % ne couvrent pas P(stop) 45.3 % x 8.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 10.445 %) — p(stop avant cible) 0.2889 [0.24 ; 0.34], R/R 3.646, perte reelle 11.056 % (gap inclus), EV -1.1 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 0.1 % x 40.31 % + P(rien) 71.0 % x 2.91 % ne couvrent pas P(stop) 28.9 % x 11.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 11.937 %) — p(stop avant cible) 0.1809 [0.14 ; 0.22], R/R 3.195, perte reelle 12.619 % (gap inclus), EV -0.5794 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 0.1 % x 40.31 % + P(rien) 81.8 % x 2.05 % ne couvrent pas P(stop) 18.1 % x 12.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 2.39 ATR (stop 16.066 %) — p(stop avant cible) 0.0512 [0.03 ; 0.08], R/R 2.361, perte reelle 17.077 % (gap inclus), EV 0.0562 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.10 % > budget 12.00 %
   - 🟢 grid_snapped a 2.8 ATR (stop 18.517 %) — p(stop avant cible) 0.0377 [0.02 ; 0.06], R/R 2.104, perte reelle 19.156 % (gap inclus), EV 0.1392 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.75 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.89 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 1.663, perte reelle 24.243 % (gap inclus), EV 0.2778 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.03 % > budget 12.00 %
   - 🟢 grid_snapped a 4.19 ATR (stop 26.773 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 1.394, perte reelle 28.911 % (gap inclus), EV 0.3461 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.40 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.842 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.309, perte reelle 30.799 % (gap inclus), EV 0.349 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.31 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.827 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.194, perte reelle 33.75 % (gap inclus), EV 0.3606 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.07 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.811 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.12, perte reelle 36.005 % (gap inclus), EV 0.3611 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.08 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.795 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.039, perte reelle 38.795 % (gap inclus), EV 0.3583 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.779 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.965, perte reelle 41.779 % (gap inclus), EV 0.3656 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.03 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 44.764 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.901, perte reelle 44.764 % (gap inclus), EV 0.3652 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.99 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.748 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.844, perte reelle 47.748 % (gap inclus), EV 0.3698 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.92 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 133.2, ATR14 7.95 (5.968 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.368 ATR = 2.196 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.298 % | 132.8025 | 91.42 % | 94.18 % | 95.65 % | 96.24 % | 97.31 % | 97.99 % |
| 0.1 ATR | 0.597 % | 132.405 | 83.63 % | 88.25 % | 90.61 % | 92.67 % | 94.73 % | 95.78 % |
| 0.15 ATR | 0.895 % | 132.0075 | 76.33 % | 82.43 % | 85.97 % | 88.71 % | 91.44 % | 93.57 % |
| 0.2 ATR | 1.194 % | 131.61 | 70.32 % | 78.97 % | 82.91 % | 86.63 % | 89.65 % | 92.16 % |
| 0.25 ATR | 1.492 % | 131.2125 | 63.51 % | 74.53 % | 79.15 % | 83.37 % | 87.66 % | 90.85 % |
| 0.35 ATR | 2.089 % | 130.4175 | 51.87 % | 64.96 % | 70.36 % | 76.14 % | 82.59 % | 87.04 % |
| 0.5 ATR | 2.984 % | 129.225 | 36.59 % | 52.12 % | 59.78 % | 67.03 % | 75.22 % | 81.21 % |
| 0.75 ATR | 4.476 % | 127.2375 | 19.82 % | 36.13 % | 45.55 % | 55.05 % | 66.27 % | 74.57 % |
| 1.0 ATR | 5.968 % | 125.25 | 11.24 % | 26.06 % | 35.18 % | 45.35 % | 58.41 % | 67.14 % |
| 1.25 ATR | 7.461 % | 123.2625 | 6.21 % | 17.47 % | 25.49 % | 36.53 % | 49.75 % | 59.6 % |
| 1.5 ATR | 8.953 % | 121.275 | 2.96 % | 11.35 % | 18.48 % | 28.81 % | 42.59 % | 53.37 % |
| 2.0 ATR | 11.937 % | 117.3 | 0.79 % | 4.34 % | 9.19 % | 17.33 % | 29.55 % | 42.11 % |
| 2.5 ATR | 14.921 % | 113.325 | 0.3 % | 2.07 % | 4.25 % | 10.2 % | 20.6 % | 32.36 % |
| 3.0 ATR | 17.905 % | 109.35 | 0.1 % | 0.89 % | 2.08 % | 5.35 % | 13.43 % | 24.42 % |
| 4.0 ATR | 23.874 % | 101.4 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 7.06 % | 13.97 % |
| 6.0 ATR | 35.811 % | 85.5 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.93 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.34 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.61 ATR | 0.83 ATR | 1.03 ATR | 1.18 ATR | 1.60 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.06 ATR | 1.27 ATR | 1.45 ATR | 1.96 ATR | 2.42 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 1.01 ATR | 1.36 ATR | 1.67 ATR | 1.88 ATR | 2.52 ATR | 3.12 ATR |
| **10 s.** | 0.51 ATR | 1.24 ATR | 1.42 ATR | 1.87 ATR | 2.25 ATR | 2.54 ATR | 3.54 ATR | 4.85 ATR |
| **20 s.** | 0.73 ATR | 1.65 ATR | 1.87 ATR | 2.47 ATR | 2.96 ATR | 3.42 ATR | 4.99 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.417 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.476 %, prix 127.238), p(touche) 36.13 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.763–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.968 %, prix 125.2506), p(touche) 35.18 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (84.9 % des re-echantillons)
- **5 seance(s)** : plage utile 1.01–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.461 %, prix 123.2619), p(touche) 36.53 % (en stress 96.04 %)  ✅ optimum identifie (90.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.416–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.953 %, prix 121.2746), p(touche) 42.59 % (en stress 100.0 %)  ✅ optimum identifie (92.8 % des re-echantillons)
- **20 seance(s)** : plage utile 1.872–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.937 %, prix 117.2999), p(touche) 42.11 % (en stress 99.0 %)  ✅ optimum identifie (90.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : €-0.398 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 31.4 | bear 61.8 | side 6.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.424% → cible +4.684% / stop −8.0%, p_fill 24%, n_eff≈26.8) : P(cible|rempli) **9%** · **EV/risk -0.000** (×p_fill ; si rempli -0.01% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→34% · +3.0%→15% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.62% (p90 6.06%) · excursion haute méd. +1.37% / basse méd. −1.89%
- Profil de vol intra : ouverture 1.961% vs midi 0.824% vs clôture 1.048% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.864% ; recovery-V 25%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 83% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 121.5065 (VA 120.2185–123.5995 ; dernier close 118.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 57% · **stop −4.86%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.22 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.69%) · haut méd +0.49% · range méd 1.14%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.05%) · haut méd +0.58% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.19%) · haut méd +0.62% · range méd 1.69%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.35%) · haut méd +0.68% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 70% (115/159) · gap 30% · délai 0.2min · rebond 48% (59/115) (MFE +0.88%)
   - −1.0% : fill 30min 40% · séance 66% (107/159) · gap 20% · délai 8.6min · rebond 51% (59/107) (MFE +1.04%)
   - −1.5% : fill 30min 29% · séance 53% (88/159) · gap 13% · délai 12.6min · rebond 55% (48/88) (MFE +1.28%)
   - −2.0% : fill 30min 23% · séance 44% (73/159) · gap 9% · délai 20.7min · rebond 50% (41/73) (MFE +1.0%)
   - −3.0% : fill 30min 10% · séance 29% (48/159) · gap 3% · délai 251.6min · rebond 40% (24/48) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 200.1min · rebond 57% (20/32) (MFE +1.05%)
   - −5.0% : fill 30min 4% · séance 13% (24/159) · gap 0% · délai 397.7min · rebond 38% (11/24) (MFE +0.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.66%) → stop au-delà de −0.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=526 jambes) : jambe baissière méd −1.04% (p90 −2.31%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 41% (26/53)
      · −2.0% : fill 84% (41/54) · rebond 49% (20/41)
      · −3.0% : fill 59% (30/54) · rebond 40% (14/30)
      · −4.0% : fill 39% (22/54) · rebond 75% (16/22)
      · −5.0% : fill 30% (18/54) · rebond 47% (10/18)
   - **flat** (18 séances) :
      · −1.0% : fill 59% (13/18) · rebond 64% (9/13)
      · −2.0% : fill 33% (8/18) · rebond 68% (6/8)
      · −3.0% : fill 20% (5/18) · rebond 48% (3/5)
      · −4.0% : fill 6% (3/18) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 46% (41/87) · rebond 61% (24/41)
      · −2.0% : fill 23% (24/87) · rebond 46% (15/24)
      · −3.0% : fill 13% (13/87) · rebond 36% (7/13)
      · −4.0% : fill 9% (7/87) · rebond 11% (2/7)
      · −5.0% : fill 5% (4/87) · rebond 12% (1/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 61% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.18% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.1% → **scale +1.08% / runner +2.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.96%** (au-delà de la MAE q10 -4.96%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +1.62%] · haut q95 +2.08% · bas q05 -2.65%
   - 60min (n=160) : retour [-2.5% .. +1.42%] · haut q95 +2.41% · bas q05 -3.07%
   - 2h (n=160) : retour [-2.53% .. +2.22%] · haut q95 +2.56% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.61% .. +2.42%] · haut q95 +3.02% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.22% .. +3.06%] · haut q95 +3.68% · bas q05 -4.31%
   - session (n=160) : retour [-5.78% .. +2.83%] · haut q95 +4.66% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-17 — ENR earnings (J-3 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-17 — ENR earnings (J-3 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 59.8  _(momentum haussier)_
- **ADX** : 20.1  _(pas de tendance nette)_
- **MACD** : hist 1.088  _(bullish_recent)_
- **BB** : %B 0.73 · largeur 21.0%
- **ATR** : 7.95 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.058  _(accumulation)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 53.9  _(transition)_
- **MA** : MA20 127.11 · MA50 136.37 · MA200 153.55  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 -2.3% · MA200 -13.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (706269 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
