# PLTR

**Generated** : 2026-11-13T01:23:49.541278+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · $171.56  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 40/125 fenêtres (p_fill pondéré 30 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $171.56 (+2.2% vs entrée) · entrée $167.89 · stop $163.70 · T1 $172.64 · R/R 1.13  
> ↳ ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 171.56 · ATR Wilder 8.93 (5.21 %)_
- **Swing** : plage **160.97 → 153.15** (-6.17 % a -10.73 % sous la cloture, 0.88 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 160.39-164.55 (B) ; 155.68-156.75 (B). stop INDICATIF 145.17 (-5.21 % sous le bas ; sous le support 149.64-152.68 (- 0,5 ATR)).
- **Deep** : plage **153.15 → 135.7** (-10.73 % a -20.9 % sous la cloture, 1.95 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 149.64-152.68 (A) ; 144.86-149.09 (B) ; 122.64-143.28 (A) ; 138.9-142.34 (B) ; 133.49-136.88 (B). stop INDICATIF 123.85 (-8.73 % sous le bas ; sous le support 128.32-132.41 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.58 ATR sous le plus haut 20 s., RSI(2) 67.1 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 160.39-164.55 (B, -4.09 %) ; 155.68-156.75 (B, -8.63 %) ; 149.64-152.68 (A, -11.0 %) ; 144.86-149.09 (B, -13.1 %) ; 122.64-143.28 (A, -16.48 %) ; 138.9-142.34 (B, -17.03 %)
- Resistances reelles au-dessus : 174.29-176.5 (A, 1.59 %) ; 180.18-184.45 (A, 5.02 %) ; 184.81-188.37 (A, 7.72 %) ; 190.0-190.39 (B, 10.75 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.23 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **2.543 pt plus bas** dans le cas TYPIQUE (médiane), 6.398 au p90, **7.702 au pire**
   - perte réelle **13.763 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 10.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0141 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.904 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2796** [0.2168 ; 0.3497] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.36** [0.3107 ; 0.4116] _(largeur 10.1 pt, n_eff 345.7)_
   - deep : **0.3298** [0.2818 ; 0.3806] _(largeur 9.9 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.7 pt), swing (35.0 pt), deep (39.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.46 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.77 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7101** (β de hausse 1.4228, asymétrie 1.2019) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.793× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 162.0733 sur atr_grid (1.0 ATR, 5.53 %) — p(stop avant cible) 0.5261 [0.47 ; 0.58], R/R 2.477, perte reelle 5.588 % (gap inclus), CVaR 6.141 %, EV 0.7292 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2257 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.526, borne haute 0.578 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.295 %) — p(stop avant cible) 0.3613 [0.31 ; 0.41], R/R 1.643, perte reelle 8.427 % (gap inclus), EV 0.9431 % — **REFUSE**
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 1.65 ATR (stop 11.791 %) — p(stop avant cible) 0.2296 [0.19 ; 0.28], R/R 1.116, perte reelle 12.403 % (gap inclus), EV 0.6688 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.50 % > budget 12.00 %
   - ⚪ swing_based a 2.2 ATR (stop 14.845 %) — p(stop avant cible) 0.1479 [0.11 ; 0.19], R/R 0.915, perte reelle 15.129 % (gap inclus), EV 0.6963 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.69 % > budget 12.00 %
   - 🟢 support a 2.53 ATR (stop 16.677 %) — p(stop avant cible) 0.1183 [0.09 ; 0.16], R/R 0.822, perte reelle 16.838 % (gap inclus), EV 0.7356 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.06 % > budget 12.00 %
   - 🟢 support a 5.66 ATR (stop 33.971 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.399, perte reelle 34.659 % (gap inclus), EV 1.1422 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.60 % > budget 12.00 %
   - 🟢 support a 6.87 ATR (stop 40.686 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.34, perte reelle 40.686 % (gap inclus), EV 1.1477 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.53 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.382 %) — p(stop avant cible) 0.8713 [0.83 ; 0.90], R/R 9.795, perte reelle 1.413 % (gap inclus), EV 0.2251 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.871, borne haute 0.903 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.765 %) — p(stop avant cible) 0.738 [0.69 ; 0.78], R/R 4.866, perte reelle 2.845 % (gap inclus), EV 0.5397 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.738, borne haute 0.782 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.147 %) — p(stop avant cible) 0.6314 [0.58 ; 0.68], R/R 3.275, perte reelle 4.227 % (gap inclus), EV 0.4752 % — **REFUSE**
      - refuse : p_stop_first 0.631, borne haute 0.681 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.53 %) — p(stop avant cible) 0.5261 [0.47 ; 0.58], R/R 2.477, perte reelle 5.588 % (gap inclus), EV 0.7292 % — **REFUSE**
      - refuse : p_stop_first 0.526, borne haute 0.578 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 6.912 %) — p(stop avant cible) 0.4342 [0.38 ; 0.49], R/R 1.987, perte reelle 6.968 % (gap inclus), EV 1.0718 % — **REFUSE**
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 1.65 ATR (stop 10.763 %) — p(stop avant cible) 0.2898 [0.24 ; 0.34], R/R 1.222, perte reelle 11.328 % (gap inclus), EV 0.4114 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.86 % > budget 12.00 %
   - ⚪ grid_snapped a 2.2 ATR (stop 13.816 %) — p(stop avant cible) 0.1692 [0.13 ; 0.21], R/R 0.971, perte reelle 14.257 % (gap inclus), EV 0.6822 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.31 % > budget 12.00 %
   - 🟢 grid_snapped a 2.53 ATR (stop 15.648 %) — p(stop avant cible) 0.1347 [0.10 ; 0.17], R/R 0.874, perte reelle 15.836 % (gap inclus), EV 0.7393 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.15 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.354 %) — p(stop avant cible) 0.0735 [0.05 ; 0.10], R/R 0.713, perte reelle 19.425 % (gap inclus), EV 0.8444 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.46 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.119 %) — p(stop avant cible) 0.0455 [0.03 ; 0.07], R/R 0.621, perte reelle 22.283 % (gap inclus), EV 0.8779 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.13 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.884 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.549, perte reelle 25.238 % (gap inclus), EV 1.1133 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.82 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.648 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.479, perte reelle 28.908 % (gap inclus), EV 1.1381 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.71 % > budget 12.00 %
   - 🟢 grid_snapped a 5.66 ATR (stop 32.942 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.407, perte reelle 34.037 % (gap inclus), EV 1.1429 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.65 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.943 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.385, perte reelle 35.958 % (gap inclus), EV 1.1434 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.58 % > budget 12.00 %
   - 🟢 grid_snapped a 6.87 ATR (stop 39.657 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.348, perte reelle 39.74 % (gap inclus), EV 1.1481 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.473 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.334, perte reelle 41.473 % (gap inclus), EV 1.1475 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.53 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.237 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.313, perte reelle 44.237 % (gap inclus), EV 1.1475 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.53 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 171.56, ATR14 9.4867 (5.53 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.36 ATR = 1.991 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.276 % | 171.0857 | 92.75 % | 95.36 % | 96.17 % | 97.07 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.553 % | 170.6113 | 84.89 % | 89.52 % | 91.42 % | 93.73 % | 95.22 % | 96.41 % |
| 0.15 ATR | 0.829 % | 170.137 | 76.84 % | 83.67 % | 85.97 % | 89.99 % | 92.58 % | 94.25 % |
| 0.2 ATR | 1.106 % | 169.6627 | 68.98 % | 78.43 % | 81.84 % | 86.65 % | 90.35 % | 92.4 % |
| 0.25 ATR | 1.382 % | 169.1883 | 62.13 % | 73.59 % | 77.6 % | 83.01 % | 87.7 % | 90.76 % |
| 0.35 ATR | 1.935 % | 168.2396 | 50.96 % | 65.62 % | 71.14 % | 78.26 % | 83.74 % | 87.47 % |
| 0.5 ATR | 2.765 % | 166.8166 | 36.25 % | 52.72 % | 59.74 % | 69.06 % | 77.64 % | 82.65 % |
| 0.75 ATR | 4.147 % | 164.445 | 19.54 % | 35.18 % | 44.7 % | 55.41 % | 66.67 % | 75.15 % |
| 1.0 ATR | 5.53 % | 162.0733 | 8.96 % | 23.08 % | 32.69 % | 43.98 % | 56.3 % | 65.91 % |
| 1.25 ATR | 6.912 % | 159.7016 | 4.53 % | 15.62 % | 23.31 % | 34.18 % | 46.34 % | 57.08 % |
| 1.5 ATR | 8.295 % | 157.3299 | 2.01 % | 10.58 % | 17.46 % | 26.79 % | 40.04 % | 52.36 % |
| 2.0 ATR | 11.059 % | 152.5865 | 0.7 % | 4.03 % | 9.59 % | 15.98 % | 29.17 % | 39.32 % |
| 2.5 ATR | 13.824 % | 147.8432 | 0.1 % | 1.41 % | 3.43 % | 9.5 % | 19.51 % | 29.47 % |
| 3.0 ATR | 16.589 % | 143.0998 | 0.0 % | 0.6 % | 1.72 % | 5.26 % | 13.21 % | 22.38 % |
| 4.0 ATR | 22.119 % | 133.6131 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 5.18 % | 12.42 % |
| 6.0 ATR | 33.178 % | 114.6396 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 4.11 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.93 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR | 1.39 ATR | 1.97 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.29 ATR | 1.58 ATR | 1.81 ATR | 2.46 ATR | 3.07 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.30 ATR | 1.82 ATR | 2.22 ATR | 2.48 ATR | 3.40 ATR | 4.08 ATR |
| **20 s.** | 0.75 ATR | 1.59 ATR | 1.78 ATR | 2.32 ATR | 2.81 ATR | 3.24 ATR | 4.58 ATR | 5.79 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.765 %, prix 166.8164), p(touche) 36.25 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.61–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.147 %, prix 164.4454), p(touche) 35.18 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.745–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.147 %, prix 164.4454), p(touche) 44.7 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.978–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.53 %, prix 162.0727), p(touche) 43.98 % (en stress 100.0 %)  ✅ optimum identifie (85.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.303–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.295 %, prix 157.3291), p(touche) 40.04 % (en stress 100.0 %)  ✅ optimum identifie (86.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.782–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (16.589 %, prix 143.0999), p(touche) 22.38 % (en stress 95.92 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (95.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.027 | EV/share : $0.115 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 — | T3 —
- Kelly (position) : f* 0.092 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.0 | bear 11.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.133% → cible +2.825% / stop −2.5%, p_fill 30%, n_eff≈33.9) : P(cible|rempli) **13%** · **EV/risk -0.018** (×p_fill ; si rempli -0.15% du capital)
  - **swing** (entrée dip −4.7% → cible +6.487% / stop −5.803%, p_fill 22%, n_eff≈26.8) : P(cible|rempli) **27%** · **EV/risk +0.014** (×p_fill ; si rempli +0.37% du capital)
  - **deep** (entrée dip −7.272% → cible +17.984% / stop −8.992%, p_fill 16%, n_eff≈19.3) : P(cible|rempli) **10%** · **EV/risk +0.007** (×p_fill ; si rempli +0.36% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.71 · part idiosyncratique 0.29
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 30.6  _(momentum baissier)_
- **ADX** : 27.5  _(tendance etablie)_
- **MACD** : hist -2.04  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 31.5%
- **ATR** : 9.49 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.026  _(neutre)_
- **Vol ratio** : 0.42  _(volume atone)_
- **Choppiness** : 37.6  _(marche directionnel)_
- **MA** : MA20 183.26 · MA50 185.08 · MA200 153.64  _(prix < MA20)_
- **Dist MA** : MA20 -6.4% · MA50 -7.3% · MA200 +11.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (699286 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
