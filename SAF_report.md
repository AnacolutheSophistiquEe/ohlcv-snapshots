# SAF

**Generated** : 2026-11-19T01:08:55.655446+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €305.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot €305.10 (+0.5% vs entrée) · entrée €303.46 · stop €287.89 · T1 €334.59 · R/R 2.0  
> ↳ ¼-Kelly 0.033 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 162 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-18 : 305.1 · ATR Wilder 9.31 (3.05 %)_
- **Swing** : plage **293.81 → 286.82** (-3.7 % a -5.99 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 289.55-291.92 (B) ; 283.02-287.1 (B). stop INDICATIF 271.84 (-5.22 % sous le bas ; sous le support 276.49-280.94 (- 0,5 ATR)).
- **Deep** : plage **286.82 → 265.62** (-5.99 % a -12.94 % sous la cloture, 2.28 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 283.02-287.1 (B) ; 276.49-280.94 (B) ; 269.9-273.87 (A) ; 265.22-268.29 (B). stop INDICATIF 255.03 (-3.99 % sous le bas ; sous le support 259.68-263.34 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.45 ATR sous le plus haut 20 s., RSI(2) 22.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 295.38-297.85 (B, -2.38 %) ; 289.55-291.92 (B, -4.32 %) ; 283.02-287.1 (B, -5.9 %) ; 276.49-280.94 (B, -7.92 %) ; 269.9-273.87 (A, -10.24 %) ; 265.22-268.29 (B, -12.07 %)
- Resistances reelles au-dessus : 312.29-316.9 (A, 2.36 %) ; 317.14-320.7 (A, 3.95 %) ; 322.1-326.14 (A, 5.57 %) ; 326.8-329.2 (B, 7.11 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.70 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (5.64 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **4.346 pt plus bas** dans le cas TYPIQUE (médiane), 4.346 au p90, **4.346 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 5.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0034 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.405 % | p01 -2.434 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.1676** [0.1311 ; 0.2097] _(largeur 7.9 pt, n_eff 345.8)_
   - deep : **0.3153** [0.268 ; 0.3657] _(largeur 9.8 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 85.7 observations effectives », dont la borne haute a 95 % vaut environ 3.5 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-2.89 %** | CVaR **-4.34 %** | vol 1.84 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 1.04 % contre 1.94 % aujourd'hui, rapport 0.53)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.8 % vs -6.2 % si l'on extrapolait par √5 _(rapport 0.935 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3762** (β de hausse 1.3517, asymétrie 1.0181) vs FCHI — 623 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 290.1643 sur atr_based (1.5 ATR, 4.895 %) — p(stop avant cible) 0.3384 [0.29 ; 0.39], R/R 3.309, perte reelle 5.126 % (gap inclus), CVaR 6.275 %, EV 0.8068 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9307 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.13 ATR (stop 2.227 %) — p(stop avant cible) 0.6379 [0.59 ; 0.69], R/R 7.313, perte reelle 2.32 % (gap inclus), EV 0.7196 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.638, borne haute 0.687 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_based a 1.5 ATR (stop 4.895 %) — p(stop avant cible) 0.3384 [0.29 ; 0.39], R/R 3.309, perte reelle 5.126 % (gap inclus), EV 0.8068 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 3.74 ATR (stop 14.008 %) — p(stop avant cible) 0.0384 [0.02 ; 0.06], R/R 1.162, perte reelle 14.605 % (gap inclus), EV 0.3491 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.22 % > budget 12.00 %
   - 🔴 support a 4.56 ATR (stop 16.704 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 0.867, perte reelle 19.571 % (gap inclus), EV 0.4004 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.72 % > budget 12.00 %
      - ⚠ support DETECTE a 0.03 ATR du spot — compartiment <1, mesure a 47.7 % de casse (IC clusterise [0.446 ; 0.509] sur 1169 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ grid_snapped a 0.13 ATR (stop 1.388 %) — p(stop avant cible) 0.7435 [0.70 ; 0.79], R/R 11.64, perte reelle 1.457 % (gap inclus), EV 0.5428 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.744, borne haute 0.787 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 3.264 %) — p(stop avant cible) 0.5022 [0.45 ; 0.55], R/R 5.07, perte reelle 3.346 % (gap inclus), EV 0.8069 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.502, borne haute 0.555 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 4.079 %) — p(stop avant cible) 0.4034 [0.35 ; 0.46], R/R 3.93, perte reelle 4.316 % (gap inclus), EV 0.7891 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 5.711 %) — p(stop avant cible) 0.2977 [0.25 ; 0.35], R/R 2.849, perte reelle 5.955 % (gap inclus), EV 0.7204 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.527 %) — p(stop avant cible) 0.2453 [0.20 ; 0.29], R/R 2.544, perte reelle 6.668 % (gap inclus), EV 0.6743 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 7.343 %) — p(stop avant cible) 0.2006 [0.16 ; 0.25], R/R 2.274, perte reelle 7.461 % (gap inclus), EV 0.6232 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 8.159 %) — p(stop avant cible) 0.1601 [0.12 ; 0.20], R/R 2.054, perte reelle 8.257 % (gap inclus), EV 0.6096 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.975 %) — p(stop avant cible) 0.1328 [0.10 ; 0.17], R/R 1.853, perte reelle 9.155 % (gap inclus), EV 0.5492 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.791 %) — p(stop avant cible) 0.1111 [0.08 ; 0.15], R/R 1.707, perte reelle 9.941 % (gap inclus), EV 0.4891 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.74 ATR (stop 13.169 %) — p(stop avant cible) 0.0673 [0.04 ; 0.10], R/R 1.258, perte reelle 13.484 % (gap inclus), EV 0.334 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.59 % > budget 12.00 %
   - 🔴 grid_snapped a 4.56 ATR (stop 15.865 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.927, perte reelle 18.308 % (gap inclus), EV 0.3911 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.88 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.95 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.844, perte reelle 20.099 % (gap inclus), EV 0.4032 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.68 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.581 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.822, perte reelle 20.64 % (gap inclus), EV 0.4084 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.63 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 21.213 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.789, perte reelle 21.5 % (gap inclus), EV 0.4074 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 22.845 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.743, perte reelle 22.845 % (gap inclus), EV 0.4143 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.477 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.693, perte reelle 24.477 % (gap inclus), EV 0.4236 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.34 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 26.109 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.65, perte reelle 26.109 % (gap inclus), EV 0.427 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.26 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 305.1, ATR14 9.9571 (3.264 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 1.129 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.163 % | 304.6021 | 89.31 % | 92.64 % | 93.71 % | 95.57 % | 96.24 % | 97.1 % |
| 0.1 ATR | 0.326 % | 304.1043 | 81.67 % | 87.44 % | 89.29 % | 91.44 % | 93.47 % | 95.0 % |
| 0.15 ATR | 0.49 % | 303.6064 | 75.49 % | 83.91 % | 86.64 % | 89.07 % | 91.59 % | 93.21 % |
| 0.2 ATR | 0.653 % | 303.1086 | 68.24 % | 78.41 % | 82.81 % | 85.43 % | 88.92 % | 91.51 % |
| 0.25 ATR | 0.816 % | 302.6107 | 61.08 % | 73.6 % | 78.98 % | 83.27 % | 87.54 % | 90.61 % |
| 0.35 ATR | 1.142 % | 301.615 | 49.51 % | 63.59 % | 70.04 % | 77.17 % | 82.79 % | 87.81 % |
| 0.5 ATR | 1.632 % | 300.1214 | 35.29 % | 52.21 % | 59.43 % | 69.0 % | 76.36 % | 82.52 % |
| 0.75 ATR | 2.448 % | 297.6321 | 20.69 % | 35.43 % | 42.93 % | 53.54 % | 63.7 % | 72.43 % |
| 1.0 ATR | 3.264 % | 295.1429 | 10.1 % | 24.14 % | 32.91 % | 42.91 % | 55.0 % | 64.04 % |
| 1.25 ATR | 4.079 % | 292.6536 | 4.51 % | 15.7 % | 24.26 % | 33.66 % | 47.48 % | 57.34 % |
| 1.5 ATR | 4.895 % | 290.1643 | 2.35 % | 10.4 % | 16.9 % | 25.49 % | 39.27 % | 49.55 % |
| 2.0 ATR | 6.527 % | 285.1857 | 1.08 % | 4.71 % | 7.96 % | 16.24 % | 28.68 % | 40.26 % |
| 2.5 ATR | 8.159 % | 280.2071 | 0.2 % | 1.57 % | 3.93 % | 9.25 % | 19.88 % | 31.17 % |
| 3.0 ATR | 9.791 % | 275.2286 | 0.0 % | 0.98 % | 2.36 % | 6.2 % | 13.55 % | 24.68 % |
| 4.0 ATR | 13.054 % | 265.2714 | 0.0 % | 0.29 % | 0.79 % | 1.48 % | 5.44 % | 12.79 % |
| 6.0 ATR | 19.581 % | 245.3571 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.19 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.23 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.61 ATR | 0.80 ATR | 0.98 ATR | 1.12 ATR | 1.53 ATR | 1.98 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 1.00 ATR | 1.23 ATR | 1.40 ATR | 1.89 ATR | 2.37 ATR |
| **5 s.** | 0.39 ATR | 0.83 ATR | 0.95 ATR | 1.27 ATR | 1.53 ATR | 1.80 ATR | 2.45 ATR | 3.25 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.33 ATR | 1.80 ATR | 2.21 ATR | 2.49 ATR | 3.44 ATR | 4.21 ATR |
| **20 s.** | 0.69 ATR | 1.49 ATR | 1.75 ATR | 2.40 ATR | 2.98 ATR | 3.39 ATR | 4.63 ATR | 5.75 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.398 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.607–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.448 %, prix 297.6312), p(touche) 35.43 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.719–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.448 %, prix 297.6312), p(touche) 42.93 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.951–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.264 %, prix 295.1415), p(touche) 42.91 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.326–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.895 %, prix 290.1654), p(touche) 39.27 % (en stress 99.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.745–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.527 %, prix 285.1861), p(touche) 40.26 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.064 | EV/share : €0.990 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 8 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.131 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 76.9 | bear 7.1 | side 16.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.326% → cible +1.637% / stop −8.0%, p_fill 82%, n_eff≈85.7) : P(cible|rempli) **20%** · **EV/risk -0.033** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −0.538% → cible +10.259% / stop −5.129%, p_fill 84%, n_eff≈96.3) : P(cible|rempli) **2%** · **EV/risk -0.029** (×p_fill ; si rempli -0.18% du capital)
  - **deep** (entrée dip −0.698% → cible +10.437% / stop −5.218%, p_fill 83%, n_eff≈91.7) : P(cible|rempli) **11%** · **EV/risk +0.011** (×p_fill ; si rempli +0.07% du capital)
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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.0  _(surachat)_
- **ADX** : 22.7  _(pas de tendance nette)_
- **MACD** : hist 2.844  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 20.6%
- **ATR** : 9.96 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.103  _(distribution)_
- **Vol ratio** : 0.2  _(volume atone)_
- **Choppiness** : 41.6  _(transition)_
- **MA** : MA20 293.96 · MA50 312.26 · MA200 314.94  _(prix > MA20)_
- **Dist MA** : MA20 +3.8% · MA50 -2.3% · MA200 -3.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (687306 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
