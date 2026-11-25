# RHM

**Generated** : 2026-11-25T01:04:52.512310+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €734.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot €734.10 (+7.0% vs entrée) · entrée €685.94 · stop €671.49 · T1 €710.02 · R/R 1.67  
> ↳ ¼-Kelly 0.003 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.11% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 734.1 · ATR Wilder 39.67 (5.4 %)_
- **Swing** : plage **676.34 → 642.36** (-7.87 % a -12.5 % sous la cloture, 0.86 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 597.64 (-6.96 % sous le bas ; sous le support 617.47-627.13 (- 0,5 ATR)).
- **Deep** : plage **642.36 → 545.57** (-12.5 % a -25.68 % sous la cloture, 2.44 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 617.47-627.13 (C) ; 584.17-592.25 (A) ; 543.49-560.53 (C). stop INDICATIF 500.31 (-8.3 % sous le bas ; sous le support 520.14-538.86 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 8.22 ATR sous le plus haut 20 s., RSI(2) 67.5. Limite **714.26** (seance suivante), stop catastrophe 555.58, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 677.76-695.89 (A, -5.21 %) ; 617.47-627.13 (C, -14.57 %) ; 584.17-592.25 (A, -19.32 %) ; 543.49-560.53 (C, -23.64 %) ; 520.14-538.86 (B, -26.6 %) ; 499.65-519.16 (B, -29.28 %)
- Resistances reelles au-dessus : 909.0-928.8 (A, 23.83 %) ; 936.2-953.59 (A, 27.53 %) ; 976.0-987.1 (A, 32.95 %) ; 1006.4-1006.4 (B, 37.09 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.80 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (19.68 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **2.749 pt plus bas** dans le cas TYPIQUE (médiane), 2.749 au p90, **2.749 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 19.68 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0022 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.621 % | p01 -3.886 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3549** [0.2865 ; 0.4281] _(largeur 14.2 pt, n_eff 173.1)_
   - swing : **0.2413** [0.1985 ; 0.2884] _(largeur 9.0 pt, n_eff 345.8)_
   - deep : **0.2235** [0.182 ; 0.2696] _(largeur 8.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.76 %** | CVaR **-6.99 %** | vol 3.01 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.98 % contre 3.34 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.5 % vs -9.1 % si l'on extrapolait par √5 _(rapport 0.935 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5421** (β de hausse 0.581, asymétrie 0.9331) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.283× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 685.9357 sur atr_grid (1.0 ATR, 6.561 %) — p(stop avant cible) 0.5057 [0.45 ; 0.56], R/R 6.836, perte reelle 7.327 % (gap inclus), CVaR 12.524 %, EV -1.2924 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0546 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.506, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 12.52 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.842 %) — p(stop avant cible) 0.3104 [0.26 ; 0.36], R/R 4.768, perte reelle 10.506 % (gap inclus), EV -1.502 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 0.1 % x 50.09 % + P(rien) 68.9 % x 2.51 % ne couvrent pas P(stop) 31.0 % x 10.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.64 %) — p(stop avant cible) 0.8712 [0.83 ; 0.90], R/R 29.261, perte reelle 1.712 % (gap inclus), EV -0.1242 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 29.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.871, borne haute 0.903 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.0 % x 50.09 % + P(rien) 12.9 % x 10.61 % ne couvrent pas P(stop) 87.1 % x 1.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 3.28 %) — p(stop avant cible) 0.7487 [0.70 ; 0.79], R/R 14.095, perte reelle 3.554 % (gap inclus), EV -0.6877 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.749, borne haute 0.792 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 0.0 % x 50.09 % + P(rien) 25.1 % x 7.85 % ne couvrent pas P(stop) 74.9 % x 3.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 4.921 %) — p(stop avant cible) 0.6336 [0.58 ; 0.68], R/R 9.165, perte reelle 5.466 % (gap inclus), EV -1.0448 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.634, borne haute 0.683 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.0 % x 50.09 % + P(rien) 36.6 % x 6.60 % ne couvrent pas P(stop) 63.4 % x 5.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 6.561 %) — p(stop avant cible) 0.5057 [0.45 ; 0.56], R/R 6.836, perte reelle 7.327 % (gap inclus), EV -1.2924 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.506, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 0.1 % x 50.09 % + P(rien) 49.4 % x 4.83 % ne couvrent pas P(stop) 50.6 % x 7.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 8.201 %) — p(stop avant cible) 0.4041 [0.35 ; 0.46], R/R 5.556, perte reelle 9.015 % (gap inclus), EV -1.4582 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.46 %) : P(cible) 0.1 % x 50.09 % + P(rien) 59.5 % x 3.62 % ne couvrent pas P(stop) 40.4 % x 9.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 11.482 %) — p(stop avant cible) 0.2621 [0.22 ; 0.31], R/R 4.179, perte reelle 11.987 % (gap inclus), EV -1.5964 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 0.1 % x 50.09 % + P(rien) 73.7 % x 2.06 % ne couvrent pas P(stop) 26.2 % x 11.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 13.122 %) — p(stop avant cible) 0.2016 [0.16 ; 0.25], R/R 3.695, perte reelle 13.557 % (gap inclus), EV -1.7366 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 0.1 % x 50.09 % + P(rien) 79.8 % x 1.21 % ne couvrent pas P(stop) 20.2 % x 13.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 14.762 %) — p(stop avant cible) 0.165 [0.13 ; 0.21], R/R 3.308, perte reelle 15.141 % (gap inclus), EV -1.8154 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 0.1 % x 50.09 % + P(rien) 83.4 % x 0.78 % ne couvrent pas P(stop) 16.5 % x 15.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 16.402 %) — p(stop avant cible) 0.1369 [0.10 ; 0.18], R/R 2.984, perte reelle 16.787 % (gap inclus), EV -1.9294 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 0.1 % x 50.09 % + P(rien) 86.2 % x 0.39 % ne couvrent pas P(stop) 13.7 % x 16.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 18.043 %) — p(stop avant cible) 0.1086 [0.08 ; 0.14], R/R 2.728, perte reelle 18.365 % (gap inclus), EV -2.0033 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 0.1 % x 50.09 % + P(rien) 89.1 % x -0.04 % ne couvrent pas P(stop) 10.9 % x 18.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 19.683 %) — p(stop avant cible) 0.0903 [0.06 ; 0.12], R/R 2.508, perte reelle 19.976 % (gap inclus), EV -2.0825 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 0.1 % x 50.09 % + P(rien) 90.9 % x -0.34 % ne couvrent pas P(stop) 9.0 % x 19.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 22.963 %) — p(stop avant cible) 0.033 [0.02 ; 0.06], R/R 2.149, perte reelle 23.306 % (gap inclus), EV -1.9583 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.96 %) : P(cible) 0.1 % x 50.09 % + P(rien) 96.6 % x -1.26 % ne couvrent pas P(stop) 3.3 % x 23.31 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 26.244 %) — p(stop avant cible) 0.016 [0.01 ; 0.03], R/R 1.905, perte reelle 26.29 % (gap inclus), EV -1.9823 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.98 %) : P(cible) 0.1 % x 50.09 % + P(rien) 98.3 % x -1.62 % ne couvrent pas P(stop) 1.6 % x 26.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 29.524 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.697, perte reelle 29.524 % (gap inclus), EV -1.9374 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.6 % x -1.88 % ne couvrent pas P(stop) 0.3 % x 29.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 32.805 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.527, perte reelle 32.805 % (gap inclus), EV -1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.9 % x -1.86 % ne couvrent pas P(stop) 0.0 % x 32.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 36.085 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.388, perte reelle 36.085 % (gap inclus), EV -1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.9 % x -1.86 % ne couvrent pas P(stop) 0.0 % x 36.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 39.366 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.272, perte reelle 39.366 % (gap inclus), EV -1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.9 % x -1.86 % ne couvrent pas P(stop) 0.0 % x 39.37 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 42.646 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.175, perte reelle 42.646 % (gap inclus), EV -1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.9 % x -1.86 % ne couvrent pas P(stop) 0.0 % x 42.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 45.927 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.091, perte reelle 45.927 % (gap inclus), EV -1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.9 % x -1.86 % ne couvrent pas P(stop) 0.0 % x 45.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 49.207 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.018, perte reelle 49.207 % (gap inclus), EV -1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.9 % x -1.86 % ne couvrent pas P(stop) 0.0 % x 49.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 52.488 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.954, perte reelle 52.488 % (gap inclus), EV -1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.1 % x 50.09 % + P(rien) 99.9 % x -1.86 % ne couvrent pas P(stop) 0.0 % x 52.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+50.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 734.1, ATR14 48.1643 (6.561 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.39 ATR = 2.559 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.328 % | 731.6918 | 89.55 % | 92.6 % | 93.77 % | 94.95 % | 97.31 % | 97.99 % |
| 0.1 ATR | 0.656 % | 729.2835 | 83.83 % | 88.55 % | 90.42 % | 91.98 % | 95.62 % | 96.68 % |
| 0.15 ATR | 0.984 % | 726.8753 | 76.63 % | 83.42 % | 86.26 % | 88.71 % | 93.33 % | 95.28 % |
| 0.2 ATR | 1.312 % | 724.4671 | 69.92 % | 78.87 % | 82.02 % | 85.54 % | 91.24 % | 93.67 % |
| 0.25 ATR | 1.64 % | 722.0589 | 62.52 % | 73.15 % | 76.98 % | 81.39 % | 88.66 % | 91.86 % |
| 0.35 ATR | 2.296 % | 717.2425 | 53.45 % | 65.75 % | 71.15 % | 76.83 % | 85.97 % | 89.85 % |
| 0.5 ATR | 3.28 % | 710.0178 | 40.53 % | 55.18 % | 61.86 % | 69.6 % | 80.8 % | 84.82 % |
| 0.75 ATR | 4.921 % | 697.9768 | 23.57 % | 39.19 % | 47.73 % | 58.32 % | 71.44 % | 78.59 % |
| 1.0 ATR | 6.561 % | 685.9357 | 13.21 % | 27.25 % | 37.15 % | 49.41 % | 63.68 % | 72.36 % |
| 1.25 ATR | 8.201 % | 673.8946 | 7.69 % | 18.46 % | 27.08 % | 40.3 % | 55.92 % | 66.33 % |
| 1.5 ATR | 9.841 % | 661.8535 | 3.94 % | 13.43 % | 21.25 % | 32.38 % | 47.76 % | 59.3 % |
| 2.0 ATR | 13.122 % | 637.7714 | 1.78 % | 7.31 % | 12.75 % | 21.98 % | 36.22 % | 50.05 % |
| 2.5 ATR | 16.402 % | 613.6893 | 0.49 % | 3.46 % | 6.62 % | 12.97 % | 26.27 % | 40.6 % |
| 3.0 ATR | 19.683 % | 589.6071 | 0.1 % | 1.48 % | 4.05 % | 8.12 % | 18.51 % | 34.17 % |
| 4.0 ATR | 26.244 % | 541.4428 | 0.0 % | 0.39 % | 1.48 % | 3.66 % | 9.55 % | 21.81 % |
| 6.0 ATR | 39.366 % | 445.1142 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.39 % | 4.32 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.15 ATR | 1.43 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.88 ATR | 1.06 ATR | 1.21 ATR | 1.78 ATR | 2.30 ATR |
| **3 s.** | 0.28 ATR | 0.71 ATR | 0.81 ATR | 1.10 ATR | 1.34 ATR | 1.57 ATR | 2.22 ATR | 2.81 ATR |
| **5 s.** | 0.39 ATR | 0.98 ATR | 1.12 ATR | 1.48 ATR | 1.85 ATR | 2.11 ATR | 2.81 ATR | 3.70 ATR |
| **10 s.** | 0.66 ATR | 1.43 ATR | 1.62 ATR | 2.16 ATR | 2.58 ATR | 2.90 ATR | 3.95 ATR | 5.12 ATR |
| **20 s.** | 0.89 ATR | 2.00 ATR | 2.27 ATR | 3.10 ATR | 3.74 ATR | 4.21 ATR | 5.35 ATR | 5.92 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.448 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.659–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.921 %, prix 697.9749), p(touche) 39.19 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.815–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.561 %, prix 685.9357), p(touche) 37.15 % (en stress 95.1 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.121–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.201 %, prix 673.8964), p(touche) 40.3 % (en stress 97.03 %)  ✅ optimum identifie (73.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.62–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.122 %, prix 637.7714), p(touche) 36.22 % (en stress 95.05 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (95.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.267–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.402 %, prix 613.6929), p(touche) 40.6 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.006 | EV/share : €0.086 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 — | T3 —
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 23.4 | bear 70.9 | side 5.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→43% · +3.0%→26% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.92% (p90 6.37%) · excursion haute méd. +1.54% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.386% vs midi 0.887% vs clôture 1.007% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. 0.01% ; recovery-V 14%
- **σ réalisé intraday** 2.348% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 65% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1019.35 (VA 1013.75–1023.55 ; dernier close 1015.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 52% · rebond 59% · **stop −2.85%** sous le fill (sous le bruit) · cible +1.34% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 39% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.73%) · haut méd +0.46% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.14%) · haut méd +0.6% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.31%) · haut méd +0.75% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −2.38%) · haut méd +0.88% · range méd 2.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1019.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 75% (112/159) · gap 18% · délai 0.4min · rebond 57% (62/112) (MFE +1.08%)
   - −1.0% : fill 30min 42% · séance 64% (98/159) · gap 7% · délai 6.3min · rebond 59% (58/98) (MFE +1.26%)
   - −1.5% : fill 30min 26% · séance 52% (80/159) · gap 4% · délai 29.9min · rebond 59% (47/80) (MFE +1.34%)
   - −2.0% : fill 30min 16% · séance 40% (66/159) · gap 2% · délai 88.0min · rebond 52% (38/66) (MFE +1.2%)
   - −3.0% : fill 30min 6% · séance 25% (38/159) · gap 2% · délai 141.2min · rebond 42% (18/38) (MFE +0.97%)
   - −4.0% : fill 30min 2% · séance 12% (21/159) · gap 1% · délai 153.2min · rebond 60% (12/21) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 5% (11/159) · gap 0% · délai 103.2min · rebond 94% (10/11) (MFE +2.81%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.37%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.44%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.48%) → stop au-delà de −0.96% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=544 jambes) : jambe baissière méd −0.97% (p90 −2.4%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 98% (36/37) · rebond 69% (25/36)
      · −2.0% : fill 65% (28/37) · rebond 46% (16/28)
      · −3.0% : fill 46% (16/37) · rebond 33% (7/16)
      · −4.0% : fill 34% (12/37) · rebond 58% (7/12)
      · −5.0% : fill 15% (6/37) · rebond 100% (6/6)
   - **flat** (29 séances) :
      · −1.0% : fill 74% (21/29) · rebond 60% (14/21)
      · −2.0% : fill 41% (11/29) · rebond 75% (8/11)
      · −3.0% : fill 21% (6/29) · rebond 67% (3/6)
      · −4.0% : fill 3% (2/29) · rebond 62% (1/2)
      · −5.0% : fill 3% (2/29) · rebond 62% (1/2)
   - **gap-up** (93 séances) :
      · −1.0% : fill 41% (41/93) · rebond 46% (19/41)
      · −2.0% : fill 27% (27/93) · rebond 44% (14/27)
      · −3.0% : fill 15% (16/93) · rebond 41% (8/16)
      · −4.0% : fill 4% (7/93) · rebond 70% (4/7)
      · −5.0% : fill 1% (3/93) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 57% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **45min** → P(séance verte=clôture>ouverture) 65% si début vert vs 20% si rouge (base 43% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **65%** · continue >prix actuel 48% ; creux résiduel méd -1.21% (q20 -2.27%) → **SL/trailing à −2.27%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.5% → **scale +1.5% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 58%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.6%** (au-delà de la MAE q10 -3.6%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.04% .. +2.68%] · haut q95 +2.92% · bas q05 -2.8%
   - 60min (n=160) : retour [-2.51% .. +3.12%] · haut q95 +3.43% · bas q05 -3.45%
   - 2h (n=160) : retour [-3.37% .. +2.76%] · haut q95 +3.79% · bas q05 -3.97%
   - 4h (n=160) : retour [-3.21% .. +2.84%] · haut q95 +4.17% · bas q05 -4.74%
   - 6h (n=160) : retour [-3.6% .. +3.07%] · haut q95 +4.55% · bas q05 -5.07%
   - session (n=160) : retour [-4.05% .. +3.96%] · haut q95 +4.97% · bas q05 -5.07%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.27 · part idiosyncratique 0.73
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 19.4  _(survente)_
- **ADX** : 35.1  _(tendance etablie)_
- **MACD** : hist -9.271  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 57.6%
- **ATR** : 48.16 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.239  _(distribution)_
- **Vol ratio** : 0.34  _(volume atone)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 847.21 · MA50 934.92 · MA200 1186.54  _(prix < MA20)_
- **Dist MA** : MA20 -13.4% · MA50 -21.5% · MA200 -38.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (524911 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
