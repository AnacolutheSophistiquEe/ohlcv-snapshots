# AL2SI

**Generated** : 2026-10-28T01:12:57.331400+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.86  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €27.86 (+2.1% vs entrée) · entrée €27.28 · stop €26.37 · T1 €29.09 · R/R 1.99  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 27.86 · ATR Wilder 1.82 (6.52 %)_
- **Swing** : plage **25.79 → 24.5** (-7.42 % a -12.07 % sous la cloture, 0.71 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 25.0-25.4 (A). stop INDICATIF 21.69 (-11.45 % sous le bas ; sous le support 22.6-23.38 (- 0,5 ATR)).
- **Deep** : plage **24.5 → 21.32** (-12.07 % a -23.48 % sous la cloture, 1.75 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 22.6-23.38 (A). stop INDICATIF 19.19 (-9.98 % sous le bas ; sous le support 20.1-20.8 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.31 ATR sous le plus haut 20 s., RSI(2) 77.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 26.38-26.7 (B, -4.16 %) ; 25.0-25.4 (A, -8.83 %) ; 22.6-23.38 (A, -16.08 %) ; 20.1-20.8 (B, -25.34 %) ; 16.1-16.65 (A, -40.24 %) ; 14.2-15.0 (A, -46.16 %)
- Resistances reelles au-dessus : 30.0-30.8 (A, 7.68 %) ; 30.94-31.54 (B, 11.06 %) ; 33.02-33.02 (C, 18.52 %) ; 34.5-35.02 (A, 23.83 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.52 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.86 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **12.952 pt plus bas** dans le cas TYPIQUE (médiane), 21.876 au p90, **26.257 au pire**
   - perte réelle **24.668 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 11.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.05 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.401 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4572** [0.3842 ; 0.5316] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4093** [0.3584 ; 0.4617] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3241** [0.2764 ; 0.3747] _(largeur 9.8 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.9 pt), deep (26.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.3 %** | CVaR **-11.71 %** | vol 6.34 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.44 % contre 7.25 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.205** (β de hausse 0.9558, asymétrie 1.2608) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.044× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 26.3455 sur atr_grid (0.75 ATR, 5.436 %) — p(stop avant cible) 0.6744 [0.62 ; 0.72], R/R 3.549, perte reelle 5.814 % (gap inclus), CVaR 10.528 %, EV 0.618 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3131 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.674, borne haute 0.722 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.42 ATR (stop 13.433 %) — p(stop avant cible) 0.2839 [0.24 ; 0.33], R/R 1.273, perte reelle 16.215 % (gap inclus), EV 1.7057 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.23 % > budget 12.00 %
   - 🟢 support a 2.6 ATR (stop 22.047 %) — p(stop avant cible) 0.1297 [0.10 ; 0.17], R/R 0.731, perte reelle 28.235 % (gap inclus), EV 1.5793 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.09 % > budget 12.00 %
   - 🟢 support a 3.84 ATR (stop 31.021 %) — p(stop avant cible) 0.0729 [0.05 ; 0.10], R/R 0.562, perte reelle 36.721 % (gap inclus), EV 1.776 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.34 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.812 %) — p(stop avant cible) 0.8721 [0.83 ; 0.90], R/R 10.431, perte reelle 1.978 % (gap inclus), EV 0.4733 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.872, borne haute 0.904 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.624 %) — p(stop avant cible) 0.7615 [0.71 ; 0.80], R/R 5.328, perte reelle 3.873 % (gap inclus), EV 0.7882 % — **REFUSE**
      - refuse : p_stop_first 0.761, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 5.436 %) — p(stop avant cible) 0.6744 [0.62 ; 0.72], R/R 3.549, perte reelle 5.814 % (gap inclus), EV 0.618 % — **REFUSE**
      - refuse : p_stop_first 0.674, borne haute 0.722 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 7.248 %) — p(stop avant cible) 0.5775 [0.53 ; 0.63], R/R 2.588, perte reelle 7.973 % (gap inclus), EV 0.938 % — **REFUSE**
      - refuse : p_stop_first 0.578, borne haute 0.629 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.59 % > budget 12.00 %
   - 🟢 grid_snapped a 1.42 ATR (stop 12.44 %) — p(stop avant cible) 0.3136 [0.27 ; 0.36], R/R 1.442, perte reelle 14.311 % (gap inclus), EV 1.8762 % — **REFUSE**
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.18 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 14.496 %) — p(stop avant cible) 0.2615 [0.22 ; 0.31], R/R 1.181, perte reelle 17.47 % (gap inclus), EV 1.6765 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.80 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 16.308 %) — p(stop avant cible) 0.2228 [0.18 ; 0.27], R/R 1.035, perte reelle 19.936 % (gap inclus), EV 1.5912 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.41 % > budget 12.00 %
   - 🟢 grid_snapped a 2.6 ATR (stop 21.055 %) — p(stop avant cible) 0.135 [0.10 ; 0.17], R/R 0.754, perte reelle 27.379 % (gap inclus), EV 1.6142 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.09 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 25.368 %) — p(stop avant cible) 0.089 [0.06 ; 0.12], R/R 0.633, perte reelle 32.613 % (gap inclus), EV 1.8577 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.26 % > budget 12.00 %
   - 🟢 grid_snapped a 3.84 ATR (stop 30.028 %) — p(stop avant cible) 0.075 [0.05 ; 0.11], R/R 0.573, perte reelle 36.036 % (gap inclus), EV 1.7811 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.04 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 32.616 %) — p(stop avant cible) 0.0672 [0.04 ; 0.10], R/R 0.543, perte reelle 38.031 % (gap inclus), EV 1.7788 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.90 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 36.24 %) — p(stop avant cible) 0.047 [0.03 ; 0.07], R/R 0.494, perte reelle 41.808 % (gap inclus), EV 2.0954 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.19 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.864 %) — p(stop avant cible) 0.0316 [0.02 ; 0.05], R/R 0.459, perte reelle 44.958 % (gap inclus), EV 2.3792 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 43.488 %) — p(stop avant cible) 0.0278 [0.01 ; 0.05], R/R 0.448, perte reelle 46.026 % (gap inclus), EV 2.3918 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.10 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 47.112 %) — p(stop avant cible) 0.0278 [0.01 ; 0.05], R/R 0.42, perte reelle 49.179 % (gap inclus), EV 2.3041 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.86 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 50.736 %) — p(stop avant cible) 0.0278 [0.01 ; 0.05], R/R 0.365, perte reelle 56.488 % (gap inclus), EV 2.101 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.92 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 54.36 %) — p(stop avant cible) 0.0244 [0.01 ; 0.04], R/R 0.326, perte reelle 63.341 % (gap inclus), EV 1.9485 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.98 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 57.984 %) — p(stop avant cible) 0.0244 [0.01 ; 0.04], R/R 0.326, perte reelle 63.341 % (gap inclus), EV 1.9485 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.98 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.86, ATR14 2.0193 (7.248 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.401 ATR = 2.906 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.362 % | 27.759 | 87.25 % | 90.78 % | 93.03 % | 94.49 % | 95.55 % | 97.2 % |
| 0.1 ATR | 0.725 % | 27.6581 | 82.55 % | 87.14 % | 90.28 % | 92.13 % | 94.07 % | 96.3 % |
| 0.15 ATR | 1.087 % | 27.5571 | 78.33 % | 83.51 % | 87.33 % | 88.98 % | 92.19 % | 95.2 % |
| 0.2 ATR | 1.45 % | 27.4561 | 72.65 % | 79.39 % | 83.6 % | 85.93 % | 89.81 % | 93.01 % |
| 0.25 ATR | 1.812 % | 27.3552 | 66.67 % | 74.78 % | 79.47 % | 82.58 % | 87.54 % | 91.41 % |
| 0.35 ATR | 2.537 % | 27.1533 | 54.71 % | 65.65 % | 71.22 % | 75.79 % | 82.69 % | 87.91 % |
| 0.5 ATR | 3.624 % | 26.8504 | 40.78 % | 53.88 % | 62.08 % | 68.9 % | 78.24 % | 85.51 % |
| 0.75 ATR | 5.436 % | 26.3455 | 22.65 % | 37.78 % | 47.54 % | 55.71 % | 67.46 % | 76.92 % |
| 1.0 ATR | 7.248 % | 25.8407 | 12.75 % | 24.93 % | 33.89 % | 44.19 % | 57.37 % | 68.63 % |
| 1.25 ATR | 9.06 % | 25.3359 | 7.45 % | 17.76 % | 24.75 % | 36.52 % | 50.45 % | 62.24 % |
| 1.5 ATR | 10.872 % | 24.8311 | 3.63 % | 11.38 % | 17.49 % | 28.94 % | 43.22 % | 55.94 % |
| 2.0 ATR | 14.496 % | 23.8214 | 0.88 % | 5.2 % | 9.72 % | 17.03 % | 31.75 % | 44.46 % |
| 2.5 ATR | 18.12 % | 22.8118 | 0.1 % | 2.16 % | 4.62 % | 9.84 % | 21.56 % | 34.47 % |
| 3.0 ATR | 21.744 % | 21.8021 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 15.23 % | 26.77 % |
| 4.0 ATR | 28.992 % | 19.7829 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.28 % |
| 6.0 ATR | 43.488 % | 15.7443 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.98 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.37 ATR | 1.67 ATR | 1.88 ATR | 2.49 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.27 ATR | 1.44 ATR | 1.95 ATR | 2.33 ATR | 2.62 ATR | 3.78 ATR | 5.11 ATR |
| **20 s.** | 0.81 ATR | 1.76 ATR | 1.98 ATR | 2.60 ATR | 3.19 ATR | 3.71 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.455–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.624 %, prix 26.8504), p(touche) 40.78 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (89.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.638–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.436 %, prix 26.3455), p(touche) 37.78 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.248 %, prix 25.8407), p(touche) 33.89 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.982–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.248 %, prix 25.8407), p(touche) 44.19 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.438–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.872 %, prix 24.8311), p(touche) 43.22 % (en stress 97.06 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.976–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.496 %, prix 23.8214), p(touche) 44.46 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 12.8 | bear 5.0 | side 82.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 390.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.099% → cible +6.662% / stop −3.331%, p_fill 65%, n_eff≈68.8) : P(cible|rempli) **5%** · **EV/risk -0.157** (×p_fill ; si rempli -0.81% du capital)
  - **swing** (entrée dip −4.612% → cible +9.473% / stop −7.598%, p_fill 46%, n_eff≈53.9) : P(cible|rempli) **39%** · **EV/risk -0.051** (×p_fill ; si rempli -0.83% du capital)
  - **deep** (entrée dip −7.128% → cible +12.437% / stop −11.706%, p_fill 47%, n_eff≈53.3) : P(cible|rempli) **41%** · **EV/risk -0.095** (×p_fill ; si rempli -2.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→74% · +2.0%→66% · +3.0%→50% · +5.0%→34% · +8.0%→17%
- Range intraday médian 6.93% (p90 16.1%) · excursion haute méd. +2.93% / basse méd. −3.31%
- Profil de vol intra : ouverture 4.806% vs midi 1.518% vs clôture 1.661% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. 0.151% ; recovery-V 25%
- **σ réalisé intraday** 4.419% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 26.6325 (VA 26.2575–26.7325 ; dernier close 26.53)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 91% · **stop −3.21%** sous le fill (sous le bruit) · cible +2.26% · R/R 0.7 (high win-rate)
- Gaps overnight (n=158) : méd. -0.0% · baisse 51% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −3.16%) · haut méd +0.82% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.92%) · haut méd +1.23% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −4.38%) · haut méd +1.57% · range méd 3.4%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −5.26%) · haut méd +2.01% · range méd 4.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.62 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (125/158) · gap 30% · délai 0.1min · rebond 61% (81/125) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 76% (120/158) · gap 16% · délai 0.4min · rebond 61% (79/120) (MFE +1.71%)
   - −1.5% : fill 30min 50% · séance 72% (107/158) · gap 8% · délai 2.4min · rebond 63% (68/107) (MFE +1.74%)
   - −2.0% : fill 30min 42% · séance 66% (98/158) · gap 6% · délai 7.8min · rebond 59% (60/98) (MFE +1.61%)
   - −3.0% : fill 30min 26% · séance 51% (79/158) · gap 3% · délai 31.2min · rebond 59% (53/79) (MFE +1.59%)
   - −4.0% : fill 30min 16% · séance 39% (65/158) · gap 2% · délai 55.8min · rebond 71% (49/65) (MFE +1.67%)
   - −5.0% : fill 30min 11% · séance 28% (50/158) · gap 2% · délai 48.7min · rebond 91% (46/50) (MFE +2.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.9%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.91%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −3.18%) → stop au-delà de −2.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1398 jambes) : jambe baissière méd −1.21% (p90 −2.94%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 95% (51/53) · rebond 58% (30/51)
      · −2.0% : fill 87% (46/53) · rebond 59% (26/46)
      · −3.0% : fill 76% (41/53) · rebond 59% (28/41)
      · −4.0% : fill 58% (34/53) · rebond 61% (23/34)
      · −5.0% : fill 44% (27/53) · rebond 92% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 72% (25/34) · rebond 66% (17/25)
      · −2.0% : fill 54% (19/34) · rebond 49% (11/19)
      · −3.0% : fill 40% (15/34) · rebond 60% (9/15)
      · −4.0% : fill 37% (14/34) · rebond 77% (11/14)
      · −5.0% : fill 30% (11/34) · rebond 80% (10/11)
   - **gap-up** (71 séances) :
      · −1.0% : fill 61% (44/71) · rebond 63% (32/44)
      · −2.0% : fill 52% (33/71) · rebond 65% (23/33)
      · −3.0% : fill 34% (23/71) · rebond 59% (16/23)
      · −4.0% : fill 23% (17/71) · rebond 88% (15/17)
      · −5.0% : fill 13% (12/71) · rebond 100% (12/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (77 cas) · 29% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:03** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 42% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -2.0% (q20 -4.42%) → **SL/trailing à −4.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.25% → **scale +2.14% / runner +3.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **15%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +5.57%] · haut q95 +6.82% · bas q05 -5.16%
   - 60min (n=160) : retour [-4.85% .. +7.25%] · haut q95 +8.2% · bas q05 -6.05%
   - 2h (n=160) : retour [-4.79% .. +9.19%] · haut q95 +9.95% · bas q05 -6.15%
   - 4h (n=160) : retour [-5.98% .. +9.6%] · haut q95 +9.98% · bas q05 -7.39%
   - 6h (n=160) : retour [-5.66% .. +10.41%] · haut q95 +12.17% · bas q05 -8.1%
   - session (n=160) : retour [-7.13% .. +9.93%] · haut q95 +12.72% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 4.85%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.82
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 58.6  _(momentum haussier)_
- **ADX** : 11.9  _(pas de tendance nette)_
- **MACD** : hist 0.099  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 20.1%
- **ATR** : 2.02 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.035  _(neutre)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 51.9  _(transition)_
- **MA** : MA20 26.92 · MA50 27.58 · MA200 29.55  _(prix > MA20)_
- **Dist MA** : MA20 +3.5% · MA50 +1.0% · MA200 -5.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (778911 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
