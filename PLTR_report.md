# PLTR

**Generated** : 2026-09-02T22:03:42.969399+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $169.46  

> 🟡 **WAIT-FOR-DIP** — spot +2.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $169.46 (+2.7% vs entrée) · entrée $164.94 · stop $157.76 · T1 $172.09 · R/R 1.0  
> ↳ P(T1 av. stop) 62 % _(réel 5 s)_ · EV/risk 0.2 _(réel 5 s)_ (GBM -0.024) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $163.51–$166.37 (mid $164.94)
- Spot actuel : $169.46 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : $157.76 (stop swing_plan-based (-6.9%))
- Targets : T1 $172.09 · R/R 1.0 | T2 $179.23 · R/R 1.99 | T3 $186.38 · R/R 2.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $157.76


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.9 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **3.727 pt plus bas** dans le cas TYPIQUE (médiane), 8.098 au p90, **11.032 au pire**
   - perte réelle **11.024 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 6.9 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0329 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3471** [0.2792 ; 0.4201] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.4329** [0.3814 ; 0.4855] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3873** [0.3371 ; 0.4394] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.7 pt), swing (40.7 pt), deep (42.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.707** (β de hausse 1.4119, asymétrie 1.209) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 149.7203 sur atr_grid (2.75 ATR, 11.649 %) — p(stop avant cible) 0.2432 [0.20 ; 0.29], R/R 0.669, perte reelle 14.376 % (gap inclus), CVaR 11.658 %, EV -0.0388 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.28 ATR (stop 3.262 %) — p(stop avant cible) 0.6902 [0.64 ; 0.74], R/R 1.728, perte reelle 5.563 % (gap inclus), EV -1.2439 % — **REFUSE**
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 23.9 % x 9.61 % + P(rien) 7.0 % x 4.18 % ne couvrent pas P(stop) 69.0 % x 5.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.24 ATR (stop 7.356 %) — p(stop avant cible) 0.3911 [0.34 ; 0.44], R/R 0.802, perte reelle 11.982 % (gap inclus), EV -0.848 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 35.9 % x 9.61 % + P(rien) 24.9 % x 1.53 % ne couvrent pas P(stop) 39.1 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.05 ATR (stop 15.007 %) — p(stop avant cible) 0.1411 [0.11 ; 0.18], R/R 0.536, perte reelle 17.932 % (gap inclus), EV 0.2139 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.01 % > budget 12.00 %
   - 🟢 support a 7.18 ATR (stop 32.516 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.296, perte reelle 32.516 % (gap inclus), EV 1.1458 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.52 % > budget 12.00 %
   - 🟢 support a 8.79 ATR (stop 39.314 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.245, perte reelle 39.314 % (gap inclus), EV 1.1529 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.31 % > budget 12.00 %
   - ⚪ grid_snapped a 0.28 ATR (stop 2.448 %) — p(stop avant cible) 0.7543 [0.71 ; 0.80], R/R 2.201, perte reelle 4.368 % (gap inclus), EV -1.1153 % — **REFUSE**
      - refuse : p_stop_first 0.754, borne haute 0.797 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 20.6 % x 9.61 % + P(rien) 4.0 % x 4.99 % ne couvrent pas P(stop) 75.4 % x 4.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.24 ATR (stop 6.543 %) — p(stop avant cible) 0.4514 [0.40 ; 0.50], R/R 0.903, perte reelle 10.642 % (gap inclus), EV -1.1076 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 33.9 % x 9.61 % + P(rien) 20.9 % x 2.08 % ne couvrent pas P(stop) 45.1 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.472 %) — p(stop avant cible) 0.3457 [0.30 ; 0.40], R/R 0.767, perte reelle 12.528 % (gap inclus), EV -0.5716 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 36.3 % x 9.61 % + P(rien) 29.2 % x 0.93 % ne couvrent pas P(stop) 34.6 % x 12.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.531 %) — p(stop avant cible) 0.3169 [0.27 ; 0.37], R/R 0.732, perte reelle 13.126 % (gap inclus), EV -0.5016 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 36.5 % x 9.61 % + P(rien) 31.9 % x 0.48 % ne couvrent pas P(stop) 31.7 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.59 %) — p(stop avant cible) 0.2922 [0.25 ; 0.34], R/R 0.699, perte reelle 13.763 % (gap inclus), EV -0.5015 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 36.6 % x 9.61 % + P(rien) 34.2 % x 0.01 % ne couvrent pas P(stop) 29.2 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.649 %) — p(stop avant cible) 0.2432 [0.20 ; 0.29], R/R 0.669, perte reelle 14.376 % (gap inclus), EV -0.0388 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 37.7 % x 9.61 % + P(rien) 38.0 % x -0.43 % ne couvrent pas P(stop) 24.3 % x 14.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.05 ATR (stop 14.194 %) — p(stop avant cible) 0.1638 [0.13 ; 0.21], R/R 0.59, perte reelle 16.302 % (gap inclus), EV 0.188 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.20 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 16.943 %) — p(stop avant cible) 0.1085 [0.08 ; 0.14], R/R 0.536, perte reelle 17.932 % (gap inclus), EV 0.5752 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.94 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 19.061 %) — p(stop avant cible) 0.0701 [0.05 ; 0.10], R/R 0.504, perte reelle 19.061 % (gap inclus), EV 0.8102 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.06 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.179 %) — p(stop avant cible) 0.0374 [0.02 ; 0.06], R/R 0.454, perte reelle 21.179 % (gap inclus), EV 0.9458 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.18 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 23.297 %) — p(stop avant cible) 0.019 [0.01 ; 0.04], R/R 0.413, perte reelle 23.297 % (gap inclus), EV 1.0494 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.30 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 25.415 %) — p(stop avant cible) 0.0072 [0.00 ; 0.02], R/R 0.378, perte reelle 25.415 % (gap inclus), EV 1.1146 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.41 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 27.533 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.349, perte reelle 27.533 % (gap inclus), EV 1.1449 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.53 % > budget 12.00 %
   - 🟢 grid_snapped a 7.18 ATR (stop 31.703 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.303, perte reelle 31.703 % (gap inclus), EV 1.1405 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.70 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 33.887 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.284, perte reelle 33.887 % (gap inclus), EV 1.1486 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.89 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 169.46, ATR14 7.1781 (4.236 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 1.512 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.212 % | 169.1011 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.67 % |
| 0.1 ATR | 0.424 % | 168.7422 | 84.49 % | 89.11 % | 90.92 % | 93.12 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.635 % | 168.3833 | 77.04 % | 83.47 % | 85.67 % | 89.48 % | 92.17 % | 94.25 % |
| 0.2 ATR | 0.847 % | 168.0244 | 68.98 % | 78.02 % | 81.33 % | 86.05 % | 89.94 % | 92.4 % |
| 0.25 ATR | 1.059 % | 167.6655 | 61.93 % | 73.49 % | 77.3 % | 82.71 % | 87.6 % | 90.86 % |
| 0.35 ATR | 1.483 % | 166.9477 | 50.65 % | 65.52 % | 71.04 % | 78.06 % | 83.64 % | 87.78 % |
| 0.5 ATR | 2.118 % | 165.871 | 36.15 % | 52.92 % | 59.74 % | 69.16 % | 77.95 % | 83.37 % |
| 0.75 ATR | 3.177 % | 164.0765 | 19.34 % | 35.18 % | 44.7 % | 55.51 % | 66.97 % | 76.18 % |
| 1.0 ATR | 4.236 % | 162.2819 | 8.96 % | 22.78 % | 32.59 % | 44.08 % | 56.5 % | 67.97 % |
| 1.25 ATR | 5.295 % | 160.4874 | 4.43 % | 15.42 % | 23.31 % | 34.48 % | 46.75 % | 59.24 % |
| 1.5 ATR | 6.354 % | 158.6929 | 2.01 % | 10.38 % | 17.36 % | 26.59 % | 40.04 % | 54.41 % |
| 2.0 ATR | 8.472 % | 155.1039 | 0.6 % | 3.63 % | 9.18 % | 15.47 % | 28.96 % | 40.66 % |
| 2.5 ATR | 10.59 % | 151.5148 | 0.1 % | 1.41 % | 3.13 % | 9.0 % | 19.11 % | 30.18 % |
| 3.0 ATR | 12.708 % | 147.9258 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 16.943 % | 140.7477 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 25.415 % | 126.3916 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.53 ATR | 1.90 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.95 ATR | 2.35 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.57 ATR | 1.80 ATR | 2.42 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.31 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.66 ATR | 1.84 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.118 %, prix 165.8708), p(touche) 36.15 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.612–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.177 %, prix 164.0763), p(touche) 35.18 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.745–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.177 %, prix 164.0763), p(touche) 44.7 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.98–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.236 %, prix 162.2817), p(touche) 44.08 % (en stress 100.0 %)  ✅ optimum identifie (82.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.315–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.354 %, prix 158.6925), p(touche) 40.04 % (en stress 100.0 %)  ✅ optimum identifie (89.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.842–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (12.708 %, prix 147.925), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : $-0.170 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 20 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 49.9 | side 45.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 508.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.209% → cible +4.536% / stop −2.268%, p_fill 51%, n_eff≈23.4) : P(cible|rempli) **2%** · **EV/risk -0.075** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −2.664% → cible +4.332% / stop −4.352%, p_fill 43%, n_eff≈19.5) : P(cible|rempli) **62%** · **EV/risk +0.200** (×p_fill ; si rempli +2.01% du capital)
  - **deep** (entrée dip −4.116% → cible +6.126% / stop −6.627%, p_fill 35%, n_eff≈19.0) : P(cible|rempli) **57%** · **EV/risk +0.040** (×p_fill ; si rempli +0.75% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→51% · +3.0%→30% · +5.0%→10% · +8.0%→4%
- Range intraday médian 4.01% (p90 7.17%) · excursion haute méd. +2.11% / basse méd. −1.51%
- Profil de vol intra : ouverture 3.044% vs midi 0.75% vs clôture 0.834% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr -0.01)_ ; drift intra méd. 0.674% ; recovery-V 24%
- **σ réalisé intraday** 2.556% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 47% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 183.1935 (VA 181.3565–184.1955 ; dernier close 179.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 68% · **stop −3.78%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 55% (gap-down >1% 28% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.08%) · haut méd +0.96% · range méd 1.9%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.83%) · haut méd +1.2% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.0% (p90 −3.49%) · haut méd +1.31% · range méd 2.68%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.57%) · haut méd +1.43% · range méd 2.99%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 179.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 77% (118/159) · gap 40% · délai 0.0min · rebond 58% (65/118) (MFE +1.23%)
   - −1.0% : fill 30min 55% · séance 66% (108/159) · gap 28% · délai 0.0min · rebond 66% (65/108) (MFE +1.45%)
   - −1.5% : fill 30min 42% · séance 53% (89/159) · gap 20% · délai 0.1min · rebond 66% (56/89) (MFE +1.49%)
   - −2.0% : fill 30min 37% · séance 48% (78/159) · gap 11% · délai 1.4min · rebond 68% (50/78) (MFE +1.39%)
   - −3.0% : fill 30min 20% · séance 30% (56/159) · gap 6% · délai 4.6min · rebond 55% (27/56) (MFE +1.37%)
   - −4.0% : fill 30min 14% · séance 18% (37/159) · gap 3% · délai 7.7min · rebond 53% (17/37) (MFE +1.07%)
   - −5.0% : fill 30min 8% · séance 13% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.79%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.71%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.35%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.08% (p90 −2.44%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 88% (71/76) · rebond 67% (43/71)
      · −2.0% : fill 70% (57/76) · rebond 71% (36/57)
      · −3.0% : fill 50% (43/76) · rebond 53% (21/43)
      · −4.0% : fill 32% (30/76) · rebond 56% (14/30)
      · −5.0% : fill 24% (23/76) · rebond 58% (12/23)
   - **flat** (24 séances) :
      · −1.0% : fill 72% (20/24) · rebond 41% (9/20)
      · −2.0% : fill 57% (14/24) · rebond 62% (9/14)
      · −3.0% : fill 31% (10/24) · rebond 58% (5/10)
      · −4.0% : fill 18% (6/24) · rebond 41% (3/6)
      · −5.0% : fill 10% (3/24) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 34% (17/59) · rebond 83% (13/17)
      · −2.0% : fill 16% (7/59) · rebond 57% (5/7)
      · −3.0% : fill 4% (3/59) · rebond 71% (1/3)
      · −4.0% : fill 1% (1/59) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/59) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 69% si les 15 1res min sont vertes (83 cas) · 32% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 84% si début vert vs 18% si rouge (base 53% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **84%** · continue >prix actuel 54% ; creux résiduel méd -0.9% (q20 -1.56%) → **SL/trailing à −1.56%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.18% → **scale +1.18% / runner +2.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 47%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.59%** (au-delà de la MAE q10 -2.59%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.43% .. +3.79%] · haut q95 +4.05% · bas q05 -4.01%
   - 60min (n=160) : retour [-3.6% .. +3.93%] · haut q95 +4.78% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.75% .. +5.35%] · haut q95 +5.72% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.03% .. +5.64%] · haut q95 +6.42% · bas q05 -5.15%
   - 6h (n=160) : retour [-4.04% .. +5.75%] · haut q95 +6.82% · bas q05 -5.52%
   - session (n=160) : retour [-4.02% .. +4.89%] · haut q95 +6.82% · bas q05 -5.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 3.1% / strong 4.4%) · base = 12 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 20% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.13% / p90 1.49%) · ~2.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 43.27 min, n=37)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.49%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +4.31% (q75 +7.51% / q95 +12.13%), MFE méd +5.25% / q90 +12.03%
   - Échelle scale-out : +5.25% (33%) / +7.95% (33%) / +12.03% (34%)
- **DÉSARMER** : repli > **−1.49%** depuis le plus-haut = décay → P(retournement) **82%** (préavis méd 214.54 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.03% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 58% du temps (retour médian dernière heure +0.19%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.5  _(momentum baissier)_
- **ADX** : 33.9  _(tendance etablie)_
- **MACD** : hist -1.474  _(bearish_recent)_
- **BB** : %B 0.28 · largeur 15.6%
- **ATR** : 7.18 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.113  _(accumulation)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 56.4  _(transition)_
- **MA** : MA20 175.47 · MA50 147.17 · MA200 151.31  _(prix < MA20)_
- **Dist MA** : MA20 -3.4% · MA50 +15.1% · MA200 +12.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (486909 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
