# AL2SI

**Generated** : 2026-09-01T00:12:02.893678+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €26.62  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €26.62 (+2.7% vs entrée) · entrée €25.91 · stop €24.65 · T1 €26.91 · R/R 0.79  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.196 _(réel 5 s)_ (GBM 0.099) · ¼-Kelly 0.018 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 267 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €25.70–€26.11 (mid €25.91)
- Spot actuel : €26.62 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : €24.65 (stop swing_plan-based (-7.39%))
- Targets : T1 €26.91 · R/R 0.79 | T2 €27.91 · R/R 1.59 | T3 €28.91 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.65


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.39 %)** : le gap seul le franchit 0.938 % des séances (12 fois sur 1280).
   - exécution **3.412 pt plus bas** dans le cas TYPIQUE (médiane), 19.54 au p90, **30.727 au pire**
   - perte réelle **15.687 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 7.39 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0778 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 12 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5326** [0.4582 ; 0.6059] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.427** [0.3757 ; 0.4796] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4155** [0.3644 ; 0.468] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 28.2 observations effectives », dont la borne haute a 95 % vaut environ 10.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.8 pt), swing (33.9 pt), deep (35.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.27 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.08 % contre 7.22 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1985** (β de hausse 0.9478, asymétrie 1.2644) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.879× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 23.4896 sur atr_grid (2.5 ATR, 11.759 %) — p(stop avant cible) 0.3188 [0.27 ; 0.37], R/R 0.528, perte reelle 24.668 % (gap inclus), CVaR 11.809 %, EV -2.0467 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.04 ATR (stop 7.014 %) — p(stop avant cible) 0.5506 [0.50 ; 0.60], R/R 0.865, perte reelle 15.045 % (gap inclus), EV -3.2536 % — **REFUSE**
      - refuse : p_stop_first 0.551, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.25 %) : P(cible) 37.4 % x 13.01 % + P(rien) 7.5 % x 2.10 % ne couvrent pas P(stop) 55.1 % x 15.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.21 ATR (stop 17.232 %) — p(stop avant cible) 0.2173 [0.18 ; 0.26], R/R 0.482, perte reelle 27.014 % (gap inclus), EV -0.3497 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 46.6 % x 13.01 % + P(rien) 31.7 % x -1.72 % ne couvrent pas P(stop) 21.7 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.21 ATR (stop 26.624 %) — p(stop avant cible) 0.1056 [0.08 ; 0.14], R/R 0.399, perte reelle 32.641 % (gap inclus), EV 0.7432 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.63 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.176 %) — p(stop avant cible) 0.8829 [0.85 ; 0.91], R/R 4.01, perte reelle 3.245 % (gap inclus), EV -1.3645 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.883, borne haute 0.914 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 11.4 % x 13.01 % + P(rien) 0.3 % x 5.20 % ne couvrent pas P(stop) 88.3 % x 3.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.352 %) — p(stop avant cible) 0.7916 [0.75 ; 0.83], R/R 2.198, perte reelle 5.921 % (gap inclus), EV -2.094 % — **REFUSE**
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 19.4 % x 13.01 % + P(rien) 1.4 % x 4.74 % ne couvrent pas P(stop) 79.2 % x 5.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.528 %) — p(stop avant cible) 0.7104 [0.66 ; 0.76], R/R 1.556, perte reelle 8.366 % (gap inclus), EV -2.3686 % — **REFUSE**
      - refuse : p_stop_first 0.710, borne haute 0.756 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.37 %) : P(cible) 26.7 % x 13.01 % + P(rien) 2.3 % x 4.42 % ne couvrent pas P(stop) 71.0 % x 8.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.04 ATR (stop 6.295 %) — p(stop avant cible) 0.5789 [0.53 ; 0.63], R/R 0.901, perte reelle 14.446 % (gap inclus), EV -3.5005 % — **REFUSE**
      - refuse : p_stop_first 0.579, borne haute 0.630 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.50 %) : P(cible) 36.0 % x 13.01 % + P(rien) 6.2 % x 2.97 % ne couvrent pas P(stop) 57.9 % x 14.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.232 %) — p(stop avant cible) 0.4932 [0.44 ; 0.55], R/R 0.792, perte reelle 16.422 % (gap inclus), EV -2.7848 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.78 %) : P(cible) 39.5 % x 13.01 % + P(rien) 11.2 % x 1.54 % ne couvrent pas P(stop) 49.3 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.408 %) — p(stop avant cible) 0.4197 [0.37 ; 0.47], R/R 0.674, perte reelle 19.309 % (gap inclus), EV -2.4199 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 42.7 % x 13.01 % + P(rien) 15.4 % x 0.86 % ne couvrent pas P(stop) 42.0 % x 19.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 10.583 %) — p(stop avant cible) 0.3611 [0.31 ; 0.41], R/R 0.578, perte reelle 22.515 % (gap inclus), EV -2.2658 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.27 %) : P(cible) 44.7 % x 13.01 % + P(rien) 19.2 % x 0.25 % ne couvrent pas P(stop) 36.1 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.759 %) — p(stop avant cible) 0.3188 [0.27 ; 0.37], R/R 0.528, perte reelle 24.668 % (gap inclus), EV -2.0467 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 45.2 % x 13.01 % + P(rien) 22.9 % x -0.27 % ne couvrent pas P(stop) 31.9 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 12.935 %) — p(stop avant cible) 0.2882 [0.24 ; 0.34], R/R 0.528, perte reelle 24.668 % (gap inclus), EV -1.239 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 46.0 % x 13.01 % + P(rien) 25.2 % x -0.43 % ne couvrent pas P(stop) 28.8 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.21 ATR (stop 16.513 %) — p(stop avant cible) 0.2297 [0.19 ; 0.28], R/R 0.482, perte reelle 27.014 % (gap inclus), EV -0.5629 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 46.6 % x 13.01 % + P(rien) 30.4 % x -1.39 % ne couvrent pas P(stop) 23.0 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 18.815 %) — p(stop avant cible) 0.1991 [0.16 ; 0.24], R/R 0.433, perte reelle 30.031 % (gap inclus), EV -0.6727 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 46.6 % x 13.01 % + P(rien) 33.5 % x -2.27 % ne couvrent pas P(stop) 19.9 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 21.167 %) — p(stop avant cible) 0.1566 [0.12 ; 0.20], R/R 0.433, perte reelle 30.031 % (gap inclus), EV 0.2531 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.19 % > budget 12.00 %
   - 🟢 grid_snapped a 5.21 ATR (stop 25.904 %) — p(stop avant cible) 0.1092 [0.08 ; 0.15], R/R 0.399, perte reelle 32.641 % (gap inclus), EV 0.7046 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.91 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.223 %) — p(stop avant cible) 0.0956 [0.07 ; 0.13], R/R 0.341, perte reelle 38.117 % (gap inclus), EV 0.3665 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.23 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 30.574 %) — p(stop avant cible) 0.0941 [0.07 ; 0.13], R/R 0.341, perte reelle 38.117 % (gap inclus), EV 0.3937 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.58 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 32.926 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 0.341, perte reelle 38.117 % (gap inclus), EV 0.5641 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.93 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.278 %) — p(stop avant cible) 0.0622 [0.04 ; 0.09], R/R 0.341, perte reelle 38.117 % (gap inclus), EV 1.0951 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.28 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.63 %) — p(stop avant cible) 0.0546 [0.03 ; 0.08], R/R 0.341, perte reelle 38.117 % (gap inclus), EV 1.2038 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.63 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 26.62, ATR14 1.2521 (4.704 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 1.882 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.235 % | 26.5574 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.47 % | 26.4948 | 82.45 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 96.0 % |
| 0.15 ATR | 0.706 % | 26.4322 | 78.43 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.81 % |
| 0.2 ATR | 0.941 % | 26.3696 | 72.55 % | 79.2 % | 83.2 % | 85.83 % | 89.52 % | 92.61 % |
| 0.25 ATR | 1.176 % | 26.307 | 66.47 % | 74.58 % | 79.08 % | 82.48 % | 87.24 % | 91.01 % |
| 0.35 ATR | 1.646 % | 26.1818 | 54.51 % | 65.85 % | 70.92 % | 75.79 % | 82.39 % | 87.71 % |
| 0.5 ATR | 2.352 % | 25.9939 | 40.88 % | 54.27 % | 61.89 % | 68.9 % | 77.84 % | 85.31 % |
| 0.75 ATR | 3.528 % | 25.6809 | 22.75 % | 37.88 % | 47.84 % | 55.91 % | 67.16 % | 76.62 % |
| 1.0 ATR | 4.704 % | 25.3679 | 13.04 % | 25.52 % | 34.48 % | 44.98 % | 57.67 % | 68.43 % |
| 1.25 ATR | 5.88 % | 25.0548 | 7.75 % | 17.86 % | 25.25 % | 36.52 % | 50.64 % | 62.44 % |
| 1.5 ATR | 7.056 % | 24.7418 | 3.82 % | 11.48 % | 17.88 % | 28.84 % | 43.62 % | 56.34 % |
| 2.0 ATR | 9.408 % | 24.1157 | 0.88 % | 5.4 % | 9.92 % | 17.32 % | 32.15 % | 44.76 % |
| 2.5 ATR | 11.759 % | 23.4896 | 0.1 % | 2.36 % | 5.01 % | 10.53 % | 22.26 % | 34.97 % |
| 3.0 ATR | 14.111 % | 22.8636 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.12 % | 27.67 % |
| 4.0 ATR | 18.815 % | 21.6114 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 18.98 % |
| 6.0 ATR | 28.223 % | 19.1071 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 9.29 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.02 ATR | 1.18 ATR | 1.62 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.26 ATR | 1.43 ATR | 2.00 ATR | 2.50 ATR |
| **5 s.** | 0.37 ATR | 0.89 ATR | 1.00 ATR | 1.36 ATR | 1.67 ATR | 1.88 ATR | 2.58 ATR | 3.52 ATR |
| **10 s.** | 0.57 ATR | 1.27 ATR | 1.45 ATR | 1.96 ATR | 2.36 ATR | 2.68 ATR | 3.92 ATR | 5.28 ATR |
| **20 s.** | 0.80 ATR | 1.77 ATR | 1.99 ATR | 2.63 ATR | 3.31 ATR | 3.88 ATR | 5.85 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.455–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.352 %, prix 25.9939), p(touche) 40.88 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (93.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.641–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.528 %, prix 25.6808), p(touche) 37.88 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.704 %, prix 25.3678), p(touche) 34.48 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.704 %, prix 25.3678), p(touche) 44.98 % (en stress 97.06 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.056 %, prix 24.7417), p(touche) 43.62 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.99–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.408 %, prix 24.1156), p(touche) 44.76 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.099 | EV/share : €0.124 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 43 % | T3 28 %
- Kelly (position) : f* 0.072 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.6 | bear 5.5 | side 8.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 266.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.218% → cible +1.728% / stop −1.5%, p_fill 72%, n_eff≈33.1) : P(cible|rempli) **42%** · **EV/risk -0.073** (×p_fill ; si rempli -0.15% du capital)
  - **swing** (entrée dip −2.686% → cible +3.863% / stop −4.833%, p_fill 60%, n_eff≈30.2) : P(cible|rempli) **37%** · **EV/risk -0.196** (×p_fill ; si rempli -1.57% du capital)
  - **deep** (entrée dip −4.155% → cible +5.463% / stop −7.361%, p_fill 70%, n_eff≈28.2) : P(cible|rempli) **50%** · **EV/risk -0.145** (×p_fill ; si rempli -1.53% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→68% · +3.0%→54% · +5.0%→42% · +8.0%→20%
- Range intraday médian 7.5% (p90 22.19%) · excursion haute méd. +4.2% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.335% vs midi 1.714% vs clôture 1.821% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓1% ; spike-down 72% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.135% ; recovery-V 24%
- **σ réalisé intraday** 5.275% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 70% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 27.272 (VA 27.2–27.584 ; dernier close 27.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 89% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.58% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 41% (gap-down >1% 14% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.95% (p90 −4.35%) · haut méd +0.9% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −5.44%) · haut méd +1.4% · range méd 3.18%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −5.58%) · haut méd +1.96% · range méd 4.07%
- Excursion ouverture 60min (n=160) : bas méd −1.68% (p90 −6.12%) · haut méd +2.2% · range méd 5.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 78% (122/159) · gap 21% · délai 0.3min · rebond 66% (85/122) (MFE +2.33%)
   - −1.0% : fill 30min 50% · séance 74% (116/159) · gap 14% · délai 1.2min · rebond 65% (79/116) (MFE +1.99%)
   - −1.5% : fill 30min 41% · séance 67% (103/159) · gap 10% · délai 6.7min · rebond 61% (64/103) (MFE +1.52%)
   - −2.0% : fill 30min 35% · séance 61% (95/159) · gap 5% · délai 7.3min · rebond 60% (59/95) (MFE +1.82%)
   - −3.0% : fill 30min 24% · séance 50% (81/159) · gap 4% · délai 37.1min · rebond 66% (60/81) (MFE +1.65%)
   - −4.0% : fill 30min 20% · séance 44% (71/159) · gap 3% · délai 86.3min · rebond 76% (58/71) (MFE +1.91%)
   - −5.0% : fill 30min 14% · séance 32% (58/159) · gap 2% · délai 81.6min · rebond 89% (53/58) (MFE +2.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −4.28%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.07% (p90 −4.55%) → stop au-delà de −2.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −5.09%) → stop au-delà de −3.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1530 jambes) : jambe baissière méd −1.27% (p90 −3.19%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 94% (47/50) · rebond 57% (28/47)
      · −2.0% : fill 84% (43/50) · rebond 50% (24/43)
      · −3.0% : fill 78% (41/50) · rebond 71% (32/41)
      · −4.0% : fill 73% (38/50) · rebond 68% (30/38)
      · −5.0% : fill 55% (32/50) · rebond 79% (28/32)
   - **flat** (30 séances) :
      · −1.0% : fill 72% (23/30) · rebond 65% (16/23)
      · −2.0% : fill 49% (18/30) · rebond 57% (12/18)
      · −3.0% : fill 41% (13/30) · rebond 53% (8/13)
      · −4.0% : fill 36% (12/30) · rebond 85% (10/12)
      · −5.0% : fill 22% (9/30) · rebond 100% (9/9)
   - **gap-up** (79 séances) :
      · −1.0% : fill 63% (46/79) · rebond 71% (35/46)
      · −2.0% : fill 52% (34/79) · rebond 71% (23/34)
      · −3.0% : fill 38% (27/79) · rebond 66% (20/27)
      · −4.0% : fill 30% (21/79) · rebond 84% (18/21)
      · −5.0% : fill 24% (17/79) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 55% si les 15 1res min sont vertes (74 cas) · 34% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:02** → P(séance verte=clôture>ouverture) 73% si début vert vs 13% si rouge (base 44% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 43% ; creux résiduel méd -2.73% (q20 -4.95%) → **SL/trailing à −4.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.37% → **scale +1.72% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **13%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.69%** (au-delà de la MAE q10 -6.69%), cible rebond +1.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.06% .. +6.27%] · haut q95 +7.81% · bas q05 -7.25%
   - 60min (n=160) : retour [-5.78% .. +6.2%] · haut q95 +8.53% · bas q05 -7.63%
   - 2h (n=160) : retour [-5.88% .. +9.11%] · haut q95 +9.95% · bas q05 -7.88%
   - 4h (n=160) : retour [-6.44% .. +9.0%] · haut q95 +11.5% · bas q05 -9.63%
   - 6h (n=160) : retour [-6.7% .. +9.3%] · haut q95 +13.05% · bas q05 -10.4%
   - session (n=160) : retour [-7.66% .. +11.84%] · haut q95 +13.25% · bas q05 -11.08%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 40.8  _(momentum baissier)_
- **ADX** : 9.9  _(pas de tendance nette)_
- **MACD** : hist 0.233  _(pas de croisement recent)_
- **BB** : %B 0.37 · largeur 12.9%
- **ATR** : 1.25 (41.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.09  _(distribution)_
- **Vol ratio** : 0.46  _(volume atone)_
- **Choppiness** : 62.1  _(marche en range (choppy))_
- **MA** : MA20 27.09 · MA50 28.33 · MA200 26.21  _(prix < MA20)_
- **Dist MA** : MA20 -1.7% · MA50 -6.0% · MA200 +1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (789744 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
