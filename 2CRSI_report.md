# AL2SI

**Generated** : 2026-09-29T00:15:44.848125+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €29.06  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €29.06 (+0.8% vs entrée) · entrée €28.84 · stop €27.89 · T1 €30.73 · R/R 1.99  
> ↳ P(T1 av. stop) 14 % _(réel 5 s)_ · EV/risk -0.125 _(réel 5 s)_ (GBM 0.036) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.28% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -218 % hors [0,100] (R² max 0.92). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €28.70–€28.98 (mid €28.84)
- Spot actuel : €29.06 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €27.89 (R/R 2 (resserré, parité Claude) ; -3.29 % depuis l'entree)
- Targets : T1 €30.73 · R/R 1.99 | T2 €30.79 · R/R 2.05 | T3 €30.86 · R/R 2.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €27.89


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.31 %)** : le gap seul le franchit 0.625 % des séances (8 fois sur 1280).
   - exécution **7.313 pt plus bas** dans le cas TYPIQUE (médiane), 21.141 au p90, **28.807 au pire**
   - perte réelle **19.309 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 9.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0625 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4682** [0.3949 ; 0.5425] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4177** [0.3666 ; 0.4702] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3059** [0.2591 ; 0.3559] _(largeur 9.7 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.7 pt), swing (32.6 pt), deep (33.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.29 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.37 % contre 7.06 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.204** (β de hausse 0.9506, asymétrie 1.2665) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.847× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 27.5997 sur grid_snapped (0.45 ATR, 5.025 %) — p(stop avant cible) 0.6479 [0.60 ; 0.70], R/R 1.087, perte reelle 12.539 % (gap inclus), CVaR 5.131 %, EV -4.0029 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6842 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.648, borne haute 0.697 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 5.13 % > budget 3.62 %
- Budget de queue : **3.62 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.18 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 47.6 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.45 ATR (stop 6.09 %) — p(stop avant cible) 0.5847 [0.53 ; 0.64], R/R 1.016, perte reelle 13.415 % (gap inclus), EV -3.1892 % — **REFUSE**
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.18 % > budget 3.62 %
      - ⚠ support DETECTE a 0.45 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.441 ; 0.507] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.19 %) : P(cible) 31.3 % x 13.63 % + P(rien) 10.2 % x 3.77 % ne couvrent pas P(stop) 58.5 % x 13.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 9.984 %) — p(stop avant cible) 0.3555 [0.31 ; 0.41], R/R 0.605, perte reelle 22.515 % (gap inclus), EV -2.1271 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.04 % > budget 3.62 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 40.1 % x 13.63 % + P(rien) 24.4 % x 1.71 % ne couvrent pas P(stop) 35.5 % x 22.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.59 ATR (stop 13.616 %) — p(stop avant cible) 0.2463 [0.20 ; 0.29], R/R 0.552, perte reelle 24.668 % (gap inclus), EV -0.12 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.66 % > budget 3.62 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 41.5 % x 13.63 % + P(rien) 33.8 % x 0.87 % ne couvrent pas P(stop) 24.6 % x 24.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.1 ATR (stop 17.033 %) — p(stop avant cible) 0.196 [0.16 ; 0.24], R/R 0.504, perte reelle 27.014 % (gap inclus), EV 0.3359 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.06 % > budget 3.62 %
   - 🟢 support a 3.34 ATR (stop 25.292 %) — p(stop avant cible) 0.1003 [0.07 ; 0.14], R/R 0.417, perte reelle 32.641 % (gap inclus), EV 1.2819 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.30 % > budget 3.62 %
   - 🔴 grid_snapped a 0.45 ATR (stop 5.025 %) — p(stop avant cible) 0.6479 [0.60 ; 0.70], R/R 1.087, perte reelle 12.539 % (gap inclus), EV -4.0029 % — **REFUSE**
      - refuse : p_stop_first 0.648, borne haute 0.697 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 5.13 % > budget 3.62 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.00 %) : P(cible) 28.1 % x 13.63 % + P(rien) 7.1 % x 4.15 % ne couvrent pas P(stop) 64.8 % x 12.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 8.32 %) — p(stop avant cible) 0.4617 [0.41 ; 0.51], R/R 0.83, perte reelle 16.422 % (gap inclus), EV -2.2092 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.39 % > budget 3.62 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 35.5 % x 13.63 % + P(rien) 18.3 % x 2.93 % ne couvrent pas P(stop) 46.2 % x 16.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.59 ATR (stop 12.551 %) — p(stop avant cible) 0.2622 [0.22 ; 0.31], R/R 0.552, perte reelle 24.668 % (gap inclus), EV -0.513 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.60 % > budget 3.62 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 41.1 % x 13.63 % + P(rien) 32.7 % x 1.09 % ne couvrent pas P(stop) 26.2 % x 24.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.1 ATR (stop 15.968 %) — p(stop avant cible) 0.2108 [0.17 ; 0.26], R/R 0.504, perte reelle 27.014 % (gap inclus), EV 0.0851 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.00 % > budget 3.62 %
   - ⚪ atr_grid a 2.75 ATR (stop 18.304 %) — p(stop avant cible) 0.1855 [0.15 ; 0.23], R/R 0.454, perte reelle 30.031 % (gap inclus), EV -0.0544 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 3.62 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 41.7 % x 13.63 % + P(rien) 39.8 % x -0.40 % ne couvrent pas P(stop) 18.6 % x 30.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 19.969 %) — p(stop avant cible) 0.1529 [0.12 ; 0.19], R/R 0.454, perte reelle 30.031 % (gap inclus), EV 0.6921 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.99 % > budget 3.62 %
   - 🟢 grid_snapped a 3.34 ATR (stop 24.227 %) — p(stop avant cible) 0.1087 [0.08 ; 0.14], R/R 0.454, perte reelle 30.031 % (gap inclus), EV 1.4362 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.24 % > budget 3.62 %
   - ⚪ atr_grid a 4.0 ATR (stop 26.625 %) — p(stop avant cible) 0.0941 [0.07 ; 0.13], R/R 0.417, perte reelle 32.641 % (gap inclus), EV 1.3455 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.63 % > budget 3.62 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.953 %) — p(stop avant cible) 0.0845 [0.06 ; 0.12], R/R 0.358, perte reelle 38.117 % (gap inclus), EV 1.0227 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.96 % > budget 3.62 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.281 %) — p(stop avant cible) 0.0726 [0.05 ; 0.10], R/R 0.358, perte reelle 38.117 % (gap inclus), EV 1.244 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.28 % > budget 3.62 %
   - ⚪ atr_grid a 5.5 ATR (stop 36.609 %) — p(stop avant cible) 0.053 [0.03 ; 0.08], R/R 0.358, perte reelle 38.117 % (gap inclus), EV 1.7167 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.61 % > budget 3.62 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.937 %) — p(stop avant cible) 0.0357 [0.02 ; 0.06], R/R 0.341, perte reelle 39.937 % (gap inclus), EV 1.9914 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.94 % > budget 3.62 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.265 %) — p(stop avant cible) 0.0314 [0.02 ; 0.05], R/R 0.315, perte reelle 43.265 % (gap inclus), EV 1.9135 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.26 % > budget 3.62 %
   - ⚪ atr_grid a 7.0 ATR (stop 46.593 %) — p(stop avant cible) 0.0314 [0.02 ; 0.05], R/R 0.292, perte reelle 46.593 % (gap inclus), EV 1.809 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.59 % > budget 3.62 %
   - ⚪ atr_grid a 7.5 ATR (stop 49.921 %) — p(stop avant cible) 0.0314 [0.02 ; 0.05], R/R 0.273, perte reelle 49.921 % (gap inclus), EV 1.7045 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.92 % > budget 3.62 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.249 %) — p(stop avant cible) 0.0276 [0.01 ; 0.05], R/R 0.256, perte reelle 53.249 % (gap inclus), EV 1.6018 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.25 % > budget 3.62 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 29.06, ATR14 1.9343 (6.656 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.398 ATR = 2.649 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.333 % | 28.9633 | 86.67 % | 90.28 % | 92.63 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.666 % | 28.8666 | 82.06 % | 86.65 % | 89.88 % | 91.83 % | 93.77 % | 95.9 % |
| 0.15 ATR | 0.998 % | 28.7699 | 78.04 % | 82.92 % | 86.74 % | 88.68 % | 91.79 % | 94.71 % |
| 0.2 ATR | 1.331 % | 28.6731 | 72.25 % | 78.8 % | 82.91 % | 85.53 % | 89.42 % | 92.51 % |
| 0.25 ATR | 1.664 % | 28.5764 | 66.27 % | 74.19 % | 78.78 % | 82.19 % | 87.14 % | 90.91 % |
| 0.35 ATR | 2.33 % | 28.383 | 54.51 % | 65.36 % | 70.63 % | 75.39 % | 82.2 % | 87.51 % |
| 0.5 ATR | 3.328 % | 28.0929 | 40.49 % | 53.58 % | 61.49 % | 68.41 % | 77.65 % | 85.01 % |
| 0.75 ATR | 4.992 % | 27.6093 | 22.45 % | 37.19 % | 46.95 % | 55.31 % | 66.77 % | 76.22 % |
| 1.0 ATR | 6.656 % | 27.1257 | 12.84 % | 24.73 % | 33.4 % | 43.9 % | 56.87 % | 67.83 % |
| 1.25 ATR | 8.32 % | 26.6421 | 7.45 % | 17.37 % | 24.36 % | 35.83 % | 49.75 % | 61.34 % |
| 1.5 ATR | 9.984 % | 26.1586 | 3.63 % | 11.19 % | 17.09 % | 28.25 % | 42.53 % | 54.85 % |
| 2.0 ATR | 13.312 % | 25.1914 | 0.88 % | 5.1 % | 9.53 % | 16.63 % | 30.96 % | 43.06 % |
| 2.5 ATR | 16.64 % | 24.2243 | 0.1 % | 2.16 % | 4.52 % | 9.74 % | 20.87 % | 33.07 % |
| 3.0 ATR | 19.969 % | 23.2571 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 14.94 % | 25.87 % |
| 4.0 ATR | 26.625 % | 21.3229 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.18 % |
| 6.0 ATR | 39.937 % | 17.4543 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.71 ATR | 0.81 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.16 ATR | 1.60 ATR | 2.02 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.01 ATR | 1.23 ATR | 1.40 ATR | 1.97 ATR | 2.45 ATR |
| **5 s.** | 0.36 ATR | 0.87 ATR | 0.98 ATR | 1.34 ATR | 1.64 ATR | 1.85 ATR | 2.48 ATR | 3.42 ATR |
| **10 s.** | 0.56 ATR | 1.24 ATR | 1.41 ATR | 1.91 ATR | 2.29 ATR | 2.57 ATR | 3.77 ATR | 5.11 ATR |
| **20 s.** | 0.79 ATR | 1.71 ATR | 1.92 ATR | 2.50 ATR | 3.10 ATR | 3.67 ATR | 5.56 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.452–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.328 %, prix 28.0929), p(touche) 40.49 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (89.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.631–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.992 %, prix 27.6093), p(touche) 37.19 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.786–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.656 %, prix 27.1258), p(touche) 33.4 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.976–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.656 %, prix 27.1258), p(touche) 43.9 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.414–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.984 %, prix 26.1586), p(touche) 42.53 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.918–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.312 %, prix 25.1915), p(touche) 43.06 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.036 | EV/share : €0.034 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 33 % | T3 33 %
- Kelly (position) : f* 0.094 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.7 | bear 12.3 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 378.0 (= 13 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.758% → cible +6.553% / stop −3.277%, p_fill 82%, n_eff≈35.1) : P(cible|rempli) **14%** · **EV/risk -0.125** (×p_fill ; si rempli -0.50% du capital)
  - **swing** (entrée dip −1.664% → cible +15.552% / stop −7.776%, p_fill 81%, n_eff≈33.6) : P(cible|rempli) **10%** · **EV/risk -0.162** (×p_fill ; si rempli -1.56% du capital)
  - **deep** (entrée dip −2.576% → cible +7.377% / stop −10.248%, p_fill 65%, n_eff≈31.4) : P(cible|rempli) **48%** · **EV/risk -0.015** (×p_fill ; si rempli -0.23% du capital)
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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.0  _(neutre)_
- **ADX** : 20.6  _(pas de tendance nette)_
- **MACD** : hist 0.11  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 16.7%
- **ATR** : 1.93 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.055  _(accumulation)_
- **Vol ratio** : 0.3  _(volume atone)_
- **Choppiness** : 62.8  _(marche en range (choppy))_
- **MA** : MA20 28.63 · MA50 27.54 · MA200 27.91  _(prix > MA20)_
- **Dist MA** : MA20 +1.5% · MA50 +5.5% · MA200 +4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (861154 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
