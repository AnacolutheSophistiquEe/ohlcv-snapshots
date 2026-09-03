# PLTR

**Generated** : 2026-09-03T22:04:32.816282+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $182.53  

> 🟡 **WAIT-FOR-DIP** — spot +5.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $182.53 (+5.1% vs entrée) · entrée $173.72 · stop $171.11 · T1 $177.37 · R/R 1.4  
> ↳ P(T1 av. stop) 44 % · EV/risk 0.068 · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 129 % hors [0,100] (R² max 0.38). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $172.98–$174.45 (mid $173.72)
- Spot actuel : $182.53 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : $171.11 (stop swing_plan-based (-14.95%))
- Targets : T1 $177.37 · R/R 1.4 | T2 $181.02 · R/R 2.8 | T3 $184.68 · R/R 4.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $171.11


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.95 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **2.982 pt plus bas** dans le cas TYPIQUE (médiane), 2.982 au p90, **2.982 au pire**
   - perte réelle **17.932 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 14.95 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0024 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4796** [0.406 ; 0.5538] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3783** [0.3284 ; 0.4303] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3535** [0.3045 ; 0.4049] _(largeur 10.0 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7062** (β de hausse 1.4035, asymétrie 1.2157) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 160.828 sur atr_grid (2.75 ATR, 11.89 %) — p(stop avant cible) 0.1789 [0.14 ; 0.22], R/R 0.309, perte reelle 14.376 % (gap inclus), CVaR 11.898 %, EV 0.0858 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.485 %) — p(stop avant cible) 0.3194 [0.27 ; 0.37], R/R 0.431, perte reelle 10.298 % (gap inclus), EV -0.4423 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 63.5 % x 4.44 % + P(rien) 4.6 % x 0.61 % ne couvrent pas P(stop) 31.9 % x 10.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.93 ATR (stop 10.45 %) — p(stop avant cible) 0.2198 [0.18 ; 0.27], R/R 0.323, perte reelle 13.763 % (gap inclus), EV -0.2172 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 67.2 % x 4.44 % + P(rien) 10.8 % x -1.65 % ne couvrent pas P(stop) 22.0 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 4.57 ATR (stop 21.867 %) — p(stop avant cible) 0.0302 [0.02 ; 0.05], R/R 0.203, perte reelle 21.867 % (gap inclus), EV 0.7071 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.87 % > budget 12.00 %
   - 🟢 support a 8.19 ATR (stop 37.532 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.118, perte reelle 37.532 % (gap inclus), EV 0.8788 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.53 % > budget 12.00 %
   - 🟢 support a 9.65 ATR (stop 43.843 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.101, perte reelle 43.843 % (gap inclus), EV 0.8777 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.84 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.081 %) — p(stop avant cible) 0.8024 [0.76 ; 0.84], R/R 1.752, perte reelle 2.535 % (gap inclus), EV -1.1565 % — **REFUSE**
      - refuse : p_stop_first 0.802, borne haute 0.842 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 19.8 % x 4.44 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 80.2 % x 2.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.162 %) — p(stop avant cible) 0.6595 [0.61 ; 0.71], R/R 1.142, perte reelle 3.89 % (gap inclus), EV -1.0533 % — **REFUSE**
      - refuse : p_stop_first 0.659, borne haute 0.708 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 34.1 % x 4.44 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 66.0 % x 3.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.243 %) — p(stop avant cible) 0.5537 [0.50 ; 0.61], R/R 0.816, perte reelle 5.44 % (gap inclus), EV -1.0301 % — **REFUSE**
      - refuse : p_stop_first 0.554, borne haute 0.606 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 44.6 % x 4.44 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 55.4 % x 5.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.323 %) — p(stop avant cible) 0.4627 [0.41 ; 0.52], R/R 0.608, perte reelle 7.302 % (gap inclus), EV -1.0186 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 53.2 % x 4.44 % + P(rien) 0.5 % x -0.68 % ne couvrent pas P(stop) 46.3 % x 7.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.404 %) — p(stop avant cible) 0.3825 [0.33 ; 0.43], R/R 0.483, perte reelle 9.186 % (gap inclus), EV -0.8882 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 58.8 % x 4.44 % + P(rien) 3.0 % x 0.53 % ne couvrent pas P(stop) 38.2 % x 9.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.93 ATR (stop 9.629 %) — p(stop avant cible) 0.2306 [0.19 ; 0.28], R/R 0.338, perte reelle 13.126 % (gap inclus), EV -0.1769 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 67.0 % x 4.44 % + P(rien) 9.9 % x -1.27 % ne couvrent pas P(stop) 23.1 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.89 %) — p(stop avant cible) 0.1789 [0.14 ; 0.22], R/R 0.309, perte reelle 14.376 % (gap inclus), EV 0.0858 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 12.97 %) — p(stop avant cible) 0.1394 [0.11 ; 0.18], R/R 0.272, perte reelle 16.302 % (gap inclus), EV 0.1203 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 15.132 %) — p(stop avant cible) 0.1011 [0.07 ; 0.14], R/R 0.248, perte reelle 17.932 % (gap inclus), EV 0.2785 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.13 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 17.294 %) — p(stop avant cible) 0.0831 [0.06 ; 0.12], R/R 0.248, perte reelle 17.932 % (gap inclus), EV 0.4791 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ grid_snapped a 4.57 ATR (stop 21.046 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.211, perte reelle 21.046 % (gap inclus), EV 0.7073 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 23.779 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.187, perte reelle 23.779 % (gap inclus), EV 0.8232 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.78 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 25.941 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.171, perte reelle 25.941 % (gap inclus), EV 0.8309 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.94 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 28.103 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.158, perte reelle 28.103 % (gap inclus), EV 0.8695 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.10 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 30.264 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.147, perte reelle 30.264 % (gap inclus), EV 0.863 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.26 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 32.426 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.137, perte reelle 32.426 % (gap inclus), EV 0.8755 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.43 % > budget 12.00 %
   - 🟢 grid_snapped a 8.19 ATR (stop 36.71 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.121, perte reelle 36.71 % (gap inclus), EV 0.8754 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.71 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 182.53, ATR14 7.8916 (4.323 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 1.548 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.216 % | 182.1354 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.67 % |
| 0.1 ATR | 0.432 % | 181.7408 | 84.49 % | 89.11 % | 90.92 % | 93.12 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.649 % | 181.3463 | 77.04 % | 83.47 % | 85.67 % | 89.48 % | 92.17 % | 94.25 % |
| 0.2 ATR | 0.865 % | 180.9517 | 68.98 % | 78.02 % | 81.33 % | 86.05 % | 89.94 % | 92.4 % |
| 0.25 ATR | 1.081 % | 180.5571 | 61.93 % | 73.49 % | 77.3 % | 82.71 % | 87.6 % | 90.86 % |
| 0.35 ATR | 1.513 % | 179.7679 | 50.76 % | 65.52 % | 71.04 % | 78.06 % | 83.64 % | 87.78 % |
| 0.5 ATR | 2.162 % | 178.5842 | 36.25 % | 53.02 % | 59.84 % | 69.16 % | 77.95 % | 83.26 % |
| 0.75 ATR | 3.243 % | 176.6113 | 19.44 % | 35.28 % | 44.8 % | 55.51 % | 66.97 % | 76.08 % |
| 1.0 ATR | 4.323 % | 174.6384 | 9.06 % | 22.88 % | 32.69 % | 44.08 % | 56.5 % | 67.86 % |
| 1.25 ATR | 5.404 % | 172.6654 | 4.53 % | 15.52 % | 23.41 % | 34.48 % | 46.65 % | 59.14 % |
| 1.5 ATR | 6.485 % | 170.6925 | 2.11 % | 10.48 % | 17.46 % | 26.69 % | 39.94 % | 54.31 % |
| 2.0 ATR | 8.647 % | 166.7467 | 0.6 % | 3.73 % | 9.28 % | 15.47 % | 28.96 % | 40.66 % |
| 2.5 ATR | 10.809 % | 162.8009 | 0.1 % | 1.51 % | 3.23 % | 9.0 % | 19.11 % | 30.18 % |
| 3.0 ATR | 12.97 % | 158.8551 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 17.294 % | 150.9634 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 25.941 % | 135.1801 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.75 ATR | 0.99 ATR | 1.21 ATR | 1.39 ATR | 1.96 ATR | 2.35 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.57 ATR | 1.80 ATR | 2.42 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.31 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.78 ATR | 1.66 ATR | 1.84 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.162 %, prix 178.5837), p(touche) 36.25 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.243 %, prix 176.6106), p(touche) 35.28 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.747–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.243 %, prix 176.6106), p(touche) 44.8 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.98–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.323 %, prix 174.6392), p(touche) 44.08 % (en stress 100.0 %)  ✅ optimum identifie (83.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.311–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.485 %, prix 170.6929), p(touche) 39.94 % (en stress 100.0 %)  ✅ optimum identifie (89.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.841–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (12.97 %, prix 158.8559), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.114 | EV/share : $0.297 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 16 % | T3 10 %
- Kelly (position) : f* 0.055 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.0 | bear 38.0 | side 10.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 548.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.6  _(momentum haussier)_
- **ADX** : 32.6  _(tendance etablie)_
- **MACD** : hist -1.34  _(bearish_recent)_
- **BB** : %B 0.77 · largeur 11.8%
- **ATR** : 7.89 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.129  _(accumulation)_
- **Vol ratio** : 1.07  _(volume normal)_
- **Choppiness** : 60.0  _(transition)_
- **MA** : MA20 176.8 · MA50 148.55 · MA200 151.36  _(prix > MA20)_
- **Dist MA** : MA20 +3.2% · MA50 +22.9% · MA200 +20.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (750373 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
