# SOI

**Generated** : 2026-08-31T21:45:14.811342+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €114.90  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €114.90 (+1.9% vs entrée) · entrée €112.81 · stop €109.99 · T1 €117.75 · R/R 1.75  
> ↳ P(T1 av. stop) 18 % _(réel 5 s)_ · EV/risk -0.069 _(réel 5 s)_ (GBM 0.139) · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 178 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €112.17–€113.45 (mid €112.81)
- Spot actuel : €114.90 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €109.99 (stop swing_plan-based (-11.7%))
- Targets : T1 €117.75 · R/R 1.75 | T2 €120.06 · R/R 2.57 | T3 €122.37 · R/R 3.39
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €109.99


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.7 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **7.019 pt plus bas** dans le cas TYPIQUE (médiane), 15.479 au p90, **17.594 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 11.7 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0229 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.447** [0.3743 ; 0.5214] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3807** [0.3307 ; 0.4327] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.4212** [0.37 ; 0.4737] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.5 pt), swing (39.5 pt), deep (34.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.48 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.02 % contre 7.59 % aujourd'hui, rapport 0.40)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.22 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1252** (β de hausse 1.6206, asymétrie 0.6943) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut -0.048× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 101.8764 sur support (1.39 ATR, 11.335 %) — p(stop avant cible) 0.4187 [0.37 ; 0.47], R/R 0.763, perte reelle 21.456 % (gap inclus), CVaR 11.359 %, EV -4.0858 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.859 %) — p(stop avant cible) 0.519 [0.47 ; 0.57], R/R 1.069, perte reelle 15.318 % (gap inclus), EV -3.3006 % — **REFUSE**
      - refuse : p_stop_first 0.519, borne haute 0.571 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.30 %) : P(cible) 26.6 % x 16.37 % + P(rien) 21.5 % x 1.34 % ne couvrent pas P(stop) 51.9 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.39 ATR (stop 11.335 %) — p(stop avant cible) 0.4187 [0.37 ; 0.47], R/R 0.763, perte reelle 21.456 % (gap inclus), EV -4.0858 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.09 %) : P(cible) 30.4 % x 16.37 % + P(rien) 27.8 % x -0.26 % ne couvrent pas P(stop) 41.9 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.9 ATR (stop 32.083 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 0.51, perte reelle 32.083 % (gap inclus), EV 1.2442 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.08 % > budget 12.00 %
   - 🟢 support a 7.33 ATR (stop 46.444 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.353, perte reelle 46.444 % (gap inclus), EV 1.3085 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.44 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.476 %) — p(stop avant cible) 0.8803 [0.84 ; 0.91], R/R 5.149, perte reelle 3.18 % (gap inclus), EV -1.1108 % — **REFUSE**
      - refuse : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.880, borne haute 0.911 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 9.6 % x 16.37 % + P(rien) 2.4 % x 5.13 % ne couvrent pas P(stop) 88.0 % x 3.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.953 %) — p(stop avant cible) 0.783 [0.74 ; 0.82], R/R 3.051, perte reelle 5.366 % (gap inclus), EV -1.2516 % — **REFUSE**
      - refuse : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 16.3 % x 16.37 % + P(rien) 5.4 % x 5.14 % ne couvrent pas P(stop) 78.3 % x 5.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.429 %) — p(stop avant cible) 0.6909 [0.64 ; 0.74], R/R 1.89, perte reelle 8.664 % (gap inclus), EV -2.0767 % — **REFUSE**
      - refuse : p_stop_first 0.691, borne haute 0.738 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 21.5 % x 16.37 % + P(rien) 9.4 % x 4.08 % ne couvrent pas P(stop) 69.1 % x 8.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.906 %) — p(stop avant cible) 0.6294 [0.58 ; 0.68], R/R 1.241, perte reelle 13.196 % (gap inclus), EV -4.0126 % — **REFUSE**
      - refuse : p_stop_first 0.629, borne haute 0.679 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.01 %) : P(cible) 23.3 % x 16.37 % + P(rien) 13.7 % x 3.44 % ne couvrent pas P(stop) 62.9 % x 13.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.39 ATR (stop 9.953 %) — p(stop avant cible) 0.4681 [0.42 ; 0.52], R/R 0.763, perte reelle 21.456 % (gap inclus), EV -5.2292 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.23 %) : P(cible) 28.5 % x 16.37 % + P(rien) 24.7 % x 0.59 % ne couvrent pas P(stop) 46.8 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 13.288 %) — p(stop avant cible) 0.3404 [0.29 ; 0.39], R/R 0.763, perte reelle 21.456 % (gap inclus), EV -2.3559 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.36 %) : P(cible) 33.0 % x 16.37 % + P(rien) 33.0 % x -1.38 % ne couvrent pas P(stop) 34.0 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 14.764 %) — p(stop avant cible) 0.2944 [0.25 ; 0.34], R/R 0.763, perte reelle 21.456 % (gap inclus), EV -1.6581 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 33.3 % x 16.37 % + P(rien) 37.3 % x -2.11 % ne couvrent pas P(stop) 29.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 16.241 %) — p(stop avant cible) 0.2427 [0.20 ; 0.29], R/R 0.763, perte reelle 21.456 % (gap inclus), EV -0.4936 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 35.1 % x 16.37 % + P(rien) 40.6 % x -2.57 % ne couvrent pas P(stop) 24.3 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 17.717 %) — p(stop avant cible) 0.2031 [0.16 ; 0.25], R/R 0.682, perte reelle 24.006 % (gap inclus), EV -0.3497 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 35.1 % x 16.37 % + P(rien) 44.5 % x -2.76 % ne couvrent pas P(stop) 20.3 % x 24.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 20.67 %) — p(stop avant cible) 0.1191 [0.09 ; 0.16], R/R 0.559, perte reelle 29.294 % (gap inclus), EV 0.158 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.68 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.623 %) — p(stop avant cible) 0.0751 [0.05 ; 0.11], R/R 0.559, perte reelle 29.294 % (gap inclus), EV 0.9674 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.63 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.576 %) — p(stop avant cible) 0.0508 [0.03 ; 0.08], R/R 0.559, perte reelle 29.294 % (gap inclus), EV 1.2058 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.58 % > budget 12.00 %
   - 🟢 grid_snapped a 4.9 ATR (stop 30.701 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 0.533, perte reelle 30.701 % (gap inclus), EV 1.2896 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.70 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.435 %) — p(stop avant cible) 0.0224 [0.01 ; 0.04], R/R 0.462, perte reelle 35.435 % (gap inclus), EV 1.236 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.44 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.387 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 0.427, perte reelle 38.387 % (gap inclus), EV 1.2511 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.39 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.34 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.396, perte reelle 41.34 % (gap inclus), EV 1.2925 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.34 % > budget 12.00 %
   - 🟢 grid_snapped a 7.33 ATR (stop 45.062 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.363, perte reelle 45.062 % (gap inclus), EV 1.3085 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.06 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.246 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.347, perte reelle 47.246 % (gap inclus), EV 1.3085 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.25 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 114.9, ATR14 6.7857 (5.906 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 2.12 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.295 % | 114.5607 | 91.08 % | 94.11 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.591 % | 114.2214 | 84.9 % | 89.99 % | 92.04 % | 94.59 % | 96.24 % | 97.4 % |
| 0.15 ATR | 0.886 % | 113.8821 | 77.94 % | 85.08 % | 87.92 % | 91.14 % | 93.77 % | 95.3 % |
| 0.2 ATR | 1.181 % | 113.5429 | 69.51 % | 80.08 % | 83.99 % | 88.29 % | 91.59 % | 93.41 % |
| 0.25 ATR | 1.476 % | 113.2036 | 63.04 % | 76.35 % | 80.75 % | 86.61 % | 90.31 % | 92.81 % |
| 0.35 ATR | 2.067 % | 112.525 | 50.88 % | 67.81 % | 73.77 % | 81.5 % | 86.05 % | 90.21 % |
| 0.5 ATR | 2.953 % | 111.5071 | 35.98 % | 55.54 % | 62.97 % | 73.62 % | 81.4 % | 87.51 % |
| 0.75 ATR | 4.429 % | 109.8107 | 16.96 % | 35.53 % | 47.25 % | 59.15 % | 73.79 % | 81.32 % |
| 1.0 ATR | 5.906 % | 108.1143 | 8.24 % | 24.14 % | 34.28 % | 48.13 % | 65.58 % | 76.02 % |
| 1.25 ATR | 7.382 % | 106.4179 | 4.12 % | 15.7 % | 25.44 % | 37.89 % | 57.27 % | 70.33 % |
| 1.5 ATR | 8.859 % | 104.7214 | 2.35 % | 10.7 % | 18.66 % | 30.22 % | 49.36 % | 64.24 % |
| 2.0 ATR | 11.812 % | 101.3286 | 0.59 % | 4.61 % | 8.94 % | 18.31 % | 35.51 % | 53.95 % |
| 2.5 ATR | 14.764 % | 97.9357 | 0.29 % | 2.45 % | 4.81 % | 11.71 % | 24.63 % | 45.85 % |
| 3.0 ATR | 17.717 % | 94.5429 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 17.21 % | 37.86 % |
| 4.0 ATR | 23.623 % | 87.7571 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.79 % | 24.68 % |
| 6.0 ATR | 35.435 % | 74.1857 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.19 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.63 ATR | 0.81 ATR | 0.98 ATR | 1.12 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.79 ATR | 1.04 ATR | 1.27 ATR | 1.45 ATR | 1.95 ATR | 2.48 ATR |
| **5 s.** | 0.47 ATR | 0.96 ATR | 1.08 ATR | 1.41 ATR | 1.72 ATR | 1.93 ATR | 2.69 ATR | 3.59 ATR |
| **10 s.** | 0.71 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.48 ATR | 2.81 ATR | 3.97 ATR | 5.79 ATR |
| **20 s.** | 1.04 ATR | 2.24 ATR | 2.55 ATR | 3.37 ATR | 3.98 ATR | 4.75 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.632–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.793–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.906 %, prix 108.114), p(touche) 34.28 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.076–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.382 %, prix 106.4181), p(touche) 37.89 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.657–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.553–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.139 | EV/share : €0.392 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 30 % | T3 30 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.2 | bear 5.1 | side 9.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 230.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.815% → cible +4.378% / stop −2.5%, p_fill 60%, n_eff≈27.8) : P(cible|rempli) **18%** · **EV/risk -0.069** (×p_fill ; si rempli -0.29% du capital)
  - **swing** (entrée dip −3.999% → cible +16.043% / stop −8.021%, p_fill 51%, n_eff≈22.0) : P(cible|rempli) **16%** · **EV/risk -0.019** (×p_fill ; si rempli -0.30% du capital)
  - **deep** (entrée dip −6.178% → cible +23.155% / stop −11.577%, p_fill 57%, n_eff≈25.7) : P(cible|rempli) **22%** · **EV/risk -0.146** (×p_fill ; si rempli -2.96% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→65% · +3.0%→50% · +5.0%→31% · +8.0%→9%
- Range intraday médian 7.72% (p90 13.93%) · excursion haute méd. +3.14% / basse méd. −3.33%
- Profil de vol intra : ouverture 4.789% vs midi 1.354% vs clôture 2.088% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑0%/↓2% ; spike-down 72% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. -0.618% ; recovery-V 34%
- **σ réalisé intraday** 4.354% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 55% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 109.7812 (VA 109.5113–110.4563 ; dernier close 108.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 47% · rebond 85% · **stop −7.73%** sous le fill (sous le bruit) · cible +3.23% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 41% (gap-down >1% 28% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.07% (p90 −3.52%) · haut méd +0.92% · range méd 2.7%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −4.88%) · haut méd +1.25% · range méd 3.25%
- Excursion ouverture 30min (n=160) : bas méd −1.45% (p90 −5.16%) · haut méd +1.39% · range méd 3.77%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.6%) · haut méd +1.78% · range méd 3.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 108.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 78% (126/159) · gap 36% · délai 0.1min · rebond 69% (89/126) (MFE +1.75%)
   - −1.0% : fill 30min 57% · séance 72% (114/159) · gap 28% · délai 0.2min · rebond 74% (85/114) (MFE +2.0%)
   - −1.5% : fill 30min 51% · séance 65% (106/159) · gap 22% · délai 0.3min · rebond 75% (79/106) (MFE +2.33%)
   - −2.0% : fill 30min 43% · séance 60% (95/159) · gap 19% · délai 0.4min · rebond 70% (72/95) (MFE +2.48%)
   - −3.0% : fill 30min 34% · séance 47% (78/159) · gap 10% · délai 1.2min · rebond 85% (67/78) (MFE +3.23%)
   - −4.0% : fill 30min 26% · séance 39% (64/159) · gap 6% · délai 5.9min · rebond 80% (54/64) (MFE +3.47%)
   - −5.0% : fill 30min 17% · séance 31% (48/159) · gap 2% · délai 26.8min · rebond 70% (38/48) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −3.52%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.47%) → stop au-delà de −2.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.29%) → stop au-delà de −1.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1340 jambes) : jambe baissière méd −1.31% (p90 −3.16%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 97% (56/58) · rebond 68% (38/56)
      · −2.0% : fill 93% (53/58) · rebond 68% (40/53)
      · −3.0% : fill 81% (47/58) · rebond 81% (40/47)
      · −4.0% : fill 67% (39/58) · rebond 89% (36/39)
      · −5.0% : fill 53% (31/58) · rebond 77% (26/31)
   - **flat** (14 séances) :
      · −1.0% : fill 93% (11/14) · rebond 78% (9/11)
      · −2.0% : fill 73% (10/14) · rebond 79% (9/10)
      · −3.0% : fill 71% (9/14) · rebond 78% (8/9)
      · −4.0% : fill 57% (8/14) · rebond 56% (5/8)
      · −5.0% : fill 56% (7/14) · rebond 72% (6/7)
   - **gap-up** (87 séances) :
      · −1.0% : fill 53% (47/87) · rebond 82% (38/47)
      · −2.0% : fill 36% (32/87) · rebond 70% (23/32)
      · −3.0% : fill 21% (22/87) · rebond 96% (19/22)
      · −4.0% : fill 18% (17/87) · rebond 68% (13/17)
      · −5.0% : fill 13% (10/87) · rebond 48% (6/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 63% si les 15 1res min sont vertes (77 cas) · 32% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 72% si début vert vs 24% si rouge (base 48% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **72%** · continue >prix actuel 51% ; creux résiduel méd -1.98% (q20 -5.12%) → **SL/trailing à −5.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.23% / q75 +4.34% → **scale +2.23% / runner +4.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 66%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.67%** (au-delà de la MAE q10 -8.67%), cible rebond +2.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.73% .. +6.14%] · haut q95 +7.52% · bas q05 -6.04%
   - 60min (n=160) : retour [-5.5% .. +6.71%] · haut q95 +7.92% · bas q05 -6.62%
   - 2h (n=160) : retour [-6.21% .. +6.34%] · haut q95 +10.13% · bas q05 -7.58%
   - 4h (n=160) : retour [-7.07% .. +8.36%] · haut q95 +12.01% · bas q05 -8.27%
   - 6h (n=160) : retour [-8.14% .. +9.45%] · haut q95 +12.5% · bas q05 -9.44%
   - session (n=160) : retour [-11.52% .. +11.66%] · haut q95 +14.32% · bas q05 -12.77%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 8% vs absente 4% (base 6%)
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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 44.0  _(momentum baissier)_
- **ADX** : 13.4  _(pas de tendance nette)_
- **MACD** : hist -1.047  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 30.4%
- **ATR** : 6.79 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.219  _(distribution)_
- **Vol ratio** : 1.34  _(volume normal)_
- **Choppiness** : 43.9  _(transition)_
- **MA** : MA20 117.67 · MA50 110.16 · MA200 79.13  _(prix < MA20)_
- **Dist MA** : MA20 -2.4% · MA50 +4.3% · MA200 +45.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (801948 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
