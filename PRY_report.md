# PRY

**Generated** : 2026-11-19T01:13:33.413327+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €108.15  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 26/125 fenêtres (p_fill pondéré 22 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €108.15 (+4.5% vs entrée) · entrée €103.48 · stop €95.20 · T1 €106.04 · R/R 0.31  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-18 : 108.15 · ATR Wilder 4.98 (4.6 %)_
- **Swing** : plage **102.62 → 98.97** (-5.11 % a -8.49 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 94.95 (-4.06 % sous le bas ; sous le support 97.44-98.8 (- 0,5 ATR)).
- **Deep** : plage **98.97 → 87.78** (-8.49 % a -18.83 % sous la cloture, 2.25 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 97.44-98.8 (A) ; 94.5-96.88 (A) ; 91.78-92.37 (A) ; 89.22-91.32 (A). stop INDICATIF 83.73 (-4.62 % sous le bas ; sous le support 86.22-86.95 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.51 ATR sous le plus haut 20 s., RSI(2) 64.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 103.98-105.76 (C, -2.21 %) ; 97.44-98.8 (A, -8.64 %) ; 94.5-96.88 (A, -10.42 %) ; 91.78-92.37 (A, -14.59 %) ; 89.22-91.32 (A, -15.56 %) ; 86.22-86.95 (B, -19.6 %)
- Resistances reelles au-dessus : 110.3-112.3 (A, 1.99 %) ; 115.65-117.1 (A, 6.93 %) ; 122.29-123.2 (A, 13.07 %) ; 129.4-131.2 (A, 19.65 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.26 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1270).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.26 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.903 % | p01 -3.733 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0002** [0.0 ; 0.0149] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.3567** [0.3076 ; 0.4082] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.291** [0.245 ; 0.3405] _(largeur 9.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 22.0 observations effectives », dont la borne haute a 95 % vaut environ 13.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.3 %** | CVaR **-6.01 %** | vol 2.69 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.76 % contre 2.85 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.73 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.857 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0382** (β de hausse 1.215, asymétrie 0.8545) vs FTSEMIB — 568 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.461× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 100.4448 sur atr_based (1.5 ATR, 7.125 %) — p(stop avant cible) 0.3714 [0.32 ; 0.42], R/R 5.768, perte reelle 7.433 % (gap inclus), CVaR 9.381 %, EV -0.1327 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.125 %) — p(stop avant cible) 0.3714 [0.32 ; 0.42], R/R 5.768, perte reelle 7.433 % (gap inclus), EV -0.1327 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.0 % x 42.88 % + P(rien) 62.9 % x 4.18 % ne couvrent pas P(stop) 37.1 % x 7.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+42.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ swing_based a 2.12 ATR (stop 12.252 %) — p(stop avant cible) 0.1117 [0.08 ; 0.15], R/R 3.116, perte reelle 13.759 % (gap inclus), EV 0.3593 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.61 % > budget 12.00 %
   - ⚪ sr_based a 3.74 ATR (stop 19.959 %) — p(stop avant cible) 0.0279 [0.01 ; 0.05], R/R 2.106, perte reelle 20.357 % (gap inclus), EV 0.4952 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 12.00 %
   - 🟢 support a 5.33 ATR (stop 27.504 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.429, perte reelle 30.012 % (gap inclus), EV 0.5447 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.44 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.187 %) — p(stop avant cible) 0.8784 [0.84 ; 0.91], R/R 33.373, perte reelle 1.285 % (gap inclus), EV -0.1358 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 33.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.878, borne haute 0.910 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.0 % x 42.88 % + P(rien) 12.2 % x 8.16 % ne couvrent pas P(stop) 87.8 % x 1.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+42.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.375 %) — p(stop avant cible) 0.7678 [0.72 ; 0.81], R/R 17.154, perte reelle 2.499 % (gap inclus), EV -0.3214 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 17.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.768, borne haute 0.810 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 42.88 % + P(rien) 23.2 % x 6.88 % ne couvrent pas P(stop) 76.8 % x 2.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+42.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 3.562 %) — p(stop avant cible) 0.6665 [0.62 ; 0.71], R/R 11.539, perte reelle 3.716 % (gap inclus), EV -0.4217 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.666, borne haute 0.715 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 0.0 % x 42.88 % + P(rien) 33.4 % x 6.16 % ne couvrent pas P(stop) 66.6 % x 3.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+42.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 4.75 %) — p(stop avant cible) 0.5619 [0.51 ; 0.61], R/R 8.792, perte reelle 4.877 % (gap inclus), EV -0.4885 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.562, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 0.0 % x 42.88 % + P(rien) 43.8 % x 5.14 % ne couvrent pas P(stop) 56.2 % x 4.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+42.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 5.937 %) — p(stop avant cible) 0.445 [0.39 ; 0.50], R/R 7.063, perte reelle 6.071 % (gap inclus), EV -0.2462 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.0 % x 42.88 % + P(rien) 55.5 % x 4.42 % ne couvrent pas P(stop) 44.5 % x 6.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+42.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 8.312 %) — p(stop avant cible) 0.2944 [0.25 ; 0.34], R/R 4.754, perte reelle 9.02 % (gap inclus), EV -0.0888 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.0 % x 42.88 % + P(rien) 70.6 % x 3.64 % ne couvrent pas P(stop) 29.4 % x 9.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+42.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 2.12 ATR (stop 11.483 %) — p(stop avant cible) 0.1416 [0.11 ; 0.18], R/R 3.414, perte reelle 12.561 % (gap inclus), EV 0.3013 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.53 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 13.062 %) — p(stop avant cible) 0.1095 [0.08 ; 0.15], R/R 2.871, perte reelle 14.935 % (gap inclus), EV 0.2398 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.10 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 14.249 %) — p(stop avant cible) 0.082 [0.06 ; 0.11], R/R 2.678, perte reelle 16.012 % (gap inclus), EV 0.418 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
   - ⚪ grid_snapped a 3.74 ATR (stop 19.189 %) — p(stop avant cible) 0.0393 [0.02 ; 0.06], R/R 2.17, perte reelle 19.758 % (gap inclus), EV 0.466 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.75 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.374 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 1.915, perte reelle 22.393 % (gap inclus), EV 0.5331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.56 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 23.748 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 1.734, perte reelle 24.732 % (gap inclus), EV 0.5442 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.45 % > budget 12.00 %
   - 🟢 grid_snapped a 5.33 ATR (stop 26.734 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 1.59, perte reelle 26.959 % (gap inclus), EV 0.5506 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.498 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.325, perte reelle 32.353 % (gap inclus), EV 0.5508 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 30.873 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.325, perte reelle 32.353 % (gap inclus), EV 0.5508 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 33.248 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.29, perte reelle 33.248 % (gap inclus), EV 0.5561 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.623 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.204, perte reelle 35.623 % (gap inclus), EV 0.5561 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.23 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.997 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.128, perte reelle 37.997 % (gap inclus), EV 0.5561 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.23 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 108.15, ATR14 5.1368 (4.75 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 1.634 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.237 % | 107.8932 | 91.68 % | 93.95 % | 94.64 % | 95.43 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.475 % | 107.6363 | 84.95 % | 88.9 % | 91.17 % | 92.94 % | 95.3 % | 96.37 % |
| 0.15 ATR | 0.712 % | 107.3795 | 77.43 % | 84.34 % | 87.5 % | 90.46 % | 93.31 % | 94.55 % |
| 0.2 ATR | 0.95 % | 107.1226 | 69.5 % | 79.19 % | 82.84 % | 87.08 % | 91.21 % | 92.73 % |
| 0.25 ATR | 1.187 % | 106.8658 | 61.88 % | 74.33 % | 78.77 % | 83.4 % | 88.61 % | 90.72 % |
| 0.35 ATR | 1.662 % | 106.3521 | 49.21 % | 64.12 % | 71.23 % | 76.94 % | 84.32 % | 88.09 % |
| 0.5 ATR | 2.375 % | 105.5816 | 35.05 % | 52.33 % | 60.42 % | 68.19 % | 77.32 % | 82.74 % |
| 0.75 ATR | 3.562 % | 104.2974 | 19.7 % | 34.79 % | 43.85 % | 55.07 % | 65.93 % | 74.57 % |
| 1.0 ATR | 4.75 % | 103.0132 | 10.0 % | 23.59 % | 32.24 % | 45.13 % | 56.84 % | 66.8 % |
| 1.25 ATR | 5.937 % | 101.729 | 5.45 % | 16.25 % | 24.4 % | 35.29 % | 48.35 % | 59.13 % |
| 1.5 ATR | 7.125 % | 100.4448 | 2.38 % | 9.61 % | 16.47 % | 25.05 % | 37.76 % | 50.76 % |
| 2.0 ATR | 9.499 % | 97.8764 | 0.4 % | 4.06 % | 7.74 % | 14.81 % | 25.47 % | 39.15 % |
| 2.5 ATR | 11.874 % | 95.308 | 0.0 % | 1.68 % | 3.57 % | 8.45 % | 16.68 % | 28.76 % |
| 3.0 ATR | 14.249 % | 92.7396 | 0.0 % | 0.89 % | 1.88 % | 4.57 % | 10.69 % | 20.89 % |
| 4.0 ATR | 18.999 % | 87.6029 | 0.0 % | 0.2 % | 0.69 % | 2.09 % | 5.69 % | 13.02 % |
| 6.0 ATR | 28.498 % | 77.3293 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 2.0 % | 4.24 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.79 ATR | 0.97 ATR | 1.12 ATR | 1.49 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.73 ATR | 0.98 ATR | 1.23 ATR | 1.39 ATR | 1.87 ATR | 2.33 ATR |
| **5 s.** | 0.38 ATR | 0.88 ATR | 1.00 ATR | 1.31 ATR | 1.50 ATR | 1.75 ATR | 2.38 ATR | 2.94 ATR |
| **10 s.** | 0.55 ATR | 1.20 ATR | 1.33 ATR | 1.69 ATR | 2.03 ATR | 2.31 ATR | 3.14 ATR | 4.37 ATR |
| **20 s.** | 0.74 ATR | 1.53 ATR | 1.75 ATR | 2.30 ATR | 2.74 ATR | 3.11 ATR | 4.69 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.395 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.604–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.562 %, prix 104.2977), p(touche) 34.79 % (en stress 88.12 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.733–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.562 %, prix 104.2977), p(touche) 43.85 % (en stress 96.04 %)  ✅ optimum identifie (68.2 % des re-echantillons)
- **5 seance(s)** : plage utile 1.003–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.937 %, prix 101.7291), p(touche) 35.29 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.329–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.125 %, prix 100.4443), p(touche) 37.76 % (en stress 98.02 %)  ✅ optimum identifie (60.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.748–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.499 %, prix 97.8768), p(touche) 39.15 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 72.8 | bear 21.8 | side 5.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 108.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.326% → cible +2.482% / stop −8.0%, p_fill 22%, n_eff≈22.0) : P(cible|rempli) **15%** · **EV/risk -0.002** (×p_fill ; si rempli -0.08% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.74 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.9  _(momentum baissier)_
- **ADX** : 16.0  _(pas de tendance nette)_
- **MACD** : hist 0.697  _(pas de croisement recent)_
- **BB** : %B 0.57 · largeur 16.6%
- **ATR** : 5.14 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.052  _(accumulation)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 59.4  _(transition)_
- **MA** : MA20 106.83 · MA50 115.32 · MA200 122.23  _(prix > MA20)_
- **Dist MA** : MA20 +1.2% · MA50 -6.2% · MA200 -11.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (698242 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
