# SRT3

**Generated** : 2026-10-16T21:40:55.819419+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €261.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 9/121 fenêtres (p_fill pondéré 7 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €261.00 (+6.0% vs entrée) · entrée €246.13 · stop €237.21 · T1 €261.17 · R/R 1.69  
> ↳ ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 261.0 · ATR Wilder 8.54 (3.27 %)_
- **Swing** : plage **249.51 → 242.67** (-4.4 % a -7.02 % sous la cloture, 0.8 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 247.02-251.19 (B) ; 241.86-245.73 (A). stop INDICATIF 232.41 (-4.23 % sous le bas ; sous le support 236.68-240.8 (- 0,5 ATR)).
- **Deep** : plage **242.67 → 225.07** (-7.02 % a -13.77 % sous la cloture, 2.06 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 241.86-245.73 (A) ; 236.68-240.8 (B) ; 232.0-235.99 (B) ; 227.55-231.42 (A) ; 222.39-226.52 (A). stop INDICATIF 212.98 (-5.37 % sous le bas ; sous le support 217.25-221.24 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.28 ATR sous le plus haut 20 s., RSI(2) 75.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 251.3-255.5 (B, -2.11 %) ; 247.02-251.19 (B, -3.76 %) ; 241.86-245.73 (A, -5.85 %) ; 236.68-240.8 (B, -7.74 %) ; 232.0-235.99 (B, -9.58 %) ; 227.55-231.42 (A, -11.33 %)
- Resistances reelles au-dessus : 266.78-270.86 (A, 2.21 %) ; 271.9-275.96 (A, 4.18 %) ; 288.55-290.03 (A, 10.56 %) ; 294.6-297.38 (A, 12.87 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.11 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **0.862 pt plus bas** dans le cas TYPIQUE (médiane), 4.249 au p90, **5.095 au pire**
   - perte réelle **11.278 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 9.11 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0051 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.602 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1204** [0.0783 ; 0.1751] _(largeur 9.7 pt, n_eff 173.1)_
   - swing : **0.4622** [0.4101 ; 0.5149] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4073** [0.3565 ; 0.4597] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.53 %** | vol 2.84 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.16 % si l'on extrapolait par √5 _(rapport 1.089 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0868** (β de hausse 1.1702, asymétrie 0.9287) vs GDAXI — 598 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.354× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 254.3089 sur atr_grid (0.75 ATR, 2.564 %) — p(stop avant cible) 0.6905 [0.64 ; 0.74], R/R 2.939, perte reelle 2.623 % (gap inclus), CVaR 3.361 %, EV 0.2435 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3612 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.691, borne haute 0.738 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.127 %) — p(stop avant cible) 0.4497 [0.40 ; 0.50], R/R 1.477, perte reelle 5.219 % (gap inclus), EV 0.5999 % — **REFUSE**
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.09 ATR (stop 9.487 %) — p(stop avant cible) 0.1764 [0.14 ; 0.22], R/R 0.803, perte reelle 9.595 % (gap inclus), EV 0.8553 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.13 ATR (stop 13.027 %) — p(stop avant cible) 0.0793 [0.05 ; 0.11], R/R 0.586, perte reelle 13.156 % (gap inclus), EV 0.8784 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.23 % > budget 12.00 %
   - 🟢 support a 7.08 ATR (stop 26.535 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.287, perte reelle 26.872 % (gap inclus), EV 1.0977 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.90 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.855 %) — p(stop avant cible) 0.8847 [0.85 ; 0.92], R/R 8.732, perte reelle 0.883 % (gap inclus), EV 0.0594 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 8.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.885, borne haute 0.915 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.709 %) — p(stop avant cible) 0.7948 [0.75 ; 0.83], R/R 4.413, perte reelle 1.747 % (gap inclus), EV 0.059 % — **REFUSE**
      - refuse : p_stop_first 0.795, borne haute 0.835 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 2.564 %) — p(stop avant cible) 0.6905 [0.64 ; 0.74], R/R 2.939, perte reelle 2.623 % (gap inclus), EV 0.2435 % — **REFUSE**
      - refuse : p_stop_first 0.691, borne haute 0.738 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 3.418 %) — p(stop avant cible) 0.5978 [0.55 ; 0.65], R/R 2.202, perte reelle 3.501 % (gap inclus), EV 0.4166 % — **REFUSE**
      - refuse : p_stop_first 0.598, borne haute 0.648 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 4.273 %) — p(stop avant cible) 0.5326 [0.48 ; 0.58], R/R 1.761, perte reelle 4.378 % (gap inclus), EV 0.3857 % — **REFUSE**
      - refuse : p_stop_first 0.533, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 5.982 %) — p(stop avant cible) 0.3716 [0.32 ; 0.42], R/R 1.263, perte reelle 6.102 % (gap inclus), EV 0.7732 % — **REFUSE**
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.09 ATR (stop 8.184 %) — p(stop avant cible) 0.2431 [0.20 ; 0.29], R/R 0.924, perte reelle 8.341 % (gap inclus), EV 0.7747 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.13 ATR (stop 11.724 %) — p(stop avant cible) 0.1093 [0.08 ; 0.15], R/R 0.655, perte reelle 11.761 % (gap inclus), EV 0.8508 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 13.673 %) — p(stop avant cible) 0.0633 [0.04 ; 0.09], R/R 0.558, perte reelle 13.812 % (gap inclus), EV 0.9247 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.85 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.382 %) — p(stop avant cible) 0.0374 [0.02 ; 0.06], R/R 0.487, perte reelle 15.842 % (gap inclus), EV 0.9417 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.96 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.091 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 0.42, perte reelle 18.344 % (gap inclus), EV 1.061 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.43 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.8 %) — p(stop avant cible) 0.0108 [0.00 ; 0.03], R/R 0.393, perte reelle 19.624 % (gap inclus), EV 1.0555 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.54 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 20.509 %) — p(stop avant cible) 0.0085 [0.00 ; 0.02], R/R 0.361, perte reelle 21.34 % (gap inclus), EV 1.0544 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.218 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.327, perte reelle 23.57 % (gap inclus), EV 1.0804 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.22 % > budget 12.00 %
   - 🟢 grid_snapped a 7.08 ATR (stop 25.233 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.29, perte reelle 26.606 % (gap inclus), EV 1.0982 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.89 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.345 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.282, perte reelle 27.345 % (gap inclus), EV 1.0959 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.91 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 261.0, ATR14 8.9214 (3.418 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.38 ATR = 1.299 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 260.5539 | 88.95 % | 92.69 % | 94.27 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.342 % | 260.1079 | 82.45 % | 88.25 % | 90.71 % | 93.37 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.513 % | 259.6618 | 74.95 % | 83.51 % | 86.76 % | 90.3 % | 93.43 % | 94.77 % |
| 0.2 ATR | 0.684 % | 259.2157 | 68.24 % | 78.58 % | 82.81 % | 87.23 % | 92.14 % | 94.17 % |
| 0.25 ATR | 0.855 % | 258.7696 | 62.92 % | 75.22 % | 79.55 % | 84.85 % | 90.35 % | 92.86 % |
| 0.35 ATR | 1.196 % | 257.8775 | 52.96 % | 68.71 % | 73.62 % | 80.5 % | 86.97 % | 90.75 % |
| 0.5 ATR | 1.709 % | 256.5393 | 38.17 % | 56.27 % | 64.03 % | 73.76 % | 82.39 % | 87.94 % |
| 0.75 ATR | 2.564 % | 254.3089 | 19.13 % | 36.62 % | 47.53 % | 59.01 % | 71.94 % | 81.21 % |
| 1.0 ATR | 3.418 % | 252.0786 | 9.86 % | 24.48 % | 34.58 % | 47.62 % | 62.59 % | 74.07 % |
| 1.25 ATR | 4.273 % | 249.8482 | 4.73 % | 14.91 % | 24.51 % | 38.12 % | 52.94 % | 66.83 % |
| 1.5 ATR | 5.127 % | 247.6179 | 2.17 % | 9.87 % | 17.59 % | 30.5 % | 45.47 % | 60.8 % |
| 2.0 ATR | 6.836 % | 243.1571 | 0.59 % | 4.34 % | 7.81 % | 16.63 % | 34.03 % | 50.95 % |
| 2.5 ATR | 8.545 % | 238.6964 | 0.3 % | 1.88 % | 4.55 % | 10.3 % | 23.58 % | 40.9 % |
| 3.0 ATR | 10.255 % | 234.2357 | 0.2 % | 1.38 % | 2.77 % | 6.04 % | 16.82 % | 33.57 % |
| 4.0 ATR | 13.673 % | 225.3143 | 0.0 % | 0.59 % | 1.68 % | 3.47 % | 8.66 % | 19.8 % |
| 6.0 ATR | 20.509 % | 207.4714 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.58 ATR | 0.64 ATR | 0.82 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.94 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.41 ATR | 1.89 ATR | 2.43 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.42 ATR | 1.70 ATR | 1.88 ATR | 2.54 ATR | 3.40 ATR |
| **10 s.** | 0.68 ATR | 1.35 ATR | 1.52 ATR | 2.05 ATR | 2.43 ATR | 2.77 ATR | 3.84 ATR | 5.11 ATR |
| **20 s.** | 0.97 ATR | 2.05 ATR | 2.30 ATR | 3.04 ATR | 3.62 ATR | 3.98 ATR | 5.54 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.709 %, prix 256.5395), p(touche) 38.17 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.643–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.564 %, prix 254.308), p(touche) 36.62 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.418 %, prix 252.079), p(touche) 34.58 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.069–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.273 %, prix 249.8475), p(touche) 38.12 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.521–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.836 %, prix 243.158), p(touche) 34.03 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.296–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.545 %, prix 238.6976), p(touche) 40.9 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.072 | EV/share : €0.639 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 6 % | T3 0 %
- Kelly (position) : f* 0.06 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 41.4 | bear 7.2 | side 51.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 522.0 (= 2 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.588% → cible +2.726% / stop −3.0%, p_fill 19%, n_eff≈23.0) : P(cible|rempli) **18%** · **EV/risk +0.011** (×p_fill ; si rempli +0.18% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=12))
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

**Factor** : R² 0.15 · part idiosyncratique 0.85
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 47.7  _(neutre)_
- **ADX** : 22.7  _(pas de tendance nette)_
- **MACD** : hist 0.019  _(bullish_recent)_
- **BB** : %B 0.74 · largeur 8.2%
- **ATR** : 8.92 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.023  _(neutre)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 56.9  _(transition)_
- **MA** : MA20 255.99 · MA50 246.76 · MA200 233.84  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 +5.8% · MA200 +11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (808827 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
