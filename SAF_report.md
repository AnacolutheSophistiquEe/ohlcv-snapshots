# SAF

**Generated** : 2026-10-26T01:08:46.820923+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 1/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €271.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €271.80 (+3.8% vs entrée) · entrée €261.91 · stop €240.96 · T1 €266.86 · R/R 0.24  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -367 % hors [0,100] (R² max 0.63). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 271.8 · ATR Wilder 9.75 (3.59 %)_
- **Swing** : plage **260.04 → 253.05** (-4.33 % a -6.9 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 259.68-263.34 (A) ; 253.75-257.96 (A). stop INDICATIF 243.83 (-3.64 % sous le bas ; sous le support 248.71-252.29 (- 0,5 ATR)).
- **Deep** : plage **253.05 → 233.27** (-6.9 % a -14.18 % sous la cloture, 2.03 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 248.71-252.29 (A) ; 242.02-245.25 (B) ; 229.11-233.95 (B). stop INDICATIF 223.52 (-4.18 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 7.06 ATR sous le plus haut 20 s., RSI(2) 0.8. Limite **266.92** (seance suivante), stop catastrophe 227.91, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 265.22-268.29 (B, -1.29 %) ; 259.68-263.34 (A, -3.11 %) ; 253.75-257.96 (A, -5.09 %) ; 248.71-252.29 (A, -7.18 %) ; 242.02-245.25 (B, -9.77 %) ; 229.11-233.95 (B, -13.92 %)
- Resistances reelles au-dessus : 276.49-280.94 (A, 1.73 %) ; 283.02-287.1 (A, 4.13 %) ; 289.55-291.92 (A, 6.53 %) ; 295.38-297.85 (A, 8.68 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.70 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (10.91 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.91 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.397 % | p01 -2.434 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.2524** [0.2088 ; 0.3001] _(largeur 9.1 pt, n_eff 345.8)_
   - deep : **0.2491** [0.2057 ; 0.2966] _(largeur 9.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.26 %** | CVaR **-4.57 %** | vol 2.19 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.15 % contre 1.98 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.74 % vs -6.2 % si l'on extrapolait par √5 _(rapport 0.926 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3827** (β de hausse 1.3509, asymétrie 1.0235) vs FCHI — 620 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 256.9714 sur atr_based (1.5 ATR, 5.456 %) — p(stop avant cible) 0.2816 [0.24 ; 0.33], R/R 5.894, perte reelle 5.548 % (gap inclus), CVaR 5.976 %, EV 0.6122 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.456 %) — p(stop avant cible) 0.2816 [0.24 ; 0.33], R/R 5.894, perte reelle 5.548 % (gap inclus), EV 0.6122 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 0.25 ATR (stop 0.909 %) — p(stop avant cible) 0.8385 [0.80 ; 0.87], R/R 34.318, perte reelle 0.953 % (gap inclus), EV 0.1649 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 34.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.839, borne haute 0.874 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.819 %) — p(stop avant cible) 0.6951 [0.65 ; 0.74], R/R 17.289, perte reelle 1.892 % (gap inclus), EV 0.3164 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 17.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.695, borne haute 0.742 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 2.728 %) — p(stop avant cible) 0.5652 [0.51 ; 0.62], R/R 11.596, perte reelle 2.82 % (gap inclus), EV 0.4925 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.565, borne haute 0.617 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 3.637 %) — p(stop avant cible) 0.4397 [0.39 ; 0.49], R/R 8.775, perte reelle 3.727 % (gap inclus), EV 0.5432 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.25 ATR (stop 4.546 %) — p(stop avant cible) 0.3506 [0.30 ; 0.40], R/R 7.072, perte reelle 4.624 % (gap inclus), EV 0.5885 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 6.365 %) — p(stop avant cible) 0.2417 [0.20 ; 0.29], R/R 5.086, perte reelle 6.429 % (gap inclus), EV 0.552 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 7.274 %) — p(stop avant cible) 0.1631 [0.13 ; 0.20], R/R 4.434, perte reelle 7.375 % (gap inclus), EV 0.5621 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 8.184 %) — p(stop avant cible) 0.1219 [0.09 ; 0.16], R/R 3.917, perte reelle 8.349 % (gap inclus), EV 0.5086 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.5 ATR (stop 9.093 %) — p(stop avant cible) 0.0859 [0.06 ; 0.12], R/R 3.481, perte reelle 9.395 % (gap inclus), EV 0.49 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.75 ATR (stop 10.002 %) — p(stop avant cible) 0.0673 [0.04 ; 0.10], R/R 3.197, perte reelle 10.23 % (gap inclus), EV 0.4629 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 3.0 ATR (stop 10.911 %) — p(stop avant cible) 0.0553 [0.03 ; 0.08], R/R 2.907, perte reelle 11.25 % (gap inclus), EV 0.4513 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 12.73 %) — p(stop avant cible) 0.0352 [0.02 ; 0.06], R/R 2.425, perte reelle 13.483 % (gap inclus), EV 0.4312 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.16 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 14.549 %) — p(stop avant cible) 0.016 [0.01 ; 0.03], R/R 2.015, perte reelle 16.233 % (gap inclus), EV 0.4152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.49 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.367 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.679, perte reelle 19.477 % (gap inclus), EV 0.4366 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.186 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 1.625, perte reelle 20.126 % (gap inclus), EV 0.4396 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 20.004 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 1.574, perte reelle 20.779 % (gap inclus), EV 0.4456 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.0 ATR (stop 21.823 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.491, perte reelle 21.936 % (gap inclus), EV 0.4498 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.5 ATR (stop 23.641 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.383, perte reelle 23.641 % (gap inclus), EV 0.4597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 7.0 ATR (stop 25.46 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.284, perte reelle 25.46 % (gap inclus), EV 0.4665 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 7.5 ATR (stop 27.278 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.199, perte reelle 27.278 % (gap inclus), EV 0.4665 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 8.0 ATR (stop 29.097 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.124, perte reelle 29.097 % (gap inclus), EV 0.4665 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 271.8, ATR14 9.8857 (3.637 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 1.262 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.182 % | 271.3057 | 89.41 % | 92.64 % | 93.81 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.364 % | 270.8114 | 81.76 % | 87.44 % | 89.39 % | 91.54 % | 93.57 % | 95.0 % |
| 0.15 ATR | 0.546 % | 270.3171 | 75.59 % | 83.81 % | 86.64 % | 89.07 % | 91.59 % | 93.11 % |
| 0.2 ATR | 0.727 % | 269.8228 | 68.63 % | 78.61 % | 83.1 % | 85.73 % | 89.22 % | 91.41 % |
| 0.25 ATR | 0.909 % | 269.3286 | 61.47 % | 73.99 % | 79.37 % | 83.66 % | 87.93 % | 90.51 % |
| 0.35 ATR | 1.273 % | 268.34 | 49.61 % | 63.79 % | 70.24 % | 77.46 % | 83.09 % | 87.61 % |
| 0.5 ATR | 1.819 % | 266.8571 | 35.29 % | 52.11 % | 59.33 % | 68.9 % | 76.36 % | 82.12 % |
| 0.75 ATR | 2.728 % | 264.3857 | 20.78 % | 35.82 % | 43.12 % | 53.64 % | 63.8 % | 71.83 % |
| 1.0 ATR | 3.637 % | 261.9143 | 10.1 % | 24.34 % | 33.1 % | 43.01 % | 54.8 % | 63.14 % |
| 1.25 ATR | 4.546 % | 259.4428 | 4.41 % | 15.6 % | 24.17 % | 33.56 % | 47.28 % | 56.34 % |
| 1.5 ATR | 5.456 % | 256.9714 | 2.25 % | 10.21 % | 16.7 % | 25.3 % | 38.87 % | 48.35 % |
| 2.0 ATR | 7.274 % | 252.0286 | 0.98 % | 4.51 % | 7.66 % | 15.75 % | 27.7 % | 38.46 % |
| 2.5 ATR | 9.093 % | 247.0857 | 0.2 % | 1.47 % | 3.73 % | 8.86 % | 18.99 % | 29.37 % |
| 3.0 ATR | 10.911 % | 242.1428 | 0.0 % | 0.88 % | 2.16 % | 5.81 % | 12.66 % | 22.88 % |
| 4.0 ATR | 14.549 % | 232.2571 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.99 % |
| 6.0 ATR | 21.823 % | 212.4857 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.61 ATR | 0.81 ATR | 0.99 ATR | 1.12 ATR | 1.52 ATR | 1.96 ATR |
| **3 s.** | 0.30 ATR | 0.64 ATR | 0.72 ATR | 1.00 ATR | 1.23 ATR | 1.39 ATR | 1.87 ATR | 2.34 ATR |
| **5 s.** | 0.39 ATR | 0.84 ATR | 0.95 ATR | 1.27 ATR | 1.52 ATR | 1.78 ATR | 2.42 ATR | 3.17 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.32 ATR | 1.76 ATR | 2.15 ATR | 2.44 ATR | 3.33 ATR | 3.94 ATR |
| **20 s.** | 0.67 ATR | 1.45 ATR | 1.67 ATR | 2.30 ATR | 2.84 ATR | 3.24 ATR | 4.25 ATR | 5.50 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.609–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.728 %, prix 264.3853), p(touche) 35.82 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.721–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.728 %, prix 264.3853), p(touche) 43.12 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.953–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.637 %, prix 261.9146), p(touche) 43.01 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.318–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.456 %, prix 256.9706), p(touche) 38.87 % (en stress 99.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.669–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.274 %, prix 252.0293), p(touche) 38.46 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 24.1 | bear 12.0 | side 63.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 15.3  _(survente)_
- **ADX** : 30.3  _(tendance etablie)_
- **MACD** : hist -3.252  _(pas de croisement recent)_
- **BB** : %B -0.32 · largeur 17.8%
- **ATR** : 9.89 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.261  _(distribution)_
- **Vol ratio** : 2.71  _(volume au-dessus de la moyenne)_
- **Choppiness** : 28.6  _(marche directionnel)_
- **MA** : MA20 318.06 · MA50 328.63 · MA200 315.9  _(prix < MA20)_
- **Dist MA** : MA20 -14.5% · MA50 -17.3% · MA200 -14.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (773655 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
