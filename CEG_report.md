# CEG

**Generated** : 2026-10-26T01:26:51.860313+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $253.45  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $253.45 (+6.7% vs entrée) · entrée $237.58 · stop $218.57 · T1 $245.52 · R/R 0.42  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 253.45 · ATR Wilder 13.22 (5.22 %)_
- **Swing** : plage **235.74 → 226.0** (-6.99 % a -10.83 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 232.79-236.2 (A) ; 224.73-229.28 (A) ; 216.13-228.28 (B). stop INDICATIF 212.78 (-5.85 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **226.0 → 201.2** (-10.83 % a -20.62 % sous la cloture, 1.88 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 224.73-229.28 (A) ; 216.13-228.28 (B) ; 200.78-206.79 (B). stop INDICATIF 184.87 (-8.12 % sous le bas ; sous le support 191.48-196.82 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.26 ATR sous le plus haut 20 s., RSI(2) 21.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 240.14-246.18 (A, -2.87 %) ; 232.79-236.2 (A, -6.81 %) ; 224.73-229.28 (A, -9.54 %) ; 216.13-228.28 (B, -9.93 %) ; 200.78-206.79 (B, -18.41 %) ; 191.48-196.82 (B, -22.34 %)
- Resistances reelles au-dessus : 263.92-268.72 (A, 4.13 %) ; 275.99-282.34 (A, 8.89 %) ; 284.07-286.56 (A, 12.08 %) ; 291.53-294.09 (A, 15.02 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.01 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (18.78 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1195).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -4.432 % | pire -15.824 % _(sur 1195 séances)_
- **P(stop avant cible)** _(source : daily, 1196 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0084** [0.0013 ; 0.0313] _(largeur 3.0 pt, n_eff 173.1)_
   - swing : **0.2575** [0.2135 ; 0.3055] _(largeur 9.2 pt, n_eff 345.5)_
   - deep : **0.2211** [0.1798 ; 0.2671] _(largeur 8.7 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.34 %** | vol 2.88 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.70 % contre 2.90 % aujourd'hui, rapport 1.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.14 % vs -9.78 % si l'on extrapolait par √5 _(rapport 1.037 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1795** (β de hausse 1.1891, asymétrie 0.9919) vs SPY — 553 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 249.4826 sur atr_grid (0.25 ATR, 1.565 %) — p(stop avant cible) 0.8692 [0.83 ; 0.90], R/R 28.131, perte reelle 1.678 % (gap inclus), CVaR 3.32 %, EV -0.2417 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.6373 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 28.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.869, borne haute 0.902 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **3.37 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.183 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 20.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.59 ATR (stop 7.012 %) — p(stop avant cible) 0.4195 [0.37 ; 0.47], R/R 6.535, perte reelle 7.221 % (gap inclus), EV 0.0039 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.76 % > budget 3.37 %
   - ⚪ atr_based a 1.5 ATR (stop 9.392 %) — p(stop avant cible) 0.3079 [0.26 ; 0.36], R/R 4.967, perte reelle 9.501 % (gap inclus), EV -0.1647 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 10.06 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.1 % x 47.19 % + P(rien) 69.2 % x 3.95 % ne couvrent pas P(stop) 30.8 % x 9.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.565 %) — p(stop avant cible) 0.8692 [0.83 ; 0.90], R/R 28.131, perte reelle 1.678 % (gap inclus), EV -0.2417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 28.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.869, borne haute 0.902 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.0 % x 47.19 % + P(rien) 13.1 % x 9.21 % ne couvrent pas P(stop) 86.9 % x 1.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.59 ATR (stop 5.597 %) — p(stop avant cible) 0.5367 [0.48 ; 0.59], R/R 8.181, perte reelle 5.768 % (gap inclus), EV -0.2059 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.537, borne haute 0.589 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.44 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.1 % x 47.19 % + P(rien) 46.3 % x 6.18 % ne couvrent pas P(stop) 53.7 % x 5.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 7.827 %) — p(stop avant cible) 0.3714 [0.32 ; 0.42], R/R 5.912, perte reelle 7.983 % (gap inclus), EV -0.0385 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.98 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.1 % x 47.19 % + P(rien) 62.8 % x 4.61 % ne couvrent pas P(stop) 37.1 % x 7.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 10.957 %) — p(stop avant cible) 0.249 [0.21 ; 0.30], R/R 4.272, perte reelle 11.046 % (gap inclus), EV -0.1898 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.40 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.1 % x 47.19 % + P(rien) 75.0 % x 3.37 % ne couvrent pas P(stop) 24.9 % x 11.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 12.523 %) — p(stop avant cible) 0.1934 [0.15 ; 0.24], R/R 3.737, perte reelle 12.628 % (gap inclus), EV -0.2531 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.93 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.1 % x 47.19 % + P(rien) 80.6 % x 2.68 % ne couvrent pas P(stop) 19.3 % x 12.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 14.088 %) — p(stop avant cible) 0.1362 [0.10 ; 0.18], R/R 3.339, perte reelle 14.135 % (gap inclus), EV -0.1829 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.22 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.1 % x 47.19 % + P(rien) 86.3 % x 1.99 % ne couvrent pas P(stop) 13.6 % x 14.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 15.653 %) — p(stop avant cible) 0.0844 [0.06 ; 0.12], R/R 3.006, perte reelle 15.696 % (gap inclus), EV -0.0282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.73 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.1 % x 47.19 % + P(rien) 91.5 % x 1.39 % ne couvrent pas P(stop) 8.4 % x 15.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 17.219 %) — p(stop avant cible) 0.0498 [0.03 ; 0.08], R/R 2.723, perte reelle 17.333 % (gap inclus), EV -0.0032 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 3.37 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 0.1 % x 47.19 % + P(rien) 95.0 % x 0.88 % ne couvrent pas P(stop) 5.0 % x 17.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+47.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 18.784 %) — p(stop avant cible) 0.0273 [0.01 ; 0.05], R/R 2.485, perte reelle 18.99 % (gap inclus), EV 0.0501 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.58 % > budget 3.37 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.915 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 2.144, perte reelle 22.015 % (gap inclus), EV 0.1273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.26 % > budget 3.37 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.045 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 1.884, perte reelle 25.045 % (gap inclus), EV 0.1438 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.32 % > budget 3.37 %
   - ⚪ atr_grid a 4.5 ATR (stop 28.176 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.661, perte reelle 28.42 % (gap inclus), EV 0.1468 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 3.37 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.307 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.507, perte reelle 31.307 % (gap inclus), EV 0.1506 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 3.37 %
   - ⚪ atr_grid a 5.5 ATR (stop 34.438 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.37, perte reelle 34.438 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.21 % > budget 3.37 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.568 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.256, perte reelle 37.568 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.21 % > budget 3.37 %
   - ⚪ atr_grid a 6.5 ATR (stop 40.699 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.16, perte reelle 40.699 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.21 % > budget 3.37 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.83 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.077, perte reelle 43.83 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.21 % > budget 3.37 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.96 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.005, perte reelle 46.96 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.21 % > budget 3.37 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.091 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.942, perte reelle 50.091 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.21 % > budget 3.37 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 253.45, ATR14 15.8694 (6.261 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 2.436 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.313 % | 252.6565 | 91.66 % | 94.65 % | 95.61 % | 96.67 % | 97.62 % | 98.03 % |
| 0.1 ATR | 0.626 % | 251.8631 | 85.56 % | 90.47 % | 92.5 % | 94.09 % | 95.68 % | 96.83 % |
| 0.15 ATR | 0.939 % | 251.0696 | 79.14 % | 86.3 % | 88.53 % | 90.66 % | 93.84 % | 95.52 % |
| 0.2 ATR | 1.252 % | 250.2761 | 72.09 % | 80.84 % | 84.14 % | 86.79 % | 91.36 % | 94.21 % |
| 0.25 ATR | 1.565 % | 249.4826 | 65.24 % | 75.37 % | 79.42 % | 83.14 % | 88.66 % | 92.25 % |
| 0.35 ATR | 2.191 % | 247.8957 | 53.9 % | 66.06 % | 71.7 % | 76.91 % | 84.23 % | 88.76 % |
| 0.5 ATR | 3.131 % | 245.5153 | 38.82 % | 53.0 % | 59.7 % | 66.49 % | 77.11 % | 83.08 % |
| 0.75 ATR | 4.696 % | 241.5479 | 20.43 % | 36.83 % | 45.44 % | 53.71 % | 66.85 % | 76.2 % |
| 1.0 ATR | 6.261 % | 237.5806 | 11.23 % | 24.09 % | 33.44 % | 43.72 % | 57.88 % | 69.87 % |
| 1.25 ATR | 7.827 % | 233.6132 | 5.78 % | 16.06 % | 24.33 % | 35.88 % | 51.62 % | 63.76 % |
| 1.5 ATR | 9.392 % | 229.6459 | 2.78 % | 10.71 % | 17.36 % | 29.0 % | 44.6 % | 57.64 % |
| 2.0 ATR | 12.523 % | 221.7111 | 0.86 % | 4.28 % | 9.11 % | 17.83 % | 31.43 % | 46.18 % |
| 2.5 ATR | 15.653 % | 213.7764 | 0.43 % | 2.25 % | 4.72 % | 10.85 % | 21.06 % | 36.35 % |
| 3.0 ATR | 18.784 % | 205.8417 | 0.0 % | 1.07 % | 2.79 % | 6.87 % | 15.44 % | 28.49 % |
| 4.0 ATR | 25.045 % | 189.9723 | 0.0 % | 0.21 % | 0.86 % | 2.69 % | 7.02 % | 14.19 % |
| 6.0 ATR | 37.568 % | 158.2334 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.76 % | 2.73 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.06 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.55 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.67 ATR | 0.76 ATR | 1.01 ATR | 1.23 ATR | 1.41 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.84 ATR | 0.97 ATR | 1.35 ATR | 1.68 ATR | 1.90 ATR | 2.61 ATR | 3.45 ATR |
| **10 s.** | 0.55 ATR | 1.31 ATR | 1.49 ATR | 1.94 ATR | 2.31 ATR | 2.59 ATR | 3.65 ATR | 4.64 ATR |
| **20 s.** | 0.80 ATR | 1.83 ATR | 2.06 ATR | 2.71 ATR | 3.24 ATR | 3.59 ATR | 4.73 ATR | 5.60 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.131 %, prix 245.5145), p(touche) 38.82 % (en stress 82.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.696 %, prix 241.548), p(touche) 36.83 % (en stress 88.3 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.759–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.261 %, prix 237.5815), p(touche) 33.44 % (en stress 95.74 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.968–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.261 %, prix 237.5815), p(touche) 43.72 % (en stress 96.81 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.486–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.392 %, prix 229.646), p(touche) 44.6 % (en stress 98.92 %)  ✅ optimum identifie (73.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.06–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.653 %, prix 213.7775), p(touche) 36.35 % (en stress 95.65 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (87.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.1 | bear 70.0 | side 24.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→62% · +2.0%→34% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.36% (p90 5.65%) · excursion haute méd. +1.38% / basse méd. −1.56%
- Profil de vol intra : ouverture 2.53% vs midi 0.658% vs clôture 0.771% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr 0.005)_ ; drift intra méd. -0.554% ; recovery-V 16%
- **σ réalisé intraday** 2.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 59% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 253.5534 (VA 252.1149–254.9919 ; dernier close 253.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 39% · **stop −2.72%** sous le fill (sous le bruit) · cible +0.65% · R/R 0.24 (high win-rate)
- Gaps overnight (n=159) : méd. 0.39% · baisse 43% (gap-down >1% 15% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.8%) · haut méd +0.66% · range méd 1.52%
- Excursion ouverture 15min (n=160) : bas méd −0.97% (p90 −2.69%) · haut méd +0.84% · range méd 2.02%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −3.19%) · haut méd +0.92% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.18% (p90 −3.97%) · haut méd +1.01% · range méd 2.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 253.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 68% (102/159) · gap 29% · délai 0.0min · rebond 38% (45/102) (MFE +0.8%)
   - −1.0% : fill 30min 46% · séance 58% (87/159) · gap 15% · délai 1.4min · rebond 46% (38/87) (MFE +0.97%)
   - −1.5% : fill 30min 41% · séance 52% (75/159) · gap 7% · délai 4.1min · rebond 52% (34/75) (MFE +1.03%)
   - −2.0% : fill 30min 30% · séance 46% (64/159) · gap 4% · délai 9.6min · rebond 52% (33/64) (MFE +1.03%)
   - −3.0% : fill 30min 15% · séance 25% (35/159) · gap 3% · délai 14.2min · rebond 50% (15/35) (MFE +0.96%)
   - −4.0% : fill 30min 9% · séance 15% (21/159) · gap 0% · délai 21.4min · rebond 39% (10/21) (MFE +0.65%)
   - −5.0% : fill 30min 3% · séance 10% (13/159) · gap 0% · délai 61.8min · rebond 33% (7/13) (MFE +0.56%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.42%) → stop au-delà de −0.98% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −1.41%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.48%) → stop au-delà de −1.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=471 jambes) : jambe baissière méd −1.09% (p90 −2.58%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 94% (42/45) · rebond 46% (19/42)
      · −2.0% : fill 88% (37/45) · rebond 54% (19/37)
      · −3.0% : fill 51% (22/45) · rebond 40% (8/22)
      · −4.0% : fill 41% (18/45) · rebond 38% (8/18)
      · −5.0% : fill 26% (12/45) · rebond 32% (6/12)
   - **flat** (24 séances) :
      · −1.0% : fill 52% (15/24) · rebond 31% (3/15)
      · −2.0% : fill 40% (11/24) · rebond 64% (6/11)
      · −3.0% : fill 11% (5/24) · rebond 18% (1/5)
      · −4.0% : fill 3% (2/24) · rebond 28% (1/2)
      · −5.0% : fill 1% (1/24) · rebond 100% (1/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 34% (30/90) · rebond 52% (16/30)
      · −2.0% : fill 19% (16/90) · rebond 41% (8/16)
      · −3.0% : fill 11% (8/90) · rebond 92% (6/8)
      · −4.0% : fill 0% (1/90) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/90) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 62% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 80% si début vert vs 16% si rouge (base 42% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **80%** · continue >prix actuel 46% ; creux résiduel méd -1.18% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +2.04% → **scale +1.2% / runner +2.04%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **16%** (continue à baisser 56%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.3%** (au-delà de la MAE q10 -2.3%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.44% .. +2.01%] · haut q95 +3.41% · bas q05 -3.51%
   - 60min (n=160) : retour [-3.66% .. +2.94%] · haut q95 +3.74% · bas q05 -4.68%
   - 2h (n=160) : retour [-3.81% .. +3.8%] · haut q95 +4.14% · bas q05 -5.27%
   - 4h (n=160) : retour [-4.48% .. +3.64%] · haut q95 +4.31% · bas q05 -5.39%
   - 6h (n=160) : retour [-4.7% .. +3.8%] · haut q95 +4.82% · bas q05 -5.75%
   - session (n=160) : retour [-4.6% .. +3.49%] · haut q95 +4.82% · bas q05 -5.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **32%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.11% (p75 1.79% / p90 2.39%) · ~1.0 replis/séance, durée méd 169.74 min. P(nouveau plus-haut après repli) :
   - −0.5% → **68%** (reprise méd 29.55 min, n=17)
   - −1.0% → **67%** (reprise méd 182.65 min, n=9)
   - −1.5% → **45%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.39%** (p90, défaut prudent ; serré/agressif −1.79%) ; extension open→close méd +3.62% (q75 +4.52% / q95 +6.21%), MFE méd +4.59% / q90 +5.86%
   - Échelle scale-out : +4.59% (33%) / +5.3% (33%) / +5.86% (34%)
- **DÉSARMER** : repli > **−2.39%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.86% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.49%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.7  _(momentum baissier)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist -3.247  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 24.4%
- **ATR** : 15.87 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.044  _(neutre)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 48.0  _(transition)_
- **MA** : MA20 273.16 · MA50 274.18 · MA200 281.27  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -7.6% · MA200 -9.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (777511 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
