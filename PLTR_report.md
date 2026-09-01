# PLTR

**Generated** : 2026-09-01T22:03:39.183842+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $179.92  

> 🟡 **WAIT-FOR-DIP** — spot +11.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $179.92 (+11.1% vs entrée) · entrée $161.96 · stop $155.17 · T1 $168.49 · R/R 0.96  
> ↳ P(T1 av. stop) 77 % · EV/risk 0.362 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 126 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $160.66–$163.27 (mid $161.96)
- Spot actuel : $179.92 (+11.1% au-dessus de la zone — repli à attendre)
- Stop : $155.17 (stop swing_plan-based (-13.76%))
- Targets : T1 $168.49 · R/R 0.96 | T2 $175.02 · R/R 1.92 | T3 $181.55 · R/R 2.89
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $155.17


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.76 %)** : le gap seul le franchit 0.16 % des séances (2 fois sur 1253).
   - exécution **2.542 pt plus bas** dans le cas TYPIQUE (médiane), 3.846 au p90, **4.172 au pire**
   - perte réelle **16.302 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 13.76 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0041 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4459** [0.3733 ; 0.5203] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4523** [0.4004 ; 0.505] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.3718** [0.3221 ; 0.4236] _(largeur 10.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7082** (β de hausse 1.4133, asymétrie 1.2086) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 159.5301 sur atr_grid (3.0 ATR, 11.333 %) — p(stop avant cible) 0.2316 [0.19 ; 0.28], R/R 0.427, perte reelle 14.376 % (gap inclus), CVaR 11.343 %, EV -0.4125 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.666 %) — p(stop avant cible) 0.4597 [0.41 ; 0.51], R/R 0.633, perte reelle 9.704 % (gap inclus), EV -1.592 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 46.1 % x 6.14 % + P(rien) 7.9 % x 0.50 % ne couvrent pas P(stop) 46.0 % x 9.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.82 ATR (stop 9.26 %) — p(stop avant cible) 0.2879 [0.24 ; 0.34], R/R 0.468, perte reelle 13.126 % (gap inclus), EV -0.6691 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 53.6 % x 6.14 % + P(rien) 17.6 % x -1.03 % ne couvrent pas P(stop) 28.8 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 4.9 ATR (stop 20.904 %) — p(stop avant cible) 0.0402 [0.02 ; 0.06], R/R 0.294, perte reelle 20.904 % (gap inclus), EV 0.4924 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.90 % > budget 12.00 %
   - 🟢 support a 9.13 ATR (stop 36.856 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.167, perte reelle 36.856 % (gap inclus), EV 0.7269 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.86 % > budget 12.00 %
   - 🟢 support a 10.82 ATR (stop 43.259 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.142, perte reelle 43.259 % (gap inclus), EV 0.7279 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.26 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.944 %) — p(stop avant cible) 0.8618 [0.82 ; 0.90], R/R 2.58, perte reelle 2.379 % (gap inclus), EV -1.202 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.862, borne haute 0.895 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 13.8 % x 6.14 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 86.2 % x 2.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.889 %) — p(stop avant cible) 0.7487 [0.70 ; 0.79], R/R 1.827, perte reelle 3.36 % (gap inclus), EV -0.9743 % — **REFUSE**
      - refuse : p_stop_first 0.749, borne haute 0.792 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 25.1 % x 6.14 % + P(rien) 0.0 % x 0.48 % ne couvrent pas P(stop) 74.9 % x 3.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.833 %) — p(stop avant cible) 0.6687 [0.62 ; 0.72], R/R 1.228, perte reelle 5.0 % (gap inclus), EV -1.3331 % — **REFUSE**
      - refuse : p_stop_first 0.669, borne haute 0.717 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.33 %) : P(cible) 32.5 % x 6.14 % + P(rien) 0.6 % x 2.28 % ne couvrent pas P(stop) 66.9 % x 5.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.778 %) — p(stop avant cible) 0.5913 [0.54 ; 0.64], R/R 0.925, perte reelle 6.638 % (gap inclus), EV -1.5668 % — **REFUSE**
      - refuse : p_stop_first 0.591, borne haute 0.642 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 38.0 % x 6.14 % + P(rien) 2.8 % x 0.84 % ne couvrent pas P(stop) 59.1 % x 6.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.722 %) — p(stop avant cible) 0.51 [0.46 ; 0.56], R/R 0.762, perte reelle 8.06 % (gap inclus), EV -1.4246 % — **REFUSE**
      - refuse : p_stop_first 0.510, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 43.5 % x 6.14 % + P(rien) 5.5 % x 0.26 % ne couvrent pas P(stop) 51.0 % x 8.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.82 ATR (stop 8.014 %) — p(stop avant cible) 0.3366 [0.29 ; 0.39], R/R 0.512, perte reelle 11.982 % (gap inclus), EV -0.7877 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.79 %) : P(cible) 53.3 % x 6.14 % + P(rien) 13.0 % x -0.21 % ne couvrent pas P(stop) 33.7 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.5 %) — p(stop avant cible) 0.3118 [0.26 ; 0.36], R/R 0.49, perte reelle 12.528 % (gap inclus), EV -0.7018 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 53.5 % x 6.14 % + P(rien) 15.4 % x -0.50 % ne couvrent pas P(stop) 31.2 % x 12.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.388 %) — p(stop avant cible) 0.2713 [0.23 ; 0.32], R/R 0.446, perte reelle 13.763 % (gap inclus), EV -0.6898 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 53.8 % x 6.14 % + P(rien) 19.0 % x -1.37 % ne couvrent pas P(stop) 27.1 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.333 %) — p(stop avant cible) 0.2316 [0.19 ; 0.28], R/R 0.427, perte reelle 14.376 % (gap inclus), EV -0.4125 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 54.7 % x 6.14 % + P(rien) 22.1 % x -1.99 % ne couvrent pas P(stop) 23.2 % x 14.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 13.222 %) — p(stop avant cible) 0.1646 [0.13 ; 0.21], R/R 0.377, perte reelle 16.302 % (gap inclus), EV -0.1853 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 55.6 % x 6.14 % + P(rien) 27.9 % x -3.28 % ne couvrent pas P(stop) 16.5 % x 16.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 15.11 %) — p(stop avant cible) 0.1255 [0.09 ; 0.16], R/R 0.342, perte reelle 17.932 % (gap inclus), EV -0.0483 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 55.8 % x 6.14 % + P(rien) 31.7 % x -3.85 % ne couvrent pas P(stop) 12.6 % x 17.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 16.999 %) — p(stop avant cible) 0.1058 [0.08 ; 0.14], R/R 0.342, perte reelle 17.932 % (gap inclus), EV 0.1727 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.00 % > budget 12.00 %
   - ⚪ grid_snapped a 4.9 ATR (stop 19.657 %) — p(stop avant cible) 0.0557 [0.04 ; 0.08], R/R 0.312, perte reelle 19.657 % (gap inclus), EV 0.4627 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.66 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.666 %) — p(stop avant cible) 0.0233 [0.01 ; 0.04], R/R 0.271, perte reelle 22.666 % (gap inclus), EV 0.5997 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.67 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.554 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 0.25, perte reelle 24.554 % (gap inclus), EV 0.6702 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.55 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.443 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.232, perte reelle 26.443 % (gap inclus), EV 0.7026 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.44 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.332 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.217, perte reelle 28.332 % (gap inclus), EV 0.718 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.33 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.221 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.203, perte reelle 30.221 % (gap inclus), EV 0.7121 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.22 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 179.92, ATR14 6.7966 (3.778 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.356 ATR = 1.345 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 179.5802 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.67 % |
| 0.1 ATR | 0.378 % | 179.2403 | 84.39 % | 89.01 % | 90.82 % | 93.02 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.567 % | 178.9005 | 76.94 % | 83.37 % | 85.57 % | 89.38 % | 92.17 % | 94.25 % |
| 0.2 ATR | 0.756 % | 178.5607 | 68.88 % | 77.92 % | 81.23 % | 85.95 % | 89.94 % | 92.4 % |
| 0.25 ATR | 0.944 % | 178.2208 | 61.83 % | 73.39 % | 77.19 % | 82.71 % | 87.6 % | 90.86 % |
| 0.35 ATR | 1.322 % | 177.5412 | 50.55 % | 65.42 % | 70.94 % | 78.06 % | 83.64 % | 87.78 % |
| 0.5 ATR | 1.889 % | 176.5217 | 36.15 % | 52.82 % | 59.64 % | 69.16 % | 78.05 % | 83.37 % |
| 0.75 ATR | 2.833 % | 174.8225 | 19.34 % | 35.18 % | 44.6 % | 55.51 % | 67.07 % | 76.18 % |
| 1.0 ATR | 3.778 % | 173.1234 | 8.96 % | 22.78 % | 32.59 % | 44.08 % | 56.5 % | 67.86 % |
| 1.25 ATR | 4.722 % | 171.4242 | 4.43 % | 15.42 % | 23.31 % | 34.48 % | 46.75 % | 59.24 % |
| 1.5 ATR | 5.666 % | 169.725 | 2.01 % | 10.38 % | 17.36 % | 26.59 % | 40.04 % | 54.41 % |
| 2.0 ATR | 7.555 % | 166.3267 | 0.6 % | 3.63 % | 9.18 % | 15.47 % | 28.96 % | 40.66 % |
| 2.5 ATR | 9.444 % | 162.9284 | 0.1 % | 1.41 % | 3.13 % | 9.0 % | 19.11 % | 30.18 % |
| 3.0 ATR | 11.333 % | 159.5301 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 15.11 % | 152.7334 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 22.666 % | 139.1401 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.53 ATR | 1.90 ATR |
| **3 s.** | 0.28 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.95 ATR | 2.35 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.57 ATR | 1.80 ATR | 2.42 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.31 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.66 ATR | 1.84 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.889 %, prix 176.5213), p(touche) 36.15 % (en stress 82.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.833 %, prix 174.8229), p(touche) 35.18 % (en stress 95.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.743–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.833 %, prix 174.8229), p(touche) 44.6 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.98–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.778 %, prix 173.1226), p(touche) 44.08 % (en stress 100.0 %)  ✅ optimum identifie (83.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.315–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.666 %, prix 169.7257), p(touche) 40.04 % (en stress 100.0 %)  ✅ optimum identifie (90.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.842–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (11.333 %, prix 159.5297), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.03 | EV/share : $-0.202 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 22 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 25.5 | side 69.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 540.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→51% · +3.0%→30% · +5.0%→10% · +8.0%→4%
- Range intraday médian 4.01% (p90 7.17%) · excursion haute méd. +2.11% / basse méd. −1.51%
- Profil de vol intra : ouverture 3.034% vs midi 0.747% vs clôture 0.84% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑1%/↓0% ; spike-down 51% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr -0.017)_ ; drift intra méd. 0.787% ; recovery-V 26%
- **σ réalisé intraday** 2.567% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 44% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 187.1612 (VA 185.8288–187.5713 ; dernier close 186.38)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 67% · **stop −3.79%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 55% (gap-down >1% 26% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.09%) · haut méd +0.97% · range méd 1.91%
- Excursion ouverture 15min (n=160) : bas méd −0.81% (p90 −2.84%) · haut méd +1.2% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −3.49%) · haut méd +1.29% · range méd 2.68%
- Excursion ouverture 60min (n=160) : bas méd −1.16% (p90 −3.58%) · haut méd +1.39% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 186.38 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (118/159) · gap 39% · délai 0.0min · rebond 59% (66/118) (MFE +1.23%)
   - −1.0% : fill 30min 54% · séance 66% (108/159) · gap 26% · délai 0.0min · rebond 65% (65/108) (MFE +1.53%)
   - −1.5% : fill 30min 41% · séance 52% (89/159) · gap 18% · délai 0.3min · rebond 65% (56/89) (MFE +1.38%)
   - −2.0% : fill 30min 35% · séance 47% (78/159) · gap 11% · délai 1.4min · rebond 67% (50/78) (MFE +1.37%)
   - −3.0% : fill 30min 21% · séance 29% (56/159) · gap 6% · délai 3.6min · rebond 58% (28/56) (MFE +1.8%)
   - −4.0% : fill 30min 14% · séance 19% (38/159) · gap 3% · délai 8.2min · rebond 53% (18/38) (MFE +1.09%)
   - −5.0% : fill 30min 8% · séance 13% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −1.85%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.71%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.35%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=549 jambes) : jambe baissière méd −1.06% (p90 −2.46%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 88% (70/75) · rebond 65% (42/70)
      · −2.0% : fill 69% (56/75) · rebond 69% (35/56)
      · −3.0% : fill 48% (42/75) · rebond 57% (21/42)
      · −4.0% : fill 33% (30/75) · rebond 56% (14/30)
      · −5.0% : fill 25% (23/75) · rebond 58% (12/23)
   - **flat** (25 séances) :
      · −1.0% : fill 72% (21/25) · rebond 42% (10/21)
      · −2.0% : fill 57% (15/25) · rebond 63% (10/15)
      · −3.0% : fill 32% (11/25) · rebond 59% (6/11)
      · −4.0% : fill 19% (7/25) · rebond 44% (4/7)
      · −5.0% : fill 10% (3/25) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 34% (17/59) · rebond 83% (13/17)
      · −2.0% : fill 16% (7/59) · rebond 57% (5/7)
      · −3.0% : fill 4% (3/59) · rebond 71% (1/3)
      · −4.0% : fill 1% (1/59) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/59) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 72% si les 15 1res min sont vertes (83 cas) · 32% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 22% si rouge (base 54% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **86%** · continue >prix actuel 58% ; creux résiduel méd -0.86% (q20 -1.61%) → **SL/trailing à −1.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +2.22% → **scale +1.2% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **22%** (continue à baisser 44%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.48%** (au-delà de la MAE q10 -2.48%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.46% .. +3.81%] · haut q95 +4.05% · bas q05 -4.02%
   - 60min (n=160) : retour [-3.6% .. +3.93%] · haut q95 +4.78% · bas q05 -4.25%
   - 2h (n=160) : retour [-3.78% .. +5.39%] · haut q95 +5.92% · bas q05 -4.52%
   - 4h (n=160) : retour [-4.04% .. +5.64%] · haut q95 +6.47% · bas q05 -5.21%
   - 6h (n=160) : retour [-4.09% .. +5.82%] · haut q95 +6.83% · bas q05 -5.57%
   - session (n=160) : retour [-4.03% .. +4.94%] · haut q95 +6.83% · bas q05 -5.57%


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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 58.3  _(momentum haussier)_
- **ADX** : 36.2  _(tendance etablie)_
- **MACD** : hist -0.389  _(pas de croisement recent)_
- **BB** : %B 0.66 · largeur 17.7%
- **ATR** : 6.8 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.047  _(neutre)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 60.1  _(transition)_
- **MA** : MA20 174.92 · MA50 146.11 · MA200 151.33  _(prix > MA20)_
- **Dist MA** : MA20 +2.9% · MA50 +23.1% · MA200 +18.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (777666 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
