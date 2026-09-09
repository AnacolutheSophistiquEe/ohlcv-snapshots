# PLTR

**Generated** : 2026-09-09T00:39:31.132376+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $170.29  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $170.29 (+3.0% vs entrée) · entrée $165.31 · stop $156.97 · T1 $172.19 · R/R 0.82  
> ↳ P(T1 av. stop) 69 % _(réel 5 s)_ · EV/risk 0.159 _(réel 5 s)_ (GBM -0.044) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.1 % ≠ (strike 172.5 − spot 170.29)/spot = +1.3 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $163.94–$166.69 (mid $165.31)
- Spot actuel : $170.29 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : $156.97 (stop swing_plan-based (-7.82%))
- Targets : T1 $172.19 · R/R 0.82 | T2 $179.06 · R/R 1.65 | T3 $185.93 · R/R 2.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $156.97


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.82 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1253).
   - exécution **3.898 pt plus bas** dans le cas TYPIQUE (médiane), 7.83 au p90, **10.112 au pire**
   - perte réelle **11.982 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 7.82 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0266 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4063** [0.3352 ; 0.4805] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3571** [0.308 ; 0.4086] _(largeur 10.1 pt, n_eff 345.7)_
   - deep : **0.3285** [0.2806 ; 0.3793] _(largeur 9.9 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (39.3 pt), swing (38.9 pt), deep (42.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.09 %** | CVaR **-7.27 %** | vol 3.84 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.71 % contre 4.47 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6994** (β de hausse 1.4109, asymétrie 1.2045) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 151.5187 sur atr_grid (2.25 ATR, 11.023 %) — p(stop avant cible) 0.2606 [0.22 ; 0.31], R/R 0.726, perte reelle 13.763 % (gap inclus), CVaR 11.034 %, EV -0.0969 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.75 ATR (stop 5.849 %) — p(stop avant cible) 0.487 [0.43 ; 0.54], R/R 1.03, perte reelle 9.704 % (gap inclus), EV -1.1682 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 31.2 % x 9.99 % + P(rien) 20.1 % x 2.20 % ne couvrent pas P(stop) 48.7 % x 9.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.18 ATR (stop 7.982 %) — p(stop avant cible) 0.3691 [0.32 ; 0.42], R/R 0.834, perte reelle 11.982 % (gap inclus), EV -0.5926 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 34.5 % x 9.99 % + P(rien) 28.6 % x 1.33 % ne couvrent pas P(stop) 36.9 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.72 ATR (stop 15.528 %) — p(stop avant cible) 0.1274 [0.10 ; 0.17], R/R 0.557, perte reelle 17.932 % (gap inclus), EV 0.4533 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.53 % > budget 12.00 %
   - 🟢 support a 6.28 ATR (stop 32.951 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.303, perte reelle 32.951 % (gap inclus), EV 1.2192 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.95 % > budget 12.00 %
   - 🔴 support a 7.66 ATR (stop 39.716 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.252, perte reelle 39.716 % (gap inclus), EV 1.2249 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.72 % > budget 12.00 %
      - ⚠ support DETECTE a 7.66 ATR du spot — compartiment >=6, mesure a 46.2 % de casse (IC clusterise [0.333 ; 0.612] sur 52 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 1.225 %) — p(stop avant cible) 0.8809 [0.84 ; 0.91], R/R 3.71, perte reelle 2.694 % (gap inclus), EV -1.247 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.881, borne haute 0.912 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 10.7 % x 9.99 % + P(rien) 1.2 % x 4.69 % ne couvrent pas P(stop) 88.1 % x 2.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.75 ATR (stop 5.139 %) — p(stop avant cible) 0.5474 [0.49 ; 0.60], R/R 1.142, perte reelle 8.752 % (gap inclus), EV -1.433 % — **REFUSE**
      - refuse : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.43 %) : P(cible) 29.1 % x 9.99 % + P(rien) 16.2 % x 2.80 % ne couvrent pas P(stop) 54.7 % x 8.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.18 ATR (stop 7.272 %) — p(stop avant cible) 0.3908 [0.34 ; 0.44], R/R 0.872, perte reelle 11.461 % (gap inclus), EV -0.6035 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 34.4 % x 9.99 % + P(rien) 26.5 % x 1.64 % ne couvrent pas P(stop) 39.1 % x 11.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.798 %) — p(stop avant cible) 0.3097 [0.26 ; 0.36], R/R 0.761, perte reelle 13.126 % (gap inclus), EV -0.3746 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 35.0 % x 9.99 % + P(rien) 34.0 % x 0.56 % ne couvrent pas P(stop) 31.0 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.023 %) — p(stop avant cible) 0.2606 [0.22 ; 0.31], R/R 0.726, perte reelle 13.763 % (gap inclus), EV -0.0969 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 35.6 % x 9.99 % + P(rien) 38.4 % x -0.17 % ne couvrent pas P(stop) 26.1 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.72 ATR (stop 14.818 %) — p(stop avant cible) 0.1448 [0.11 ; 0.18], R/R 0.557, perte reelle 17.932 % (gap inclus), EV 0.2218 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.82 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.147 %) — p(stop avant cible) 0.1065 [0.08 ; 0.14], R/R 0.557, perte reelle 17.932 % (gap inclus), EV 0.6563 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.15 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 19.597 %) — p(stop avant cible) 0.0573 [0.04 ; 0.09], R/R 0.51, perte reelle 19.597 % (gap inclus), EV 0.9499 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.60 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.046 %) — p(stop avant cible) 0.0294 [0.02 ; 0.05], R/R 0.453, perte reelle 22.046 % (gap inclus), EV 1.0804 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.496 %) — p(stop avant cible) 0.009 [0.00 ; 0.02], R/R 0.408, perte reelle 24.496 % (gap inclus), EV 1.1734 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.50 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 26.945 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.371, perte reelle 26.945 % (gap inclus), EV 1.1981 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.95 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 29.395 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.34, perte reelle 29.395 % (gap inclus), EV 1.2122 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.39 % > budget 12.00 %
   - 🟢 grid_snapped a 6.28 ATR (stop 32.241 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.31, perte reelle 32.241 % (gap inclus), EV 1.2206 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.24 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.294 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.291, perte reelle 34.294 % (gap inclus), EV 1.219 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.29 % > budget 12.00 %
   - 🔴 grid_snapped a 7.66 ATR (stop 39.006 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.256, perte reelle 39.006 % (gap inclus), EV 1.2249 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.01 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 170.29, ATR14 8.3428 (4.899 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 1.754 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.245 % | 169.8729 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.56 % |
| 0.1 ATR | 0.49 % | 169.4557 | 84.39 % | 89.01 % | 90.92 % | 93.12 % | 94.82 % | 96.3 % |
| 0.15 ATR | 0.735 % | 169.0386 | 76.94 % | 83.37 % | 85.67 % | 89.48 % | 92.17 % | 94.15 % |
| 0.2 ATR | 0.98 % | 168.6214 | 68.98 % | 78.02 % | 81.43 % | 86.05 % | 89.94 % | 92.3 % |
| 0.25 ATR | 1.225 % | 168.2043 | 61.93 % | 73.49 % | 77.4 % | 82.71 % | 87.6 % | 90.76 % |
| 0.35 ATR | 1.715 % | 167.37 | 50.76 % | 65.52 % | 71.14 % | 78.06 % | 83.64 % | 87.68 % |
| 0.5 ATR | 2.45 % | 166.1186 | 36.25 % | 53.02 % | 59.94 % | 69.16 % | 77.95 % | 83.16 % |
| 0.75 ATR | 3.674 % | 164.0329 | 19.54 % | 35.38 % | 44.9 % | 55.51 % | 66.97 % | 75.87 % |
| 1.0 ATR | 4.899 % | 161.9472 | 9.06 % | 22.98 % | 32.8 % | 44.08 % | 56.4 % | 67.66 % |
| 1.25 ATR | 6.124 % | 159.8615 | 4.53 % | 15.62 % | 23.51 % | 34.48 % | 46.54 % | 58.93 % |
| 1.5 ATR | 7.349 % | 157.7758 | 2.11 % | 10.58 % | 17.56 % | 26.79 % | 39.94 % | 54.21 % |
| 2.0 ATR | 9.798 % | 153.6044 | 0.6 % | 3.73 % | 9.38 % | 15.67 % | 28.96 % | 40.66 % |
| 2.5 ATR | 12.248 % | 149.433 | 0.1 % | 1.51 % | 3.33 % | 9.2 % | 19.11 % | 30.18 % |
| 3.0 ATR | 14.697 % | 145.2616 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 19.597 % | 136.9188 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 29.395 % | 120.2333 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.21 ATR | 1.40 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.58 ATR | 1.80 ATR | 2.44 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.16 ATR | 1.31 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.78 ATR | 1.66 ATR | 1.84 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.45 %, prix 166.1179), p(touche) 36.25 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.674 %, prix 164.0335), p(touche) 35.38 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.674 %, prix 164.0335), p(touche) 44.9 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.98–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.899 %, prix 161.9475), p(touche) 44.08 % (en stress 100.0 %)  ✅ optimum identifie (83.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.308–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.349 %, prix 157.7754), p(touche) 39.94 % (en stress 100.0 %)  ✅ optimum identifie (89.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.84–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (14.697 %, prix 145.2625), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.044 | EV/share : $-0.364 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 21 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 34.8 | side 60.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 511.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.33% → cible +4.176% / stop −2.088%, p_fill 51%, n_eff≈21.2) : P(cible|rempli) **2%** · **EV/risk -0.153** (×p_fill ; si rempli -0.63% du capital)
  - **swing** (entrée dip −2.921% → cible +4.157% / stop −5.047%, p_fill 37%, n_eff≈19.4) : P(cible|rempli) **69%** · **EV/risk +0.159** (×p_fill ; si rempli +2.14% du capital)
  - **deep** (entrée dip −4.511% → cible +5.879% / stop −7.696%, p_fill 33%, n_eff≈15.4) : P(cible|rempli) **71%** · **EV/risk +0.123** (×p_fill ; si rempli +2.91% du capital)
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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.2  _(neutre)_
- **ADX** : 29.7  _(tendance etablie)_
- **MACD** : hist -2.346  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 12.1%
- **ATR** : 8.34 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.034  _(neutre)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 62.1  _(marche en range (choppy))_
- **MA** : MA20 176.67 · MA50 151.04 · MA200 151.39  _(prix < MA20)_
- **Dist MA** : MA20 -3.6% · MA50 +12.7% · MA200 +12.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (758097 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
