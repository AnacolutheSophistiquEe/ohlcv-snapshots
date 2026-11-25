# SAF

**Generated** : 2026-11-25T01:09:14.628367+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €299.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot €299.50 (+0.4% vs entrée) · entrée €298.17 · stop €274.32 · T1 €302.75 · R/R 0.19  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -79 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 299.5 · ATR Wilder 9.22 (3.08 %)_
- **Swing** : plage **288.33 → 281.74** (-3.73 % a -5.93 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 283.02-287.1 (B). stop INDICATIF 271.88 (-3.5 % sous le bas ; sous le support 276.49-280.94 (- 0,5 ATR)).
- **Deep** : plage **281.74 → 260.39** (-5.93 % a -13.06 % sous la cloture, 2.32 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 276.49-280.94 (B) ; 269.9-273.87 (A) ; 265.22-268.29 (B) ; 259.68-263.34 (A). stop INDICATIF 249.14 (-4.32 % sous le bas ; sous le support 253.75-257.96 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.07 ATR sous le plus haut 20 s., RSI(2) 46.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 289.55-291.92 (B, -2.53 %) ; 283.02-287.1 (B, -4.14 %) ; 276.49-280.94 (B, -6.2 %) ; 269.9-273.87 (A, -8.56 %) ; 265.22-268.29 (B, -10.42 %) ; 259.68-263.34 (A, -12.07 %)
- Resistances reelles au-dessus : 306.9-310.9 (A, 2.47 %) ; 312.29-316.9 (A, 4.27 %) ; 317.14-320.7 (A, 5.89 %) ; 322.1-326.14 (A, 7.55 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.70 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (4.04 %)** : le gap seul le franchit 0.312 % des séances (4 fois sur 1280).
   - exécution **1.165 pt plus bas** dans le cas TYPIQUE (médiane), 4.564 au p90, **5.946 au pire**
   - perte réelle **6.163 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 4.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0066 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.405 % | p01 -2.434 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.3454** [0.2967 ; 0.3966] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.3511** [0.3022 ; 0.4025] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 78.9 observations effectives », dont la borne haute a 95 % vaut environ 3.8 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-2.89 %** | CVaR **-4.34 %** | vol 1.85 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 1.08 % contre 1.98 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.63 % vs -6.21 % si l'on extrapolait par √5 _(rapport 0.906 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3825** (β de hausse 1.3551, asymétrie 1.0202) vs FCHI — 622 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 287.6542 sur sr_based (0.68 ATR, 3.955 %) — p(stop avant cible) 0.4139 [0.36 ; 0.47], R/R 4.881, perte reelle 4.2 % (gap inclus), CVaR 5.754 %, EV 0.7358 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.68 ATR (stop 3.955 %) — p(stop avant cible) 0.4139 [0.36 ; 0.47], R/R 4.881, perte reelle 4.2 % (gap inclus), EV 0.7358 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 3.43 ATR (stop 12.368 %) — p(stop avant cible) 0.0727 [0.05 ; 0.10], R/R 1.623, perte reelle 12.632 % (gap inclus), EV 0.3637 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.75 % > budget 12.00 %
   - 🔴 support a 4.34 ATR (stop 15.167 %) — p(stop avant cible) 0.0147 [0.01 ; 0.03], R/R 1.24, perte reelle 16.527 % (gap inclus), EV 0.3533 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.08 % > budget 12.00 %
      - ⚠ support DETECTE a 0.58 ATR du spot — compartiment <1, mesure a 49.2 % de casse (IC clusterise [0.458 ; 0.523] sur 1200 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.765 %) — p(stop avant cible) 0.8496 [0.81 ; 0.88], R/R 25.358, perte reelle 0.808 % (gap inclus), EV 0.3597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 25.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.850, borne haute 0.884 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.68 ATR (stop 3.001 %) — p(stop avant cible) 0.5273 [0.47 ; 0.58], R/R 6.608, perte reelle 3.103 % (gap inclus), EV 0.7633 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.527, borne haute 0.580 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.5 ATR (stop 4.59 %) — p(stop avant cible) 0.3637 [0.31 ; 0.42], R/R 4.274, perte reelle 4.797 % (gap inclus), EV 0.7221 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 5.355 %) — p(stop avant cible) 0.309 [0.26 ; 0.36], R/R 3.678, perte reelle 5.573 % (gap inclus), EV 0.7141 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 6.12 %) — p(stop avant cible) 0.28 [0.23 ; 0.33], R/R 3.254, perte reelle 6.301 % (gap inclus), EV 0.6582 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 6.885 %) — p(stop avant cible) 0.23 [0.19 ; 0.28], R/R 2.932, perte reelle 6.992 % (gap inclus), EV 0.5793 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 7.65 %) — p(stop avant cible) 0.1896 [0.15 ; 0.23], R/R 2.643, perte reelle 7.758 % (gap inclus), EV 0.5521 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.415 %) — p(stop avant cible) 0.144 [0.11 ; 0.18], R/R 2.403, perte reelle 8.53 % (gap inclus), EV 0.5616 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.18 %) — p(stop avant cible) 0.1226 [0.09 ; 0.16], R/R 2.192, perte reelle 9.352 % (gap inclus), EV 0.5056 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.43 ATR (stop 11.413 %) — p(stop avant cible) 0.0913 [0.06 ; 0.13], R/R 1.773, perte reelle 11.564 % (gap inclus), EV 0.3586 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 grid_snapped a 4.34 ATR (stop 14.213 %) — p(stop avant cible) 0.0295 [0.02 ; 0.05], R/R 1.369, perte reelle 14.979 % (gap inclus), EV 0.3522 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.03 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.829 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 1.046, perte reelle 19.6 % (gap inclus), EV 0.375 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.68 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.359 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 1.017, perte reelle 20.152 % (gap inclus), EV 0.3778 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.889 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.989, perte reelle 20.729 % (gap inclus), EV 0.3832 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.59 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.419 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.946, perte reelle 21.683 % (gap inclus), EV 0.3883 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.50 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.949 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.893, perte reelle 22.949 % (gap inclus), EV 0.3938 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.36 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.479 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.837, perte reelle 24.479 % (gap inclus), EV 0.3979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.31 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 299.5, ATR14 9.1643 (3.06 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 1.062 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.153 % | 299.0418 | 89.31 % | 92.64 % | 93.71 % | 95.57 % | 96.24 % | 97.1 % |
| 0.1 ATR | 0.306 % | 298.5836 | 81.57 % | 87.44 % | 89.29 % | 91.44 % | 93.47 % | 95.0 % |
| 0.15 ATR | 0.459 % | 298.1254 | 75.49 % | 84.0 % | 86.74 % | 89.17 % | 91.69 % | 93.31 % |
| 0.2 ATR | 0.612 % | 297.6671 | 68.24 % | 78.51 % | 82.91 % | 85.53 % | 88.92 % | 91.51 % |
| 0.25 ATR | 0.765 % | 297.2089 | 61.18 % | 73.8 % | 79.08 % | 83.37 % | 87.54 % | 90.61 % |
| 0.35 ATR | 1.071 % | 296.2925 | 49.61 % | 63.89 % | 70.14 % | 77.36 % | 82.89 % | 87.71 % |
| 0.5 ATR | 1.53 % | 294.9179 | 35.39 % | 52.4 % | 59.63 % | 69.29 % | 76.56 % | 82.42 % |
| 0.75 ATR | 2.295 % | 292.6268 | 20.69 % | 35.53 % | 43.22 % | 53.94 % | 63.9 % | 72.63 % |
| 1.0 ATR | 3.06 % | 290.3357 | 10.1 % | 24.24 % | 33.1 % | 43.11 % | 55.09 % | 64.24 % |
| 1.25 ATR | 3.825 % | 288.0446 | 4.51 % | 15.8 % | 24.46 % | 33.86 % | 47.58 % | 57.54 % |
| 1.5 ATR | 4.59 % | 285.7536 | 2.35 % | 10.4 % | 16.9 % | 25.59 % | 39.37 % | 49.75 % |
| 2.0 ATR | 6.12 % | 281.1714 | 1.08 % | 4.71 % | 7.96 % | 16.24 % | 28.68 % | 40.46 % |
| 2.5 ATR | 7.65 % | 276.5893 | 0.2 % | 1.57 % | 3.93 % | 9.25 % | 19.88 % | 31.27 % |
| 3.0 ATR | 9.18 % | 272.0071 | 0.0 % | 0.98 % | 2.36 % | 6.2 % | 13.55 % | 24.78 % |
| 4.0 ATR | 12.239 % | 262.8429 | 0.0 % | 0.29 % | 0.79 % | 1.48 % | 5.44 % | 12.89 % |
| 6.0 ATR | 18.359 % | 244.5143 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.19 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.23 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.98 ATR | 1.13 ATR | 1.53 ATR | 1.98 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 1.00 ATR | 1.23 ATR | 1.40 ATR | 1.89 ATR | 2.37 ATR |
| **5 s.** | 0.39 ATR | 0.84 ATR | 0.96 ATR | 1.28 ATR | 1.53 ATR | 1.80 ATR | 2.45 ATR | 3.25 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.33 ATR | 1.80 ATR | 2.21 ATR | 2.49 ATR | 3.44 ATR | 4.21 ATR |
| **20 s.** | 0.69 ATR | 1.49 ATR | 1.76 ATR | 2.41 ATR | 2.98 ATR | 3.40 ATR | 4.64 ATR | 5.75 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.399 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.61–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.295 %, prix 292.6265), p(touche) 35.53 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.723–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.295 %, prix 292.6265), p(touche) 43.22 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.956–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.06 %, prix 290.3353), p(touche) 43.11 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.329–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.59 %, prix 285.7529), p(touche) 39.37 % (en stress 99.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.756–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.12 %, prix 281.1706), p(touche) 40.46 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 9.4 | bear 5.6 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.446% → cible +1.537% / stop −8.0%, p_fill 76%, n_eff≈78.9) : P(cible|rempli) **19%** · **EV/risk -0.034** (×p_fill ; si rempli -0.35% du capital)
  - **swing** (entrée dip −0.98% → cible +3.455% / stop −3.09%, p_fill 68%, n_eff≈77.9) : P(cible|rempli) **26%** · **EV/risk -0.068** (×p_fill ; si rempli -0.31% du capital)
  - **deep** (entrée dip −1.51% → cible +4.912% / stop −4.66%, p_fill 72%, n_eff≈78.1) : P(cible|rempli) **36%** · **EV/risk -0.043** (×p_fill ; si rempli -0.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→73% · +1.0%→50% · +2.0%→21% · +3.0%→6% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.44% (p90 3.66%) · excursion haute méd. +1.01% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.464% vs midi 0.52% vs clôture 0.69% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.714% ; recovery-V 9%
- **σ réalisé intraday** 1.704% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 70% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 275.7587 (VA 272.0312–278.4212 ; dernier close 270.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 15% · rebond 30% · **stop −0.98%** sous le fill (sous le bruit) · cible +0.56% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. 0.15% · baisse 41% (gap-down >1% 4% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.42% (p90 −1.66%) · haut méd +0.23% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.45% (p90 −1.94%) · haut méd +0.35% · range méd 1.04%
- Excursion ouverture 30min (n=160) : bas méd −0.54% (p90 −2.04%) · haut méd +0.51% · range méd 1.21%
- Excursion ouverture 60min (n=160) : bas méd −0.62% (p90 −2.06%) · haut méd +0.52% · range méd 1.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 271.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 63% (95/159) · gap 13% · délai 0.4min · rebond 34% (36/95) (MFE +0.77%)
   - −1.0% : fill 30min 30% · séance 50% (77/159) · gap 4% · délai 13.7min · rebond 43% (36/77) (MFE +0.61%)
   - −1.5% : fill 30min 18% · séance 34% (50/159) · gap 2% · délai 15.5min · rebond 32% (19/50) (MFE +0.66%)
   - −2.0% : fill 30min 10% · séance 28% (40/159) · gap 2% · délai 101.1min · rebond 36% (15/40) (MFE +0.73%)
   - −3.0% : fill 30min 2% · séance 15% (19/159) · gap 2% · délai 391.3min · rebond 30% (7/19) (MFE +0.56%)
   - −4.0% : fill 30min 2% · séance 3% (4/159) · gap 0% · délai 37.1min · rebond 24% (2/4) (MFE +0.38%)
   - −5.0% : fill 30min 2% · séance 2% (2/159) · gap 0% · délai 55.7min · rebond 0% (0/2) (MFE +0.11%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −0.76%) → stop au-delà de −0.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −0.64%) → stop au-delà de −0.43% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.01%) → stop au-delà de −0.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=200 jambes) : jambe baissière méd −1.06% (p90 −2.63%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (27 séances) :
      · −1.0% : fill 82% (22/27) · rebond 28% (7/22)
      · −2.0% : fill 56% (15/27) · rebond 14% (5/15)
      · −3.0% : fill 37% (8/27) · rebond 26% (3/8)
      · −4.0% : fill 11% (2/27) · rebond 21% (1/2)
      · −5.0% : fill 9% (1/27) · rebond 0% (0/1)
   - **flat** (51 séances) :
      · −1.0% : fill 55% (28/51) · rebond 41% (14/28)
      · −2.0% : fill 30% (13/51) · rebond 45% (4/13)
      · −3.0% : fill 12% (5/51) · rebond 13% (1/5)
      · −4.0% : fill 0% (0/51) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/51) · rebond 0% (0/0)
   - **gap-up** (81 séances) :
      · −1.0% : fill 31% (27/81) · rebond 65% (15/27)
      · −2.0% : fill 11% (12/81) · rebond 71% (6/12)
      · −3.0% : fill 7% (6/81) · rebond 67% (3/6)
      · −4.0% : fill 1% (2/81) · rebond 38% (1/2)
      · −5.0% : fill 0% (1/81) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 69% si les 15 1res min sont vertes (77 cas) · 23% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **41min** → P(séance verte=clôture>ouverture) 77% si début vert vs 16% si rouge (base 45% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 39min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **77%** · continue >prix actuel 56% ; creux résiduel méd -0.74% (q20 -1.2%) → **SL/trailing à −1.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.91% / q75 +1.31% → **scale +0.91% / runner +1.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **16%** (continue à baisser 60%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.32%** (au-delà de la MAE q10 -2.32%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.73% .. +1.21%] · haut q95 +1.77% · bas q05 -2.22%
   - 60min (n=160) : retour [-1.91% .. +1.59%] · haut q95 +1.82% · bas q05 -2.29%
   - 2h (n=160) : retour [-2.25% .. +1.74%] · haut q95 +2.19% · bas q05 -2.59%
   - 4h (n=160) : retour [-2.83% .. +1.83%] · haut q95 +2.3% · bas q05 -3.03%
   - 6h (n=160) : retour [-2.4% .. +2.06%] · haut q95 +2.56% · bas q05 -3.94%
   - session (n=160) : retour [-3.08% .. +1.92%] · haut q95 +2.83% · bas q05 -3.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.5  _(momentum haussier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist 0.682  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 16.6%
- **ATR** : 9.16 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.098  _(distribution)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 53.6  _(transition)_
- **MA** : MA20 297.57 · MA50 310.24 · MA200 314.81  _(prix > MA20)_
- **Dist MA** : MA20 +0.6% · MA50 -3.5% · MA200 -4.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (510214 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
