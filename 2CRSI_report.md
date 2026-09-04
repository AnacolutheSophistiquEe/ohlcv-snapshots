# AL2SI

**Generated** : 2026-09-04T21:47:13.973034+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €28.76  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €28.76 (+0.5% vs entrée) · entrée €28.61 · stop €26.33 · T1 €29.16 · R/R 0.24  
> ↳ P(T1 av. stop) 52 % _(réel 5 s)_ · EV/risk -0.058 _(réel 5 s)_ (GBM -0.026) · ¼-Kelly 0.061 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 1308 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €28.51–€28.72 (mid €28.61)
- Spot actuel : €28.76 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €26.33 (stop swing_plan-based (-6.08%))
- Targets : T1 €29.16 · R/R 0.24 | T2 €29.70 · R/R 0.48 | T3 €30.25 · R/R 0.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.33


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.08 %)** : le gap seul le franchit 1.25 % des séances (16 fois sur 1280).
   - exécution **3.289 pt plus bas** dans le cas TYPIQUE (médiane), 19.909 au p90, **32.037 au pire**
   - perte réelle **13.415 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 6.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0917 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0857** [0.0508 ; 0.1343] _(largeur 8.4 pt, n_eff 173.1)_
   - swing : **0.441** [0.3893 ; 0.4936] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4163** [0.3652 ; 0.4688] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.6 pt), swing (31.6 pt), deep (32.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.28 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.13 % contre 7.27 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2175** (β de hausse 0.9486, asymétrie 1.2835) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.955× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 26.26 sur atr_grid (1.75 ATR, 8.693 %) — p(stop avant cible) 0.4537 [0.40 ; 0.51], R/R 0.633, perte reelle 18.187 % (gap inclus), CVaR 8.76 %, EV -3.1726 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.41 ATR (stop 4.411 %) — p(stop avant cible) 0.6549 [0.60 ; 0.70], R/R 1.036, perte reelle 11.112 % (gap inclus), EV -3.5998 % — **REFUSE**
      - refuse : p_stop_first 0.655, borne haute 0.704 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 30.9 % x 11.51 % + P(rien) 3.6 % x 3.29 % ne couvrent pas P(stop) 65.5 % x 11.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.451 %) — p(stop avant cible) 0.5218 [0.47 ; 0.57], R/R 0.734, perte reelle 15.687 % (gap inclus), EV -3.5514 % — **REFUSE**
      - refuse : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.55 %) : P(cible) 39.1 % x 11.51 % + P(rien) 8.8 % x 1.55 % ne couvrent pas P(stop) 52.2 % x 15.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.41 ATR (stop 14.355 %) — p(stop avant cible) 0.2627 [0.22 ; 0.31], R/R 0.467, perte reelle 24.668 % (gap inclus), EV -1.0416 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 49.2 % x 11.51 % + P(rien) 24.5 % x -0.92 % ne couvrent pas P(stop) 26.3 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.31 ATR (stop 23.813 %) — p(stop avant cible) 0.1192 [0.09 ; 0.16], R/R 0.383, perte reelle 30.031 % (gap inclus), EV 0.5104 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.83 % > budget 12.00 %
   - 🟢 grid_snapped a 0.41 ATR (stop 3.507 %) — p(stop avant cible) 0.7086 [0.66 ; 0.75], R/R 1.376, perte reelle 8.366 % (gap inclus), EV -2.7531 % — **REFUSE**
      - refuse : p_stop_first 0.709, borne haute 0.755 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.75 %) : P(cible) 26.9 % x 11.51 % + P(rien) 2.3 % x 3.59 % ne couvrent pas P(stop) 70.9 % x 8.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 6.209 %) — p(stop avant cible) 0.5681 [0.52 ; 0.62], R/R 0.828, perte reelle 13.9 % (gap inclus), EV -3.5313 % — **REFUSE**
      - refuse : p_stop_first 0.568, borne haute 0.620 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.53 %) : P(cible) 36.5 % x 11.51 % + P(rien) 6.7 % x 2.45 % ne couvrent pas P(stop) 56.8 % x 13.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.693 %) — p(stop avant cible) 0.4537 [0.40 ; 0.51], R/R 0.633, perte reelle 18.187 % (gap inclus), EV -3.1726 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.17 %) : P(cible) 42.9 % x 11.51 % + P(rien) 11.8 % x 1.24 % ne couvrent pas P(stop) 45.4 % x 18.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.934 %) — p(stop avant cible) 0.3821 [0.33 ; 0.43], R/R 0.511, perte reelle 22.515 % (gap inclus), EV -3.2912 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.29 %) : P(cible) 46.2 % x 11.51 % + P(rien) 15.6 % x -0.06 % ne couvrent pas P(stop) 38.2 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.41 ATR (stop 13.451 %) — p(stop avant cible) 0.2712 [0.23 ; 0.32], R/R 0.467, perte reelle 24.668 % (gap inclus), EV -1.2151 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 49.1 % x 11.51 % + P(rien) 23.8 % x -0.73 % ne couvrent pas P(stop) 27.1 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 17.385 %) — p(stop avant cible) 0.2115 [0.17 ; 0.26], R/R 0.426, perte reelle 27.014 % (gap inclus), EV -0.6364 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 49.4 % x 11.51 % + P(rien) 29.5 % x -2.05 % ne couvrent pas P(stop) 21.1 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 19.869 %) — p(stop avant cible) 0.1694 [0.13 ; 0.21], R/R 0.383, perte reelle 30.031 % (gap inclus), EV -0.3304 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 49.8 % x 11.51 % + P(rien) 33.2 % x -2.94 % ne couvrent pas P(stop) 16.9 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.31 ATR (stop 22.909 %) — p(stop avant cible) 0.1298 [0.10 ; 0.17], R/R 0.383, perte reelle 30.031 % (gap inclus), EV 0.3308 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.93 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.836 %) — p(stop avant cible) 0.1103 [0.08 ; 0.15], R/R 0.353, perte reelle 32.641 % (gap inclus), EV 0.3362 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.85 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.32 %) — p(stop avant cible) 0.1028 [0.07 ; 0.14], R/R 0.302, perte reelle 38.117 % (gap inclus), EV -0.1467 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 49.8 % x 11.51 % + P(rien) 39.9 % x -4.92 % ne couvrent pas P(stop) 10.3 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 29.803 %) — p(stop avant cible) 0.0927 [0.07 ; 0.13], R/R 0.302, perte reelle 38.117 % (gap inclus), EV 0.0556 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.81 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.287 %) — p(stop avant cible) 0.0842 [0.06 ; 0.12], R/R 0.302, perte reelle 38.117 % (gap inclus), EV 0.2194 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.771 %) — p(stop avant cible) 0.0642 [0.04 ; 0.09], R/R 0.302, perte reelle 38.117 % (gap inclus), EV 0.6678 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.77 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.254 %) — p(stop avant cible) 0.0582 [0.04 ; 0.09], R/R 0.302, perte reelle 38.117 % (gap inclus), EV 0.8067 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.25 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 39.738 %) — p(stop avant cible) 0.0392 [0.02 ; 0.06], R/R 0.29, perte reelle 39.738 % (gap inclus), EV 1.1065 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.74 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 28.76, ATR14 1.4286 (4.967 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 1.987 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.248 % | 28.6886 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.497 % | 28.6171 | 82.45 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 95.9 % |
| 0.15 ATR | 0.745 % | 28.5457 | 78.43 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.71 % |
| 0.2 ATR | 0.993 % | 28.4743 | 72.55 % | 79.2 % | 83.2 % | 85.73 % | 89.42 % | 92.51 % |
| 0.25 ATR | 1.242 % | 28.4029 | 66.47 % | 74.58 % | 79.08 % | 82.38 % | 87.14 % | 90.91 % |
| 0.35 ATR | 1.739 % | 28.26 | 54.51 % | 65.75 % | 70.92 % | 75.69 % | 82.29 % | 87.61 % |
| 0.5 ATR | 2.484 % | 28.0457 | 40.88 % | 54.07 % | 61.89 % | 68.8 % | 77.74 % | 85.11 % |
| 0.75 ATR | 3.725 % | 27.6886 | 22.84 % | 37.78 % | 47.84 % | 55.81 % | 66.86 % | 76.42 % |
| 1.0 ATR | 4.967 % | 27.3314 | 13.04 % | 25.42 % | 34.38 % | 44.88 % | 57.27 % | 68.23 % |
| 1.25 ATR | 6.209 % | 26.9743 | 7.75 % | 17.86 % | 25.05 % | 36.52 % | 50.35 % | 62.04 % |
| 1.5 ATR | 7.451 % | 26.6171 | 3.82 % | 11.48 % | 17.78 % | 28.84 % | 43.32 % | 55.94 % |
| 2.0 ATR | 9.934 % | 25.9029 | 0.88 % | 5.3 % | 9.82 % | 17.13 % | 31.85 % | 44.36 % |
| 2.5 ATR | 12.418 % | 25.1886 | 0.1 % | 2.36 % | 4.91 % | 10.43 % | 22.06 % | 34.57 % |
| 3.0 ATR | 14.902 % | 24.4743 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.02 % | 27.27 % |
| 4.0 ATR | 19.869 % | 23.0457 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 18.58 % |
| 6.0 ATR | 29.803 % | 20.1886 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 8.89 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.01 ATR | 1.18 ATR | 1.62 ATR | 2.05 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.25 ATR | 1.42 ATR | 1.99 ATR | 2.49 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 1.00 ATR | 1.36 ATR | 1.66 ATR | 1.88 ATR | 2.56 ATR | 3.52 ATR |
| **10 s.** | 0.56 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.35 ATR | 2.67 ATR | 3.92 ATR | 5.28 ATR |
| **20 s.** | 0.79 ATR | 1.76 ATR | 1.97 ATR | 2.61 ATR | 3.26 ATR | 3.84 ATR | 5.77 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.455–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.484 %, prix 28.0456), p(touche) 40.88 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (91.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.639–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.725 %, prix 27.6887), p(touche) 37.78 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.967 %, prix 27.3315), p(touche) 34.38 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.997–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.967 %, prix 27.3315), p(touche) 44.88 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.44–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.451 %, prix 26.6171), p(touche) 43.32 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.972–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.934 %, prix 25.903), p(touche) 44.36 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.026 | EV/share : €-0.060 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 66 % | T2 49 % | T3 41 %
- Kelly (position) : f* 0.243 | ¼-Kelly 0.061 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 6.3 | side 8.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 374.0 (= 13 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.5% → cible +1.902% / stop −8.0%, p_fill 87%, n_eff≈35.9) : P(cible|rempli) **52%** · **EV/risk -0.058** (×p_fill ; si rempli -0.54% du capital)
  - **swing** (entrée dip −1.113% → cible +4.254% / stop −5.023%, p_fill 83%, n_eff≈36.0) : P(cible|rempli) **43%** · **EV/risk -0.168** (×p_fill ; si rempli -1.02% du capital)
  - **deep** (entrée dip −1.719% → cible +6.015% / stop −7.581%, p_fill 83%, n_eff≈34.6) : P(cible|rempli) **49%** · **EV/risk -0.045** (×p_fill ; si rempli -0.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→75% · +2.0%→66% · +3.0%→52% · +5.0%→42% · +8.0%→20%
- Range intraday médian 7.5% (p90 22.19%) · excursion haute méd. +3.87% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.305% vs midi 1.705% vs clôture 1.811% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.096)_ ; drift intra méd. -0.368% ; recovery-V 21%
- **σ réalisé intraday** 5.086% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 72% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 25.5693 (VA 25.5693–25.7103 ; dernier close 25.66)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 89% · **stop −5.18%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 41% (gap-down >1% 13% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −4.35%) · haut méd +0.77% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −5.24%) · haut méd +1.24% · range méd 3.08%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −5.56%) · haut méd +1.94% · range méd 3.94%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −6.11%) · haut méd +2.06% · range méd 4.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 25.72 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 79% (122/159) · gap 22% · délai 0.3min · rebond 63% (84/122) (MFE +2.11%)
   - −1.0% : fill 30min 50% · séance 75% (116/159) · gap 13% · délai 1.2min · rebond 62% (78/116) (MFE +1.88%)
   - −1.5% : fill 30min 42% · séance 68% (103/159) · gap 9% · délai 6.7min · rebond 60% (64/103) (MFE +1.45%)
   - −2.0% : fill 30min 36% · séance 62% (95/159) · gap 5% · délai 13.6min · rebond 62% (60/95) (MFE +1.56%)
   - −3.0% : fill 30min 23% · séance 52% (81/159) · gap 4% · délai 41.0min · rebond 61% (58/81) (MFE +1.55%)
   - −4.0% : fill 30min 19% · séance 42% (69/159) · gap 3% · délai 86.3min · rebond 76% (56/69) (MFE +1.91%)
   - −5.0% : fill 30min 13% · séance 31% (57/159) · gap 2% · délai 85.2min · rebond 89% (52/57) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −4.28%) → stop au-delà de −1.87% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.07% (p90 −4.55%) → stop au-delà de −2.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −5.09%) → stop au-delà de −3.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1522 jambes) : jambe baissière méd −1.25% (p90 −3.19%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 95% (46/49) · rebond 53% (27/46)
      · −2.0% : fill 85% (42/49) · rebond 54% (24/42)
      · −3.0% : fill 79% (40/49) · rebond 65% (30/40)
      · −4.0% : fill 68% (36/49) · rebond 67% (28/36)
      · −5.0% : fill 51% (31/49) · rebond 79% (27/31)
   - **flat** (30 séances) :
      · −1.0% : fill 72% (23/30) · rebond 65% (16/23)
      · −2.0% : fill 49% (18/30) · rebond 57% (12/18)
      · −3.0% : fill 41% (13/30) · rebond 53% (8/13)
      · −4.0% : fill 36% (12/30) · rebond 85% (10/12)
      · −5.0% : fill 22% (9/30) · rebond 100% (9/9)
   - **gap-up** (80 séances) :
      · −1.0% : fill 64% (47/80) · rebond 67% (35/47)
      · −2.0% : fill 54% (35/80) · rebond 73% (24/35)
      · −3.0% : fill 41% (28/80) · rebond 60% (20/28)
      · −4.0% : fill 29% (21/80) · rebond 84% (18/21)
      · −5.0% : fill 23% (17/80) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 55% si les 15 1res min sont vertes (73 cas) · 31% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:02** → P(séance verte=clôture>ouverture) 73% si début vert vs 12% si rouge (base 43% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 43% ; creux résiduel méd -2.73% (q20 -4.95%) → **SL/trailing à −4.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.37% → **scale +1.72% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **12%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.51%** (au-delà de la MAE q10 -6.51%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.01% .. +6.19%] · haut q95 +7.8% · bas q05 -7.17%
   - 60min (n=160) : retour [-5.76% .. +6.19%] · haut q95 +8.32% · bas q05 -7.63%
   - 2h (n=160) : retour [-5.84% .. +8.72%] · haut q95 +9.95% · bas q05 -7.84%
   - 4h (n=160) : retour [-6.32% .. +8.85%] · haut q95 +11.46% · bas q05 -9.54%
   - 6h (n=160) : retour [-6.7% .. +9.28%] · haut q95 +12.72% · bas q05 -10.21%
   - session (n=160) : retour [-7.57% .. +11.44%] · haut q95 +13.24% · bas q05 -11.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.8  _(momentum haussier)_
- **ADX** : 11.0  _(pas de tendance nette)_
- **MACD** : hist 0.337  _(pas de croisement recent)_
- **BB** : %B 0.92 · largeur 13.9%
- **ATR** : 1.43 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.127  _(distribution)_
- **Vol ratio** : 1.21  _(volume normal)_
- **Choppiness** : 60.0  _(transition)_
- **MA** : MA20 27.15 · MA50 28.39 · MA200 26.5  _(prix > MA20)_
- **Dist MA** : MA20 +5.9% · MA50 +1.3% · MA200 +8.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (761667 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
