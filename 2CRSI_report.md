# AL2SI

**Generated** : 2026-09-18T00:16:15.874254+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €28.72  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €28.72 (+1.1% vs entrée) · entrée €28.42 · stop €26.47 · T1 €29.92 · R/R 0.77  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk -0.199 _(réel 5 s)_ (GBM 0.138) · ¼-Kelly 0.026 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 246 % hors [0,100] (R² max 0.92). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €28.12–€28.72 (mid €28.42)
- Spot actuel : €28.72 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : €26.47 (stop swing_plan-based (-7.84%))
- Targets : T1 €29.92 · R/R 0.77 | T2 €31.41 · R/R 1.53 | T3 €32.90 · R/R 2.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.84 %)** : le gap seul le franchit 0.86 % des séances (11 fois sur 1279).
   - exécution **3.908 pt plus bas** dans le cas TYPIQUE (médiane), 19.325 au p90, **30.277 au pire**
   - perte réelle **16.422 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 7.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0738 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.815 % | pire -38.117 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5016** [0.4276 ; 0.5755] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3715** [0.3218 ; 0.4233] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3033** [0.2566 ; 0.3532] _(largeur 9.7 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.6 pt), swing (31.2 pt), deep (32.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.29 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.38 % contre 7.26 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.77 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.211** (β de hausse 0.9449, asymétrie 1.2816) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.9× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 25.4035 sur grid_snapped (1.4 ATR, 11.548 %) — p(stop avant cible) 0.3128 [0.27 ; 0.36], R/R 0.647, perte reelle 22.515 % (gap inclus), CVaR 11.599 %, EV -0.8106 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.28 ATR (stop 5.382 %) — p(stop avant cible) 0.6322 [0.58 ; 0.68], R/R 1.162, perte reelle 12.539 % (gap inclus), EV -3.5146 % — **REFUSE**
      - refuse : p_stop_first 0.632, borne haute 0.682 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.28 ATR du spot — compartiment <1, mesure a 50.6 % de casse (IC clusterise [0.471 ; 0.543] sur 1124 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.51 %) : P(cible) 28.0 % x 14.57 % + P(rien) 8.8 % x 3.80 % ne couvrent pas P(stop) 63.2 % x 12.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.2 %) — p(stop avant cible) 0.3647 [0.32 ; 0.42], R/R 0.647, perte reelle 22.515 % (gap inclus), EV -1.9459 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 40.4 % x 14.57 % + P(rien) 23.1 % x 1.63 % ne couvrent pas P(stop) 36.5 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.4 ATR (stop 13.009 %) — p(stop avant cible) 0.2763 [0.23 ; 0.33], R/R 0.591, perte reelle 24.668 % (gap inclus), EV -0.5957 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 41.0 % x 14.57 % + P(rien) 31.4 % x 0.79 % ne couvrent pas P(stop) 27.6 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.9 ATR (stop 16.454 %) — p(stop avant cible) 0.2215 [0.18 ; 0.27], R/R 0.539, perte reelle 27.014 % (gap inclus), EV 0.0195 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.49 % > budget 12.00 %
   - 🟢 support a 3.13 ATR (stop 24.811 %) — p(stop avant cible) 0.1054 [0.08 ; 0.14], R/R 0.485, perte reelle 30.031 % (gap inclus), EV 1.6737 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.82 % > budget 12.00 %
   - 🔴 grid_snapped a 0.28 ATR (stop 3.92 %) — p(stop avant cible) 0.7011 [0.65 ; 0.75], R/R 1.6, perte reelle 9.107 % (gap inclus), EV -2.5618 % — **REFUSE**
      - refuse : p_stop_first 0.701, borne haute 0.748 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.56 %) : P(cible) 24.6 % x 14.57 % + P(rien) 5.3 % x 4.50 % ne couvrent pas P(stop) 70.1 % x 9.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.8 %) — p(stop avant cible) 0.5549 [0.50 ; 0.61], R/R 0.968, perte reelle 15.045 % (gap inclus), EV -3.1785 % — **REFUSE**
      - refuse : p_stop_first 0.555, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.18 %) : P(cible) 32.8 % x 14.57 % + P(rien) 11.8 % x 3.39 % ne couvrent pas P(stop) 55.5 % x 15.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.4 ATR (stop 11.548 %) — p(stop avant cible) 0.3128 [0.27 ; 0.36], R/R 0.647, perte reelle 22.515 % (gap inclus), EV -0.8106 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 40.8 % x 14.57 % + P(rien) 27.9 % x 1.01 % ne couvrent pas P(stop) 31.3 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.9 ATR (stop 14.993 %) — p(stop avant cible) 0.2534 [0.21 ; 0.30], R/R 0.591, perte reelle 24.668 % (gap inclus), EV -0.0381 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 41.6 % x 14.57 % + P(rien) 33.1 % x 0.47 % ne couvrent pas P(stop) 25.3 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 18.699 %) — p(stop avant cible) 0.1949 [0.16 ; 0.24], R/R 0.485, perte reelle 30.031 % (gap inclus), EV -0.1279 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 41.6 % x 14.57 % + P(rien) 38.9 % x -0.86 % ne couvrent pas P(stop) 19.5 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.13 ATR (stop 23.349 %) — p(stop avant cible) 0.1151 [0.08 ; 0.15], R/R 0.485, perte reelle 30.031 % (gap inclus), EV 1.5522 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.36 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 27.199 %) — p(stop avant cible) 0.0981 [0.07 ; 0.13], R/R 0.382, perte reelle 38.117 % (gap inclus), EV 0.9425 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.21 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 30.598 %) — p(stop avant cible) 0.0878 [0.06 ; 0.12], R/R 0.382, perte reelle 38.117 % (gap inclus), EV 1.1469 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.60 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.998 %) — p(stop avant cible) 0.0672 [0.04 ; 0.10], R/R 0.382, perte reelle 38.117 % (gap inclus), EV 1.4725 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.00 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 37.398 %) — p(stop avant cible) 0.0555 [0.04 ; 0.08], R/R 0.382, perte reelle 38.117 % (gap inclus), EV 1.8656 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 40.798 %) — p(stop avant cible) 0.0374 [0.02 ; 0.06], R/R 0.357, perte reelle 40.798 % (gap inclus), EV 2.1226 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.80 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 44.198 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 0.33, perte reelle 44.198 % (gap inclus), EV 2.0424 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 47.597 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 0.306, perte reelle 47.597 % (gap inclus), EV 1.9306 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.60 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 50.997 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 0.286, perte reelle 50.997 % (gap inclus), EV 1.8188 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.00 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 54.397 %) — p(stop avant cible) 0.0289 [0.01 ; 0.05], R/R 0.268, perte reelle 54.397 % (gap inclus), EV 1.7148 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.40 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 28.72, ATR14 1.9529 (6.8 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.399 ATR = 2.713 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.34 % | 28.6224 | 86.85 % | 90.47 % | 92.82 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.68 % | 28.5247 | 82.34 % | 86.84 % | 89.97 % | 91.82 % | 93.76 % | 95.9 % |
| 0.15 ATR | 1.02 % | 28.4271 | 78.31 % | 83.2 % | 86.92 % | 88.77 % | 91.78 % | 94.7 % |
| 0.2 ATR | 1.36 % | 28.3294 | 72.42 % | 79.08 % | 83.09 % | 85.62 % | 89.41 % | 92.5 % |
| 0.25 ATR | 1.7 % | 28.2318 | 66.34 % | 74.46 % | 78.96 % | 82.27 % | 87.13 % | 90.9 % |
| 0.35 ATR | 2.38 % | 28.0365 | 54.56 % | 65.52 % | 70.8 % | 75.47 % | 82.18 % | 87.5 % |
| 0.5 ATR | 3.4 % | 27.7436 | 40.73 % | 53.83 % | 61.75 % | 68.57 % | 77.62 % | 85.0 % |
| 0.75 ATR | 5.1 % | 27.2554 | 22.67 % | 37.62 % | 47.59 % | 55.67 % | 66.73 % | 76.3 % |
| 1.0 ATR | 6.8 % | 26.7671 | 13.05 % | 25.15 % | 34.12 % | 44.53 % | 57.03 % | 68.0 % |
| 1.25 ATR | 8.5 % | 26.2789 | 7.65 % | 17.78 % | 25.07 % | 36.45 % | 50.0 % | 61.7 % |
| 1.5 ATR | 10.199 % | 25.7907 | 3.83 % | 11.59 % | 17.7 % | 28.97 % | 42.97 % | 55.2 % |
| 2.0 ATR | 13.599 % | 24.8143 | 0.88 % | 5.4 % | 9.93 % | 17.14 % | 31.49 % | 43.5 % |
| 2.5 ATR | 16.999 % | 23.8379 | 0.1 % | 2.36 % | 4.92 % | 10.34 % | 21.49 % | 33.7 % |
| 3.0 ATR | 20.399 % | 22.8614 | 0.1 % | 0.98 % | 2.56 % | 7.09 % | 15.45 % | 26.4 % |
| 4.0 ATR | 27.199 % | 20.9086 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.01 % | 17.7 % |
| 6.0 ATR | 40.798 % | 17.0029 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 8.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.42 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.18 ATR | 1.63 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 2.00 ATR | 2.49 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 0.99 ATR | 1.36 ATR | 1.67 ATR | 1.88 ATR | 2.55 ATR | 3.52 ATR |
| **10 s.** | 0.56 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.33 ATR | 2.62 ATR | 3.85 ATR | 5.17 ATR |
| **20 s.** | 0.79 ATR | 1.72 ATR | 1.94 ATR | 2.55 ATR | 3.16 ATR | 3.74 ATR | 5.59 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.454–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.4 %, prix 27.7435), p(touche) 40.73 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (90.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.636–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.1 %, prix 27.2553), p(touche) 37.62 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.798–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.8 %, prix 26.767), p(touche) 34.12 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.989–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.8 %, prix 26.767), p(touche) 44.53 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.428–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.199 %, prix 25.7908), p(touche) 42.97 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.936–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.599 %, prix 24.8144), p(touche) 43.5 % (en stress 97.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.138 | EV/share : €0.269 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 38 % | T3 24 %
- Kelly (position) : f* 0.103 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.8 | bear 5.7 | side 8.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 488.0 (= 17 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.47% → cible +2.351% / stop −2.05%, p_fill 84%, n_eff≈36.0) : P(cible|rempli) **48%** · **EV/risk +0.010** (×p_fill ; si rempli +0.02% du capital)
  - **swing** (entrée dip −1.041% → cible +5.258% / stop −6.871%, p_fill 88%, n_eff≈36.7) : P(cible|rempli) **41%** · **EV/risk -0.199** (×p_fill ; si rempli -1.54% du capital)
  - **deep** (entrée dip −1.601% → cible +7.435% / stop −10.365%, p_fill 80%, n_eff≈34.2) : P(cible|rempli) **50%** · **EV/risk -0.003** (×p_fill ; si rempli -0.04% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 55.9  _(momentum haussier)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist 0.165  _(pas de croisement recent)_
- **BB** : %B 0.73 · largeur 17.7%
- **ATR** : 1.95 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.026  _(neutre)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 54.2  _(transition)_
- **MA** : MA20 27.6 · MA50 27.32 · MA200 27.19  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +5.1% · MA200 +5.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759664 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
