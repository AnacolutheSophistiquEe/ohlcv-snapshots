# SAF

**Generated** : 2026-10-09T21:47:00.447716+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €316.20  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 43/125 fenêtres (p_fill pondéré 33 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €316.20 (+1.6% vs entrée) · entrée €311.08 · stop €286.20 · T1 €315.36 · R/R 0.17  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-09 : 316.2 · ATR Wilder 8.32 (2.63 %)_
- **Swing** : plage **306.49 → 300.93** (-3.07 % a -4.83 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 300.92-303.89 (B) ; 295.38-302.1 (B). stop INDICATIF 285.39 (-5.16 % sous le bas ; sous le support 289.55-291.92 (- 0,5 ATR)).
- **Deep** : plage **300.93 → 283.58** (-4.83 % a -10.32 % sous la cloture, 2.08 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 300.92-303.89 (B) ; 295.38-302.1 (B) ; 289.55-291.92 (B) ; 283.02-287.1 (A). stop INDICATIF 274.11 (-3.34 % sous le bas ; sous le support 278.27-280.94 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.94 ATR sous le plus haut 20 s., RSI(2) 44.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 307.05-310.9 (B, -1.68 %) ; 300.92-303.89 (B, -3.89 %) ; 295.38-302.1 (B, -4.46 %) ; 289.55-291.92 (B, -7.68 %) ; 283.02-287.1 (A, -9.2 %) ; 278.27-280.94 (B, -11.15 %)
- Resistances reelles au-dessus : 322.1-326.14 (A, 1.87 %) ; 326.8-329.2 (B, 3.35 %) ; 337.5-340.7 (A, 6.74 %) ; 344.03-346.9 (B, 8.8 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (6.27 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **3.716 pt plus bas** dans le cas TYPIQUE (médiane), 3.716 au p90, **3.716 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 6.27 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0029 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.395 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.3725** [0.3228 ; 0.4243] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3369** [0.2886 ; 0.3879] _(largeur 9.9 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 35.9 observations effectives », dont la borne haute a 95 % vaut environ 8.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.9 pt), swing (43.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.1 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.12 % contre 1.98 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3866** (β de hausse 1.3518, asymétrie 1.0257) vs FCHI — 620 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 303.3536 sur atr_based (1.5 ATR, 4.063 %) — p(stop avant cible) 0.3689 [0.32 ; 0.42], R/R 3.417, perte reelle 4.154 % (gap inclus), CVaR 4.703 %, EV 0.9152 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.7413 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.063 %) — p(stop avant cible) 0.3689 [0.32 ; 0.42], R/R 3.417, perte reelle 4.154 % (gap inclus), EV 0.9152 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ sr_based a 2.49 ATR (stop 8.403 %) — p(stop avant cible) 0.1115 [0.08 ; 0.15], R/R 1.654, perte reelle 8.582 % (gap inclus), EV 0.8663 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 6.6 ATR (stop 19.532 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.688, perte reelle 20.626 % (gap inclus), EV 0.7859 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.07 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.677 %) — p(stop avant cible) 0.8777 [0.84 ; 0.91], R/R 19.88, perte reelle 0.714 % (gap inclus), EV 0.1967 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 19.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.878, borne haute 0.909 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.354 %) — p(stop avant cible) 0.7465 [0.70 ; 0.79], R/R 9.977, perte reelle 1.423 % (gap inclus), EV 0.4239 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.747, borne haute 0.790 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 2.031 %) — p(stop avant cible) 0.6417 [0.59 ; 0.69], R/R 6.758, perte reelle 2.1 % (gap inclus), EV 0.6348 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.642, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 2.709 %) — p(stop avant cible) 0.5454 [0.49 ; 0.60], R/R 5.05, perte reelle 2.811 % (gap inclus), EV 0.7327 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 3.386 %) — p(stop avant cible) 0.4522 [0.40 ; 0.50], R/R 4.108, perte reelle 3.456 % (gap inclus), EV 0.7947 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 4.74 %) — p(stop avant cible) 0.2992 [0.25 ; 0.35], R/R 2.955, perte reelle 4.803 % (gap inclus), EV 1.0115 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 5.417 %) — p(stop avant cible) 0.2511 [0.21 ; 0.30], R/R 2.575, perte reelle 5.512 % (gap inclus), EV 1.0012 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.49 ATR (stop 7.558 %) — p(stop avant cible) 0.1373 [0.10 ; 0.18], R/R 1.844, perte reelle 7.699 % (gap inclus), EV 0.9287 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.48 %) — p(stop avant cible) 0.0794 [0.05 ; 0.11], R/R 1.459, perte reelle 9.726 % (gap inclus), EV 0.8195 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 10.834 %) — p(stop avant cible) 0.0586 [0.04 ; 0.09], R/R 1.269, perte reelle 11.184 % (gap inclus), EV 0.7961 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 12.188 %) — p(stop avant cible) 0.0373 [0.02 ; 0.06], R/R 1.118, perte reelle 12.694 % (gap inclus), EV 0.8007 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 13.543 %) — p(stop avant cible) 0.029 [0.01 ; 0.05], R/R 0.991, perte reelle 14.324 % (gap inclus), EV 0.7565 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.66 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.897 %) — p(stop avant cible) 0.014 [0.01 ; 0.03], R/R 0.849, perte reelle 16.721 % (gap inclus), EV 0.7539 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.72 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.251 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.73, perte reelle 19.45 % (gap inclus), EV 0.7774 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.26 % > budget 12.00 %
   - 🟢 grid_snapped a 6.6 ATR (stop 18.687 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.695, perte reelle 20.415 % (gap inclus), EV 0.787 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.05 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 20.314 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.679, perte reelle 20.914 % (gap inclus), EV 0.7845 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.10 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 21.668 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.65, perte reelle 21.833 % (gap inclus), EV 0.7905 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 316.2, ATR14 8.5643 (2.709 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 0.94 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.135 % | 315.7718 | 89.41 % | 92.64 % | 93.81 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.271 % | 315.3436 | 81.67 % | 87.24 % | 89.19 % | 91.34 % | 93.37 % | 94.81 % |
| 0.15 ATR | 0.406 % | 314.9154 | 75.29 % | 83.42 % | 86.25 % | 88.68 % | 91.2 % | 92.71 % |
| 0.2 ATR | 0.542 % | 314.4872 | 68.43 % | 78.31 % | 82.71 % | 85.33 % | 88.82 % | 91.01 % |
| 0.25 ATR | 0.677 % | 314.0589 | 61.37 % | 73.7 % | 79.08 % | 83.27 % | 87.54 % | 90.11 % |
| 0.35 ATR | 0.948 % | 313.2025 | 49.61 % | 63.49 % | 69.84 % | 76.97 % | 82.59 % | 87.11 % |
| 0.5 ATR | 1.354 % | 311.9179 | 35.49 % | 51.91 % | 59.14 % | 68.5 % | 75.87 % | 81.62 % |
| 0.75 ATR | 2.031 % | 309.7768 | 20.88 % | 35.53 % | 42.83 % | 53.05 % | 63.11 % | 71.13 % |
| 1.0 ATR | 2.709 % | 307.6357 | 10.0 % | 23.85 % | 32.61 % | 42.22 % | 53.81 % | 62.14 % |
| 1.25 ATR | 3.386 % | 305.4947 | 4.41 % | 15.41 % | 23.87 % | 33.17 % | 46.29 % | 55.34 % |
| 1.5 ATR | 4.063 % | 303.3536 | 2.25 % | 10.11 % | 16.5 % | 24.9 % | 38.08 % | 47.35 % |
| 2.0 ATR | 5.417 % | 299.0714 | 0.98 % | 4.51 % | 7.56 % | 15.35 % | 26.9 % | 37.46 % |
| 2.5 ATR | 6.771 % | 294.7893 | 0.2 % | 1.47 % | 3.73 % | 8.66 % | 18.3 % | 28.47 % |
| 3.0 ATR | 8.126 % | 290.5072 | 0.0 % | 0.88 % | 2.16 % | 5.71 % | 12.17 % | 22.28 % |
| 4.0 ATR | 10.834 % | 281.9429 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.89 % |
| 6.0 ATR | 16.251 % | 264.8143 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.51 ATR | 1.96 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.22 ATR | 1.38 ATR | 1.86 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.82 ATR | 0.94 ATR | 1.25 ATR | 1.50 ATR | 1.76 ATR | 2.40 ATR | 3.15 ATR |
| **10 s.** | 0.52 ATR | 1.13 ATR | 1.29 ATR | 1.73 ATR | 2.11 ATR | 2.40 ATR | 3.29 ATR | 3.94 ATR |
| **20 s.** | 0.66 ATR | 1.42 ATR | 1.62 ATR | 2.25 ATR | 2.78 ATR | 3.20 ATR | 4.23 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.605–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.031 %, prix 309.778), p(touche) 35.53 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.717–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.031 %, prix 309.778), p(touche) 42.83 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.936–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.709 %, prix 307.6342), p(touche) 42.22 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.289–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.063 %, prix 303.3528), p(touche) 38.08 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.619–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.417 %, prix 299.0715), p(touche) 37.46 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 9.0 | bear 34.9 | side 56.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.62% → cible +1.377% / stop −8.0%, p_fill 33%, n_eff≈35.9) : P(cible|rempli) **33%** · **EV/risk -0.004** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −3.562% → cible +3.14% / stop −2.809%, p_fill 13%, n_eff≈18.2) : P(cible|rempli) **52%** · **EV/risk +0.034** (×p_fill ; si rempli +0.71% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=12))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→50% · +2.0%→24% · +3.0%→8% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.49% (p90 4.07%) · excursion haute méd. +0.98% / basse méd. −0.99%
- Profil de vol intra : ouverture 1.488% vs midi 0.546% vs clôture 0.685% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.099 ; mean-reverting — autocorr -0.058)_ ; drift intra méd. -0.278% ; recovery-V 20%
- **σ réalisé intraday** 1.556% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 68% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 332.2313 (VA 330.9188–333.8062 ; dernier close 330.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 30% · **stop −1.38%** sous le fill (sous le bruit) · cible +0.71% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.28% · baisse 36% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.37% (p90 −1.37%) · haut méd +0.21% · range méd 0.8%
- Excursion ouverture 15min (n=160) : bas méd −0.37% (p90 −1.58%) · haut méd +0.37% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.45% (p90 −1.67%) · haut méd +0.52% · range méd 1.11%
- Excursion ouverture 60min (n=160) : bas méd −0.61% (p90 −1.81%) · haut méd +0.57% · range méd 1.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 330.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 59% (92/159) · gap 8% · délai 1.0min · rebond 36% (35/92) (MFE +0.77%)
   - −1.0% : fill 30min 24% · séance 47% (74/159) · gap 1% · délai 30.6min · rebond 47% (36/74) (MFE +0.87%)
   - −1.5% : fill 30min 9% · séance 28% (46/159) · gap 0% · délai 80.2min · rebond 28% (18/46) (MFE +0.62%)
   - −2.0% : fill 30min 3% · séance 23% (38/159) · gap 0% · délai 218.5min · rebond 30% (14/38) (MFE +0.71%)
   - −3.0% : fill 30min 1% · séance 9% (16/159) · gap 0% · délai 398.1min · rebond 20% (6/16) (MFE +0.54%)
   - −4.0% : fill 30min 0% · séance 1% (4/159) · gap 0% · délai 282.8min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −0.66%) → stop au-delà de −0.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.08% (p90 −0.99%) → stop au-delà de −0.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=198 jambes) : jambe baissière méd −1.05% (p90 −2.41%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (23 séances) :
      · −1.0% : fill 83% (19/23) · rebond 30% (6/19)
      · −2.0% : fill 53% (13/23) · rebond 24% (5/13)
      · −3.0% : fill 21% (6/23) · rebond 18% (2/6)
      · −4.0% : fill 5% (2/23) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/23) · rebond 0% (0/0)
   - **flat** (45 séances) :
      · −1.0% : fill 52% (24/45) · rebond 48% (13/24)
      · −2.0% : fill 29% (11/45) · rebond 23% (2/11)
      · −3.0% : fill 11% (4/45) · rebond 19% (1/4)
      · −4.0% : fill 0% (0/45) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/45) · rebond 0% (0/0)
   - **gap-up** (91 séances) :
      · −1.0% : fill 32% (31/91) · rebond 60% (17/31)
      · −2.0% : fill 9% (14/91) · rebond 56% (7/14)
      · −3.0% : fill 4% (6/91) · rebond 27% (3/6)
      · −4.0% : fill 1% (2/91) · rebond 38% (1/2)
      · −5.0% : fill 0% (1/91) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 66% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 79% si début vert vs 20% si rouge (base 46% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 34min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **79%** · continue >prix actuel 60% ; creux résiduel méd -0.73% (q20 -1.22%) → **SL/trailing à −1.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.41% → **scale +1.0% / runner +1.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **20%** (continue à baisser 59%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.24%** (au-delà de la MAE q10 -2.24%), cible rebond +0.86% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.27%] · haut q95 +1.76% · bas q05 -1.94%
   - 60min (n=160) : retour [-1.63% .. +1.69%] · haut q95 +1.9% · bas q05 -1.98%
   - 2h (n=160) : retour [-1.79% .. +1.94%] · haut q95 +2.35% · bas q05 -2.39%
   - 4h (n=160) : retour [-1.87% .. +1.93%] · haut q95 +2.53% · bas q05 -2.72%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.78%
   - session (n=160) : retour [-2.86% .. +2.04%] · haut q95 +2.99% · bas q05 -3.47%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.6  _(momentum baissier)_
- **ADX** : 16.3  _(pas de tendance nette)_
- **MACD** : hist -1.51  _(bearish_recent)_
- **BB** : %B 0.08 · largeur 8.6%
- **ATR** : 8.56 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.19  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 48.0  _(transition)_
- **MA** : MA20 327.96 · MA50 338.42 · MA200 315.91  _(prix < MA20)_
- **Dist MA** : MA20 -3.6% · MA50 -6.6% · MA200 +0.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (884977 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
