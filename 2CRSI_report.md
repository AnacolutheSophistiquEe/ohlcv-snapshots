# AL2SI

**Generated** : 2026-09-25T21:53:45.404272+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €29.08  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot €29.08 (+1.7% vs entrée) · entrée €28.59 · stop €26.63 · T1 €30.73 · R/R 1.09  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.102 _(réel 5 s)_ (GBM 0.198) · ¼-Kelly 0.023 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -321 % hors [0,100] (R² max 0.92). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €28.28–€28.89 (mid €28.59)
- Spot actuel : €29.08 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €26.63 (stop swing_plan-based (-8.43%))
- Targets : T1 €30.73 · R/R 1.09 | T2 €33.02 · R/R 2.26 | T3 €33.18 · R/R 2.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.63


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.43 %)** : le gap seul le franchit 0.859 % des séances (11 fois sur 1280).
   - exécution **3.318 pt plus bas** dans le cas TYPIQUE (médiane), 18.735 au p90, **29.687 au pire**
   - perte réelle **16.422 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 8.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0687 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5629** [0.4885 ; 0.6352] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4169** [0.3658 ; 0.4694] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3547** [0.3057 ; 0.4062] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.0 pt), swing (32.6 pt), deep (33.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.29 % contre 7.13 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1995** (β de hausse 0.9506, asymétrie 1.2618) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.854× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 26.1464 sur atr_based (1.5 ATR, 10.088 %) — p(stop avant cible) 0.3561 [0.31 ; 0.41], R/R 0.627, perte reelle 22.515 % (gap inclus), CVaR 10.146 %, EV -2.0682 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 49.8 % de la queue et il ne reste que -1061.59 EUR a partager. Prix du risque -0.364 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.46 ATR (stop 6.753 %) — p(stop avant cible) 0.559 [0.51 ; 0.61], R/R 0.938, perte reelle 15.045 % (gap inclus), EV -3.4879 % — **REFUSE**
      - refuse : p_stop_first 0.559, borne haute 0.611 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.46 ATR du spot — compartiment <1, mesure a 48.0 % de casse (IC clusterise [0.451 ; 0.508] sur 1182 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.49 %) : P(cible) 32.0 % x 14.12 % + P(rien) 12.1 % x 3.36 % ne couvrent pas P(stop) 55.9 % x 15.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.088 %) — p(stop avant cible) 0.3561 [0.31 ; 0.41], R/R 0.627, perte reelle 22.515 % (gap inclus), EV -2.0682 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 38.8 % x 14.12 % + P(rien) 25.6 % x 1.85 % ne couvrent pas P(stop) 35.6 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.58 ATR (stop 14.288 %) — p(stop avant cible) 0.2454 [0.20 ; 0.29], R/R 0.572, perte reelle 24.668 % (gap inclus), EV -0.1316 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 39.9 % x 14.12 % + P(rien) 35.6 % x 0.82 % ne couvrent pas P(stop) 24.5 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.09 ATR (stop 17.689 %) — p(stop avant cible) 0.198 [0.16 ; 0.24], R/R 0.523, perte reelle 27.014 % (gap inclus), EV 0.2372 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.72 % > budget 12.00 %
   - 🟢 support a 3.31 ATR (stop 25.942 %) — p(stop avant cible) 0.0978 [0.07 ; 0.13], R/R 0.432, perte reelle 32.641 % (gap inclus), EV 1.3456 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.95 % > budget 12.00 %
   - 🔴 grid_snapped a 0.46 ATR (stop 5.112 %) — p(stop avant cible) 0.6489 [0.60 ; 0.70], R/R 1.126, perte reelle 12.539 % (gap inclus), EV -3.9657 % — **REFUSE**
      - refuse : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.97 %) : P(cible) 27.3 % x 14.12 % + P(rien) 7.8 % x 4.04 % ne couvrent pas P(stop) 64.9 % x 12.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.407 %) — p(stop avant cible) 0.4687 [0.42 ; 0.52], R/R 0.86, perte reelle 16.422 % (gap inclus), EV -2.2318 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.23 %) : P(cible) 35.0 % x 14.12 % + P(rien) 18.2 % x 2.92 % ne couvrent pas P(stop) 46.9 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.58 ATR (stop 12.647 %) — p(stop avant cible) 0.2712 [0.23 ; 0.32], R/R 0.572, perte reelle 24.668 % (gap inclus), EV -0.7315 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 39.4 % x 14.12 % + P(rien) 33.5 % x 1.18 % ne couvrent pas P(stop) 27.1 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.09 ATR (stop 16.048 %) — p(stop avant cible) 0.215 [0.17 ; 0.26], R/R 0.523, perte reelle 27.014 % (gap inclus), EV -0.0424 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 40.0 % x 14.12 % + P(rien) 38.5 % x 0.31 % ne couvrent pas P(stop) 21.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 20.176 %) — p(stop avant cible) 0.1579 [0.12 ; 0.20], R/R 0.47, perte reelle 30.031 % (gap inclus), EV 0.5384 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.20 % > budget 12.00 %
   - 🟢 grid_snapped a 3.31 ATR (stop 24.301 %) — p(stop avant cible) 0.1093 [0.08 ; 0.15], R/R 0.47, perte reelle 30.031 % (gap inclus), EV 1.4698 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.31 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 26.901 %) — p(stop avant cible) 0.0943 [0.07 ; 0.13], R/R 0.432, perte reelle 32.641 % (gap inclus), EV 1.3842 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.91 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 30.264 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 0.37, perte reelle 38.117 % (gap inclus), EV 1.0517 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.626 %) — p(stop avant cible) 0.0686 [0.05 ; 0.10], R/R 0.37, perte reelle 38.117 % (gap inclus), EV 1.3054 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.63 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 36.989 %) — p(stop avant cible) 0.0533 [0.03 ; 0.08], R/R 0.37, perte reelle 38.117 % (gap inclus), EV 1.7543 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 40.352 %) — p(stop avant cible) 0.0359 [0.02 ; 0.06], R/R 0.35, perte reelle 40.352 % (gap inclus), EV 2.0162 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.35 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.714 %) — p(stop avant cible) 0.0316 [0.02 ; 0.05], R/R 0.323, perte reelle 43.714 % (gap inclus), EV 1.9372 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 47.077 %) — p(stop avant cible) 0.0316 [0.02 ; 0.05], R/R 0.3, perte reelle 47.077 % (gap inclus), EV 1.831 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.08 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 50.44 %) — p(stop avant cible) 0.0316 [0.02 ; 0.05], R/R 0.28, perte reelle 50.44 % (gap inclus), EV 1.7247 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.44 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.802 %) — p(stop avant cible) 0.0277 [0.01 ; 0.05], R/R 0.262, perte reelle 53.802 % (gap inclus), EV 1.6267 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.80 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 29.08, ATR14 1.9557 (6.725 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.398 ATR = 2.677 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.336 % | 28.9822 | 86.67 % | 90.28 % | 92.63 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.673 % | 28.8844 | 82.06 % | 86.65 % | 89.88 % | 91.93 % | 93.77 % | 95.9 % |
| 0.15 ATR | 1.009 % | 28.7866 | 78.04 % | 82.92 % | 86.74 % | 88.78 % | 91.79 % | 94.71 % |
| 0.2 ATR | 1.345 % | 28.6889 | 72.25 % | 78.8 % | 82.91 % | 85.63 % | 89.42 % | 92.51 % |
| 0.25 ATR | 1.681 % | 28.5911 | 66.27 % | 74.19 % | 78.78 % | 82.28 % | 87.14 % | 90.91 % |
| 0.35 ATR | 2.354 % | 28.3955 | 54.51 % | 65.26 % | 70.63 % | 75.49 % | 82.2 % | 87.51 % |
| 0.5 ATR | 3.363 % | 28.1021 | 40.49 % | 53.58 % | 61.49 % | 68.5 % | 77.65 % | 85.01 % |
| 0.75 ATR | 5.044 % | 27.6132 | 22.45 % | 37.19 % | 47.05 % | 55.41 % | 66.77 % | 76.22 % |
| 1.0 ATR | 6.725 % | 27.1243 | 12.84 % | 24.73 % | 33.5 % | 44.0 % | 56.97 % | 67.83 % |
| 1.25 ATR | 8.407 % | 26.6354 | 7.55 % | 17.47 % | 24.46 % | 35.93 % | 49.85 % | 61.34 % |
| 1.5 ATR | 10.088 % | 26.1464 | 3.73 % | 11.29 % | 17.19 % | 28.35 % | 42.63 % | 54.85 % |
| 2.0 ATR | 13.451 % | 25.1686 | 0.88 % | 5.1 % | 9.53 % | 16.63 % | 30.96 % | 42.96 % |
| 2.5 ATR | 16.813 % | 24.1907 | 0.1 % | 2.16 % | 4.52 % | 9.74 % | 20.87 % | 33.07 % |
| 3.0 ATR | 20.176 % | 23.2129 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 14.94 % | 25.87 % |
| 4.0 ATR | 26.901 % | 21.2571 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.18 % |
| 6.0 ATR | 40.352 % | 17.3457 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.71 ATR | 0.81 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.16 ATR | 1.60 ATR | 2.02 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.01 ATR | 1.24 ATR | 1.40 ATR | 1.97 ATR | 2.45 ATR |
| **5 s.** | 0.36 ATR | 0.87 ATR | 0.98 ATR | 1.35 ATR | 1.64 ATR | 1.86 ATR | 2.48 ATR | 3.42 ATR |
| **10 s.** | 0.56 ATR | 1.25 ATR | 1.42 ATR | 1.91 ATR | 2.29 ATR | 2.57 ATR | 3.77 ATR | 5.11 ATR |
| **20 s.** | 0.79 ATR | 1.70 ATR | 1.91 ATR | 2.50 ATR | 3.10 ATR | 3.67 ATR | 5.56 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.452–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.363 %, prix 28.102), p(touche) 40.49 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (88.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.631–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.044 %, prix 27.6132), p(touche) 37.19 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.788–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.725 %, prix 27.1244), p(touche) 33.5 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.978–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.725 %, prix 27.1244), p(touche) 44.0 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.418–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.088 %, prix 26.1464), p(touche) 42.63 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.914–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.451 %, prix 25.1684), p(touche) 42.96 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.198 | EV/share : €0.386 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 82.2 | bear 12.8 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 378.0 (= 13 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.776% → cible +4.584% / stop −2.292%, p_fill 82%, n_eff≈35.1) : P(cible|rempli) **26%** · **EV/risk +0.005** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −1.705% → cible +7.504% / stop −6.842%, p_fill 79%, n_eff≈32.8) : P(cible|rempli) **32%** · **EV/risk -0.102** (×p_fill ; si rempli -0.88% du capital)
  - **deep** (entrée dip −2.632% → cible +16.617% / stop −10.361%, p_fill 65%, n_eff≈31.4) : P(cible|rempli) **15%** · **EV/risk -0.103** (×p_fill ; si rempli -1.63% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→76% · +2.0%→68% · +3.0%→54% · +5.0%→41% · +8.0%→21%
- Range intraday médian 7.92% (p90 22.19%) · excursion haute méd. +4.07% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.308% vs midi 1.708% vs clôture 1.799% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 7% · trend ↑2%/↓1% ; spike-down 71% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.082)_ ; drift intra méd. 0.153% ; recovery-V 24%
- **σ réalisé intraday** 4.977% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 67% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 28.2728 (VA 28.0733–28.5862 ; dernier close 28.62)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 89% · **stop −5.18%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.23% · baisse 42% (gap-down >1% 14% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −4.33%) · haut méd +0.81% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −4.9%) · haut méd +1.34% · range méd 3.08%
- Excursion ouverture 30min (n=160) : bas méd −1.41% (p90 −5.48%) · haut méd +1.96% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −1.53% (p90 −6.01%) · haut méd +2.1% · range méd 4.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 78% (123/159) · gap 22% · délai 0.3min · rebond 64% (85/123) (MFE +2.38%)
   - −1.0% : fill 30min 51% · séance 75% (117/159) · gap 14% · délai 1.2min · rebond 64% (80/117) (MFE +2.0%)
   - −1.5% : fill 30min 43% · séance 68% (104/159) · gap 9% · délai 6.7min · rebond 63% (66/104) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 62% (96/159) · gap 5% · délai 13.5min · rebond 62% (61/96) (MFE +1.57%)
   - −3.0% : fill 30min 22% · séance 51% (81/159) · gap 4% · délai 42.5min · rebond 59% (57/81) (MFE +1.47%)
   - −4.0% : fill 30min 18% · séance 42% (70/159) · gap 2% · délai 88.6min · rebond 77% (57/70) (MFE +1.84%)
   - −5.0% : fill 30min 12% · séance 30% (57/159) · gap 2% · délai 85.2min · rebond 89% (52/57) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −4.03%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.0% (p90 −4.32%) → stop au-delà de −2.56% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.98% (p90 −4.76%) → stop au-delà de −2.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1523 jambes) : jambe baissière méd −1.24% (p90 −3.1%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 95% (48/51) · rebond 59% (29/48)
      · −2.0% : fill 87% (44/51) · rebond 54% (25/44)
      · −3.0% : fill 76% (41/51) · rebond 60% (30/41)
      · −4.0% : fill 66% (37/51) · rebond 70% (29/37)
      · −5.0% : fill 45% (31/51) · rebond 79% (27/31)
   - **flat** (30 séances) :
      · −1.0% : fill 72% (23/30) · rebond 65% (16/23)
      · −2.0% : fill 49% (18/30) · rebond 57% (12/18)
      · −3.0% : fill 41% (13/30) · rebond 53% (8/13)
      · −4.0% : fill 36% (12/30) · rebond 85% (10/12)
      · −5.0% : fill 22% (9/30) · rebond 100% (9/9)
   - **gap-up** (78 séances) :
      · −1.0% : fill 62% (46/78) · rebond 67% (35/46)
      · −2.0% : fill 52% (34/78) · rebond 74% (24/34)
      · −3.0% : fill 39% (27/78) · rebond 60% (19/27)
      · −4.0% : fill 28% (21/78) · rebond 84% (18/21)
      · −5.0% : fill 22% (17/78) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (74 cas) · 32% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 69% si début vert vs 22% si rouge (base 44% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **69%** · continue >prix actuel 56% ; creux résiduel méd -2.58% (q20 -5.56%) → **SL/trailing à −5.56%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.47% / q75 +5.87% → **scale +3.47% / runner +5.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **22%** (continue à baisser 61%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.72%** (au-delà de la MAE q10 -7.72%), cible rebond +2.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.93% .. +6.13%] · haut q95 +7.67% · bas q05 -7.05%
   - 60min (n=160) : retour [-5.72% .. +6.19%] · haut q95 +8.22% · bas q05 -7.63%
   - 2h (n=160) : retour [-5.75% .. +8.33%] · haut q95 +9.95% · bas q05 -7.79%
   - 4h (n=160) : retour [-6.16% .. +8.77%] · haut q95 +11.4% · bas q05 -9.41%
   - 6h (n=160) : retour [-6.69% .. +9.25%] · haut q95 +12.36% · bas q05 -9.9%
   - session (n=160) : retour [-7.46% .. +11.07%] · haut q95 +13.23% · bas q05 -10.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.9  _(neutre)_
- **ADX** : 20.7  _(pas de tendance nette)_
- **MACD** : hist 0.171  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 18.1%
- **ATR** : 1.96 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.02  _(neutre)_
- **Vol ratio** : 1.07  _(volume normal)_
- **Choppiness** : 63.2  _(marche en range (choppy))_
- **MA** : MA20 28.49 · MA50 27.48 · MA200 27.82  _(prix > MA20)_
- **Dist MA** : MA20 +2.1% · MA50 +5.8% · MA200 +4.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (873928 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
