# PLTR

**Generated** : 2026-10-30T01:25:54.521989+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $196.43  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (4 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $196.43 (+1.0% vs entrée) · entrée $194.49 · stop $189.63 · T1 $198.78 · R/R 0.88  
> ↳ ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-29 : 196.43 · ATR Wilder 7.72 (3.93 %)_
- **Swing** : plage **187.51 → 180.79** (-4.54 % a -7.96 % sous la cloture, 0.87 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 184.45-188.2 (A) ; 180.18-182.44 (B). stop INDICATIF 170.43 (-5.73 % sous le bas ; sous le support 174.29-176.5 (- 0,5 ATR)).
- **Deep** : plage **180.79 → 167.15** (-7.96 % a -14.91 % sous la cloture, 1.77 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 180.18-182.44 (B) ; 174.29-176.5 (B) ; 168.9-172.0 (B). stop INDICATIF 160.69 (-3.86 % sous le bas ; sous le support 164.55-166.35 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.14 ATR sous le plus haut 20 s., RSI(2) 23.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 188.37-190.39 (B, -3.08 %) ; 184.45-188.2 (A, -4.19 %) ; 180.18-182.44 (B, -7.12 %) ; 174.29-176.5 (B, -10.15 %) ; 168.9-172.0 (B, -12.44 %) ; 164.55-166.35 (A, -15.32 %)
- Resistances reelles au-dessus : 198.88-202.63 (B, 1.24 %) ; 207.52-207.52 (C, 5.64 %) ; 212.94-212.94 (C, 8.4 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.55 %)** : le gap seul le franchit 0.878 % des séances (11 fois sur 1253).
   - exécution **3.395 pt plus bas** dans le cas TYPIQUE (médiane), 8.122 au p90, **11.382 au pire**
   - perte réelle **10.642 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 6.55 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0359 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2454** [0.1859 ; 0.3134] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.4179** [0.3668 ; 0.4704] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4095** [0.3586 ; 0.4619] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.0 pt), deep (26.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.12 %** | CVaR **-8.42 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.77 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 1.699** (β de hausse 1.4194, asymétrie 1.197) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 185.2188 sur grid_snapped (1.01 ATR, 5.71 %) — p(stop avant cible) 0.4934 [0.44 ; 0.55], R/R 2.162, perte reelle 5.767 % (gap inclus), CVaR 6.27 %, EV 0.9856 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2794 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.01 ATR (stop 6.435 %) — p(stop avant cible) 0.4361 [0.38 ; 0.49], R/R 1.921, perte reelle 6.491 % (gap inclus), EV 1.2047 % — **REFUSE**
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 1.6 ATR (stop 9.01 %) — p(stop avant cible) 0.3052 [0.26 ; 0.36], R/R 1.371, perte reelle 9.095 % (gap inclus), EV 1.2469 % — **REFUSE**
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 support a 2.32 ATR (stop 12.183 %) — p(stop avant cible) 0.1833 [0.15 ; 0.23], R/R 1.008, perte reelle 12.367 % (gap inclus), EV 1.3035 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.86 % > budget 12.00 %
      - ⚠ support DETECTE a 0.91 ATR du spot — compartiment <1, mesure a 48.9 % de casse (IC clusterise [0.458 ; 0.522] sur 1149 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 9.16 ATR (stop 42.02 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.297, perte reelle 42.02 % (gap inclus), EV 1.7529 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.42 % > budget 12.00 %
   - 🟢 support a 10.5 ATR (stop 47.885 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.26, perte reelle 47.885 % (gap inclus), EV 1.7529 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.42 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.092 %) — p(stop avant cible) 0.9019 [0.87 ; 0.93], R/R 11.104, perte reelle 1.123 % (gap inclus), EV 0.1206 % — **REFUSE**
      - refuse : cible atteinte seulement 8.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.902, borne haute 0.930 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.183 %) — p(stop avant cible) 0.7749 [0.73 ; 0.82], R/R 5.505, perte reelle 2.265 % (gap inclus), EV 0.5504 % — **REFUSE**
      - refuse : p_stop_first 0.775, borne haute 0.817 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 3.275 %) — p(stop avant cible) 0.6728 [0.62 ; 0.72], R/R 3.723, perte reelle 3.349 % (gap inclus), EV 0.7154 % — **REFUSE**
      - refuse : p_stop_first 0.673, borne haute 0.721 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 1.01 ATR (stop 5.71 %) — p(stop avant cible) 0.4934 [0.44 ; 0.55], R/R 2.162, perte reelle 5.767 % (gap inclus), EV 0.9856 % — **REFUSE**
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 1.6 ATR (stop 8.285 %) — p(stop avant cible) 0.3367 [0.29 ; 0.39], R/R 1.49, perte reelle 8.366 % (gap inclus), EV 1.29 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 grid_snapped a 2.32 ATR (stop 11.458 %) — p(stop avant cible) 0.2157 [0.17 ; 0.26], R/R 1.073, perte reelle 11.619 % (gap inclus), EV 1.1392 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.15 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 13.101 %) — p(stop avant cible) 0.1609 [0.13 ; 0.20], R/R 0.937, perte reelle 13.301 % (gap inclus), EV 1.2608 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.74 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 15.284 %) — p(stop avant cible) 0.1135 [0.08 ; 0.15], R/R 0.803, perte reelle 15.533 % (gap inclus), EV 1.2539 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.85 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 17.468 %) — p(stop avant cible) 0.0797 [0.05 ; 0.11], R/R 0.707, perte reelle 17.637 % (gap inclus), EV 1.3785 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.74 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 19.651 %) — p(stop avant cible) 0.0467 [0.03 ; 0.07], R/R 0.629, perte reelle 19.827 % (gap inclus), EV 1.5165 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.68 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.835 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.563, perte reelle 22.159 % (gap inclus), EV 1.6113 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.62 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 24.018 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 0.508, perte reelle 24.541 % (gap inclus), EV 1.711 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.87 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 26.201 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.454, perte reelle 27.481 % (gap inclus), EV 1.7289 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.74 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 28.385 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.422, perte reelle 29.559 % (gap inclus), EV 1.7406 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 30.568 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.393, perte reelle 31.702 % (gap inclus), EV 1.7373 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.75 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 32.752 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.367, perte reelle 33.969 % (gap inclus), EV 1.7478 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.54 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 34.935 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.355, perte reelle 35.164 % (gap inclus), EV 1.7491 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.51 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 196.435, ATR14 8.5781 (4.367 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.361 ATR = 1.576 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.218 % | 196.0061 | 92.95 % | 95.46 % | 96.27 % | 97.07 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.437 % | 195.5772 | 85.1 % | 89.62 % | 91.52 % | 93.73 % | 95.22 % | 96.41 % |
| 0.15 ATR | 0.655 % | 195.1483 | 77.14 % | 83.87 % | 86.18 % | 89.99 % | 92.58 % | 94.25 % |
| 0.2 ATR | 0.873 % | 194.7194 | 69.18 % | 78.53 % | 81.94 % | 86.55 % | 90.35 % | 92.4 % |
| 0.25 ATR | 1.092 % | 194.2905 | 62.24 % | 73.59 % | 77.6 % | 82.91 % | 87.7 % | 90.76 % |
| 0.35 ATR | 1.528 % | 193.4326 | 51.06 % | 65.52 % | 71.14 % | 78.16 % | 83.74 % | 87.47 % |
| 0.5 ATR | 2.183 % | 192.1459 | 36.15 % | 52.62 % | 59.54 % | 68.76 % | 77.64 % | 82.65 % |
| 0.75 ATR | 3.275 % | 190.0014 | 19.23 % | 34.98 % | 44.3 % | 55.01 % | 66.36 % | 75.15 % |
| 1.0 ATR | 4.367 % | 187.8569 | 8.76 % | 22.78 % | 32.39 % | 43.58 % | 55.89 % | 65.91 % |
| 1.25 ATR | 5.459 % | 185.7123 | 4.33 % | 15.22 % | 23.11 % | 33.87 % | 45.93 % | 56.98 % |
| 1.5 ATR | 6.55 % | 183.5678 | 2.01 % | 10.28 % | 17.15 % | 26.39 % | 39.43 % | 52.36 % |
| 2.0 ATR | 8.734 % | 179.2787 | 0.7 % | 3.83 % | 9.28 % | 15.67 % | 28.66 % | 39.01 % |
| 2.5 ATR | 10.917 % | 174.9896 | 0.1 % | 1.41 % | 3.33 % | 9.2 % | 18.9 % | 28.95 % |
| 3.0 ATR | 13.101 % | 170.7006 | 0.0 % | 0.6 % | 1.61 % | 4.85 % | 12.5 % | 21.66 % |
| 4.0 ATR | 17.468 % | 162.1224 | 0.0 % | 0.0 % | 0.3 % | 1.42 % | 4.57 % | 11.7 % |
| 6.0 ATR | 26.201 % | 144.9661 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.52 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.38 ATR | 1.95 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.56 ATR | 1.80 ATR | 2.44 ATR | 2.98 ATR |
| **10 s.** | 0.56 ATR | 1.15 ATR | 1.29 ATR | 1.80 ATR | 2.19 ATR | 2.44 ATR | 3.31 ATR | 3.95 ATR |
| **20 s.** | 0.75 ATR | 1.59 ATR | 1.78 ATR | 2.30 ATR | 2.77 ATR | 3.17 ATR | 4.42 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.183 %, prix 192.1468), p(touche) 36.15 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.608–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.275 %, prix 190.0018), p(touche) 34.98 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.739–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.275 %, prix 190.0018), p(touche) 44.3 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.969–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.367 %, prix 187.8567), p(touche) 43.58 % (en stress 100.0 %)  ✅ optimum identifie (85.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.286–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.55 %, prix 183.5685), p(touche) 39.43 % (en stress 100.0 %)  ✅ optimum identifie (85.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.776–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.101 %, prix 170.7), p(touche) 21.66 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.045 | EV/share : $0.218 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 13 % | T3 —
- Kelly (position) : f* 0.099 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.8 | bear 5.1 | side 82.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 176.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.995% → cible +2.205% / stop −2.5%, p_fill 73%, n_eff≈76.3) : P(cible|rempli) **35%** · **EV/risk +0.090** (×p_fill ; si rempli +0.31% du capital)
  - **swing** (entrée dip −2.183% → cible +4.991% / stop −4.464%, p_fill 48%, n_eff≈57.9) : P(cible|rempli) **43%** · **EV/risk +0.048** (×p_fill ; si rempli +0.45% du capital)
  - **deep** (entrée dip −3.37% → cible +11.729% / stop −6.779%, p_fill 44%, n_eff≈52.4) : P(cible|rempli) **19%** · **EV/risk +0.003** (×p_fill ; si rempli +0.04% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.67 · part idiosyncratique 0.33
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-02 — PLTR earnings (J-2 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-02 — PLTR earnings (J-2 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 38.0  _(momentum baissier)_
- **ADX** : 20.3  _(pas de tendance nette)_
- **MACD** : hist -1.078  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 13.0%
- **ATR** : 8.58 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.08  _(accumulation)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 54.5  _(transition)_
- **MA** : MA20 197.48 · MA50 186.7 · MA200 153.54  _(prix < MA20)_
- **Dist MA** : MA20 -0.5% · MA50 +5.2% · MA200 +27.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (796416 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
