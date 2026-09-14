# PLTR

**Generated** : 2026-09-14T00:36:42.858627+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $167.23  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $167.23 (+0.9% vs entrée) · entrée $165.73 · stop $163.25 · T1 $168.65 · R/R 1.18  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.05 _(réel 5 s)_ (GBM 0.074) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $165.15–$166.32 (mid $165.73)
- Spot actuel : $167.23 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $163.25 (stop swing_plan-based (-6.53%))
- Targets : T1 $168.65 · R/R 1.18 | T2 $171.58 · R/R 2.36 | T3 $174.50 · R/R 3.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $163.25


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.53 %)** : le gap seul le franchit 0.877 % des séances (11 fois sur 1254).
   - exécution **3.415 pt plus bas** dans le cas TYPIQUE (médiane), 8.142 au p90, **11.402 au pire**
   - perte réelle **10.642 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 6.53 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0361 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.88 % | p01 -6.138 % | pire -17.932 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4708** [0.3974 ; 0.5451] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.384** [0.3339 ; 0.4361] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3354** [0.2872 ; 0.3864] _(largeur 9.9 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.6 pt), swing (35.2 pt), deep (34.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.09 %** | CVaR **-7.27 %** | vol 3.83 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.62 % contre 4.46 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.973 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6981** (β de hausse 1.4084, asymétrie 1.2057) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.795× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 150.0512 sur atr_grid (2.25 ATR, 10.273 %) — p(stop avant cible) 0.3039 [0.26 ; 0.35], R/R 0.803, perte reelle 13.763 % (gap inclus), CVaR 10.287 %, EV -0.5343 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.4 ATR (stop 4.365 %) — p(stop avant cible) 0.6356 [0.58 ; 0.69], R/R 1.491, perte reelle 7.412 % (gap inclus), EV -1.7149 % — **REFUSE**
      - refuse : p_stop_first 0.636, borne haute 0.685 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 23.5 % x 11.05 % + P(rien) 13.0 % x 3.10 % ne couvrent pas P(stop) 63.6 % x 7.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 0.88 ATR (stop 6.58 %) — p(stop avant cible) 0.4523 [0.40 ; 0.51], R/R 1.038, perte reelle 10.642 % (gap inclus), EV -0.9833 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 29.9 % x 11.05 % + P(rien) 24.8 % x 2.10 % ne couvrent pas P(stop) 45.2 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 2.58 ATR (stop 14.305 %) — p(stop avant cible) 0.1593 [0.12 ; 0.20], R/R 0.678, perte reelle 16.302 % (gap inclus), EV 0.2986 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.31 % > budget 12.00 %
      - ⚠ support DETECTE a 0.78 ATR du spot — compartiment <1, mesure a 46.4 % de casse (IC clusterise [0.434 ; 0.494] sur 1185 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 6.46 ATR (stop 32.047 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.345, perte reelle 32.047 % (gap inclus), EV 1.2114 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.05 % > budget 12.00 %
   - 🟢 support a 7.97 ATR (stop 38.936 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.284, perte reelle 38.936 % (gap inclus), EV 1.2163 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.94 % > budget 12.00 %
   - ⚪ grid_snapped a 0.4 ATR (stop 3.192 %) — p(stop avant cible) 0.7054 [0.66 ; 0.75], R/R 2.031, perte reelle 5.44 % (gap inclus), EV -1.203 % — **REFUSE**
      - refuse : p_stop_first 0.705, borne haute 0.752 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 20.5 % x 11.05 % + P(rien) 8.9 % x 4.08 % ne couvrent pas P(stop) 70.5 % x 5.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.88 ATR (stop 5.407 %) — p(stop avant cible) 0.5405 [0.49 ; 0.59], R/R 1.203, perte reelle 9.186 % (gap inclus), EV -1.5646 % — **REFUSE**
      - refuse : p_stop_first 0.540, borne haute 0.593 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.56 %) : P(cible) 26.0 % x 11.05 % + P(rien) 20.0 % x 2.66 % ne couvrent pas P(stop) 54.0 % x 9.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.99 %) — p(stop avant cible) 0.3714 [0.32 ; 0.42], R/R 0.922, perte reelle 11.982 % (gap inclus), EV -0.6093 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 31.1 % x 11.05 % + P(rien) 31.7 % x 1.26 % ne couvrent pas P(stop) 37.1 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.131 %) — p(stop avant cible) 0.3273 [0.28 ; 0.38], R/R 0.842, perte reelle 13.126 % (gap inclus), EV -0.5436 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 31.5 % x 11.05 % + P(rien) 35.8 % x 0.76 % ne couvrent pas P(stop) 32.7 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 10.273 %) — p(stop avant cible) 0.3039 [0.26 ; 0.35], R/R 0.803, perte reelle 13.763 % (gap inclus), EV -0.5343 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 31.6 % x 11.05 % + P(rien) 38.0 % x 0.40 % ne couvrent pas P(stop) 30.4 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 2.58 ATR (stop 13.132 %) — p(stop avant cible) 0.1943 [0.16 ; 0.24], R/R 0.678, perte reelle 16.302 % (gap inclus), EV 0.0425 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.14 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 15.979 %) — p(stop avant cible) 0.1204 [0.09 ; 0.16], R/R 0.616, perte reelle 17.932 % (gap inclus), EV 0.4846 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.98 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 18.262 %) — p(stop avant cible) 0.087 [0.06 ; 0.12], R/R 0.605, perte reelle 18.262 % (gap inclus), EV 0.754 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.26 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 20.545 %) — p(stop avant cible) 0.0493 [0.03 ; 0.08], R/R 0.538, perte reelle 20.545 % (gap inclus), EV 0.9424 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.55 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 22.828 %) — p(stop avant cible) 0.0243 [0.01 ; 0.04], R/R 0.484, perte reelle 22.828 % (gap inclus), EV 1.0942 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.83 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 25.111 %) — p(stop avant cible) 0.0072 [0.00 ; 0.02], R/R 0.44, perte reelle 25.111 % (gap inclus), EV 1.1769 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.11 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 27.393 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.403, perte reelle 27.393 % (gap inclus), EV 1.2104 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.39 % > budget 12.00 %
   - 🟢 grid_snapped a 6.46 ATR (stop 30.874 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.358, perte reelle 30.874 % (gap inclus), EV 1.1968 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.87 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 34.242 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.323, perte reelle 34.242 % (gap inclus), EV 1.2102 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.24 % > budget 12.00 %
   - 🟢 grid_snapped a 7.97 ATR (stop 37.763 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.293, perte reelle 37.763 % (gap inclus), EV 1.2136 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.76 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 167.23, ATR14 7.635 (4.566 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 1.634 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.228 % | 166.8482 | 92.45 % | 94.96 % | 95.77 % | 96.57 % | 97.87 % | 98.56 % |
| 0.1 ATR | 0.457 % | 166.4665 | 84.41 % | 89.02 % | 90.93 % | 93.13 % | 94.82 % | 96.31 % |
| 0.15 ATR | 0.685 % | 166.0847 | 76.96 % | 83.38 % | 85.69 % | 89.49 % | 92.18 % | 94.15 % |
| 0.2 ATR | 0.913 % | 165.703 | 69.11 % | 78.05 % | 81.45 % | 86.06 % | 89.95 % | 92.31 % |
| 0.25 ATR | 1.141 % | 165.3212 | 62.07 % | 73.51 % | 77.42 % | 82.73 % | 87.61 % | 90.77 % |
| 0.35 ATR | 1.598 % | 164.5577 | 50.8 % | 65.56 % | 71.07 % | 78.08 % | 83.65 % | 87.69 % |
| 0.5 ATR | 2.283 % | 163.4125 | 36.12 % | 53.07 % | 59.88 % | 69.19 % | 77.97 % | 83.18 % |
| 0.75 ATR | 3.424 % | 161.5037 | 19.42 % | 35.35 % | 44.86 % | 55.56 % | 66.9 % | 75.9 % |
| 1.0 ATR | 4.566 % | 159.595 | 8.95 % | 22.86 % | 32.76 % | 44.14 % | 56.35 % | 67.38 % |
| 1.25 ATR | 5.707 % | 157.6862 | 4.43 % | 15.41 % | 23.39 % | 34.44 % | 46.5 % | 58.67 % |
| 1.5 ATR | 6.848 % | 155.7775 | 2.11 % | 10.47 % | 17.34 % | 26.77 % | 39.8 % | 53.95 % |
| 2.0 ATR | 9.131 % | 151.96 | 0.6 % | 3.73 % | 9.38 % | 15.76 % | 28.93 % | 40.62 % |
| 2.5 ATR | 11.414 % | 148.1425 | 0.1 % | 1.51 % | 3.33 % | 9.29 % | 19.09 % | 30.15 % |
| 3.0 ATR | 13.697 % | 144.325 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.89 % | 22.56 % |
| 4.0 ATR | 18.262 % | 136.69 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.79 % |
| 6.0 ATR | 27.393 % | 121.42 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.53 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.75 ATR | 0.99 ATR | 1.21 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.58 ATR | 1.81 ATR | 2.44 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.16 ATR | 1.31 ATR | 1.81 ATR | 2.20 ATR | 2.45 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.78 ATR | 1.65 ATR | 1.84 ATR | 2.36 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.283 %, prix 163.4121), p(touche) 36.12 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.424 %, prix 161.504), p(touche) 35.35 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.424 %, prix 161.504), p(touche) 44.86 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.981–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.566 %, prix 159.5943), p(touche) 44.14 % (en stress 100.0 %)  ✅ optimum identifie (82.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.306–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.848 %, prix 155.7781), p(touche) 39.8 % (en stress 100.0 %)  ✅ optimum identifie (88.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.836–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.697 %, prix 144.3245), p(touche) 22.56 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.074 | EV/share : $0.184 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 21 % | T3 11 %
- Kelly (position) : f* 0.061 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 51.4 | side 43.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 167.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.893% → cible +1.762% / stop −1.5%, p_fill 65%, n_eff≈27.8) : P(cible|rempli) **40%** · **EV/risk -0.050** (×p_fill ; si rempli -0.11% du capital)
  - **swing** (entrée dip −1.964% → cible +3.941% / stop −4.657%, p_fill 58%, n_eff≈26.0) : P(cible|rempli) **65%** · **EV/risk +0.169** (×p_fill ; si rempli +1.36% du capital)
  - **deep** (entrée dip −3.042% → cible +5.573% / stop −7.063%, p_fill 54%, n_eff≈23.9) : P(cible|rempli) **73%** · **EV/risk +0.196** (×p_fill ; si rempli +2.57% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→49% · +3.0%→30% · +5.0%→11% · +8.0%→4%
- Range intraday médian 4.13% (p90 7.39%) · excursion haute méd. +1.92% / basse méd. −1.67%
- Profil de vol intra : ouverture 3.101% vs midi 0.751% vs clôture 0.844% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 24% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.151 ; neutre — autocorr 0.004)_ ; drift intra méd. 0.512% ; recovery-V 20%
- **σ réalisé intraday** 2.612% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 50% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 174.1906 (VA 173.9824–176.0649 ; dernier close 174.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 52% · **stop −3.93%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.27 (high win-rate)
- Gaps overnight (n=159) : méd. -0.28% · baisse 56% (gap-down >1% 30% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.97% · range méd 1.91%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.79%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −3.47%) · haut méd +1.3% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.16% (p90 −3.55%) · haut méd +1.39% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 174.33 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (119/159) · gap 42% · délai 0.0min · rebond 55% (64/119) (MFE +1.16%)
   - −1.0% : fill 30min 56% · séance 66% (109/159) · gap 30% · délai 0.0min · rebond 62% (65/109) (MFE +1.34%)
   - −1.5% : fill 30min 44% · séance 54% (91/159) · gap 20% · délai 0.1min · rebond 62% (56/91) (MFE +1.27%)
   - −2.0% : fill 30min 38% · séance 49% (80/159) · gap 10% · délai 1.4min · rebond 63% (50/80) (MFE +1.35%)
   - −3.0% : fill 30min 23% · séance 32% (58/159) · gap 6% · délai 4.6min · rebond 54% (28/58) (MFE +1.36%)
   - −4.0% : fill 30min 15% · séance 21% (39/159) · gap 3% · délai 8.2min · rebond 52% (18/39) (MFE +1.06%)
   - −5.0% : fill 30min 7% · séance 14% (28/159) · gap 1% · délai 28.8min · rebond 45% (13/28) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.72%) → stop au-delà de −1.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −1.71%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.28%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=552 jambes) : jambe baissière méd −1.07% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 89% (72/77) · rebond 61% (43/72)
      · −2.0% : fill 72% (59/77) · rebond 64% (36/59)
      · −3.0% : fill 54% (45/77) · rebond 52% (22/45)
      · −4.0% : fill 37% (32/77) · rebond 54% (15/32)
      · −5.0% : fill 26% (24/77) · rebond 50% (12/24)
   - **flat** (24 séances) :
      · −1.0% : fill 72% (20/24) · rebond 41% (9/20)
      · −2.0% : fill 57% (14/24) · rebond 62% (9/14)
      · −3.0% : fill 31% (10/24) · rebond 58% (5/10)
      · −4.0% : fill 18% (6/24) · rebond 41% (3/6)
      · −5.0% : fill 10% (3/24) · rebond 9% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 33% (17/58) · rebond 83% (13/17)
      · −2.0% : fill 15% (7/58) · rebond 57% (5/7)
      · −3.0% : fill 4% (3/58) · rebond 71% (1/3)
      · −4.0% : fill 1% (1/58) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 70% si les 15 1res min sont vertes (83 cas) · 30% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 85% si début vert vs 17% si rouge (base 52% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **85%** · continue >prix actuel 55% ; creux résiduel méd -0.84% (q20 -1.49%) → **SL/trailing à −1.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +2.18% → **scale +1.06% / runner +2.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **17%** (continue à baisser 51%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.77%** (au-delà de la MAE q10 -2.77%), cible rebond +1.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.41% .. +4.57%] · haut q95 +4.99% · bas q05 -3.97%
   - 60min (n=160) : retour [-3.45% .. +5.92%] · haut q95 +6.29% · bas q05 -4.19%
   - 2h (n=160) : retour [-4.1% .. +6.18%] · haut q95 +6.97% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.41% .. +5.88%] · haut q95 +6.96% · bas q05 -5.82%
   - 6h (n=160) : retour [-4.59% .. +6.51%] · haut q95 +7.39% · bas q05 -6.3%
   - session (n=160) : retour [-4.24% .. +5.84%] · haut q95 +7.69% · bas q05 -6.3%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 3.1% / strong 4.4%) · base = 12 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **40%**. Lecture précoce 30 min : signature présente → 19% vs absente 4% (base 8%)
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.8  _(momentum baissier)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist -3.155  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 14.2%
- **ATR** : 7.64 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.098  _(distribution)_
- **Vol ratio** : 0.54  _(volume atone)_
- **Choppiness** : 56.9  _(transition)_
- **MA** : MA20 175.55 · MA50 153.93 · MA200 151.52  _(prix < MA20)_
- **Dist MA** : MA20 -4.7% · MA50 +8.6% · MA200 +10.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (753349 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
