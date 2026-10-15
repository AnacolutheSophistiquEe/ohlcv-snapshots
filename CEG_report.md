# CEG

**Generated** : 2026-10-15T00:25:57.725590+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $279.62  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 0/121 fenêtres (p_fill pondéré 0 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $279.62 (+13.1% vs entrée) · entrée $247.21 · stop $231.01 · T1 $265.33 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -2.8 % ≠ (strike 287.5 − spot 279.62)/spot = +2.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 279.62 · ATR Wilder 14.2 (5.08 %)_
- **Swing** : plage **260.58 → 250.19** (-6.81 % a -10.53 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 255.71-260.27 (A) ; 248.38-250.55 (B). stop INDICATIF 233.04 (-6.85 % sous le bas ; sous le support 240.14-247.2 (- 0,5 ATR)).
- **Deep** : plage **250.19 → 223.51** (-10.53 % a -20.06 % sous la cloture, 1.88 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 248.38-250.55 (B) ; 240.14-247.2 (A) ; 232.79-236.2 (A) ; 224.73-229.28 (A) ; 216.13-228.28 (B). stop INDICATIF 209.32 (-6.35 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.13 ATR sous le plus haut 20 s., RSI(2) 14.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 255.71-260.27 (A, -6.92 %) ; 248.38-250.55 (B, -10.4 %) ; 240.14-247.2 (A, -11.59 %) ; 232.79-236.2 (A, -15.53 %) ; 224.73-229.28 (A, -18.0 %) ; 216.13-228.28 (B, -18.36 %)
- Resistances reelles au-dessus : 284.07-286.56 (A, 1.59 %) ; 291.53-294.09 (A, 4.26 %) ; 299.33-305.8 (A, 7.05 %) ; 306.91-309.97 (A, 9.76 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.02 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (17.38 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1188).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 17.38 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.862 % | p01 -4.433 % | pire -15.824 % _(sur 1188 séances)_
- **P(stop avant cible)** _(source : daily, 1189 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0091** [0.0015 ; 0.0325] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.2717** [0.2268 ; 0.3204] _(largeur 9.4 pt, n_eff 345.5)_
   - deep : **0.2525** [0.2089 ; 0.3002] _(largeur 9.1 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.32 %** | CVaR **-6.27 %** | vol 2.86 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.79 % contre 2.98 % aujourd'hui, rapport 1.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.92 % vs -9.72 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1741** (β de hausse 1.1828, asymétrie 0.9927) vs SPY — 550 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 259.3658 sur atr_grid (1.25 ATR, 7.243 %) — p(stop avant cible) 0.395 [0.34 ; 0.45], R/R 4.481, perte reelle 7.449 % (gap inclus), CVaR 8.869 %, EV 0.0928 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9487 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.692 %) — p(stop avant cible) 0.3317 [0.28 ; 0.38], R/R 3.787, perte reelle 8.815 % (gap inclus), EV -0.0216 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.8 % x 33.38 % + P(rien) 66.1 % x 4.00 % ne couvrent pas P(stop) 33.2 % x 8.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 2.2 ATR (stop 15.72 %) — p(stop avant cible) 0.0843 [0.06 ; 0.12], R/R 2.118, perte reelle 15.764 % (gap inclus), EV 0.1251 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.79 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.449 %) — p(stop avant cible) 0.872 [0.83 ; 0.90], R/R 21.563, perte reelle 1.548 % (gap inclus), EV -0.1358 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 21.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.872, borne haute 0.904 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.5 % x 33.38 % + P(rien) 12.3 % x 8.55 % ne couvrent pas P(stop) 87.2 % x 1.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.897 %) — p(stop avant cible) 0.7282 [0.68 ; 0.77], R/R 10.862, perte reelle 3.073 % (gap inclus), EV -0.0469 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 10.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.728, borne haute 0.773 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 0.7 % x 33.38 % + P(rien) 26.5 % x 7.35 % ne couvrent pas P(stop) 72.8 % x 3.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.346 %) — p(stop avant cible) 0.6265 [0.57 ; 0.68], R/R 7.397, perte reelle 4.513 % (gap inclus), EV -0.2728 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 7.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.626, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 0.8 % x 33.38 % + P(rien) 36.6 % x 6.28 % ne couvrent pas P(stop) 62.6 % x 4.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 5.795 %) — p(stop avant cible) 0.5056 [0.45 ; 0.56], R/R 5.575, perte reelle 5.988 % (gap inclus), EV 0.0152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.506, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 7.243 %) — p(stop avant cible) 0.395 [0.34 ; 0.45], R/R 4.481, perte reelle 7.449 % (gap inclus), EV 0.0928 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 10.141 %) — p(stop avant cible) 0.2705 [0.23 ; 0.32], R/R 3.257, perte reelle 10.249 % (gap inclus), EV -0.0137 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 0.8 % x 33.38 % + P(rien) 72.2 % x 3.47 % ne couvrent pas P(stop) 27.1 % x 10.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.2 ATR (stop 14.492 %) — p(stop avant cible) 0.1221 [0.09 ; 0.16], R/R 2.296, perte reelle 14.54 % (gap inclus), EV 0.062 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.61 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.384 %) — p(stop avant cible) 0.0494 [0.03 ; 0.08], R/R 1.902, perte reelle 17.546 % (gap inclus), EV 0.1515 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.53 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.282 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 1.637, perte reelle 20.385 % (gap inclus), EV 0.2441 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.84 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.179 %) — p(stop avant cible) 0.008 [0.00 ; 0.02], R/R 1.437, perte reelle 23.228 % (gap inclus), EV 0.3038 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.076 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 1.278, perte reelle 26.128 % (gap inclus), EV 0.3085 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.46 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.974 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 1.148, perte reelle 29.067 % (gap inclus), EV 0.306 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.871 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.047, perte reelle 31.871 % (gap inclus), EV 0.3147 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.34 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.769 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.96, perte reelle 34.769 % (gap inclus), EV 0.3152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.666 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.886, perte reelle 37.666 % (gap inclus), EV 0.3152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.563 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.823, perte reelle 40.563 % (gap inclus), EV 0.3152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.461 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.768, perte reelle 43.461 % (gap inclus), EV 0.3152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.358 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.72, perte reelle 46.358 % (gap inclus), EV 0.3152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 279.62, ATR14 16.2034 (5.795 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 2.254 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.29 % | 278.8098 | 91.59 % | 94.61 % | 95.57 % | 96.65 % | 97.61 % | 98.02 % |
| 0.1 ATR | 0.579 % | 277.9997 | 85.45 % | 90.4 % | 92.44 % | 94.05 % | 95.65 % | 96.81 % |
| 0.15 ATR | 0.869 % | 277.1895 | 78.99 % | 86.19 % | 88.44 % | 90.58 % | 93.8 % | 95.49 % |
| 0.2 ATR | 1.159 % | 276.3793 | 71.98 % | 80.8 % | 84.02 % | 86.69 % | 91.4 % | 94.17 % |
| 0.25 ATR | 1.449 % | 275.5692 | 65.19 % | 75.3 % | 79.27 % | 83.01 % | 88.68 % | 92.19 % |
| 0.35 ATR | 2.028 % | 273.9488 | 53.88 % | 65.91 % | 71.49 % | 76.73 % | 84.22 % | 88.67 % |
| 0.5 ATR | 2.897 % | 271.5183 | 38.79 % | 52.86 % | 59.5 % | 66.34 % | 77.04 % | 82.95 % |
| 0.75 ATR | 4.346 % | 267.4675 | 20.26 % | 36.68 % | 45.14 % | 53.35 % | 66.7 % | 76.02 % |
| 1.0 ATR | 5.795 % | 263.4166 | 11.31 % | 24.06 % | 33.15 % | 43.29 % | 57.67 % | 69.75 % |
| 1.25 ATR | 7.243 % | 259.3658 | 5.82 % | 16.07 % | 24.19 % | 35.5 % | 51.47 % | 63.7 % |
| 1.5 ATR | 8.692 % | 255.315 | 2.8 % | 10.68 % | 17.39 % | 28.9 % | 44.5 % | 57.76 % |
| 2.0 ATR | 11.59 % | 247.2133 | 0.86 % | 4.31 % | 9.18 % | 17.75 % | 31.23 % | 46.53 % |
| 2.5 ATR | 14.487 % | 239.1116 | 0.43 % | 2.27 % | 4.75 % | 10.93 % | 21.11 % | 36.63 % |
| 3.0 ATR | 17.384 % | 231.0099 | 0.0 % | 1.08 % | 2.81 % | 6.93 % | 15.56 % | 28.71 % |
| 4.0 ATR | 23.179 % | 214.8066 | 0.0 % | 0.22 % | 0.86 % | 2.71 % | 7.07 % | 14.3 % |
| 6.0 ATR | 34.769 % | 182.3999 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.76 % | 2.75 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.06 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.23 ATR | 1.40 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.83 ATR | 0.96 ATR | 1.34 ATR | 1.68 ATR | 1.90 ATR | 2.62 ATR | 3.46 ATR |
| **10 s.** | 0.55 ATR | 1.30 ATR | 1.48 ATR | 1.93 ATR | 2.31 ATR | 2.60 ATR | 3.65 ATR | 4.66 ATR |
| **20 s.** | 0.79 ATR | 1.85 ATR | 2.08 ATR | 2.73 ATR | 3.26 ATR | 3.60 ATR | 4.75 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.438–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.897 %, prix 271.5194), p(touche) 38.79 % (en stress 81.72 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.621–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.346 %, prix 267.4677), p(touche) 36.68 % (en stress 88.17 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.753–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.795 %, prix 263.416), p(touche) 33.15 % (en stress 95.7 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.958–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.795 %, prix 263.416), p(touche) 43.29 % (en stress 96.77 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.482–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.692 %, prix 255.3154), p(touche) 44.5 % (en stress 98.91 %)  ✅ optimum identifie (70.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.077–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.487 %, prix 239.1114), p(touche) 36.63 % (en stress 95.6 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.018 | EV/share : $-0.288 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 5 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 8.9 | bear 69.4 | side 21.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 251.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→61% · +2.0%→33% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.35% (p90 5.52%) · excursion haute méd. +1.42% / basse méd. −1.56%
- Profil de vol intra : ouverture 2.454% vs midi 0.669% vs clôture 0.758% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑1%/↓0% ; spike-down 51% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr 0.022)_ ; drift intra méd. -0.452% ; recovery-V 16%
- **σ réalisé intraday** 2.399% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 68% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 254.8755 (VA 253.3035–256.4475 ; dernier close 257.55)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 37% · rebond 57% · **stop −2.7%** sous le fill (sous le bruit) · cible +1.1% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 38% (gap-down >1% 10% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −1.58%) · haut méd +0.77% · range méd 1.41%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.27%) · haut méd +0.93% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.61%) · haut méd +1.01% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.14% (p90 −3.48%) · haut méd +1.13% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 257.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 66% (103/159) · gap 26% · délai 1.3min · rebond 43% (50/103) (MFE +0.8%)
   - −1.0% : fill 30min 38% · séance 53% (87/159) · gap 10% · délai 2.5min · rebond 43% (40/87) (MFE +0.95%)
   - −1.5% : fill 30min 32% · séance 45% (72/159) · gap 6% · délai 10.5min · rebond 52% (36/72) (MFE +1.02%)
   - −2.0% : fill 30min 25% · séance 37% (59/159) · gap 3% · délai 21.2min · rebond 57% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 9% · séance 18% (32/159) · gap 2% · délai 31.6min · rebond 45% (14/32) (MFE +0.78%)
   - −4.0% : fill 30min 6% · séance 9% (18/159) · gap 1% · délai 9.3min · rebond 42% (10/18) (MFE +0.76%)
   - −5.0% : fill 30min 4% · séance 6% (11/159) · gap 0% · délai 17.8min · rebond 70% (8/11) (MFE +1.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −1.1%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.32% (p90 −1.17%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.23%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.08% (p90 −2.55%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 91% (40/43) · rebond 45% (21/40)
      · −2.0% : fill 80% (33/43) · rebond 57% (18/33)
      · −3.0% : fill 36% (18/43) · rebond 29% (6/18)
      · −4.0% : fill 28% (14/43) · rebond 39% (7/14)
      · −5.0% : fill 20% (10/43) · rebond 69% (7/10)
   - **flat** (27 séances) :
      · −1.0% : fill 47% (18/27) · rebond 11% (4/18)
      · −2.0% : fill 30% (11/27) · rebond 47% (6/11)
      · −3.0% : fill 13% (6/27) · rebond 24% (2/6)
      · −4.0% : fill 5% (3/27) · rebond 43% (2/3)
      · −5.0% : fill 1% (1/27) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 34% (29/89) · rebond 52% (15/29)
      · −2.0% : fill 16% (15/89) · rebond 61% (9/15)
      · −3.0% : fill 9% (8/89) · rebond 88% (6/8)
      · −4.0% : fill 1% (1/89) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/89) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 59% si les 15 1res min sont vertes (86 cas) · 30% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 85% si début vert vs 8% si rouge (base 44% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.88% (q20 -1.57%) → **SL/trailing à −1.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.8% / q75 +1.26% → **scale +0.8% / runner +1.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **8%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.22%** (au-delà de la MAE q10 -2.22%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.58% .. +2.04%] · haut q95 +3.04% · bas q05 -4.75%
   - 60min (n=160) : retour [-3.48% .. +2.54%] · haut q95 +3.33% · bas q05 -4.99%
   - 2h (n=160) : retour [-3.71% .. +2.98%] · haut q95 +3.95% · bas q05 -5.37%
   - 4h (n=160) : retour [-3.72% .. +3.29%] · haut q95 +4.1% · bas q05 -5.37%
   - 6h (n=160) : retour [-3.86% .. +3.44%] · haut q95 +4.48% · bas q05 -5.37%
   - session (n=160) : retour [-3.61% .. +3.56%] · haut q95 +4.53% · bas q05 -5.47%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 4.4% / strong 2.5%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.89% / p90 2.36%) · ~1.0 replis/séance, durée méd 144.56 min. P(nouveau plus-haut après repli) :
   - −0.5% → **69%** (reprise méd 24.3 min, n=22)
   - −1.0% → **69%** (reprise méd 179.47 min, n=11)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.36%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.62% (q75 +4.82% / q95 +6.2%), MFE méd +4.65% / q90 +5.84%
   - Échelle scale-out : +4.65% (33%) / +5.3% (33%) / +5.84% (34%)
- **DÉSARMER** : repli > **−2.36%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.84% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.48%)


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 57.6  _(momentum haussier)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist 2.589  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 24.4%
- **ATR** : 16.2 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.009  _(neutre)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 48.8  _(transition)_
- **MA** : MA20 272.37 · MA50 275.21 · MA200 284.39  _(prix > MA20)_
- **Dist MA** : MA20 +2.7% · MA50 +1.6% · MA200 -1.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (888669 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
