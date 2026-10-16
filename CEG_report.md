# CEG

**Generated** : 2026-10-16T00:28:38.119120+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $275.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 0/121 fenêtres (p_fill pondéré 0 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $275.00 (+13.8% vs entrée) · entrée $241.74 · stop $225.11 · T1 $260.33 · R/R 1.12  
> ↳ ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.9 % ≠ (strike 287.5 − spot 275.00)/spot = +4.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-15 : 275.0 · ATR Wilder 14.03 (5.1 %)_
- **Swing** : plage **256.2 → 245.99** (-6.84 % a -10.55 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 255.71-260.27 (A) ; 247.2-250.55 (A) ; 240.14-246.18 (A). stop INDICATIF 225.77 (-8.22 % sous le bas ; sous le support 232.79-236.2 (- 0,5 ATR)).
- **Deep** : plage **245.99 → 219.53** (-10.55 % a -20.17 % sous la cloture, 1.89 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 240.14-246.18 (A) ; 232.79-236.2 (A) ; 224.73-229.28 (A) ; 216.13-228.28 (B). stop INDICATIF 193.76 (-11.74 % sous le bas ; sous le support 200.78-206.79 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.48 ATR sous le plus haut 20 s., RSI(2) 10.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 263.92-268.72 (B, -2.28 %) ; 255.71-260.27 (A, -5.35 %) ; 247.2-250.55 (A, -8.89 %) ; 240.14-246.18 (A, -10.48 %) ; 232.79-236.2 (A, -14.11 %) ; 224.73-229.28 (A, -16.63 %)
- Resistances reelles au-dessus : 284.07-286.56 (A, 3.3 %) ; 291.53-294.09 (A, 6.01 %) ; 299.33-305.8 (A, 8.85 %) ; 306.91-309.97 (A, 11.6 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.02 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (18.14 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1189).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.14 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.862 % | p01 -4.433 % | pire -15.824 % _(sur 1189 séances)_
- **P(stop avant cible)** _(source : daily, 1190 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.009** [0.0015 ; 0.0323] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.2531** [0.2094 ; 0.3009] _(largeur 9.1 pt, n_eff 345.5)_
   - deep : **0.2302** [0.1882 ; 0.2767] _(largeur 8.9 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.32 %** | CVaR **-6.27 %** | vol 2.86 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.79 % contre 2.91 % aujourd'hui, rapport 1.65)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.91 % vs -9.71 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1741** (β de hausse 1.1856, asymétrie 0.9903) vs SPY — 550 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 254.2119 sur atr_grid (1.25 ATR, 7.559 %) — p(stop avant cible) 0.3722 [0.32 ; 0.42], R/R 4.593, perte reelle 7.744 % (gap inclus), CVaR 8.94 %, EV 0.1215 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.966 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.071 %) — p(stop avant cible) 0.3099 [0.26 ; 0.36], R/R 3.869, perte reelle 9.194 % (gap inclus), EV 0.026 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 1.87 ATR (stop 14.318 %) — p(stop avant cible) 0.1296 [0.10 ; 0.17], R/R 2.475, perte reelle 14.372 % (gap inclus), EV 0.0964 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.46 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.512 %) — p(stop avant cible) 0.8711 [0.83 ; 0.90], R/R 21.927, perte reelle 1.622 % (gap inclus), EV -0.1962 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 21.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.871, borne haute 0.903 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.3 % x 35.57 % + P(rien) 12.6 % x 8.86 % ne couvrent pas P(stop) 87.1 % x 1.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.024 %) — p(stop avant cible) 0.7187 [0.67 ; 0.76], R/R 11.057, perte reelle 3.217 % (gap inclus), EV -0.0634 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 11.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.719, borne haute 0.764 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.5 % x 35.57 % + P(rien) 27.6 % x 7.48 % ne couvrent pas P(stop) 71.9 % x 3.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.536 %) — p(stop avant cible) 0.6236 [0.57 ; 0.67], R/R 7.56, perte reelle 4.706 % (gap inclus), EV -0.394 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.624, borne haute 0.673 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.5 % x 35.57 % + P(rien) 37.1 % x 6.35 % ne couvrent pas P(stop) 62.4 % x 4.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.047 %) — p(stop avant cible) 0.4878 [0.44 ; 0.54], R/R 5.706, perte reelle 6.234 % (gap inclus), EV 0.0105 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.25 ATR (stop 7.559 %) — p(stop avant cible) 0.3722 [0.32 ; 0.42], R/R 4.593, perte reelle 7.744 % (gap inclus), EV 0.1215 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 1.87 ATR (stop 13.133 %) — p(stop avant cible) 0.174 [0.14 ; 0.22], R/R 2.691, perte reelle 13.218 % (gap inclus), EV -0.0113 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 0.5 % x 35.57 % + P(rien) 82.0 % x 2.55 % ne couvrent pas P(stop) 17.4 % x 13.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 15.119 %) — p(stop avant cible) 0.1049 [0.08 ; 0.14], R/R 2.348, perte reelle 15.149 % (gap inclus), EV 0.0987 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.18 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 16.631 %) — p(stop avant cible) 0.0557 [0.04 ; 0.08], R/R 2.132, perte reelle 16.686 % (gap inclus), EV 0.2006 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.69 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 18.142 %) — p(stop avant cible) 0.0431 [0.03 ; 0.07], R/R 1.942, perte reelle 18.314 % (gap inclus), EV 0.1795 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.03 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.166 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 1.678, perte reelle 21.2 % (gap inclus), EV 0.3189 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.41 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 24.19 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 1.471, perte reelle 24.19 % (gap inclus), EV 0.3491 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 27.214 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 1.304, perte reelle 27.288 % (gap inclus), EV 0.3393 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.58 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.237 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 1.177, perte reelle 30.237 % (gap inclus), EV 0.3492 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.261 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.07, perte reelle 33.261 % (gap inclus), EV 0.3494 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.285 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.98, perte reelle 36.285 % (gap inclus), EV 0.351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.308 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.905, perte reelle 39.308 % (gap inclus), EV 0.351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 42.332 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.84, perte reelle 42.332 % (gap inclus), EV 0.351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 45.356 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.784, perte reelle 45.356 % (gap inclus), EV 0.351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 48.38 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.735, perte reelle 48.38 % (gap inclus), EV 0.351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 275.0, ATR14 16.6305 (6.047 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 2.352 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.302 % | 274.1685 | 91.6 % | 94.61 % | 95.58 % | 96.65 % | 97.61 % | 98.02 % |
| 0.1 ATR | 0.605 % | 273.3369 | 85.47 % | 90.41 % | 92.45 % | 94.05 % | 95.65 % | 96.81 % |
| 0.15 ATR | 0.907 % | 272.5054 | 79.01 % | 86.21 % | 88.46 % | 90.59 % | 93.8 % | 95.49 % |
| 0.2 ATR | 1.209 % | 271.6739 | 72.01 % | 80.82 % | 84.03 % | 86.7 % | 91.41 % | 94.18 % |
| 0.25 ATR | 1.512 % | 270.8424 | 65.23 % | 75.32 % | 79.29 % | 83.03 % | 88.7 % | 92.2 % |
| 0.35 ATR | 2.117 % | 269.1793 | 53.93 % | 65.95 % | 71.52 % | 76.76 % | 84.24 % | 88.68 % |
| 0.5 ATR | 3.024 % | 266.6847 | 38.86 % | 52.91 % | 59.55 % | 66.38 % | 77.07 % | 82.97 % |
| 0.75 ATR | 4.536 % | 262.5271 | 20.34 % | 36.64 % | 45.2 % | 53.41 % | 66.74 % | 76.04 % |
| 1.0 ATR | 6.047 % | 258.3695 | 11.3 % | 24.03 % | 33.23 % | 43.35 % | 57.72 % | 69.78 % |
| 1.25 ATR | 7.559 % | 254.2119 | 5.81 % | 16.06 % | 24.27 % | 35.57 % | 51.41 % | 63.74 % |
| 1.5 ATR | 9.071 % | 250.0542 | 2.8 % | 10.67 % | 17.37 % | 28.86 % | 44.46 % | 57.8 % |
| 2.0 ATR | 12.095 % | 241.739 | 0.86 % | 4.31 % | 9.17 % | 17.73 % | 31.2 % | 46.48 % |
| 2.5 ATR | 15.119 % | 233.4237 | 0.43 % | 2.26 % | 4.75 % | 10.92 % | 21.09 % | 36.59 % |
| 3.0 ATR | 18.142 % | 225.1085 | 0.0 % | 1.08 % | 2.8 % | 6.92 % | 15.54 % | 28.68 % |
| 4.0 ATR | 24.19 % | 208.478 | 0.0 % | 0.22 % | 0.86 % | 2.7 % | 7.07 % | 14.29 % |
| 6.0 ATR | 36.285 % | 175.217 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.76 % | 2.75 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.06 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.75 ATR | 1.01 ATR | 1.23 ATR | 1.41 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.83 ATR | 0.96 ATR | 1.35 ATR | 1.67 ATR | 1.90 ATR | 2.62 ATR | 3.46 ATR |
| **10 s.** | 0.55 ATR | 1.30 ATR | 1.48 ATR | 1.93 ATR | 2.31 ATR | 2.60 ATR | 3.65 ATR | 4.66 ATR |
| **20 s.** | 0.79 ATR | 1.84 ATR | 2.08 ATR | 2.73 ATR | 3.26 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.024 %, prix 266.684), p(touche) 38.86 % (en stress 81.72 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.622–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.536 %, prix 262.526), p(touche) 36.64 % (en stress 88.17 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.754–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.047 %, prix 258.3707), p(touche) 33.23 % (en stress 95.7 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.959–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.047 %, prix 258.3707), p(touche) 43.35 % (en stress 96.77 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.481–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.071 %, prix 250.0548), p(touche) 44.46 % (en stress 98.91 %)  ✅ optimum identifie (71.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.075–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.119 %, prix 233.4228), p(touche) 36.59 % (en stress 95.6 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.013 | EV/share : $0.225 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 5 % | T3 0 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 17.4 | bear 54.5 | side 28.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 245.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=3))
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.48 · part idiosyncratique 0.52
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 54.8  _(neutre)_
- **ADX** : 20.6  _(pas de tendance nette)_
- **MACD** : hist 1.26  _(pas de croisement recent)_
- **BB** : %B 0.53 · largeur 24.1%
- **ATR** : 16.63 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.025  _(neutre)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 49.8  _(transition)_
- **MA** : MA20 272.97 · MA50 275.42 · MA200 283.98  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -0.2% · MA200 -3.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (842835 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
