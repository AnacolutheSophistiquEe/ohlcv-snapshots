# SRT3

**Generated** : 2026-10-20T21:40:50.555490+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €264.70  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 8/121 fenêtres (p_fill pondéré 6 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €264.70 (+6.8% vs entrée) · entrée €247.80 · stop €239.10 · T1 €257.52 · R/R 1.12  
> ↳ ¼-Kelly 0.019 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-20 : 264.7 · ATR Wilder 8.27 (3.12 %)_
- **Swing** : plage **253.58 → 246.97** (-4.2 % a -6.7 % sous la cloture, 0.8 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 250.3-254.32 (B) ; 245.25-249.2 (B). stop INDICATIF 236.57 (-4.21 % sous le bas ; sous le support 240.7-244.46 (- 0,5 ATR)).
- **Deep** : plage **246.97 → 229.94** (-6.7 % a -13.13 % sous la cloture, 2.06 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 245.25-249.2 (B) ; 240.7-244.46 (A) ; 235.99-239.47 (B) ; 231.42-234.8 (B) ; 226.52-230.2 (A). stop INDICATIF 218.25 (-5.08 % sous le bas ; sous le support 222.39-226.2 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.87 ATR sous le plus haut 20 s., RSI(2) 89.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 255.36-258.01 (B, -2.53 %) ; 250.3-254.32 (B, -3.92 %) ; 245.25-249.2 (B, -5.85 %) ; 240.7-244.46 (A, -7.65 %) ; 235.99-239.47 (B, -9.53 %) ; 231.42-234.8 (B, -11.3 %)
- Resistances reelles au-dessus : 270.0-273.78 (A, 2.0 %) ; 288.55-290.03 (A, 9.01 %) ; 294.6-297.38 (A, 11.3 %) ; 314.42-318.19 (B, 18.78 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.67 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **2.418 pt plus bas** dans le cas TYPIQUE (médiane), 4.112 au p90, **4.535 au pire**
   - perte réelle **12.088 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 9.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0038 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.602 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1799** [0.1282 ; 0.2422] _(largeur 11.4 pt, n_eff 173.1)_
   - swing : **0.442** [0.3903 ; 0.4946] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3949** [0.3444 ; 0.4471] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.53 %** | vol 2.84 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.16 % si l'on extrapolait par √5 _(rapport 1.089 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0892** (β de hausse 1.1738, asymétrie 0.9279) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.359× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 260.35 sur atr_grid (0.5 ATR, 1.643 %) — p(stop avant cible) 0.7181 [0.67 ; 0.76], R/R 2.788, perte reelle 1.664 % (gap inclus), CVaR 1.946 %, EV 0.1043 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4592 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.718, borne haute 0.764 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.93 %) — p(stop avant cible) 0.4214 [0.37 ; 0.47], R/R 0.925, perte reelle 5.017 % (gap inclus), EV 0.2516 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.57 ATR (stop 10.432 %) — p(stop avant cible) 0.1406 [0.11 ; 0.18], R/R 0.442, perte reelle 10.499 % (gap inclus), EV 0.5367 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.63 ATR (stop 13.93 %) — p(stop avant cible) 0.0549 [0.03 ; 0.08], R/R 0.33, perte reelle 14.078 % (gap inclus), EV 0.6473 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.09 % > budget 12.00 %
   - 🟢 support a 7.69 ATR (stop 27.259 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.17, perte reelle 27.285 % (gap inclus), EV 0.7904 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.75 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.822 %) — p(stop avant cible) 0.82 [0.78 ; 0.86], R/R 5.516, perte reelle 0.841 % (gap inclus), EV 0.1454 % — **REFUSE**
      - refuse : p_stop_first 0.820, borne haute 0.858 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.643 %) — p(stop avant cible) 0.7181 [0.67 ; 0.76], R/R 2.788, perte reelle 1.664 % (gap inclus), EV 0.1043 % — **REFUSE**
      - refuse : p_stop_first 0.718, borne haute 0.764 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.75 ATR (stop 2.465 %) — p(stop avant cible) 0.6307 [0.58 ; 0.68], R/R 1.845, perte reelle 2.514 % (gap inclus), EV 0.117 % — **REFUSE**
      - refuse : p_stop_first 0.631, borne haute 0.680 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 3.287 %) — p(stop avant cible) 0.551 [0.50 ; 0.60], R/R 1.379, perte reelle 3.363 % (gap inclus), EV 0.1585 % — **REFUSE**
      - refuse : p_stop_first 0.551, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 4.108 %) — p(stop avant cible) 0.4776 [0.43 ; 0.53], R/R 1.099, perte reelle 4.222 % (gap inclus), EV 0.1714 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 5.752 %) — p(stop avant cible) 0.3576 [0.31 ; 0.41], R/R 0.794, perte reelle 5.846 % (gap inclus), EV 0.4359 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.573 %) — p(stop avant cible) 0.3112 [0.26 ; 0.36], R/R 0.695, perte reelle 6.676 % (gap inclus), EV 0.4977 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 7.395 %) — p(stop avant cible) 0.2627 [0.22 ; 0.31], R/R 0.619, perte reelle 7.491 % (gap inclus), EV 0.5401 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.57 ATR (stop 9.426 %) — p(stop avant cible) 0.1655 [0.13 ; 0.21], R/R 0.486, perte reelle 9.546 % (gap inclus), EV 0.5719 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.86 %) — p(stop avant cible) 0.156 [0.12 ; 0.20], R/R 0.465, perte reelle 9.972 % (gap inclus), EV 0.5728 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.63 ATR (stop 12.925 %) — p(stop avant cible) 0.0735 [0.05 ; 0.10], R/R 0.357, perte reelle 13.006 % (gap inclus), EV 0.6162 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.04 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.79 %) — p(stop avant cible) 0.0406 [0.02 ; 0.07], R/R 0.308, perte reelle 15.048 % (gap inclus), EV 0.6432 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.57 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.434 %) — p(stop avant cible) 0.017 [0.01 ; 0.03], R/R 0.268, perte reelle 17.295 % (gap inclus), EV 0.7226 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.77 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.077 %) — p(stop avant cible) 0.0111 [0.00 ; 0.03], R/R 0.245, perte reelle 18.936 % (gap inclus), EV 0.7522 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.35 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.72 %) — p(stop avant cible) 0.0088 [0.00 ; 0.02], R/R 0.229, perte reelle 20.225 % (gap inclus), EV 0.755 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.32 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 21.364 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 0.205, perte reelle 22.598 % (gap inclus), EV 0.7494 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.43 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 23.007 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.191, perte reelle 24.257 % (gap inclus), EV 0.7779 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.04 % > budget 12.00 %
   - 🟢 grid_snapped a 7.69 ATR (stop 26.253 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.173, perte reelle 26.868 % (gap inclus), EV 0.7929 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.74 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 264.7, ATR14 8.7 (3.287 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 1.252 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.164 % | 264.265 | 89.05 % | 92.79 % | 94.37 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.329 % | 263.83 | 82.54 % | 88.35 % | 90.81 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.493 % | 263.395 | 75.05 % | 83.61 % | 86.86 % | 90.5 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.657 % | 262.96 | 68.34 % | 78.68 % | 82.81 % | 87.43 % | 92.34 % | 94.37 % |
| 0.25 ATR | 0.822 % | 262.525 | 63.02 % | 75.32 % | 79.55 % | 85.05 % | 90.55 % | 93.07 % |
| 0.35 ATR | 1.15 % | 261.655 | 53.06 % | 68.81 % | 73.62 % | 80.59 % | 87.16 % | 90.95 % |
| 0.5 ATR | 1.643 % | 260.35 | 38.26 % | 56.37 % | 64.03 % | 73.76 % | 82.59 % | 88.14 % |
| 0.75 ATR | 2.465 % | 258.175 | 19.13 % | 36.62 % | 47.53 % | 59.01 % | 72.14 % | 81.31 % |
| 1.0 ATR | 3.287 % | 256.0 | 9.86 % | 24.48 % | 34.58 % | 47.62 % | 62.69 % | 74.07 % |
| 1.25 ATR | 4.108 % | 253.825 | 4.73 % | 14.91 % | 24.51 % | 38.12 % | 52.94 % | 66.83 % |
| 1.5 ATR | 4.93 % | 251.65 | 2.17 % | 9.87 % | 17.59 % | 30.5 % | 45.47 % | 60.8 % |
| 2.0 ATR | 6.573 % | 247.3 | 0.59 % | 4.34 % | 7.81 % | 16.63 % | 34.03 % | 50.95 % |
| 2.5 ATR | 8.217 % | 242.95 | 0.3 % | 1.88 % | 4.55 % | 10.3 % | 23.58 % | 40.9 % |
| 3.0 ATR | 9.86 % | 238.6 | 0.2 % | 1.38 % | 2.77 % | 6.04 % | 16.82 % | 33.57 % |
| 4.0 ATR | 13.147 % | 229.9 | 0.0 % | 0.59 % | 1.68 % | 3.47 % | 8.66 % | 19.8 % |
| 6.0 ATR | 19.72 % | 212.5 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.64 ATR | 0.82 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.94 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.41 ATR | 1.89 ATR | 2.43 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.42 ATR | 1.70 ATR | 1.88 ATR | 2.54 ATR | 3.40 ATR |
| **10 s.** | 0.68 ATR | 1.35 ATR | 1.52 ATR | 2.05 ATR | 2.43 ATR | 2.77 ATR | 3.84 ATR | 5.11 ATR |
| **20 s.** | 0.97 ATR | 2.05 ATR | 2.30 ATR | 3.04 ATR | 3.62 ATR | 3.98 ATR | 5.54 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.643 %, prix 260.351), p(touche) 38.26 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.644–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.465 %, prix 258.1752), p(touche) 36.62 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.287 %, prix 255.9993), p(touche) 34.58 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.069–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.108 %, prix 253.8261), p(touche) 38.12 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.521–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.573 %, prix 247.3013), p(touche) 34.03 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.296–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.217 %, prix 242.9496), p(touche) 40.9 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.08 | EV/share : €0.696 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 15 % | T3 2 %
- Kelly (position) : f* 0.074 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 25.6 | bear 5.0 | side 69.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 529.0 (= 2 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.903% → cible +1.692% / stop −2.5%, p_fill 13%, n_eff≈16.3) : P(cible|rempli) **37%** · **EV/risk +0.006** (×p_fill ; si rempli +0.12% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→44% · +3.0%→23% · +5.0%→7% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.12%) · excursion haute méd. +1.77% / basse méd. −1.47%
- Profil de vol intra : ouverture 1.936% vs midi 0.828% vs clôture 0.957% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. 0.284% ; recovery-V 26%
- **σ réalisé intraday** 2.228% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 61% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 252.4856 (VA 251.8969–253.2706 ; dernier close 252.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 46% · rebond 59% · **stop −1.74%** sous le fill (sous le bruit) · cible +1.24% · R/R 0.71 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 58% (gap-down >1% 6% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.26% (p90 −1.61%) · haut méd +0.6% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.3% (p90 −1.79%) · haut méd +0.78% · range méd 1.34%
- Excursion ouverture 30min (n=160) : bas méd −0.43% (p90 −1.9%) · haut méd +0.86% · range méd 1.52%
- Excursion ouverture 60min (n=160) : bas méd −0.49% (p90 −2.03%) · haut méd +0.91% · range méd 1.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 251.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 80% (123/159) · gap 25% · délai 0.5min · rebond 51% (67/123) (MFE +1.04%)
   - −1.0% : fill 30min 39% · séance 67% (103/159) · gap 6% · délai 7.9min · rebond 58% (60/103) (MFE +1.2%)
   - −1.5% : fill 30min 22% · séance 46% (78/159) · gap 2% · délai 38.9min · rebond 59% (45/78) (MFE +1.24%)
   - −2.0% : fill 30min 7% · séance 32% (57/159) · gap 0% · délai 236.0min · rebond 50% (29/57) (MFE +1.06%)
   - −3.0% : fill 30min 2% · séance 10% (26/159) · gap 0% · délai 183.5min · rebond 50% (12/26) (MFE +0.88%)
   - −4.0% : fill 30min 1% · séance 5% (13/159) · gap 0% · délai 55.4min · rebond 62% (8/13) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 3% (7/159) · gap 0% · délai 141.9min · rebond 84% (6/7) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −1.59%) → stop au-delà de −1.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.07% (p90 −1.59%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.99%) → stop au-delà de −1.15% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=442 jambes) : jambe baissière méd −1.02% (p90 −2.22%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 78% (49/61) · rebond 61% (30/49)
      · −2.0% : fill 37% (27/61) · rebond 47% (14/27)
      · −3.0% : fill 13% (15/61) · rebond 34% (7/15)
      · −4.0% : fill 6% (8/61) · rebond 60% (6/8)
      · −5.0% : fill 3% (4/61) · rebond 100% (4/4)
   - **flat** (40 séances) :
      · −1.0% : fill 61% (25/40) · rebond 53% (12/25)
      · −2.0% : fill 34% (16/40) · rebond 49% (7/16)
      · −3.0% : fill 6% (5/40) · rebond 34% (1/5)
      · −4.0% : fill 2% (2/40) · rebond 0% (0/2)
      · −5.0% : fill 2% (1/40) · rebond 0% (0/1)
   - **gap-up** (58 séances) :
      · −1.0% : fill 56% (29/58) · rebond 57% (18/29)
      · −2.0% : fill 22% (14/58) · rebond 59% (8/14)
      · −3.0% : fill 9% (6/58) · rebond 88% (4/6)
      · −4.0% : fill 6% (3/58) · rebond 89% (2/3)
      · −5.0% : fill 5% (2/58) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 56% si les 15 1res min sont vertes (88 cas) · 42% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 67% si début vert vs 27% si rouge (base 50% · écart 40 pts) ; prédictivité sature ensuite (plafond brut 235min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **67%** · continue >prix actuel 50% ; creux résiduel méd -1.2% (q20 -2.49%) → **SL/trailing à −2.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.95% / q75 +1.97% → **scale +0.95% / runner +1.97%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **27%** (continue à baisser 50%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.65%** (au-delà de la MAE q10 -2.65%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.07% .. +2.01%] · haut q95 +2.53% · bas q05 -2.81%
   - 60min (n=160) : retour [-2.27% .. +2.33%] · haut q95 +2.72% · bas q05 -2.84%
   - 2h (n=160) : retour [-2.12% .. +2.25%] · haut q95 +2.93% · bas q05 -2.95%
   - 4h (n=160) : retour [-2.23% .. +2.43%] · haut q95 +3.11% · bas q05 -3.15%
   - 6h (n=160) : retour [-2.48% .. +2.87%] · haut q95 +3.58% · bas q05 -3.16%
   - session (n=160) : retour [-3.0% .. +4.36%] · haut q95 +5.16% · bas q05 -3.82%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 54.9  _(neutre)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist 0.371  _(bullish_recent)_
- **BB** : %B 0.86 · largeur 8.2%
- **ATR** : 8.7 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.005  _(neutre)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 56.0  _(transition)_
- **MA** : MA20 257.16 · MA50 247.72 · MA200 233.82  _(prix > MA20)_
- **Dist MA** : MA20 +2.9% · MA50 +6.9% · MA200 +13.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (777641 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
