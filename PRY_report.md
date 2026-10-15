# PRY

**Generated** : 2026-10-15T00:12:47.556285+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €113.75  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 0/121 fenêtres (p_fill pondéré 0 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €113.75 (+15.2% vs entrée) · entrée €98.77 · stop €94.02 · T1 €104.08 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -117 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 113.75 · ATR Wilder 4.75 (4.17 %)_
- **Swing** : plage **108.6 → 105.39** (-4.53 % a -7.35 % sous la cloture, 0.68 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 103.98-110.08 (B). stop INDICATIF 100.65 (-4.5 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **105.39 → 96.89** (-7.35 % a -14.83 % sous la cloture, 1.79 ATR) — touchee 39 % → 15 % du temps en 20 seances ; supports reels dans la plage : 103.98-110.08 (B) ; 96.88-99.95 (B). stop INDICATIF 92.12 (-4.92 % sous le bas ; sous le support 94.5-95.09 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 3.68 ATR sous le plus haut 20 s., RSI(2) 2.1. Limite **111.38** (seance suivante), stop catastrophe 92.39, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 110.3-110.3 (C, -3.03 %) ; 103.98-110.08 (B, -3.23 %) ; 96.88-99.95 (B, -12.13 %) ; 94.5-95.09 (A, -16.4 %) ; 91.78-92.37 (A, -18.79 %) ; 89.22-91.32 (A, -19.72 %)
- Resistances reelles au-dessus : 115.85-117.1 (A, 1.85 %) ; 122.29-123.2 (A, 7.51 %) ; 129.4-131.2 (A, 13.76 %) ; 134.3-134.9 (A, 18.07 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.57 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (17.34 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1270).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 17.34 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.3758** [0.326 ; 0.4277] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.2491** [0.2057 ; 0.2966] _(largeur 9.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.11 %** | CVaR **-5.62 %** | vol 2.45 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.55 % contre 2.86 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.52 % vs -7.57 % si l'on extrapolait par √5 _(rapport 0.861 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0304** (β de hausse 1.2321, asymétrie 0.8362) vs FTSEMIB — 565 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.357× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 100.6973 sur atr_grid (2.75 ATR, 11.475 %) — p(stop avant cible) 0.0914 [0.06 ; 0.13], R/R 3.085, perte reelle 11.65 % (gap inclus), CVaR 11.796 %, EV 1.2471 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.259 %) — p(stop avant cible) 0.365 [0.32 ; 0.42], R/R 5.598, perte reelle 6.421 % (gap inclus), EV 0.6108 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ sr_based a 5.84 ATR (stop 26.496 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.343, perte reelle 26.77 % (gap inclus), EV 1.4533 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.55 % > budget 12.00 %
   - 🟢 support a 7.41 ATR (stop 33.06 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.087, perte reelle 33.06 % (gap inclus), EV 1.4612 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.41 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.043 %) — p(stop avant cible) 0.8844 [0.85 ; 0.91], R/R 30.833, perte reelle 1.166 % (gap inclus), EV -0.0591 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 30.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.884, borne haute 0.915 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.0 % x 35.95 % + P(rien) 11.6 % x 8.41 % ne couvrent pas P(stop) 88.4 % x 1.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+35.9 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.086 %) — p(stop avant cible) 0.7657 [0.72 ; 0.81], R/R 16.124, perte reelle 2.229 % (gap inclus), EV 0.0015 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 16.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.766, borne haute 0.808 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 3.13 %) — p(stop avant cible) 0.6494 [0.60 ; 0.70], R/R 10.83, perte reelle 3.319 % (gap inclus), EV 0.0988 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 4.173 %) — p(stop avant cible) 0.5498 [0.50 ; 0.60], R/R 8.333, perte reelle 4.314 % (gap inclus), EV 0.1614 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.550, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 5.216 %) — p(stop avant cible) 0.4499 [0.40 ; 0.50], R/R 6.694, perte reelle 5.37 % (gap inclus), EV 0.2562 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 7.302 %) — p(stop avant cible) 0.2809 [0.24 ; 0.33], R/R 4.837, perte reelle 7.431 % (gap inclus), EV 0.8381 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 8.345 %) — p(stop avant cible) 0.2316 [0.19 ; 0.28], R/R 4.255, perte reelle 8.448 % (gap inclus), EV 0.8619 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 9.389 %) — p(stop avant cible) 0.1935 [0.15 ; 0.24], R/R 3.792, perte reelle 9.481 % (gap inclus), EV 0.9407 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.5 ATR (stop 10.432 %) — p(stop avant cible) 0.1399 [0.11 ; 0.18], R/R 3.412, perte reelle 10.535 % (gap inclus), EV 1.0911 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.75 ATR (stop 11.475 %) — p(stop avant cible) 0.0914 [0.06 ; 0.13], R/R 3.085, perte reelle 11.65 % (gap inclus), EV 1.2471 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 3.0 ATR (stop 12.518 %) — p(stop avant cible) 0.0692 [0.05 ; 0.10], R/R 2.82, perte reelle 12.748 % (gap inclus), EV 1.2902 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 14.604 %) — p(stop avant cible) 0.0325 [0.02 ; 0.06], R/R 2.445, perte reelle 14.705 % (gap inclus), EV 1.4298 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.41 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 16.691 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 2.104, perte reelle 17.085 % (gap inclus), EV 1.4661 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.24 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 18.777 %) — p(stop avant cible) 0.0102 [0.00 ; 0.03], R/R 1.813, perte reelle 19.826 % (gap inclus), EV 1.4502 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.61 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 20.863 %) — p(stop avant cible) 0.0079 [0.00 ; 0.02], R/R 1.626, perte reelle 22.112 % (gap inclus), EV 1.4386 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.88 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.95 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 1.497, perte reelle 24.02 % (gap inclus), EV 1.4379 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.87 % > budget 12.00 %
   - ⚪ grid_snapped a 5.84 ATR (stop 25.612 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.371, perte reelle 26.212 % (gap inclus), EV 1.4551 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 27.122 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 1.316, perte reelle 27.306 % (gap inclus), EV 1.4562 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 29.209 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 1.111, perte reelle 32.353 % (gap inclus), EV 1.4542 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.53 % > budget 12.00 %
   - 🟢 grid_snapped a 7.41 ATR (stop 32.175 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 1.111, perte reelle 32.353 % (gap inclus), EV 1.4542 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.53 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 113.75, ATR14 4.7464 (4.173 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.44 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.209 % | 113.5127 | 91.88 % | 94.05 % | 94.74 % | 95.53 % | 97.2 % | 97.78 % |
| 0.1 ATR | 0.417 % | 113.2754 | 85.25 % | 89.0 % | 91.17 % | 92.94 % | 95.1 % | 96.17 % |
| 0.15 ATR | 0.626 % | 113.038 | 77.92 % | 84.44 % | 87.5 % | 90.46 % | 92.91 % | 94.15 % |
| 0.2 ATR | 0.835 % | 112.8007 | 70.0 % | 79.29 % | 82.74 % | 86.98 % | 90.71 % | 92.23 % |
| 0.25 ATR | 1.043 % | 112.5634 | 62.28 % | 74.33 % | 78.57 % | 83.2 % | 88.11 % | 90.21 % |
| 0.35 ATR | 1.46 % | 112.0887 | 49.41 % | 63.83 % | 70.73 % | 76.54 % | 83.72 % | 87.39 % |
| 0.5 ATR | 2.086 % | 111.3768 | 34.95 % | 51.93 % | 59.82 % | 67.59 % | 76.42 % | 81.74 % |
| 0.75 ATR | 3.13 % | 110.1902 | 19.31 % | 34.49 % | 43.25 % | 54.27 % | 64.74 % | 73.26 % |
| 1.0 ATR | 4.173 % | 109.0036 | 9.9 % | 23.19 % | 31.55 % | 44.23 % | 55.54 % | 65.19 % |
| 1.25 ATR | 5.216 % | 107.817 | 5.54 % | 15.86 % | 23.91 % | 34.49 % | 47.05 % | 57.52 % |
| 1.5 ATR | 6.259 % | 106.6304 | 2.48 % | 9.61 % | 16.17 % | 24.45 % | 36.56 % | 49.04 % |
| 2.0 ATR | 8.345 % | 104.2571 | 0.4 % | 3.96 % | 7.54 % | 14.02 % | 24.28 % | 37.34 % |
| 2.5 ATR | 10.432 % | 101.8839 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.58 % | 26.74 % |
| 3.0 ATR | 12.518 % | 99.5107 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.69 % | 18.97 % |
| 4.0 ATR | 16.691 % | 94.7643 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 25.036 % | 85.2714 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.48 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.29 ATR | 1.49 ATR | 1.71 ATR | 2.33 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.30 ATR | 1.65 ATR | 1.97 ATR | 2.25 ATR | 2.97 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.47 ATR | 1.67 ATR | 2.21 ATR | 2.61 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.599–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.13 %, prix 110.1896), p(touche) 34.49 % (en stress 88.12 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.724–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.13 %, prix 110.1896), p(touche) 43.25 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.981–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.173 %, prix 109.0032), p(touche) 44.23 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.299–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.259 %, prix 106.6304), p(touche) 36.56 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.673–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.345 %, prix 104.2576), p(touche) 37.34 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.057 | EV/share : €-0.269 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 4 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.0 | bear 10.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→40% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.71% (p90 6.32%) · excursion haute méd. +1.5% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.21% vs midi 0.779% vs clôture 1.066% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.354% ; recovery-V 21%
- **σ réalisé intraday** 2.479% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 65% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 129.9327 (VA 129.5263–130.8813 ; dernier close 130.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 60% · **stop −2.81%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.51% · baisse 35% (gap-down >1% 13% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −2.05%) · haut méd +0.51% · range méd 1.3%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.32%) · haut méd +0.61% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.41%) · haut méd +0.74% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −1.05% (p90 −2.93%) · haut méd +0.83% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 129.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 65% (109/159) · gap 19% · délai 0.4min · rebond 54% (61/109) (MFE +1.1%)
   - −1.0% : fill 30min 39% · séance 54% (90/159) · gap 13% · délai 1.3min · rebond 60% (54/90) (MFE +1.25%)
   - −1.5% : fill 30min 24% · séance 45% (72/159) · gap 7% · délai 21.4min · rebond 51% (39/72) (MFE +1.06%)
   - −2.0% : fill 30min 18% · séance 37% (60/159) · gap 3% · délai 42.5min · rebond 51% (34/60) (MFE +1.01%)
   - −3.0% : fill 30min 6% · séance 23% (40/159) · gap 1% · délai 93.7min · rebond 60% (26/40) (MFE +1.15%)
   - −4.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 282.0min · rebond 57% (15/25) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 9% (16/159) · gap 0% · délai 394.7min · rebond 66% (11/16) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.89%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.31% (p90 −1.63%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.76%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=487 jambes) : jambe baissière méd −1.06% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 94% (39/43) · rebond 49% (19/39)
      · −2.0% : fill 77% (31/43) · rebond 58% (18/31)
      · −3.0% : fill 47% (23/43) · rebond 50% (14/23)
      · −4.0% : fill 30% (15/43) · rebond 57% (9/15)
      · −5.0% : fill 26% (12/43) · rebond 57% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 48% (15/27) · rebond 74% (11/15)
      · −2.0% : fill 27% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 16% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 6% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 38% (36/89) · rebond 65% (24/36)
      · −2.0% : fill 23% (21/89) · rebond 30% (9/21)
      · −3.0% : fill 14% (12/89) · rebond 80% (9/12)
      · −4.0% : fill 9% (8/89) · rebond 54% (5/8)
      · −5.0% : fill 4% (3/89) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 63% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 82% si début vert vs 21% si rouge (base 46% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **82%** · continue >prix actuel 45% ; creux résiduel méd -1.18% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.01% → **scale +1.07% / runner +2.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **21%** (continue à baisser 66%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.77%** (au-delà de la MAE q10 -3.77%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.93% .. +2.17%] · haut q95 +3.13% · bas q05 -3.36%
   - 60min (n=160) : retour [-3.28% .. +2.31%] · haut q95 +3.46% · bas q05 -3.58%
   - 2h (n=160) : retour [-3.32% .. +2.69%] · haut q95 +3.52% · bas q05 -4.05%
   - 4h (n=160) : retour [-3.46% .. +3.2%] · haut q95 +4.0% · bas q05 -4.46%
   - 6h (n=160) : retour [-3.73% .. +3.5%] · haut q95 +4.42% · bas q05 -4.65%
   - session (n=160) : retour [-4.58% .. +3.44%] · haut q95 +4.53% · bas q05 -6.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.7 · part idiosyncratique 0.3
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 36.4  _(momentum baissier)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist -1.05  _(bearish_recent)_
- **BB** : %B -0.17 · largeur 12.4%
- **ATR** : 4.75 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.214  _(distribution)_
- **Vol ratio** : 1.25  _(volume normal)_
- **Choppiness** : 50.1  _(transition)_
- **MA** : MA20 124.09 · MA50 123.92 · MA200 120.64  _(prix < MA20)_
- **Dist MA** : MA20 -8.3% · MA50 -8.2% · MA200 -5.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (885813 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
