# PRY

**Generated** : 2026-11-25T01:13:41.863753+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €97.78  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot €97.78 (+2.1% vs entrée) · entrée €95.77 · stop €88.11 · T1 €98.46 · R/R 0.35  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 97.78 · ATR Wilder 5.65 (5.78 %)_
- **Swing** : plage **91.5 → 87.36** (-6.42 % a -10.66 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 89.22-91.82 (A). stop INDICATIF 83.39 (-4.54 % sous le bas ; sous le support 86.22-86.95 (- 0,5 ATR)).
- **Deep** : plage **87.36 → 74.67** (-10.66 % a -23.64 % sous la cloture, 2.25 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 86.22-86.95 (B) ; 83.16-84.97 (A) ; 79.43-81.87 (A) ; 76.37-78.57 (A). stop INDICATIF 68.11 (-8.78 % sous le bas ; sous le support 70.94-72.58 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.16 ATR sous le plus haut 20 s., RSI(2) 23.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 92.05-94.5 (A, -3.36 %) ; 89.22-91.82 (A, -6.1 %) ; 86.22-86.95 (B, -11.07 %) ; 83.16-84.97 (A, -13.1 %) ; 79.43-81.87 (A, -16.27 %) ; 76.37-78.57 (A, -19.64 %)
- Resistances reelles au-dessus : 103.98-105.9 (A, 6.34 %) ; 110.3-112.3 (A, 12.8 %) ; 115.65-117.1 (A, 18.28 %) ; 119.65-122.29 (A, 22.37 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.04 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1270).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.917 % | p01 -3.733 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0002** [0.0 ; 0.0149] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.3219** [0.2743 ; 0.3725] _(largeur 9.8 pt, n_eff 345.8)_
   - deep : **0.2693** [0.2246 ; 0.3178] _(largeur 9.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (30.8 pt), deep (33.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.35 %** | CVaR **-6.27 %** | vol 2.75 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.79 % contre 3.02 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.78 % vs -7.96 % si l'on extrapolait par √5 _(rapport 0.852 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0631** (β de hausse 1.2117, asymétrie 0.8773) vs FTSEMIB — 569 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.598× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 91.0403 sur atr_grid (1.25 ATR, 6.893 %) — p(stop avant cible) 0.3828 [0.33 ; 0.43], R/R 8.162, perte reelle 7.1 % (gap inclus), CVaR 8.405 %, EV -0.1641 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.271 %) — p(stop avant cible) 0.2939 [0.25 ; 0.34], R/R 6.46, perte reelle 8.971 % (gap inclus), EV -0.0553 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.0 % x 57.95 % + P(rien) 70.6 % x 3.66 % ne couvrent pas P(stop) 29.4 % x 8.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ sr_based a 1.59 ATR (stop 11.219 %) — p(stop avant cible) 0.1596 [0.12 ; 0.20], R/R 4.749, perte reelle 12.202 % (gap inclus), EV 0.2106 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.36 % > budget 12.00 %
   - 🟢 support a 3.15 ATR (stop 19.825 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 2.867, perte reelle 20.212 % (gap inclus), EV 0.4993 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.83 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.379 %) — p(stop avant cible) 0.8544 [0.81 ; 0.89], R/R 39.329, perte reelle 1.474 % (gap inclus), EV -0.1673 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 39.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.854, borne haute 0.889 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 57.95 % + P(rien) 14.6 % x 7.50 % ne couvrent pas P(stop) 85.4 % x 1.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.757 %) — p(stop avant cible) 0.7256 [0.68 ; 0.77], R/R 19.935, perte reelle 2.907 % (gap inclus), EV -0.2341 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.726, borne haute 0.771 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.0 % x 57.95 % + P(rien) 27.4 % x 6.83 % ne couvrent pas P(stop) 72.6 % x 2.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 4.136 %) — p(stop avant cible) 0.6103 [0.56 ; 0.66], R/R 13.665, perte reelle 4.241 % (gap inclus), EV -0.3916 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 13.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.610, borne haute 0.661 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.0 % x 57.95 % + P(rien) 39.0 % x 5.64 % ne couvrent pas P(stop) 61.0 % x 4.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 5.514 %) — p(stop avant cible) 0.4766 [0.42 ; 0.53], R/R 10.262, perte reelle 5.647 % (gap inclus), EV -0.2324 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.0 % x 57.95 % + P(rien) 52.3 % x 4.70 % ne couvrent pas P(stop) 47.7 % x 5.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 6.893 %) — p(stop avant cible) 0.3828 [0.33 ; 0.43], R/R 8.162, perte reelle 7.1 % (gap inclus), EV -0.1641 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.0 % x 57.95 % + P(rien) 61.7 % x 4.14 % ne couvrent pas P(stop) 38.3 % x 7.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+58.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.59 ATR (stop 10.436 %) — p(stop avant cible) 0.2014 [0.16 ; 0.25], R/R 5.205, perte reelle 11.133 % (gap inclus), EV 0.0835 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.24 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 12.407 %) — p(stop avant cible) 0.1092 [0.08 ; 0.15], R/R 4.181, perte reelle 13.859 % (gap inclus), EV 0.3929 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.57 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.786 %) — p(stop avant cible) 0.0838 [0.06 ; 0.12], R/R 3.686, perte reelle 15.721 % (gap inclus), EV 0.4446 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.03 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.164 %) — p(stop avant cible) 0.0654 [0.04 ; 0.10], R/R 3.451, perte reelle 16.794 % (gap inclus), EV 0.5313 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.30 % > budget 12.00 %
   - 🟢 grid_snapped a 3.15 ATR (stop 19.042 %) — p(stop avant cible) 0.0438 [0.03 ; 0.07], R/R 2.967, perte reelle 19.534 % (gap inclus), EV 0.4869 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.98 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.057 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 2.533, perte reelle 22.875 % (gap inclus), EV 0.5786 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.42 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.814 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 2.274, perte reelle 25.484 % (gap inclus), EV 0.5887 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.571 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 1.93, perte reelle 30.029 % (gap inclus), EV 0.5875 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.328 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.791, perte reelle 32.353 % (gap inclus), EV 0.591 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.085 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.752, perte reelle 33.085 % (gap inclus), EV 0.597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.842 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.617, perte reelle 35.842 % (gap inclus), EV 0.597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 38.599 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.501, perte reelle 38.599 % (gap inclus), EV 0.597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.357 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.401, perte reelle 41.357 % (gap inclus), EV 0.597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.114 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.314, perte reelle 44.114 % (gap inclus), EV 0.597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 97.78, ATR14 5.3918 (5.514 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.902 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.276 % | 97.5104 | 91.68 % | 93.95 % | 94.64 % | 95.43 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.551 % | 97.2408 | 84.95 % | 88.8 % | 91.07 % | 92.94 % | 95.3 % | 96.37 % |
| 0.15 ATR | 0.827 % | 96.9712 | 77.43 % | 84.24 % | 87.3 % | 90.46 % | 93.21 % | 94.55 % |
| 0.2 ATR | 1.103 % | 96.7016 | 69.6 % | 79.09 % | 82.64 % | 87.08 % | 91.01 % | 92.73 % |
| 0.25 ATR | 1.379 % | 96.4321 | 61.98 % | 74.33 % | 78.57 % | 83.4 % | 88.41 % | 90.72 % |
| 0.35 ATR | 1.93 % | 95.8929 | 49.31 % | 64.12 % | 71.13 % | 76.94 % | 84.12 % | 87.99 % |
| 0.5 ATR | 2.757 % | 95.0841 | 35.25 % | 52.43 % | 60.52 % | 68.49 % | 77.32 % | 82.85 % |
| 0.75 ATR | 4.136 % | 93.7362 | 19.8 % | 34.99 % | 43.95 % | 55.17 % | 66.03 % | 74.77 % |
| 1.0 ATR | 5.514 % | 92.3882 | 10.0 % | 23.69 % | 32.54 % | 45.43 % | 56.94 % | 66.9 % |
| 1.25 ATR | 6.893 % | 91.0403 | 5.45 % | 16.35 % | 24.6 % | 35.29 % | 48.45 % | 59.23 % |
| 1.5 ATR | 8.271 % | 89.6923 | 2.38 % | 9.71 % | 16.67 % | 25.05 % | 37.86 % | 50.76 % |
| 2.0 ATR | 11.028 % | 86.9964 | 0.4 % | 4.16 % | 7.84 % | 14.81 % | 25.47 % | 39.15 % |
| 2.5 ATR | 13.786 % | 84.3005 | 0.0 % | 1.68 % | 3.57 % | 8.45 % | 16.68 % | 28.76 % |
| 3.0 ATR | 16.543 % | 81.6046 | 0.0 % | 0.89 % | 1.88 % | 4.57 % | 10.69 % | 20.89 % |
| 4.0 ATR | 22.057 % | 76.2129 | 0.0 % | 0.2 % | 0.69 % | 2.09 % | 5.69 % | 13.02 % |
| 6.0 ATR | 33.085 % | 65.4293 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 2.0 % | 4.24 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.97 ATR | 1.13 ATR | 1.49 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.73 ATR | 0.99 ATR | 1.24 ATR | 1.40 ATR | 1.88 ATR | 2.33 ATR |
| **5 s.** | 0.38 ATR | 0.88 ATR | 1.01 ATR | 1.31 ATR | 1.50 ATR | 1.75 ATR | 2.38 ATR | 2.94 ATR |
| **10 s.** | 0.55 ATR | 1.20 ATR | 1.33 ATR | 1.70 ATR | 2.03 ATR | 2.31 ATR | 3.14 ATR | 4.37 ATR |
| **20 s.** | 0.74 ATR | 1.53 ATR | 1.75 ATR | 2.30 ATR | 2.74 ATR | 3.11 ATR | 4.69 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.396 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.607–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.136 %, prix 93.7358), p(touche) 34.99 % (en stress 87.13 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.734–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.136 %, prix 93.7358), p(touche) 43.95 % (en stress 96.04 %)  ✅ optimum identifie (69.5 % des re-echantillons)
- **5 seance(s)** : plage utile 1.011–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.271 %, prix 89.6926), p(touche) 25.05 % (en stress 89.11 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.331–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.271 %, prix 89.6926), p(touche) 37.86 % (en stress 98.02 %)  ✅ optimum identifie (62.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.748–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.028 %, prix 86.9968), p(touche) 39.15 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : €-0.249 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.0 | bear 30.4 | side 63.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.054% → cible +2.815% / stop −8.0%, p_fill 48%, n_eff≈49.1) : P(cible|rempli) **14%** · **EV/risk -0.043** (×p_fill ; si rempli -0.71% du capital)
  - **swing** (entrée dip −4.526% → cible +6.457% / stop −5.776%, p_fill 32%, n_eff≈37.4) : P(cible|rempli) **24%** · **EV/risk -0.047** (×p_fill ; si rempli -0.84% du capital)
  - **deep** (entrée dip −6.999% → cible +9.374% / stop −8.893%, p_fill 27%, n_eff≈29.9) : P(cible|rempli) **32%** · **EV/risk +0.030** (×p_fill ; si rempli +1.01% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→64% · +2.0%→38% · +3.0%→23% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.91% (p90 6.39%) · excursion haute méd. +1.39% / basse méd. −1.8%
- Profil de vol intra : ouverture 2.349% vs midi 0.783% vs clôture 1.094% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑0%/↓2% ; spike-down 60% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr 0.012)_ ; drift intra méd. -1.197% ; recovery-V 21%
- **σ réalisé intraday** 2.694% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 76% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 98.2458 (VA 97.8063–98.9783 ; dernier close 98.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 29% · rebond 70% · **stop −3.71%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. 0.53% · baisse 36% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −2.11%) · haut méd +0.38% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.84%) · haut méd +0.52% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −3.39%) · haut méd +0.62% · range méd 1.89%
- Excursion ouverture 60min (n=160) : bas méd −1.19% (p90 −3.66%) · haut méd +0.75% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 99.08 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 70% (113/159) · gap 24% · délai 0.4min · rebond 49% (62/113) (MFE +0.99%)
   - −1.0% : fill 30min 41% · séance 62% (94/159) · gap 16% · délai 2.4min · rebond 52% (54/94) (MFE +1.04%)
   - −1.5% : fill 30min 30% · séance 53% (76/159) · gap 10% · délai 21.2min · rebond 41% (38/76) (MFE +0.77%)
   - −2.0% : fill 30min 23% · séance 44% (63/159) · gap 6% · délai 26.7min · rebond 58% (38/63) (MFE +1.03%)
   - −3.0% : fill 30min 9% · séance 29% (43/159) · gap 2% · délai 84.2min · rebond 70% (30/43) (MFE +1.6%)
   - −4.0% : fill 30min 5% · séance 18% (26/159) · gap 2% · délai 229.5min · rebond 49% (14/26) (MFE +0.95%)
   - −5.0% : fill 30min 3% · séance 13% (18/159) · gap 0% · délai 267.1min · rebond 70% (12/18) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.87%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.38% (p90 −1.5%) → stop au-delà de −1.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.69%) → stop au-delà de −1.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=488 jambes) : jambe baissière méd −1.11% (p90 −2.74%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 96% (41/45) · rebond 38% (18/41)
      · −2.0% : fill 84% (33/45) · rebond 55% (19/33)
      · −3.0% : fill 54% (24/45) · rebond 71% (16/24)
      · −4.0% : fill 36% (15/45) · rebond 63% (9/15)
      · −5.0% : fill 28% (12/45) · rebond 73% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 53% (15/27) · rebond 78% (11/15)
      · −2.0% : fill 25% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 15% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 5% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (87 séances) :
      · −1.0% : fill 47% (38/87) · rebond 59% (25/38)
      · −2.0% : fill 29% (22/87) · rebond 59% (12/22)
      · −3.0% : fill 20% (14/87) · rebond 75% (11/14)
      · −4.0% : fill 13% (9/87) · rebond 28% (4/9)
      · −5.0% : fill 9% (5/87) · rebond 69% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 60% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 41% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 279min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -1.25% (q20 -2.04%) → **SL/trailing à −2.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.02% / q75 +2.15% → **scale +1.02% / runner +2.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **21%** (continue à baisser 64%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.16%** (au-delà de la MAE q10 -4.16%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.28% .. +2.1%] · haut q95 +3.19% · bas q05 -3.99%
   - 60min (n=160) : retour [-3.73% .. +2.17%] · haut q95 +3.52% · bas q05 -4.4%
   - 2h (n=160) : retour [-4.27% .. +2.64%] · haut q95 +3.99% · bas q05 -5.11%
   - 4h (n=160) : retour [-4.12% .. +2.69%] · haut q95 +4.11% · bas q05 -5.31%
   - 6h (n=160) : retour [-5.24% .. +3.41%] · haut q95 +4.21% · bas q05 -5.56%
   - session (n=160) : retour [-5.48% .. +3.26%] · haut q95 +4.45% · bas q05 -6.56%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.77 · part idiosyncratique 0.23
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.8  _(momentum baissier)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist -0.218  _(bearish_recent)_
- **BB** : %B -0.02 · largeur 16.6%
- **ATR** : 5.39 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.074  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 62.3  _(marche en range (choppy))_
- **MA** : MA20 107.03 · MA50 113.83 · MA200 122.23  _(prix < MA20)_
- **Dist MA** : MA20 -8.6% · MA50 -14.1% · MA200 -20.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (519736 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
