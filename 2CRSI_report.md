# AL2SI

**Generated** : 2026-10-09T21:51:56.336185+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €24.80  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (5 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €24.80 (+1.8% vs entrée) · entrée €24.35 · stop €23.82 · T1 €25.40 · R/R 1.98  
> ↳ ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.17% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-09 : 24.8 · ATR Wilder 1.81 (7.31 %)_
- **Swing** : plage **22.75 → 21.44** (-8.28 % a -13.54 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 22.6-23.38 (B). stop INDICATIF 19.19 (-10.49 % sous le bas ; sous le support 20.1-20.8 (- 0,5 ATR)).
- **Deep** : plage **21.44 → 18.24** (-13.54 % a -26.44 % sous la cloture, 1.77 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 20.1-20.8 (B). stop INDICATIF 15.19 (-16.71 % sous le bas ; sous le support 16.1-16.65 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.63 ATR sous le plus haut 20 s., RSI(2) 50.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 22.6-23.38 (B, -5.73 %) ; 20.1-20.8 (B, -16.13 %) ; 16.1-16.65 (A, -32.86 %) ; 14.2-15.0 (A, -39.52 %) ; 13.0-13.24 (B, -46.61 %) ; 11.76-12.4 (A, -50.0 %)
- Resistances reelles au-dessus : 26.38-26.7 (A, 6.37 %) ; 28.18-29.0 (B, 13.63 %) ; 30.0-30.8 (A, 20.97 %) ; 30.94-31.54 (B, 24.76 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.66 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **10.726 pt plus bas** dans le cas TYPIQUE (médiane), 21.981 au p90, **27.457 au pire**
   - perte réelle **22.515 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 10.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0556 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5806** [0.5063 ; 0.6523] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4306** [0.3792 ; 0.4832] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3607** [0.3114 ; 0.4123] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.4 pt), deep (25.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.24 %** | CVaR **-11.74 %** | vol 6.33 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 3.90 % contre 7.07 % aujourd'hui, rapport 0.55)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2168** (β de hausse 0.9576, asymétrie 1.2706) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.117× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 23.5636 sur atr_grid (0.75 ATR, 4.986 %) — p(stop avant cible) 0.6785 [0.63 ; 0.73], R/R 4.137, perte reelle 5.298 % (gap inclus), CVaR 9.214 %, EV 1.1917 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3202 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.678, borne haute 0.726 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 38.2 % de la queue et il ne reste que -1251.71 EUR a partager. Prix du risque -0.354 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.33 ATR (stop 12.008 %) — p(stop avant cible) 0.3025 [0.26 ; 0.35], R/R 1.552, perte reelle 14.126 % (gap inclus), EV 2.5477 % — **REFUSE**
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.82 % > budget 12.00 %
   - 🟢 support a 2.85 ATR (stop 22.089 %) — p(stop avant cible) 0.139 [0.11 ; 0.18], R/R 0.776, perte reelle 28.261 % (gap inclus), EV 1.8048 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.14 % > budget 12.00 %
   - 🟢 support a 4.94 ATR (stop 36.0 %) — p(stop avant cible) 0.0519 [0.03 ; 0.08], R/R 0.528, perte reelle 41.543 % (gap inclus), EV 2.3374 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.76 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.662 %) — p(stop avant cible) 0.8764 [0.84 ; 0.91], R/R 12.023, perte reelle 1.823 % (gap inclus), EV 0.516 % — **REFUSE**
      - refuse : cible atteinte seulement 8.1 % du temps (< 15 %) meme a 10 seances : le R/R de 12.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.876, borne haute 0.908 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.324 %) — p(stop avant cible) 0.7645 [0.72 ; 0.81], R/R 6.11, perte reelle 3.587 % (gap inclus), EV 1.0371 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.764, borne haute 0.807 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.986 %) — p(stop avant cible) 0.6785 [0.63 ; 0.73], R/R 4.137, perte reelle 5.298 % (gap inclus), EV 1.1917 % — **REFUSE**
      - refuse : p_stop_first 0.678, borne haute 0.726 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 6.647 %) — p(stop avant cible) 0.5841 [0.53 ; 0.64], R/R 2.944, perte reelle 7.444 % (gap inclus), EV 1.2717 % — **REFUSE**
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.96 % > budget 12.00 %
   - 🟢 grid_snapped a 1.33 ATR (stop 10.865 %) — p(stop avant cible) 0.3569 [0.31 ; 0.41], R/R 1.762, perte reelle 12.437 % (gap inclus), EV 2.4604 % — **REFUSE**
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.08 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 13.295 %) — p(stop avant cible) 0.2674 [0.22 ; 0.32], R/R 1.329, perte reelle 16.487 % (gap inclus), EV 2.396 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.35 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.957 %) — p(stop avant cible) 0.2419 [0.20 ; 0.29], R/R 1.199, perte reelle 18.274 % (gap inclus), EV 2.2285 % — **REFUSE**
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.83 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.619 %) — p(stop avant cible) 0.2087 [0.17 ; 0.25], R/R 1.059, perte reelle 20.686 % (gap inclus), EV 2.1074 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.33 % > budget 12.00 %
   - 🟢 grid_snapped a 2.85 ATR (stop 20.946 %) — p(stop avant cible) 0.1447 [0.11 ; 0.18], R/R 0.802, perte reelle 27.312 % (gap inclus), EV 1.8549 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.14 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 23.266 %) — p(stop avant cible) 0.1045 [0.08 ; 0.14], R/R 0.71, perte reelle 30.89 % (gap inclus), EV 2.1513 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.14 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 26.59 %) — p(stop avant cible) 0.0894 [0.06 ; 0.12], R/R 0.651, perte reelle 33.649 % (gap inclus), EV 2.0812 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.20 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.914 %) — p(stop avant cible) 0.0803 [0.06 ; 0.11], R/R 0.609, perte reelle 35.978 % (gap inclus), EV 2.0356 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.66 % > budget 12.00 %
   - 🟢 grid_snapped a 4.94 ATR (stop 34.857 %) — p(stop avant cible) 0.0556 [0.04 ; 0.08], R/R 0.539, perte reelle 40.651 % (gap inclus), EV 2.2895 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.30 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.885 %) — p(stop avant cible) 0.0339 [0.02 ; 0.06], R/R 0.487, perte reelle 44.961 % (gap inclus), EV 2.6771 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.42 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.209 %) — p(stop avant cible) 0.0298 [0.02 ; 0.05], R/R 0.477, perte reelle 45.991 % (gap inclus), EV 2.6929 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.08 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 46.532 %) — p(stop avant cible) 0.0298 [0.02 ; 0.05], R/R 0.448, perte reelle 48.937 % (gap inclus), EV 2.6051 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.84 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 49.856 %) — p(stop avant cible) 0.0298 [0.02 ; 0.05], R/R 0.403, perte reelle 54.395 % (gap inclus), EV 2.4424 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.09 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.18 %) — p(stop avant cible) 0.0262 [0.01 ; 0.05], R/R 0.356, perte reelle 61.605 % (gap inclus), EV 2.2591 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.71 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 24.8, ATR14 1.6486 (6.647 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 2.659 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.332 % | 24.7176 | 87.06 % | 90.58 % | 92.93 % | 94.39 % | 95.55 % | 97.1 % |
| 0.1 ATR | 0.665 % | 24.6351 | 82.55 % | 87.05 % | 90.28 % | 92.13 % | 94.07 % | 96.2 % |
| 0.15 ATR | 0.997 % | 24.5527 | 78.43 % | 83.42 % | 87.23 % | 88.98 % | 92.19 % | 95.1 % |
| 0.2 ATR | 1.329 % | 24.4703 | 72.65 % | 79.29 % | 83.4 % | 85.83 % | 89.81 % | 92.91 % |
| 0.25 ATR | 1.662 % | 24.3879 | 66.67 % | 74.68 % | 79.27 % | 82.48 % | 87.54 % | 91.31 % |
| 0.35 ATR | 2.327 % | 24.223 | 54.71 % | 65.75 % | 71.12 % | 75.69 % | 82.59 % | 87.81 % |
| 0.5 ATR | 3.324 % | 23.9757 | 40.59 % | 53.88 % | 61.98 % | 68.8 % | 78.04 % | 85.41 % |
| 0.75 ATR | 4.986 % | 23.5636 | 22.75 % | 37.68 % | 47.45 % | 55.71 % | 67.16 % | 76.72 % |
| 1.0 ATR | 6.647 % | 23.1514 | 12.84 % | 25.02 % | 33.89 % | 44.29 % | 57.17 % | 68.13 % |
| 1.25 ATR | 8.309 % | 22.7393 | 7.45 % | 17.66 % | 24.66 % | 36.42 % | 50.25 % | 61.74 % |
| 1.5 ATR | 9.971 % | 22.3271 | 3.63 % | 11.38 % | 17.39 % | 28.84 % | 42.93 % | 55.34 % |
| 2.0 ATR | 13.295 % | 21.5029 | 0.88 % | 5.2 % | 9.63 % | 16.73 % | 31.26 % | 43.56 % |
| 2.5 ATR | 16.619 % | 20.6786 | 0.1 % | 2.16 % | 4.62 % | 9.74 % | 21.07 % | 33.37 % |
| 3.0 ATR | 19.942 % | 19.8543 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 15.03 % | 25.97 % |
| 4.0 ATR | 26.59 % | 18.2057 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.28 % |
| 6.0 ATR | 39.885 % | 14.9086 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.98 ATR | 2.46 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 0.98 ATR | 1.36 ATR | 1.66 ATR | 1.86 ATR | 2.48 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.26 ATR | 1.43 ATR | 1.93 ATR | 2.31 ATR | 2.59 ATR | 3.77 ATR | 5.11 ATR |
| **20 s.** | 0.80 ATR | 1.73 ATR | 1.94 ATR | 2.52 ATR | 3.11 ATR | 3.69 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.453–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.324 %, prix 23.9756), p(touche) 40.59 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (90.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.637–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.986 %, prix 23.5635), p(touche) 37.68 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.647 %, prix 23.1515), p(touche) 33.89 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.984–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.647 %, prix 23.1515), p(touche) 44.29 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.429–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.971 %, prix 22.3272), p(touche) 42.93 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.939–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.295 %, prix 21.5028), p(touche) 43.56 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.05 | EV/share : €0.027 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 — | T3 —
- Kelly (position) : f* 0.057 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 11.9 | side 83.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.824% → cible +4.33% / stop −2.165%, p_fill 68%, n_eff≈71.9) : P(cible|rempli) **15%** · **EV/risk -0.235** (×p_fill ; si rempli -0.75% du capital)
  - **swing** (entrée dip −4.012% → cible +7.743% / stop −6.926%, p_fill 48%, n_eff≈57.0) : P(cible|rempli) **43%** · **EV/risk -0.074** (×p_fill ; si rempli -1.07% du capital)
  - **deep** (entrée dip −6.198% → cible +20.435% / stop −10.631%, p_fill 50%, n_eff≈57.3) : P(cible|rempli) **16%** · **EV/risk -0.066** (×p_fill ; si rempli -1.42% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→75% · +2.0%→68% · +3.0%→53% · +5.0%→35% · +8.0%→17%
- Range intraday médian 6.98% (p90 14.96%) · excursion haute méd. +3.32% / basse méd. −3.45%
- Profil de vol intra : ouverture 4.807% vs midi 1.539% vs clôture 1.704% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 5% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -0.405% ; recovery-V 23%
- **σ réalisé intraday** 4.412% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 70% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 25.8615 (VA 25.2245–26.7435 ; dernier close 26.98)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 88% · **stop −3.68%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.6 (high win-rate)
- Gaps overnight (n=158) : méd. 0.23% · baisse 41% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −3.41%) · haut méd +0.73% · range méd 2.23%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −4.07%) · haut méd +1.39% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −4.39%) · haut méd +1.93% · range méd 3.45%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −5.59%) · haut méd +2.05% · range méd 3.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.82 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 80% (123/158) · gap 20% · délai 0.3min · rebond 62% (81/123) (MFE +1.87%)
   - −1.0% : fill 30min 50% · séance 75% (118/158) · gap 10% · délai 3.3min · rebond 60% (78/118) (MFE +1.56%)
   - −1.5% : fill 30min 43% · séance 69% (105/158) · gap 7% · délai 9.0min · rebond 58% (65/105) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 63% (97/158) · gap 4% · délai 16.0min · rebond 54% (58/97) (MFE +1.11%)
   - −3.0% : fill 30min 19% · séance 46% (79/158) · gap 2% · délai 42.4min · rebond 58% (53/79) (MFE +1.4%)
   - −4.0% : fill 30min 13% · séance 39% (68/158) · gap 1% · délai 88.4min · rebond 73% (54/68) (MFE +1.57%)
   - −5.0% : fill 30min 9% · séance 28% (53/158) · gap 1% · délai 89.9min · rebond 88% (49/53) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −3.05%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.84%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −3.92%) → stop au-delà de −2.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1483 jambes) : jambe baissière méd −1.21% (p90 −2.97%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 91% (45/47) · rebond 54% (26/45)
      · −2.0% : fill 84% (41/47) · rebond 49% (22/41)
      · −3.0% : fill 69% (37/47) · rebond 50% (25/37)
      · −4.0% : fill 61% (33/47) · rebond 58% (24/33)
      · −5.0% : fill 44% (27/47) · rebond 86% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 78% (26/34) · rebond 66% (18/26)
      · −2.0% : fill 58% (20/34) · rebond 49% (12/20)
      · −3.0% : fill 43% (16/34) · rebond 60% (10/16)
      · −4.0% : fill 40% (15/34) · rebond 77% (12/15)
      · −5.0% : fill 32% (11/34) · rebond 80% (10/11)
   - **gap-up** (77 séances) :
      · −1.0% : fill 64% (47/77) · rebond 60% (34/47)
      · −2.0% : fill 54% (36/77) · rebond 62% (24/36)
      · −3.0% : fill 34% (26/77) · rebond 67% (18/26)
      · −4.0% : fill 26% (20/77) · rebond 88% (18/20)
      · −5.0% : fill 16% (15/77) · rebond 100% (15/15)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 56% si les 15 1res min sont vertes (76 cas) · 26% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:53** → P(séance verte=clôture>ouverture) 74% si début vert vs 14% si rouge (base 41% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **74%** · continue >prix actuel 50% ; creux résiduel méd -2.8% (q20 -5.42%) → **SL/trailing à −5.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.86% / q75 +3.31% → **scale +1.86% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **14%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.93%** (au-delà de la MAE q10 -4.93%), cible rebond +1.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.2% .. +5.28%] · haut q95 +6.81% · bas q05 -5.69%
   - 60min (n=160) : retour [-5.33% .. +4.89%] · haut q95 +7.28% · bas q05 -6.85%
   - 2h (n=160) : retour [-5.2% .. +7.14%] · haut q95 +8.79% · bas q05 -7.39%
   - 4h (n=160) : retour [-6.3% .. +7.38%] · haut q95 +9.96% · bas q05 -8.17%
   - 6h (n=160) : retour [-5.99% .. +8.19%] · haut q95 +11.34% · bas q05 -8.55%
   - session (n=160) : retour [-7.17% .. +9.91%] · haut q95 +12.5% · bas q05 -9.62%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.5  _(momentum baissier)_
- **ADX** : 17.6  _(pas de tendance nette)_
- **MACD** : hist -0.522  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 26.5%
- **ATR** : 1.65 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.128  _(distribution)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 40.7  _(transition)_
- **MA** : MA20 27.72 · MA50 27.52 · MA200 28.57  _(prix < MA20)_
- **Dist MA** : MA20 -10.5% · MA50 -9.9% · MA200 -13.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (886819 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
