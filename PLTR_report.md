# PLTR

**Generated** : 2026-11-23T01:24:47.436928+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · $143.49  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $143.49 (+2.5% vs entrée) · entrée $139.99 · stop $136.49 · T1 $144.91 · R/R 1.41  
> ↳ ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -59 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-20 : 143.49 · ATR Wilder 9.13 (6.36 %)_
- **Swing** : plage **132.71 → 124.63** (-7.51 % a -13.14 % sous la cloture, 0.89 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 128.32-132.41 (B). stop INDICATIF 113.32 (-9.07 % sous le bas ; sous le support 117.89-119.41 (- 0,5 ATR)).
- **Deep** : plage **124.63 → 105.81** (-13.14 % a -26.26 % sous la cloture, 2.06 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 117.89-119.41 (A) ; 105.32-106.37 (B). stop INDICATIF 93.6 (-11.54 % sous le bas ; sous le support 98.17-98.99 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.39 ATR sous le plus haut 20 s., RSI(2) 0.6. Limite **138.92** (seance suivante), stop catastrophe 102.4, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 133.49-136.88 (B, -4.61 %) ; 128.32-132.41 (B, -7.72 %) ; 117.89-119.41 (A, -16.78 %) ; 105.32-106.37 (B, -25.87 %) ; 98.17-98.99 (C, -31.01 %) ; 84.8-89.31 (A, -37.76 %)
- Resistances reelles au-dessus : 149.64-152.68 (A, 4.29 %) ; 155.68-156.75 (A, 8.5 %) ; 160.39-164.55 (A, 11.78 %) ; 165.08-169.42 (A, 15.04 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.22 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1254).
   - exécution **2.452 pt plus bas** dans le cas TYPIQUE (médiane), 5.06 au p90, **5.712 au pire**
   - perte réelle **15.126 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 12.22 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.007 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.903 % | p01 -6.138 % | pire -17.932 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3123** [0.2468 ; 0.384] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.2807** [0.2353 ; 0.3297] _(largeur 9.4 pt, n_eff 345.7)_
   - deep : **0.2564** [0.2125 ; 0.3043] _(largeur 9.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.5 pt), swing (38.2 pt), deep (41.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.12 %** | CVaR **-8.46 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.4 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.97 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7241** (β de hausse 1.421, asymétrie 1.2134) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 131.2012 sur atr_grid (1.25 ATR, 8.564 %) — p(stop avant cible) 0.3538 [0.30 ; 0.41], R/R 3.507, perte reelle 8.791 % (gap inclus), CVaR 10.171 %, EV 1.0699 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.7307 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.277 %) — p(stop avant cible) 0.3067 [0.26 ; 0.36], R/R 2.835, perte reelle 10.875 % (gap inclus), EV 0.681 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.83 % > budget 12.00 %
   - ⚪ sr_based a 1.52 ATR (stop 12.882 %) — p(stop avant cible) 0.2031 [0.16 ; 0.25], R/R 2.301, perte reelle 13.395 % (gap inclus), EV 0.9208 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.94 % > budget 12.00 %
   - 🟢 support a 2.6 ATR (stop 20.28 %) — p(stop avant cible) 0.071 [0.05 ; 0.10], R/R 1.513, perte reelle 20.37 % (gap inclus), EV 1.013 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.41 % > budget 12.00 %
   - 🟢 support a 3.78 ATR (stop 28.309 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.045, perte reelle 29.514 % (gap inclus), EV 1.3664 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.59 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.713 %) — p(stop avant cible) 0.8537 [0.81 ; 0.89], R/R 17.308, perte reelle 1.781 % (gap inclus), EV 0.1685 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 17.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.854, borne haute 0.888 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.426 %) — p(stop avant cible) 0.6959 [0.65 ; 0.74], R/R 8.783, perte reelle 3.51 % (gap inclus), EV 0.499 % — **REFUSE**
      - refuse : cible atteinte seulement 1.9 % du temps (< 15 %) meme a 10 seances : le R/R de 8.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.696, borne haute 0.743 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 5.139 %) — p(stop avant cible) 0.5643 [0.51 ; 0.62], R/R 5.867, perte reelle 5.254 % (gap inclus), EV 0.6423 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.564, borne haute 0.616 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 6.851 %) — p(stop avant cible) 0.4513 [0.40 ; 0.50], R/R 4.44, perte reelle 6.943 % (gap inclus), EV 1.2363 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.25 ATR (stop 8.564 %) — p(stop avant cible) 0.3538 [0.30 ; 0.41], R/R 3.507, perte reelle 8.791 % (gap inclus), EV 1.0699 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 15.416 %) — p(stop avant cible) 0.1417 [0.11 ; 0.18], R/R 1.974, perte reelle 15.614 % (gap inclus), EV 0.9494 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.98 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 23.98 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 1.258, perte reelle 24.513 % (gap inclus), EV 1.3393 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.78 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 30.831 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.97, perte reelle 31.768 % (gap inclus), EV 1.3602 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.71 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 34.257 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.886, perte reelle 34.808 % (gap inclus), EV 1.373 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.47 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 37.683 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.818, perte reelle 37.699 % (gap inclus), EV 1.3738 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.41 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 41.108 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.75, perte reelle 41.108 % (gap inclus), EV 1.376 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 44.534 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.692, perte reelle 44.534 % (gap inclus), EV 1.376 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 47.96 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.643, perte reelle 47.96 % (gap inclus), EV 1.376 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 51.385 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.6, perte reelle 51.385 % (gap inclus), EV 1.376 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 54.811 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.562, perte reelle 54.811 % (gap inclus), EV 1.376 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 143.49, ATR14 9.8311 (6.851 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.364 ATR = 2.494 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.343 % | 142.9985 | 92.76 % | 95.37 % | 96.17 % | 96.97 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.685 % | 142.5069 | 85.01 % | 89.63 % | 91.43 % | 93.64 % | 95.23 % | 96.41 % |
| 0.15 ATR | 1.028 % | 142.0153 | 76.96 % | 83.79 % | 85.99 % | 89.8 % | 92.59 % | 94.26 % |
| 0.2 ATR | 1.37 % | 141.5238 | 69.22 % | 78.55 % | 81.85 % | 86.46 % | 90.36 % | 92.41 % |
| 0.25 ATR | 1.713 % | 141.0322 | 62.37 % | 73.82 % | 77.72 % | 82.83 % | 87.72 % | 90.77 % |
| 0.35 ATR | 2.398 % | 140.0491 | 51.41 % | 65.86 % | 71.27 % | 78.08 % | 83.76 % | 87.49 % |
| 0.5 ATR | 3.426 % | 138.5745 | 36.62 % | 53.07 % | 59.98 % | 69.09 % | 77.66 % | 82.67 % |
| 0.75 ATR | 5.139 % | 136.1167 | 19.62 % | 35.25 % | 44.86 % | 55.56 % | 66.8 % | 75.18 % |
| 1.0 ATR | 6.851 % | 133.6589 | 8.95 % | 23.16 % | 32.86 % | 44.04 % | 56.55 % | 65.95 % |
| 1.25 ATR | 8.564 % | 131.2012 | 4.53 % | 15.61 % | 23.29 % | 34.24 % | 46.5 % | 57.13 % |
| 1.5 ATR | 10.277 % | 128.7434 | 2.01 % | 10.57 % | 17.44 % | 26.87 % | 40.1 % | 52.41 % |
| 2.0 ATR | 13.703 % | 123.8279 | 0.7 % | 4.03 % | 9.48 % | 15.96 % | 29.24 % | 39.38 % |
| 2.5 ATR | 17.128 % | 118.9123 | 0.1 % | 1.41 % | 3.43 % | 9.49 % | 19.7 % | 29.54 % |
| 3.0 ATR | 20.554 % | 113.9968 | 0.0 % | 0.6 % | 1.71 % | 5.25 % | 13.4 % | 22.77 % |
| 4.0 ATR | 27.406 % | 104.1657 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 5.28 % | 12.92 % |
| 6.0 ATR | 41.108 % | 84.5036 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 4.21 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.93 ATR |
| **3 s.** | 0.29 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.21 ATR | 1.39 ATR | 1.97 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.29 ATR | 1.59 ATR | 1.81 ATR | 2.46 ATR | 3.07 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.31 ATR | 1.83 ATR | 2.22 ATR | 2.48 ATR | 3.42 ATR | 4.12 ATR |
| **20 s.** | 0.76 ATR | 1.59 ATR | 1.78 ATR | 2.32 ATR | 2.83 ATR | 3.28 ATR | 4.67 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.415–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.426 %, prix 138.574), p(touche) 36.62 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.139 %, prix 136.1161), p(touche) 35.25 % (en stress 93.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.139 %, prix 136.1161), p(touche) 44.86 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.979–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.851 %, prix 133.6595), p(touche) 44.04 % (en stress 100.0 %)  ✅ optimum identifie (85.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.309–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.277 %, prix 128.7435), p(touche) 40.1 % (en stress 100.0 %)  ✅ optimum identifie (86.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.784–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.128 %, prix 118.913), p(touche) 29.54 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.026 | EV/share : $0.092 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 — | T3 —
- Kelly (position) : f* 0.082 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 85.0 | side 10.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.441% → cible +3.511% / stop −2.5%, p_fill 24%, n_eff≈28.2) : P(cible|rempli) **5%** · **EV/risk -0.031** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −5.369% → cible +8.094% / stop −7.24%, p_fill 19%, n_eff≈23.0) : P(cible|rempli) **19%** · **EV/risk +0.021** (×p_fill ; si rempli +0.80% du capital)
  - **deep** (entrée dip −8.293% → cible +11.813% / stop −11.207%, p_fill 15%, n_eff≈18.5) : P(cible|rempli) **16%** · **EV/risk -0.002** (×p_fill ; si rempli -0.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→43% · +3.0%→24% · +5.0%→9% · +8.0%→2%
- Range intraday médian 3.72% (p90 6.77%) · excursion haute méd. +1.85% / basse méd. −1.63%
- Profil de vol intra : ouverture 2.877% vs midi 0.713% vs clôture 0.813% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑2%/↓0% ; spike-down 56% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. 0.287% ; recovery-V 42%
- **σ réalisé intraday** 2.426% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 45% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 195.972 (VA 195.3–196.476 ; dernier close 196.73)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 70% · **stop −3.36%** sous le fill (sous le bruit) · cible +1.83% · R/R 0.54 (high win-rate)
- Gaps overnight (n=156) : méd. -0.05% · baisse 50% (gap-down >1% 24% · >2% 6%)
- Excursion ouverture 5min (n=157) : bas méd −0.81% (p90 −1.82%) · haut méd +0.75% · range méd 1.63%
- Excursion ouverture 15min (n=157) : bas méd −0.99% (p90 −2.38%) · haut méd +1.1% · range méd 2.22%
- Excursion ouverture 30min (n=157) : bas méd −1.08% (p90 −2.85%) · haut méd +1.2% · range méd 2.5%
- Excursion ouverture 60min (n=157) : bas méd −1.29% (p90 −2.98%) · haut méd +1.3% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 196.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (116/156) · gap 36% · délai 0.0min · rebond 62% (70/116) (MFE +1.34%)
   - −1.0% : fill 30min 54% · séance 63% (102/156) · gap 24% · délai 0.1min · rebond 68% (65/102) (MFE +1.5%)
   - −1.5% : fill 30min 40% · séance 48% (82/156) · gap 15% · délai 1.5min · rebond 65% (54/82) (MFE +1.59%)
   - −2.0% : fill 30min 35% · séance 44% (74/156) · gap 6% · délai 4.6min · rebond 70% (50/74) (MFE +1.83%)
   - −3.0% : fill 30min 15% · séance 24% (46/156) · gap 2% · délai 9.3min · rebond 53% (24/46) (MFE +1.28%)
   - −4.0% : fill 30min 9% · séance 16% (30/156) · gap 1% · délai 25.1min · rebond 47% (15/30) (MFE +0.95%)
   - −5.0% : fill 30min 3% · séance 9% (19/156) · gap 0% · délai 79.0min · rebond 40% (11/19) (MFE +0.88%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.89%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.79% (p90 −1.93%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.63%) → stop au-delà de −1.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=483 jambes) : jambe baissière méd −1.06% (p90 −2.37%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 94% (70/75) · rebond 66% (45/70)
      · −2.0% : fill 74% (56/75) · rebond 74% (38/56)
      · −3.0% : fill 42% (36/75) · rebond 48% (18/36)
      · −4.0% : fill 28% (24/75) · rebond 55% (13/24)
      · −5.0% : fill 14% (16/75) · rebond 56% (11/16)
   - **flat** (21 séances) :
      · −1.0% : fill 81% (17/21) · rebond 66% (9/17)
      · −2.0% : fill 38% (11/21) · rebond 64% (8/11)
      · −3.0% : fill 20% (7/21) · rebond 59% (4/7)
      · −4.0% : fill 12% (4/21) · rebond 42% (2/4)
      · −5.0% : fill 5% (1/21) · rebond 0% (0/1)
   - **gap-up** (60 séances) :
      · −1.0% : fill 26% (15/60) · rebond 75% (11/15)
      · −2.0% : fill 13% (7/60) · rebond 45% (4/7)
      · −3.0% : fill 6% (3/60) · rebond 93% (2/3)
      · −4.0% : fill 4% (2/60) · rebond 0% (0/2)
      · −5.0% : fill 4% (2/60) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 54% en base · 65% si les 15 1res min sont vertes (87 cas) · 39% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=157) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 87% si début vert vs 18% si rouge (base 54% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **87%** · continue >prix actuel 54% ; creux résiduel méd -0.66% (q20 -1.49%) → **SL/trailing à −1.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +1.8% → **scale +1.07% / runner +1.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **18%** (continue à baisser 50%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +0.89% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.95% .. +3.37%] · haut q95 +3.8% · bas q05 -3.55%
   - 60min (n=157) : retour [-3.01% .. +3.84%] · haut q95 +4.11% · bas q05 -3.64%
   - 2h (n=157) : retour [-3.68% .. +4.68%] · haut q95 +4.75% · bas q05 -4.46%
   - 4h (n=157) : retour [-4.01% .. +4.66%] · haut q95 +5.39% · bas q05 -5.0%
   - 6h (n=157) : retour [-3.97% .. +4.83%] · haut q95 +5.39% · bas q05 -5.37%
   - session (n=157) : retour [-3.98% .. +5.0%] · haut q95 +5.58% · bas q05 -5.37%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.4% des séances sont trend-up (mild 1.9% / strong 4.5%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.99% (p75 1.44% / p90 1.62%) · ~2.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 40.57 min, n=23)
   - −1.0% → **62%** (reprise méd 61.25 min, n=10)
   - −1.5% → **58%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.62%** (p90, défaut prudent ; serré/agressif −1.44%) ; extension open→close méd +4.56% (q75 +6.33% / q95 +11.7%), MFE méd +5.12% / q90 +9.42%
   - Échelle scale-out : +5.12% (33%) / +6.79% (33%) / +9.42% (34%)
- **DÉSARMER** : repli > **−1.62%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.42% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 74% du temps (retour médian dernière heure +0.89%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.74 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.3  _(survente)_
- **ADX** : 30.1  _(tendance etablie)_
- **MACD** : hist -2.485  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 38.0%
- **ATR** : 9.83 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.1  _(distribution)_
- **Vol ratio** : 1.46  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 171.82 · MA50 183.26 · MA200 153.97  _(prix < MA20)_
- **Dist MA** : MA20 -16.5% · MA50 -21.7% · MA200 -6.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (683334 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
