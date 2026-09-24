# SMCI

**Generated** : 2026-09-24T00:34:36.405027+00:00  
**Santé technique** : 10/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $41.43  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $41.43 (+0.8% vs entrée) · entrée $41.12 · stop $38.74 · T1 $43.29 · R/R 0.91  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.311 _(réel 5 s)_ (GBM 0.049) · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $40.81–$41.43 (mid $41.12)
- Spot actuel : $41.43 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $38.74 (stop swing_plan-based (-6.5%))
- Targets : T1 $43.29 · R/R 0.91 | T2 $45.47 · R/R 1.83 | T3 $47.64 · R/R 2.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $38.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.5 %)** : le gap seul le franchit 1.915 % des séances (24 fois sur 1253).
   - exécution **4.733 pt plus bas** dans le cas TYPIQUE (médiane), 16.493 au p90, **22.551 au pire**
   - perte réelle **12.976 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 6.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.124 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.553** [0.4786 ; 0.6257] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4461** [0.3943 ; 0.4988] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3966** [0.3461 ; 0.4489] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.7 pt), swing (31.5 pt), deep (31.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.85 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.79 % contre 6.52 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5271** (β de hausse 1.2233, asymétrie 1.2483) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.839× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 36.6643 sur atr_grid (2.0 ATR, 11.503 %) — p(stop avant cible) 0.3444 [0.30 ; 0.40], R/R 0.837, perte reelle 17.9 % (gap inclus), CVaR 11.559 %, EV -1.0704 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 46.9 % de la queue et il ne reste que -384.52 EUR a partager. Prix du risque -0.123 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.24 ATR (stop 4.188 %) — p(stop avant cible) 0.7121 [0.66 ; 0.76], R/R 1.713, perte reelle 8.745 % (gap inclus), EV -2.8688 % — **REFUSE**
      - refuse : p_stop_first 0.712, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.87 %) : P(cible) 19.7 % x 14.98 % + P(rien) 9.1 % x 4.50 % ne couvrent pas P(stop) 71.2 % x 8.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 0.82 ATR (stop 7.555 %) — p(stop avant cible) 0.5316 [0.48 ; 0.58], R/R 1.106, perte reelle 13.549 % (gap inclus), EV -2.5494 % — **REFUSE**
      - refuse : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.14 ATR du spot — compartiment <1, mesure a 46.2 % de casse (IC clusterise [0.431 ; 0.493] sur 1171 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.55 %) : P(cible) 27.6 % x 14.98 % + P(rien) 19.2 % x 2.68 % ne couvrent pas P(stop) 53.2 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.75 ATR (stop 18.626 %) — p(stop avant cible) 0.1483 [0.11 ; 0.19], R/R 0.601, perte reelle 24.92 % (gap inclus), EV 0.9749 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.65 % > budget 12.00 %
   - 🟢 support a 7.57 ATR (stop 46.392 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.323, perte reelle 46.392 % (gap inclus), EV 1.252 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.39 % > budget 12.00 %
   - 🟢 support a 9.21 ATR (stop 55.805 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.269, perte reelle 55.805 % (gap inclus), EV 1.2403 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.81 % > budget 12.00 %
   - ⚪ grid_snapped a 0.24 ATR (stop 3.089 %) — p(stop avant cible) 0.7873 [0.74 ; 0.83], R/R 2.303, perte reelle 6.506 % (gap inclus), EV -2.4548 % — **REFUSE**
      - refuse : p_stop_first 0.787, borne haute 0.828 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 16.2 % x 14.98 % + P(rien) 5.1 % x 4.79 % ne couvrent pas P(stop) 78.7 % x 6.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.82 ATR (stop 6.456 %) — p(stop avant cible) 0.603 [0.55 ; 0.65], R/R 1.155, perte reelle 12.976 % (gap inclus), EV -3.6386 % — **REFUSE**
      - refuse : p_stop_first 0.603, borne haute 0.653 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.64 %) : P(cible) 24.9 % x 14.98 % + P(rien) 14.8 % x 3.08 % ne couvrent pas P(stop) 60.3 % x 12.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 8.627 %) — p(stop avant cible) 0.4618 [0.41 ; 0.51], R/R 1.06, perte reelle 14.137 % (gap inclus), EV -1.7023 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.70 %) : P(cible) 29.0 % x 14.98 % + P(rien) 24.8 % x 1.94 % ne couvrent pas P(stop) 46.2 % x 14.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.065 %) — p(stop avant cible) 0.4166 [0.37 ; 0.47], R/R 0.888, perte reelle 16.875 % (gap inclus), EV -2.0505 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 30.2 % x 14.98 % + P(rien) 28.1 % x 1.60 % ne couvrent pas P(stop) 41.7 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.503 %) — p(stop avant cible) 0.3444 [0.30 ; 0.40], R/R 0.837, perte reelle 17.9 % (gap inclus), EV -1.0704 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 31.4 % x 14.98 % + P(rien) 34.2 % x 1.15 % ne couvrent pas P(stop) 34.4 % x 17.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 12.941 %) — p(stop avant cible) 0.2816 [0.24 ; 0.33], R/R 0.78, perte reelle 19.221 % (gap inclus), EV -0.3286 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 32.7 % x 14.98 % + P(rien) 39.1 % x 0.46 % ne couvrent pas P(stop) 28.2 % x 19.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.75 ATR (stop 17.527 %) — p(stop avant cible) 0.1677 [0.13 ; 0.21], R/R 0.601, perte reelle 24.92 % (gap inclus), EV 0.6879 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.55 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.13 %) — p(stop avant cible) 0.1343 [0.10 ; 0.17], R/R 0.558, perte reelle 26.856 % (gap inclus), EV 0.9762 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.15 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.006 %) — p(stop avant cible) 0.1126 [0.08 ; 0.15], R/R 0.558, perte reelle 26.856 % (gap inclus), EV 1.2737 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.02 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.882 %) — p(stop avant cible) 0.0864 [0.06 ; 0.12], R/R 0.536, perte reelle 27.955 % (gap inclus), EV 1.4134 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.89 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.758 %) — p(stop avant cible) 0.079 [0.05 ; 0.11], R/R 0.516, perte reelle 29.051 % (gap inclus), EV 1.3629 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.76 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.633 %) — p(stop avant cible) 0.0713 [0.05 ; 0.10], R/R 0.474, perte reelle 31.633 % (gap inclus), EV 1.2061 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.63 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.509 %) — p(stop avant cible) 0.0618 [0.04 ; 0.09], R/R 0.434, perte reelle 34.509 % (gap inclus), EV 1.0839 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.385 %) — p(stop avant cible) 0.0459 [0.03 ; 0.07], R/R 0.401, perte reelle 37.385 % (gap inclus), EV 1.0767 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.38 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.261 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 0.372, perte reelle 40.261 % (gap inclus), EV 1.2501 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.26 % > budget 12.00 %
   - 🟢 grid_snapped a 7.57 ATR (stop 45.293 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.331, perte reelle 45.293 % (gap inclus), EV 1.2536 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.29 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 41.43, ATR14 2.3829 (5.752 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.343 ATR = 1.973 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.288 % | 41.3109 | 90.43 % | 93.25 % | 94.65 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.575 % | 41.1917 | 82.07 % | 87.2 % | 89.2 % | 91.2 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.863 % | 41.0726 | 74.92 % | 82.06 % | 84.96 % | 88.27 % | 90.65 % | 93.53 % |
| 0.2 ATR | 1.15 % | 40.9534 | 67.98 % | 77.32 % | 80.52 % | 85.74 % | 89.13 % | 92.2 % |
| 0.25 ATR | 1.438 % | 40.8343 | 61.93 % | 72.78 % | 76.39 % | 82.41 % | 87.09 % | 90.45 % |
| 0.35 ATR | 2.013 % | 40.596 | 49.14 % | 63.51 % | 69.73 % | 77.25 % | 82.83 % | 87.78 % |
| 0.5 ATR | 2.876 % | 40.2386 | 34.94 % | 50.1 % | 58.63 % | 68.86 % | 77.03 % | 83.47 % |
| 0.75 ATR | 4.314 % | 39.6429 | 17.42 % | 33.37 % | 43.19 % | 55.21 % | 66.46 % | 75.26 % |
| 1.0 ATR | 5.752 % | 39.0471 | 8.06 % | 21.67 % | 30.68 % | 43.78 % | 57.22 % | 68.48 % |
| 1.25 ATR | 7.189 % | 38.4514 | 3.83 % | 15.02 % | 22.5 % | 33.27 % | 48.07 % | 61.19 % |
| 1.5 ATR | 8.627 % | 37.8557 | 1.51 % | 9.68 % | 16.45 % | 26.19 % | 41.87 % | 54.93 % |
| 2.0 ATR | 11.503 % | 36.6643 | 0.3 % | 3.53 % | 8.38 % | 16.18 % | 29.88 % | 43.63 % |
| 2.5 ATR | 14.379 % | 35.4729 | 0.2 % | 1.51 % | 4.34 % | 9.81 % | 19.61 % | 31.83 % |
| 3.0 ATR | 17.255 % | 34.2814 | 0.2 % | 1.21 % | 2.62 % | 5.66 % | 14.13 % | 24.02 % |
| 4.0 ATR | 23.006 % | 31.8986 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 34.509 % | 27.1329 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.58 ATR | 0.76 ATR | 0.93 ATR | 1.06 ATR | 1.49 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.17 ATR | 1.35 ATR | 1.90 ATR | 2.42 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.56 ATR | 1.81 ATR | 2.48 ATR | 3.22 ATR |
| **10 s.** | 0.55 ATR | 1.20 ATR | 1.37 ATR | 1.87 ATR | 2.24 ATR | 2.48 ATR | 3.62 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.72 ATR | 1.94 ATR | 2.45 ATR | 2.94 ATR | 3.41 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.576–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.314 %, prix 39.6427), p(touche) 33.37 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.721–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.314 %, prix 39.6427), p(touche) 43.19 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 15.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.189 %, prix 38.4516), p(touche) 33.27 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.374–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.627 %, prix 37.8558), p(touche) 41.87 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.939–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (17.255 %, prix 34.2813), p(touche) 24.02 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.049 | EV/share : $0.116 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 31 % | T3 20 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 82.5 | bear 6.5 | side 11.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 621.0 (= 15 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.384% → cible +2.362% / stop −1.732%, p_fill 93%, n_eff≈37.9) : P(cible|rempli) **46%** · **EV/risk +0.104** (×p_fill ; si rempli +0.20% du capital)
  - **swing** (entrée dip −0.749% → cible +5.282% / stop −5.795%, p_fill 87%, n_eff≈35.2) : P(cible|rempli) **32%** · **EV/risk -0.311** (×p_fill ; si rempli -2.06% du capital)
  - **deep** (entrée dip −1.083% → cible +7.47% / stop −8.721%, p_fill 90%, n_eff≈35.0) : P(cible|rempli) **54%** · **EV/risk +0.027** (×p_fill ; si rempli +0.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→92% · +1.0%→76% · +2.0%→61% · +3.0%→46% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.2% (p90 10.79%) · excursion haute méd. +2.57% / basse méd. −2.36%
- Profil de vol intra : ouverture 4.155% vs midi 1.244% vs clôture 1.619% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.019)_ ; drift intra méd. 0.322% ; recovery-V 35%
- **σ réalisé intraday** 3.833% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 40.5704 (VA 39.4716–40.8634 ; dernier close 39.59)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 81% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.59% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 45% (gap-down >1% 36% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.79%) · haut méd +0.96% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.21%) · haut méd +1.42% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −3.93%) · haut méd +1.5% · range méd 3.68%
- Excursion ouverture 60min (n=160) : bas méd −1.72% (p90 −4.91%) · haut méd +1.81% · range méd 4.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (120/159) · gap 42% · délai 0.0min · rebond 58% (73/120) (MFE +1.37%)
   - −1.0% : fill 30min 55% · séance 69% (111/159) · gap 36% · délai 0.0min · rebond 62% (67/111) (MFE +1.61%)
   - −1.5% : fill 30min 49% · séance 63% (101/159) · gap 22% · délai 0.0min · rebond 71% (66/101) (MFE +1.61%)
   - −2.0% : fill 30min 43% · séance 55% (88/159) · gap 17% · délai 0.5min · rebond 74% (58/88) (MFE +1.91%)
   - −3.0% : fill 30min 31% · séance 48% (75/159) · gap 10% · délai 7.1min · rebond 63% (47/75) (MFE +1.9%)
   - −4.0% : fill 30min 17% · séance 36% (57/159) · gap 5% · délai 36.7min · rebond 78% (38/57) (MFE +1.88%)
   - −5.0% : fill 30min 13% · séance 27% (46/159) · gap 3% · délai 42.5min · rebond 81% (34/46) (MFE +2.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.79%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.95%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.74% (p90 −2.73%) → stop au-delà de −2.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=897 jambes) : jambe baissière méd −1.19% (p90 −2.87%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 97% (68/70) · rebond 50% (36/68)
      · −2.0% : fill 92% (64/70) · rebond 70% (39/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (35/58)
      · −4.0% : fill 65% (45/70) · rebond 78% (30/45)
      · −5.0% : fill 49% (37/70) · rebond 80% (27/37)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 40% (30/76) · rebond 77% (20/30)
      · −2.0% : fill 24% (18/76) · rebond 84% (15/18)
      · −3.0% : fill 16% (14/76) · rebond 70% (9/14)
      · −4.0% : fill 12% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 11% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 64% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:47** → P(séance verte=clôture>ouverture) 80% si début vert vs 9% si rouge (base 47% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=87) : tient le vert **80%** · continue >prix actuel 48% ; creux résiduel méd -1.35% (q20 -3.0%) → **SL/trailing à −3.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.95% → **scale +1.8% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **9%** (continue à baisser 48%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.18% .. +4.68%] · haut q95 +5.63% · bas q05 -4.48%
   - 60min (n=160) : retour [-4.4% .. +5.2%] · haut q95 +6.46% · bas q05 -5.33%
   - 2h (n=160) : retour [-4.66% .. +6.65%] · haut q95 +7.25% · bas q05 -5.84%
   - 4h (n=160) : retour [-5.17% .. +7.01%] · haut q95 +8.34% · bas q05 -6.68%
   - 6h (n=160) : retour [-5.44% .. +6.82%] · haut q95 +9.16% · bas q05 -6.9%
   - session (n=160) : retour [-6.74% .. +7.68%] · haut q95 +9.32% · bas q05 -7.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.61%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 60.1  _(momentum haussier)_
- **ADX** : 25.9  _(tendance etablie)_
- **MACD** : hist 0.137  _(bullish_recent)_
- **BB** : %B 0.9 · largeur 18.7%
- **ATR** : 2.38 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.008  _(neutre)_
- **Vol ratio** : 1.0  _(volume normal)_
- **Choppiness** : 57.4  _(transition)_
- **MA** : MA20 38.54 · MA50 34.37 · MA200 31.72  _(prix > MA20)_
- **Dist MA** : MA20 +7.5% · MA50 +20.5% · MA200 +30.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841953 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
