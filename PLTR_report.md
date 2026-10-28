# PLTR

**Generated** : 2026-10-28T01:25:40.623817+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $198.75  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $198.75 (+1.3% vs entrée) · entrée $196.22 · stop $191.32 · T1 $200.79 · R/R 0.93  
> ↳ ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 198.75 · ATR Wilder 7.84 (3.95 %)_
- **Swing** : plage **189.7 → 183.08** (-4.55 % a -7.88 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 184.45-188.37 (A). stop INDICATIF 176.26 (-3.73 % sous le bas ; sous le support 180.18-182.44 (- 0,5 ATR)).
- **Deep** : plage **183.08 → 168.98** (-7.88 % a -14.98 % sous la cloture, 1.8 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 180.18-182.44 (B) ; 174.29-176.5 (B) ; 168.9-172.0 (B). stop INDICATIF 160.63 (-4.94 % sous le bas ; sous le support 164.55-166.35 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.81 ATR sous le plus haut 20 s., RSI(2) 66.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 194.68-194.93 (B, -1.92 %) ; 190.0-190.39 (C, -4.21 %) ; 184.45-188.37 (A, -5.22 %) ; 180.18-182.44 (B, -8.21 %) ; 174.29-176.5 (B, -11.19 %) ; 168.9-172.0 (B, -13.46 %)
- Resistances reelles au-dessus : 207.52-207.52 (C, 4.41 %) ; 212.94-212.94 (C, 7.14 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.53 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1253).
   - exécution **4.188 pt plus bas** dans le cas TYPIQUE (médiane), 8.12 au p90, **10.402 au pire**
   - perte réelle **11.982 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 7.53 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0284 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2545** [0.1941 ; 0.3231] _(largeur 12.9 pt, n_eff 173.1)_
   - swing : **0.4094** [0.3585 ; 0.4618] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3752** [0.3254 ; 0.4271] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.8 pt), deep (29.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.42 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.77 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7002** (β de hausse 1.4133, asymétrie 1.203) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 184.9947 sur grid_snapped (1.21 ATR, 6.921 %) — p(stop avant cible) 0.4071 [0.36 ; 0.46], R/R 2.428, perte reelle 6.985 % (gap inclus), CVaR 7.441 %, EV 1.8717 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1906 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.21 ATR (stop 7.56 %) — p(stop avant cible) 0.3704 [0.32 ; 0.42], R/R 2.223, perte reelle 7.631 % (gap inclus), EV 1.8945 % — **REFUSE**
      - refuse : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 1.76 ATR (stop 10.133 %) — p(stop avant cible) 0.2805 [0.24 ; 0.33], R/R 1.658, perte reelle 10.228 % (gap inclus), EV 1.5896 % — **REFUSE**
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 2.43 ATR (stop 13.213 %) — p(stop avant cible) 0.1577 [0.12 ; 0.20], R/R 1.265, perte reelle 13.408 % (gap inclus), EV 1.7769 % — **REFUSE**
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.83 % > budget 12.00 %
   - 🟢 support a 8.85 ATR (stop 42.703 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.397, perte reelle 42.703 % (gap inclus), EV 2.2859 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.51 % > budget 12.00 %
   - 🟢 support a 10.11 ATR (stop 48.499 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.35, perte reelle 48.499 % (gap inclus), EV 2.2859 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.51 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.149 %) — p(stop avant cible) 0.8916 [0.86 ; 0.92], R/R 14.377, perte reelle 1.18 % (gap inclus), EV 0.2702 % — **REFUSE**
      - refuse : cible atteinte seulement 4.4 % du temps (< 15 %) meme a 10 seances : le R/R de 14.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.892, borne haute 0.921 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.299 %) — p(stop avant cible) 0.7639 [0.72 ; 0.81], R/R 7.082, perte reelle 2.395 % (gap inclus), EV 0.8427 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 7.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.764, borne haute 0.806 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 3.448 %) — p(stop avant cible) 0.6612 [0.61 ; 0.71], R/R 4.781, perte reelle 3.548 % (gap inclus), EV 0.9909 % — **REFUSE**
      - refuse : cible atteinte seulement 10.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.661, borne haute 0.710 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 1.21 ATR (stop 6.921 %) — p(stop avant cible) 0.4071 [0.36 ; 0.46], R/R 2.428, perte reelle 6.985 % (gap inclus), EV 1.8717 % — **REFUSE**
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 1.76 ATR (stop 9.494 %) — p(stop avant cible) 0.2951 [0.25 ; 0.34], R/R 1.774, perte reelle 9.559 % (gap inclus), EV 1.697 % — **REFUSE**
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.43 ATR (stop 12.574 %) — p(stop avant cible) 0.1739 [0.14 ; 0.22], R/R 1.331, perte reelle 12.747 % (gap inclus), EV 1.8461 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.18 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 13.794 %) — p(stop avant cible) 0.1468 [0.11 ; 0.19], R/R 1.208, perte reelle 14.046 % (gap inclus), EV 1.7377 % — **REFUSE**
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.53 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 16.092 %) — p(stop avant cible) 0.0985 [0.07 ; 0.13], R/R 1.041, perte reelle 16.3 % (gap inclus), EV 1.837 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.50 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 18.391 %) — p(stop avant cible) 0.0728 [0.05 ; 0.10], R/R 0.915, perte reelle 18.533 % (gap inclus), EV 1.8774 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.60 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 20.69 %) — p(stop avant cible) 0.0415 [0.02 ; 0.07], R/R 0.814, perte reelle 20.829 % (gap inclus), EV 2.0457 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 22.989 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.727, perte reelle 23.33 % (gap inclus), EV 2.2003 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.80 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 25.288 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.664, perte reelle 25.534 % (gap inclus), EV 2.251 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.83 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 27.587 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.587, perte reelle 28.87 % (gap inclus), EV 2.2768 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.71 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 29.886 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.55, perte reelle 30.828 % (gap inclus), EV 2.271 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.80 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 32.185 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.502, perte reelle 33.765 % (gap inclus), EV 2.2784 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 34.484 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.486, perte reelle 34.926 % (gap inclus), EV 2.2828 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.59 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 36.783 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.459, perte reelle 36.926 % (gap inclus), EV 2.2843 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.52 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 198.75, ATR14 9.1382 (4.598 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.361 ATR = 1.66 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.23 % | 198.2931 | 92.95 % | 95.46 % | 96.27 % | 97.07 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.46 % | 197.8362 | 84.99 % | 89.62 % | 91.52 % | 93.73 % | 95.22 % | 96.41 % |
| 0.15 ATR | 0.69 % | 197.3793 | 77.14 % | 83.87 % | 86.18 % | 89.99 % | 92.58 % | 94.25 % |
| 0.2 ATR | 0.92 % | 196.9224 | 69.18 % | 78.43 % | 81.84 % | 86.45 % | 90.35 % | 92.4 % |
| 0.25 ATR | 1.149 % | 196.4654 | 62.24 % | 73.49 % | 77.5 % | 82.91 % | 87.7 % | 90.76 % |
| 0.35 ATR | 1.609 % | 195.5516 | 51.06 % | 65.42 % | 71.04 % | 78.16 % | 83.74 % | 87.47 % |
| 0.5 ATR | 2.299 % | 194.1809 | 36.15 % | 52.42 % | 59.43 % | 68.66 % | 77.54 % | 82.65 % |
| 0.75 ATR | 3.448 % | 191.8963 | 19.23 % | 34.98 % | 44.3 % | 54.9 % | 66.26 % | 75.15 % |
| 1.0 ATR | 4.598 % | 189.6118 | 8.76 % | 22.78 % | 32.39 % | 43.48 % | 55.69 % | 66.02 % |
| 1.25 ATR | 5.747 % | 187.3272 | 4.33 % | 15.22 % | 23.11 % | 33.87 % | 45.73 % | 56.98 % |
| 1.5 ATR | 6.897 % | 185.0427 | 2.01 % | 10.28 % | 17.15 % | 26.39 % | 39.23 % | 52.36 % |
| 2.0 ATR | 9.196 % | 180.4736 | 0.7 % | 3.83 % | 9.28 % | 15.67 % | 28.56 % | 39.01 % |
| 2.5 ATR | 11.495 % | 175.9045 | 0.1 % | 1.41 % | 3.33 % | 9.2 % | 18.8 % | 28.95 % |
| 3.0 ATR | 13.794 % | 171.3354 | 0.0 % | 0.6 % | 1.61 % | 4.85 % | 12.4 % | 21.66 % |
| 4.0 ATR | 18.391 % | 162.1971 | 0.0 % | 0.0 % | 0.3 % | 1.42 % | 4.57 % | 11.7 % |
| 6.0 ATR | 27.587 % | 143.9207 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.52 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.38 ATR | 1.95 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.56 ATR | 1.80 ATR | 2.44 ATR | 2.98 ATR |
| **10 s.** | 0.56 ATR | 1.14 ATR | 1.28 ATR | 1.79 ATR | 2.18 ATR | 2.44 ATR | 3.31 ATR | 3.94 ATR |
| **20 s.** | 0.75 ATR | 1.59 ATR | 1.78 ATR | 2.30 ATR | 2.77 ATR | 3.17 ATR | 4.42 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.299 %, prix 194.1807), p(touche) 36.15 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.448 %, prix 191.8971), p(touche) 34.98 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.738–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.448 %, prix 191.8971), p(touche) 44.3 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.967–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.598 %, prix 189.6115), p(touche) 43.48 % (en stress 100.0 %)  ✅ optimum identifie (85.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.278–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.897 %, prix 185.0422), p(touche) 39.23 % (en stress 100.0 %)  ✅ optimum identifie (86.4 % des re-echantillons)
- **20 seance(s)** : plage utile 1.776–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.794 %, prix 171.3344), p(touche) 21.66 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.047 | EV/share : $0.229 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 11 % | T3 —
- Kelly (position) : f* 0.1 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.2 | bear 5.1 | side 81.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 357.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.272% → cible +2.329% / stop −2.5%, p_fill 62%, n_eff≈65.3) : P(cible|rempli) **29%** · **EV/risk +0.072** (×p_fill ; si rempli +0.29% du capital)
  - **swing** (entrée dip −2.792% → cible +9.747% / stop −4.874%, p_fill 42%, n_eff≈51.0) : P(cible|rempli) **14%** · **EV/risk +0.078** (×p_fill ; si rempli +0.90% du capital)
  - **deep** (entrée dip −4.324% → cible +11.496% / stop −7.208%, p_fill 35%, n_eff≈41.8) : P(cible|rempli) **19%** · **EV/risk +0.013** (×p_fill ; si rempli +0.28% du capital)
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

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.6  _(neutre)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist -0.963  _(pas de croisement recent)_
- **BB** : %B 0.57 · largeur 14.3%
- **ATR** : 9.14 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.025  _(neutre)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 56.9  _(transition)_
- **MA** : MA20 196.67 · MA50 185.77 · MA200 153.36  _(prix > MA20)_
- **Dist MA** : MA20 +1.1% · MA50 +7.0% · MA200 +29.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (777257 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
