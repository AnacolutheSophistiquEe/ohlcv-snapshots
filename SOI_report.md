# SOI

**Generated** : 2026-09-03T00:10:20.825216+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €111.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €111.70 (+1.2% vs entrée) · entrée €110.41 · stop €106.74 · T1 €117.75 · R/R 2.0  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk -0.094 _(réel 5 s)_ (GBM 0.032) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.32% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 135 % hors [0,100] (R² max 0.59). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.290 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €109.83–€110.99 (mid €110.41)
- Spot actuel : €111.70 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €106.74 (stop swing_plan-based (-8.47%))
- Targets : T1 €117.75 · R/R 2.0 | T2 €118.40 · R/R 2.18 | T3 €119.05 · R/R 2.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €106.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.47 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **4.415 pt plus bas** dans le cas TYPIQUE (médiane), 15.536 au p90, **20.824 au pire**
   - perte réelle **15.318 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 8.47 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0321 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3876** [0.3174 ; 0.4616] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.3848** [0.3347 ; 0.4369] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3874** [0.3372 ; 0.4395] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.9 pt), swing (37.5 pt), deep (33.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.48 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.15 % contre 7.53 % aujourd'hui, rapport 0.42)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.22 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1217** (β de hausse 1.6214, asymétrie 0.6918) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut -0.048× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 98.45 sur atr_grid (2.0 ATR, 11.862 %) — p(stop avant cible) 0.4133 [0.36 ; 0.47], R/R 0.921, perte reelle 21.456 % (gap inclus), CVaR 11.884 %, EV -3.4903 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.94 ATR (stop 8.469 %) — p(stop avant cible) 0.5363 [0.48 ; 0.59], R/R 1.289, perte reelle 15.318 % (gap inclus), EV -3.2167 % — **REFUSE**
      - refuse : p_stop_first 0.536, borne haute 0.588 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.78 ATR du spot — compartiment <1, mesure a 46.8 % de casse (IC clusterise [0.433 ; 0.502] sur 1106 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.22 %) : P(cible) 20.9 % x 19.75 % + P(rien) 25.5 % x 3.43 % ne couvrent pas P(stop) 53.6 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.53 ATR (stop 29.812 %) — p(stop avant cible) 0.0325 [0.02 ; 0.06], R/R 0.663, perte reelle 29.812 % (gap inclus), EV 1.6976 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.81 % > budget 12.00 %
   - 🟢 support a 7.02 ATR (stop 44.583 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.443, perte reelle 44.583 % (gap inclus), EV 1.6868 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.58 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.483 %) — p(stop avant cible) 0.8831 [0.85 ; 0.91], R/R 6.211, perte reelle 3.18 % (gap inclus), EV -0.9204 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.883, borne haute 0.914 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 7.8 % x 19.75 % + P(rien) 3.9 % x 8.82 % ne couvrent pas P(stop) 88.3 % x 3.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.966 %) — p(stop avant cible) 0.787 [0.74 ; 0.83], R/R 3.648, perte reelle 5.414 % (gap inclus), EV -0.9977 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.787, borne haute 0.828 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 13.2 % x 19.75 % + P(rien) 8.2 % x 8.17 % ne couvrent pas P(stop) 78.7 % x 5.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.94 ATR (stop 7.33 %) — p(stop avant cible) 0.5844 [0.53 ; 0.64], R/R 1.289, perte reelle 15.318 % (gap inclus), EV -4.0403 % — **REFUSE**
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.04 %) : P(cible) 19.9 % x 19.75 % + P(rien) 21.7 % x 4.54 % ne couvrent pas P(stop) 58.4 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.379 %) — p(stop avant cible) 0.4444 [0.39 ; 0.50], R/R 0.921, perte reelle 21.456 % (gap inclus), EV -4.1292 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.13 %) : P(cible) 24.3 % x 19.75 % + P(rien) 31.3 % x 1.95 % ne couvrent pas P(stop) 44.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.862 %) — p(stop avant cible) 0.4133 [0.36 ; 0.47], R/R 0.921, perte reelle 21.456 % (gap inclus), EV -3.4903 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.49 %) : P(cible) 25.1 % x 19.75 % + P(rien) 33.6 % x 1.27 % ne couvrent pas P(stop) 41.3 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 13.345 %) — p(stop avant cible) 0.3503 [0.30 ; 0.40], R/R 0.921, perte reelle 21.456 % (gap inclus), EV -2.1898 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.19 %) : P(cible) 26.2 % x 19.75 % + P(rien) 38.7 % x 0.37 % ne couvrent pas P(stop) 35.0 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 14.828 %) — p(stop avant cible) 0.301 [0.25 ; 0.35], R/R 0.921, perte reelle 21.456 % (gap inclus), EV -1.377 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 26.2 % x 19.75 % + P(rien) 43.6 % x -0.23 % ne couvrent pas P(stop) 30.1 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 16.31 %) — p(stop avant cible) 0.2496 [0.21 ; 0.30], R/R 0.921, perte reelle 21.456 % (gap inclus), EV -0.2342 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 27.9 % x 19.75 % + P(rien) 47.2 % x -0.81 % ne couvrent pas P(stop) 25.0 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 17.793 %) — p(stop avant cible) 0.2064 [0.17 ; 0.25], R/R 0.823, perte reelle 24.006 % (gap inclus), EV 0.0051 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.80 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.759 %) — p(stop avant cible) 0.1177 [0.09 ; 0.15], R/R 0.674, perte reelle 29.294 % (gap inclus), EV 0.5323 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.77 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.724 %) — p(stop avant cible) 0.0742 [0.05 ; 0.11], R/R 0.674, perte reelle 29.294 % (gap inclus), EV 1.351 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.73 % > budget 12.00 %
   - 🟢 grid_snapped a 4.53 ATR (stop 28.673 %) — p(stop avant cible) 0.0333 [0.02 ; 0.06], R/R 0.674, perte reelle 29.294 % (gap inclus), EV 1.7079 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.67 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.621 %) — p(stop avant cible) 0.0325 [0.02 ; 0.06], R/R 0.605, perte reelle 32.621 % (gap inclus), EV 1.6063 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.62 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.586 %) — p(stop avant cible) 0.0222 [0.01 ; 0.04], R/R 0.555, perte reelle 35.586 % (gap inclus), EV 1.6102 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.59 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.552 %) — p(stop avant cible) 0.0113 [0.00 ; 0.03], R/R 0.512, perte reelle 38.552 % (gap inclus), EV 1.6266 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.55 % > budget 12.00 %
   - 🟢 grid_snapped a 7.02 ATR (stop 43.444 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.455, perte reelle 43.444 % (gap inclus), EV 1.6868 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.44 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.449 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.416, perte reelle 47.449 % (gap inclus), EV 1.6868 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.45 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 111.7, ATR14 6.625 (5.931 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 2.123 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.297 % | 111.3687 | 91.08 % | 94.11 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.593 % | 111.0375 | 84.9 % | 89.99 % | 92.04 % | 94.59 % | 96.24 % | 97.4 % |
| 0.15 ATR | 0.89 % | 110.7062 | 77.94 % | 85.08 % | 87.92 % | 91.14 % | 93.77 % | 95.3 % |
| 0.2 ATR | 1.186 % | 110.375 | 69.51 % | 80.08 % | 83.99 % | 88.29 % | 91.59 % | 93.41 % |
| 0.25 ATR | 1.483 % | 110.0437 | 63.04 % | 76.25 % | 80.75 % | 86.61 % | 90.31 % | 92.81 % |
| 0.35 ATR | 2.076 % | 109.3812 | 50.78 % | 67.71 % | 73.67 % | 81.5 % | 86.05 % | 90.21 % |
| 0.5 ATR | 2.966 % | 108.3875 | 35.88 % | 55.45 % | 62.87 % | 73.52 % | 81.4 % | 87.51 % |
| 0.75 ATR | 4.448 % | 106.7312 | 17.06 % | 35.43 % | 47.05 % | 58.96 % | 73.69 % | 81.32 % |
| 1.0 ATR | 5.931 % | 105.075 | 8.24 % | 24.04 % | 34.18 % | 47.93 % | 65.48 % | 75.92 % |
| 1.25 ATR | 7.414 % | 103.4187 | 4.12 % | 15.7 % | 25.34 % | 37.7 % | 57.17 % | 70.23 % |
| 1.5 ATR | 8.897 % | 101.7625 | 2.35 % | 10.7 % | 18.57 % | 30.12 % | 49.36 % | 64.14 % |
| 2.0 ATR | 11.862 % | 98.45 | 0.59 % | 4.61 % | 8.94 % | 18.31 % | 35.61 % | 53.75 % |
| 2.5 ATR | 14.828 % | 95.1375 | 0.29 % | 2.45 % | 4.81 % | 11.71 % | 24.73 % | 45.65 % |
| 3.0 ATR | 17.793 % | 91.825 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 17.21 % | 37.66 % |
| 4.0 ATR | 23.724 % | 85.2 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.79 % | 24.48 % |
| 6.0 ATR | 35.586 % | 71.95 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.19 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.98 ATR | 1.12 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.79 ATR | 1.03 ATR | 1.26 ATR | 1.45 ATR | 1.95 ATR | 2.48 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.41 ATR | 1.72 ATR | 1.93 ATR | 2.69 ATR | 3.59 ATR |
| **10 s.** | 0.71 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.49 ATR | 2.81 ATR | 3.97 ATR | 5.79 ATR |
| **20 s.** | 1.04 ATR | 2.23 ATR | 2.54 ATR | 3.35 ATR | 3.96 ATR | 4.73 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.63–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.79–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.931 %, prix 105.0751), p(touche) 34.18 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.414 %, prix 103.4186), p(touche) 37.7 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.659–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.541–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : €0.117 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.089 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.8 | bear 14.9 | side 6.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 223.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.155% → cible +6.647% / stop −3.324%, p_fill 69%, n_eff≈30.6) : P(cible|rempli) **12%** · **EV/risk -0.094** (×p_fill ; si rempli -0.45% du capital)
  - **swing** (entrée dip −2.539% → cible +5.83% / stop −6.086%, p_fill 64%, n_eff≈24.7) : P(cible|rempli) **41%** · **EV/risk -0.130** (×p_fill ; si rempli -1.25% du capital)
  - **deep** (entrée dip −3.927% → cible +24.674% / stop −12.337%, p_fill 73%, n_eff≈30.2) : P(cible|rempli) **18%** · **EV/risk -0.272** (×p_fill ; si rempli -4.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→64% · +3.0%→50% · +5.0%→31% · +8.0%→9%
- Range intraday médian 7.57% (p90 13.58%) · excursion haute méd. +3.14% / basse méd. −3.25%
- Profil de vol intra : ouverture 4.677% vs midi 1.332% vs clôture 2.04% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 11% · trend ↑0%/↓2% ; spike-down 72% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.078)_ ; drift intra méd. -0.541% ; recovery-V 36%
- **σ réalisé intraday** 4.324% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 55% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 109.9788 (VA 107.6568–112.3007 ; dernier close 111.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 47% · rebond 81% · **stop −7.62%** sous le fill (sous le bruit) · cible +3.1% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 39% (gap-down >1% 27% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.15% (p90 −3.47%) · haut méd +0.87% · range méd 2.61%
- Excursion ouverture 15min (n=160) : bas méd −1.37% (p90 −4.73%) · haut méd +1.19% · range méd 3.19%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −5.11%) · haut méd +1.3% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.48%) · haut méd +1.58% · range méd 3.83%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 110.55 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 77% (125/159) · gap 35% · délai 0.1min · rebond 67% (87/125) (MFE +1.65%)
   - −1.0% : fill 30min 57% · séance 71% (114/159) · gap 27% · délai 0.2min · rebond 75% (85/114) (MFE +1.92%)
   - −1.5% : fill 30min 51% · séance 64% (106/159) · gap 22% · délai 0.3min · rebond 76% (79/106) (MFE +2.3%)
   - −2.0% : fill 30min 43% · séance 60% (95/159) · gap 19% · délai 0.5min · rebond 70% (72/95) (MFE +2.4%)
   - −3.0% : fill 30min 33% · séance 47% (78/159) · gap 9% · délai 1.5min · rebond 81% (66/78) (MFE +3.1%)
   - −4.0% : fill 30min 25% · séance 39% (65/159) · gap 6% · délai 11.3min · rebond 76% (54/65) (MFE +3.27%)
   - −5.0% : fill 30min 16% · séance 32% (49/159) · gap 2% · délai 31.6min · rebond 72% (39/49) (MFE +2.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −3.5%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.45%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.28%) → stop au-delà de −1.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1339 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 97% (55/57) · rebond 68% (37/55)
      · −2.0% : fill 93% (52/57) · rebond 68% (39/52)
      · −3.0% : fill 81% (46/57) · rebond 81% (39/46)
      · −4.0% : fill 67% (39/57) · rebond 89% (36/39)
      · −5.0% : fill 53% (31/57) · rebond 77% (26/31)
   - **flat** (14 séances) :
      · −1.0% : fill 93% (11/14) · rebond 78% (9/11)
      · −2.0% : fill 73% (10/14) · rebond 79% (9/10)
      · −3.0% : fill 71% (9/14) · rebond 78% (8/9)
      · −4.0% : fill 57% (8/14) · rebond 56% (5/8)
      · −5.0% : fill 56% (7/14) · rebond 72% (6/7)
   - **gap-up** (88 séances) :
      · −1.0% : fill 53% (48/88) · rebond 83% (39/48)
      · −2.0% : fill 37% (33/88) · rebond 73% (24/33)
      · −3.0% : fill 23% (23/88) · rebond 82% (19/23)
      · −4.0% : fill 20% (18/88) · rebond 57% (13/18)
      · −5.0% : fill 16% (11/88) · rebond 59% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 63% si les 15 1res min sont vertes (76 cas) · 33% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 73% si début vert vs 23% si rouge (base 48% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **73%** · continue >prix actuel 53% ; creux résiduel méd -1.81% (q20 -5.04%) → **SL/trailing à −5.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.35% / q75 +4.7% → **scale +2.35% / runner +4.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **23%** (continue à baisser 67%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.66%** (au-delà de la MAE q10 -8.66%), cible rebond +1.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.66% .. +6.14%] · haut q95 +7.34% · bas q05 -5.97%
   - 60min (n=160) : retour [-5.44% .. +6.71%] · haut q95 +7.88% · bas q05 -6.58%
   - 2h (n=160) : retour [-6.05% .. +6.12%] · haut q95 +9.54% · bas q05 -7.52%
   - 4h (n=160) : retour [-6.96% .. +8.22%] · haut q95 +11.69% · bas q05 -8.2%
   - 6h (n=160) : retour [-7.88% .. +9.23%] · haut q95 +12.43% · bas q05 -9.44%
   - session (n=160) : retour [-11.34% .. +11.32%] · haut q95 +14.2% · bas q05 -12.72%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 8% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.4  _(momentum baissier)_
- **ADX** : 12.6  _(pas de tendance nette)_
- **MACD** : hist -0.731  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 31.3%
- **ATR** : 6.62 (61.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.29  _(distribution)_
- **Vol ratio** : 0.31  _(volume atone)_
- **Choppiness** : 43.5  _(transition)_
- **MA** : MA20 116.81 · MA50 110.05 · MA200 79.88  _(prix < MA20)_
- **Dist MA** : MA20 -4.4% · MA50 +1.5% · MA200 +39.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (500657 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
