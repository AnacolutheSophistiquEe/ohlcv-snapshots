# AL2SI

**Generated** : 2026-09-02T00:11:33.460073+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €25.66  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €25.66 (+0.7% vs entrée) · entrée €25.47 · stop €24.24 · T1 €26.46 · R/R 0.8  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk -0.087 _(réel 5 s)_ (GBM 0.085) · ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 271 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €25.27–€25.66 (mid €25.47)
- Spot actuel : €25.66 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €24.24 (stop swing_plan-based (-5.54%))
- Targets : T1 €26.46 · R/R 0.8 | T2 €27.44 · R/R 1.6 | T3 €28.43 · R/R 2.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.24


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.54 %)** : le gap seul le franchit 1.328 % des séances (17 fois sur 1280).
   - exécution **3.669 pt plus bas** dans le cas TYPIQUE (médiane), 20.213 au p90, **32.577 au pire**
   - perte réelle **12.959 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 5.54 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0985 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0887** [0.0531 ; 0.1379] _(largeur 8.5 pt, n_eff 173.1)_
   - swing : **0.4274** [0.376 ; 0.48] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4158** [0.3647 ; 0.4683] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.3 pt), swing (31.1 pt), deep (31.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.27 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.16 % contre 7.22 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1989** (β de hausse 0.9444, asymétrie 1.2694) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.892× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 23.2014 sur atr_grid (2.0 ATR, 9.581 %) — p(stop avant cible) 0.427 [0.38 ; 0.48], R/R 0.834, perte reelle 20.706 % (gap inclus), CVaR 9.642 %, EV -2.4603 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.28 ATR (stop 3.701 %) — p(stop avant cible) 0.723 [0.67 ; 0.77], R/R 1.998, perte reelle 8.643 % (gap inclus), EV -2.2514 % — **REFUSE**
      - refuse : p_stop_first 0.723, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.28 ATR du spot — compartiment <1, mesure a 46.1 % de casse (IC clusterise [0.427 ; 0.494] sur 1133 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 21.6 % x 17.27 % + P(rien) 6.1 % x 4.34 % ne couvrent pas P(stop) 72.3 % x 8.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.186 %) — p(stop avant cible) 0.5606 [0.51 ; 0.61], R/R 1.148, perte reelle 15.045 % (gap inclus), EV -2.7169 % — **REFUSE**
      - refuse : p_stop_first 0.561, borne haute 0.612 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.72 %) : P(cible) 30.8 % x 17.27 % + P(rien) 13.1 % x 3.03 % ne couvrent pas P(stop) 56.1 % x 15.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.49 ATR (stop 14.301 %) — p(stop avant cible) 0.2756 [0.23 ; 0.32], R/R 0.7, perte reelle 24.668 % (gap inclus), EV -0.3626 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 36.5 % x 17.27 % + P(rien) 36.0 % x 0.38 % ne couvrent pas P(stop) 27.6 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.52 ATR (stop 24.044 %) — p(stop avant cible) 0.1214 [0.09 ; 0.16], R/R 0.575, perte reelle 30.031 % (gap inclus), EV 1.4851 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.06 % > budget 12.00 %
   - 🔴 grid_snapped a 0.28 ATR (stop 2.762 %) — p(stop avant cible) 0.7776 [0.73 ; 0.82], R/R 2.484, perte reelle 6.953 % (gap inclus), EV -2.0973 % — **REFUSE**
      - refuse : p_stop_first 0.778, borne haute 0.819 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.10 %) : P(cible) 17.9 % x 17.27 % + P(rien) 4.3 % x 4.91 % ne couvrent pas P(stop) 77.8 % x 6.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.791 %) — p(stop avant cible) 0.669 [0.62 ; 0.72], R/R 1.423, perte reelle 12.136 % (gap inclus), EV -3.4792 % — **REFUSE**
      - refuse : p_stop_first 0.669, borne haute 0.717 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.48 %) : P(cible) 24.8 % x 17.27 % + P(rien) 8.3 % x 4.25 % ne couvrent pas P(stop) 66.9 % x 12.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.988 %) — p(stop avant cible) 0.6092 [0.56 ; 0.66], R/R 1.287, perte reelle 13.415 % (gap inclus), EV -2.8786 % — **REFUSE**
      - refuse : p_stop_first 0.609, borne haute 0.659 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.88 %) : P(cible) 28.5 % x 17.27 % + P(rien) 10.6 % x 3.57 % ne couvrent pas P(stop) 60.9 % x 13.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.384 %) — p(stop avant cible) 0.5044 [0.45 ; 0.56], R/R 1.052, perte reelle 16.422 % (gap inclus), EV -2.2909 % — **REFUSE**
      - refuse : p_stop_first 0.504, borne haute 0.557 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.29 %) : P(cible) 32.1 % x 17.27 % + P(rien) 17.4 % x 2.56 % ne couvrent pas P(stop) 50.4 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.581 %) — p(stop avant cible) 0.427 [0.38 ; 0.48], R/R 0.834, perte reelle 20.706 % (gap inclus), EV -2.4603 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.46 %) : P(cible) 34.4 % x 17.27 % + P(rien) 22.9 % x 1.93 % ne couvrent pas P(stop) 42.7 % x 20.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.49 ATR (stop 13.362 %) — p(stop avant cible) 0.2893 [0.24 ; 0.34], R/R 0.7, perte reelle 24.668 % (gap inclus), EV -0.6096 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 36.5 % x 17.27 % + P(rien) 34.6 % x 0.66 % ne couvrent pas P(stop) 28.9 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 16.767 %) — p(stop avant cible) 0.2313 [0.19 ; 0.28], R/R 0.639, perte reelle 27.014 % (gap inclus), EV -0.0949 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 36.5 % x 17.27 % + P(rien) 40.4 % x -0.38 % ne couvrent pas P(stop) 23.1 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 19.163 %) — p(stop avant cible) 0.1971 [0.16 ; 0.24], R/R 0.575, perte reelle 30.031 % (gap inclus), EV -0.0102 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 37.0 % x 17.27 % + P(rien) 43.3 % x -1.10 % ne couvrent pas P(stop) 19.7 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.52 ATR (stop 23.105 %) — p(stop avant cible) 0.1322 [0.10 ; 0.17], R/R 0.575, perte reelle 30.031 % (gap inclus), EV 1.3029 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.12 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 26.349 %) — p(stop avant cible) 0.1051 [0.08 ; 0.14], R/R 0.529, perte reelle 32.641 % (gap inclus), EV 1.384 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.36 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.744 %) — p(stop avant cible) 0.0947 [0.07 ; 0.13], R/R 0.453, perte reelle 38.117 % (gap inclus), EV 1.0163 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.75 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 31.139 %) — p(stop avant cible) 0.0919 [0.06 ; 0.13], R/R 0.453, perte reelle 38.117 % (gap inclus), EV 1.0792 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 33.535 %) — p(stop avant cible) 0.0809 [0.06 ; 0.11], R/R 0.453, perte reelle 38.117 % (gap inclus), EV 1.2701 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.54 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.93 %) — p(stop avant cible) 0.0611 [0.04 ; 0.09], R/R 0.453, perte reelle 38.117 % (gap inclus), EV 1.7665 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.93 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 38.325 %) — p(stop avant cible) 0.0493 [0.03 ; 0.08], R/R 0.451, perte reelle 38.325 % (gap inclus), EV 1.9339 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.32 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 25.66, ATR14 1.2293 (4.791 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 1.916 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.24 % | 25.5985 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.479 % | 25.5371 | 82.45 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 95.9 % |
| 0.15 ATR | 0.719 % | 25.4756 | 78.43 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.71 % |
| 0.2 ATR | 0.958 % | 25.4141 | 72.55 % | 79.2 % | 83.2 % | 85.73 % | 89.52 % | 92.51 % |
| 0.25 ATR | 1.198 % | 25.3527 | 66.47 % | 74.58 % | 79.08 % | 82.38 % | 87.24 % | 90.91 % |
| 0.35 ATR | 1.677 % | 25.2297 | 54.51 % | 65.85 % | 70.92 % | 75.69 % | 82.39 % | 87.61 % |
| 0.5 ATR | 2.395 % | 25.0454 | 40.88 % | 54.17 % | 61.89 % | 68.8 % | 77.84 % | 85.21 % |
| 0.75 ATR | 3.593 % | 24.738 | 22.75 % | 37.78 % | 47.74 % | 55.81 % | 67.06 % | 76.52 % |
| 1.0 ATR | 4.791 % | 24.4307 | 13.04 % | 25.42 % | 34.38 % | 44.88 % | 57.57 % | 68.33 % |
| 1.25 ATR | 5.988 % | 24.1234 | 7.75 % | 17.86 % | 25.15 % | 36.42 % | 50.54 % | 62.34 % |
| 1.5 ATR | 7.186 % | 23.8161 | 3.82 % | 11.48 % | 17.78 % | 28.74 % | 43.52 % | 56.24 % |
| 2.0 ATR | 9.581 % | 23.2014 | 0.88 % | 5.4 % | 9.82 % | 17.22 % | 32.05 % | 44.66 % |
| 2.5 ATR | 11.977 % | 22.5868 | 0.1 % | 2.36 % | 4.91 % | 10.43 % | 22.16 % | 34.87 % |
| 3.0 ATR | 14.372 % | 21.9721 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.02 % | 27.57 % |
| 4.0 ATR | 19.163 % | 20.7429 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 18.88 % |
| 6.0 ATR | 28.744 % | 18.2843 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 9.19 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.01 ATR | 1.18 ATR | 1.62 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.25 ATR | 1.43 ATR | 1.99 ATR | 2.49 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 1.00 ATR | 1.36 ATR | 1.66 ATR | 1.88 ATR | 2.56 ATR | 3.52 ATR |
| **10 s.** | 0.57 ATR | 1.27 ATR | 1.45 ATR | 1.96 ATR | 2.36 ATR | 2.68 ATR | 3.92 ATR | 5.28 ATR |
| **20 s.** | 0.80 ATR | 1.77 ATR | 1.99 ATR | 2.63 ATR | 3.30 ATR | 3.87 ATR | 5.83 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.455–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.395 %, prix 25.0454), p(touche) 40.88 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (93.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.64–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.593 %, prix 24.738), p(touche) 37.78 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.791 %, prix 24.4306), p(touche) 34.38 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.997–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.791 %, prix 24.4306), p(touche) 44.88 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.447–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.186 %, prix 23.8161), p(touche) 43.52 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.985–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.581 %, prix 23.2015), p(touche) 44.66 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.085 | EV/share : €0.105 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 42 % | T3 28 %
- Kelly (position) : f* 0.059 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.6 | bear 5.5 | side 8.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 282.0 (= 11 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.337% → cible +1.735% / stop −8.0%, p_fill 86%, n_eff≈36.1) : P(cible|rempli) **56%** · **EV/risk -0.059** (×p_fill ; si rempli -0.55% du capital)
  - **swing** (entrée dip −0.749% → cible +3.879% / stop −4.827%, p_fill 90%, n_eff≈37.1) : P(cible|rempli) **51%** · **EV/risk -0.087** (×p_fill ; si rempli -0.46% du capital)
  - **deep** (entrée dip −1.124% → cible +5.485% / stop −7.268%, p_fill 93%, n_eff≈36.5) : P(cible|rempli) **46%** · **EV/risk -0.191** (×p_fill ; si rempli -1.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→75% · +2.0%→66% · +3.0%→52% · +5.0%→42% · +8.0%→20%
- Range intraday médian 7.5% (p90 22.19%) · excursion haute méd. +3.87% / basse méd. −3.93%
- Profil de vol intra : ouverture 5.336% vs midi 1.709% vs clôture 1.817% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.087)_ ; drift intra méd. -0.298% ; recovery-V 23%
- **σ réalisé intraday** 5.201% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 71% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 27.2105 (VA 26.8075–27.5825 ; dernier close 26.62)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 89% · **stop −5.18%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 40% (gap-down >1% 14% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −4.35%) · haut méd +0.81% · range méd 2.61%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −5.36%) · haut méd +1.32% · range méd 3.13%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −5.57%) · haut méd +1.96% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −1.65% (p90 −6.12%) · haut méd +2.1% · range méd 5.0%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 79% (122/159) · gap 20% · délai 0.4min · rebond 64% (85/122) (MFE +2.23%)
   - −1.0% : fill 30min 49% · séance 75% (116/159) · gap 14% · délai 1.8min · rebond 63% (79/116) (MFE +1.96%)
   - −1.5% : fill 30min 41% · séance 68% (103/159) · gap 10% · délai 6.8min · rebond 59% (64/103) (MFE +1.52%)
   - −2.0% : fill 30min 35% · séance 62% (95/159) · gap 5% · délai 7.7min · rebond 62% (60/95) (MFE +1.79%)
   - −3.0% : fill 30min 24% · séance 51% (81/159) · gap 4% · délai 39.8min · rebond 63% (59/81) (MFE +1.59%)
   - −4.0% : fill 30min 19% · séance 43% (70/159) · gap 3% · délai 86.3min · rebond 76% (57/70) (MFE +1.91%)
   - −5.0% : fill 30min 13% · séance 32% (57/159) · gap 2% · délai 85.2min · rebond 89% (52/57) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −4.28%) → stop au-delà de −1.87% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.07% (p90 −4.55%) → stop au-delà de −2.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −5.09%) → stop au-delà de −3.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1530 jambes) : jambe baissière méd −1.26% (p90 −3.19%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 94% (46/49) · rebond 57% (28/46)
      · −2.0% : fill 84% (42/49) · rebond 51% (24/42)
      · −3.0% : fill 78% (40/49) · rebond 71% (31/40)
      · −4.0% : fill 73% (37/49) · rebond 67% (29/37)
      · −5.0% : fill 55% (31/49) · rebond 79% (27/31)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 55% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:02** → P(séance verte=clôture>ouverture) 73% si début vert vs 13% si rouge (base 43% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 43% ; creux résiduel méd -2.73% (q20 -4.95%) → **SL/trailing à −4.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.37% → **scale +1.72% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **13%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.53%** (au-delà de la MAE q10 -6.53%), cible rebond +1.56% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.04% .. +6.22%] · haut q95 +7.81% · bas q05 -7.21%
   - 60min (n=160) : retour [-5.77% .. +6.2%] · haut q95 +8.4% · bas q05 -7.63%
   - 2h (n=160) : retour [-5.86% .. +8.92%] · haut q95 +9.95% · bas q05 -7.86%
   - 4h (n=160) : retour [-6.38% .. +8.93%] · haut q95 +11.48% · bas q05 -9.59%
   - 6h (n=160) : retour [-6.7% .. +9.29%] · haut q95 +12.91% · bas q05 -10.31%
   - session (n=160) : retour [-7.61% .. +11.64%] · haut q95 +13.25% · bas q05 -11.07%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 38.3  _(momentum baissier)_
- **ADX** : 9.5  _(pas de tendance nette)_
- **MACD** : hist 0.131  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 12.8%
- **ATR** : 1.23 (38.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.161  _(distribution)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 63.9  _(marche en range (choppy))_
- **MA** : MA20 27.08 · MA50 28.29 · MA200 26.27  _(prix < MA20)_
- **Dist MA** : MA20 -5.3% · MA50 -9.3% · MA200 -2.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (781225 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
