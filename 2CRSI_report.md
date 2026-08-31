# AL2SI

**Generated** : 2026-08-31T21:46:49.319386+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €26.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €26.40 (+2.3% vs entrée) · entrée €25.81 · stop €24.55 · T1 €26.82 · R/R 0.8  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.182 _(réel 5 s)_ (GBM 0.098) · ¼-Kelly 0.018 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 259 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €25.60–€26.01 (mid €25.81)
- Spot actuel : €26.40 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : €24.55 (stop swing_plan-based (-6.99%))
- Targets : T1 €26.82 · R/R 0.8 | T2 €27.84 · R/R 1.61 | T3 €28.85 · R/R 2.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.99 %)** : le gap seul le franchit 1.016 % des séances (13 fois sur 1280).
   - exécution **2.867 pt plus bas** dans le cas TYPIQUE (médiane), 19.705 au p90, **31.127 au pire**
   - perte réelle **15.045 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 6.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0818 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.533** [0.4586 ; 0.6063] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4285** [0.3771 ; 0.4811] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4191** [0.3679 ; 0.4716] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 31.2 observations effectives », dont la borne haute a 95 % vaut environ 9.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.1 pt), swing (33.1 pt), deep (33.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.27 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.08 % contre 7.23 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1989** (β de hausse 0.9478, asymétrie 1.2649) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.892× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 23.2696 sur atr_grid (2.5 ATR, 11.857 %) — p(stop avant cible) 0.3194 [0.27 ; 0.37], R/R 0.566, perte reelle 24.668 % (gap inclus), CVaR 11.907 %, EV -1.8893 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.86 ATR (stop 6.239 %) — p(stop avant cible) 0.5859 [0.53 ; 0.64], R/R 1.004, perte reelle 13.9 % (gap inclus), EV -3.1981 % — **REFUSE**
      - refuse : p_stop_first 0.586, borne haute 0.637 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.86 ATR du spot — compartiment <1, mesure a 46.4 % de casse (IC clusterise [0.430 ; 0.496] sur 1146 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.20 %) : P(cible) 33.7 % x 13.96 % + P(rien) 7.8 % x 3.22 % ne couvrent pas P(stop) 58.6 % x 13.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.03 ATR (stop 16.542 %) — p(stop avant cible) 0.2335 [0.19 ; 0.28], R/R 0.517, perte reelle 27.014 % (gap inclus), EV -0.6092 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 42.9 % x 13.96 % + P(rien) 33.8 % x -0.85 % ne couvrent pas P(stop) 23.4 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.03 ATR (stop 26.012 %) — p(stop avant cible) 0.1078 [0.08 ; 0.14], R/R 0.428, perte reelle 32.641 % (gap inclus), EV 0.8643 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.02 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.186 %) — p(stop avant cible) 0.886 [0.85 ; 0.92], R/R 4.268, perte reelle 3.27 % (gap inclus), EV -1.3538 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.886, borne haute 0.916 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 10.7 % x 13.96 % + P(rien) 0.7 % x 6.75 % ne couvrent pas P(stop) 88.6 % x 3.27 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.371 %) — p(stop avant cible) 0.7965 [0.75 ; 0.84], R/R 2.312, perte reelle 6.036 % (gap inclus), EV -2.1295 % — **REFUSE**
      - refuse : p_stop_first 0.796, borne haute 0.836 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 18.5 % x 13.96 % + P(rien) 1.8 % x 5.28 % ne couvrent pas P(stop) 79.7 % x 6.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.86 ATR (stop 5.514 %) — p(stop avant cible) 0.6343 [0.58 ; 0.68], R/R 1.077, perte reelle 12.959 % (gap inclus), EV -3.835 % — **REFUSE**
      - refuse : p_stop_first 0.634, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.84 %) : P(cible) 29.6 % x 13.96 % + P(rien) 7.0 % x 3.70 % ne couvrent pas P(stop) 63.4 % x 12.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 7.114 %) — p(stop avant cible) 0.5518 [0.50 ; 0.60], R/R 0.928, perte reelle 15.045 % (gap inclus), EV -3.0932 % — **REFUSE**
      - refuse : p_stop_first 0.552, borne haute 0.604 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.09 %) : P(cible) 35.7 % x 13.96 % + P(rien) 9.1 % x 2.47 % ne couvrent pas P(stop) 55.2 % x 15.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.3 %) — p(stop avant cible) 0.4937 [0.44 ; 0.55], R/R 0.85, perte reelle 16.422 % (gap inclus), EV -2.6564 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.66 %) : P(cible) 37.1 % x 13.96 % + P(rien) 13.6 % x 2.05 % ne couvrent pas P(stop) 49.4 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.486 %) — p(stop avant cible) 0.4223 [0.37 ; 0.47], R/R 0.723, perte reelle 19.309 % (gap inclus), EV -2.3179 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.32 %) : P(cible) 40.1 % x 13.96 % + P(rien) 17.6 % x 1.33 % ne couvrent pas P(stop) 42.2 % x 19.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 10.672 %) — p(stop avant cible) 0.3605 [0.31 ; 0.41], R/R 0.62, perte reelle 22.515 % (gap inclus), EV -2.1168 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 41.8 % x 13.96 % + P(rien) 22.2 % x 0.77 % ne couvrent pas P(stop) 36.0 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.857 %) — p(stop avant cible) 0.3194 [0.27 ; 0.37], R/R 0.566, perte reelle 24.668 % (gap inclus), EV -1.8893 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.89 %) : P(cible) 42.2 % x 13.96 % + P(rien) 25.8 % x 0.36 % ne couvrent pas P(stop) 31.9 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 13.043 %) — p(stop avant cible) 0.2929 [0.25 ; 0.34], R/R 0.566, perte reelle 24.668 % (gap inclus), EV -1.2795 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 42.3 % x 13.96 % + P(rien) 28.4 % x 0.17 % ne couvrent pas P(stop) 29.3 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.03 ATR (stop 15.817 %) — p(stop avant cible) 0.2498 [0.21 ; 0.30], R/R 0.517, perte reelle 27.014 % (gap inclus), EV -0.9184 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 42.9 % x 13.96 % + P(rien) 32.1 % x -0.49 % ne couvrent pas P(stop) 25.0 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 18.972 %) — p(stop avant cible) 0.195 [0.16 ; 0.24], R/R 0.465, perte reelle 30.031 % (gap inclus), EV -0.4447 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 43.4 % x 13.96 % + P(rien) 37.1 % x -1.73 % ne couvrent pas P(stop) 19.5 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 21.343 %) — p(stop avant cible) 0.1582 [0.12 ; 0.20], R/R 0.465, perte reelle 30.031 % (gap inclus), EV 0.2408 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.36 % > budget 12.00 %
   - 🟢 grid_snapped a 5.03 ATR (stop 25.287 %) — p(stop avant cible) 0.1126 [0.08 ; 0.15], R/R 0.428, perte reelle 32.641 % (gap inclus), EV 0.8095 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.30 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.458 %) — p(stop avant cible) 0.0955 [0.07 ; 0.13], R/R 0.366, perte reelle 38.117 % (gap inclus), EV 0.506 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.47 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 30.829 %) — p(stop avant cible) 0.0941 [0.07 ; 0.13], R/R 0.366, perte reelle 38.117 % (gap inclus), EV 0.5327 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 33.201 %) — p(stop avant cible) 0.0815 [0.06 ; 0.11], R/R 0.366, perte reelle 38.117 % (gap inclus), EV 0.7672 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.572 %) — p(stop avant cible) 0.0614 [0.04 ; 0.09], R/R 0.366, perte reelle 38.117 % (gap inclus), EV 1.253 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.57 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.944 %) — p(stop avant cible) 0.0546 [0.03 ; 0.08], R/R 0.366, perte reelle 38.117 % (gap inclus), EV 1.3477 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.94 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 26.4, ATR14 1.2521 (4.743 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 1.897 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.237 % | 26.3374 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.474 % | 26.2748 | 82.45 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 96.0 % |
| 0.15 ATR | 0.711 % | 26.2122 | 78.43 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.81 % |
| 0.2 ATR | 0.949 % | 26.1496 | 72.55 % | 79.2 % | 83.2 % | 85.83 % | 89.52 % | 92.61 % |
| 0.25 ATR | 1.186 % | 26.087 | 66.47 % | 74.58 % | 79.08 % | 82.48 % | 87.24 % | 91.01 % |
| 0.35 ATR | 1.66 % | 25.9617 | 54.51 % | 65.75 % | 70.92 % | 75.79 % | 82.39 % | 87.71 % |
| 0.5 ATR | 2.371 % | 25.7739 | 40.88 % | 54.27 % | 61.89 % | 68.9 % | 77.84 % | 85.31 % |
| 0.75 ATR | 3.557 % | 25.4609 | 22.75 % | 37.88 % | 47.84 % | 55.91 % | 67.16 % | 76.62 % |
| 1.0 ATR | 4.743 % | 25.1479 | 13.04 % | 25.52 % | 34.48 % | 44.98 % | 57.67 % | 68.43 % |
| 1.25 ATR | 5.929 % | 24.8348 | 7.75 % | 17.86 % | 25.25 % | 36.52 % | 50.64 % | 62.44 % |
| 1.5 ATR | 7.114 % | 24.5218 | 3.82 % | 11.48 % | 17.88 % | 28.84 % | 43.62 % | 56.34 % |
| 2.0 ATR | 9.486 % | 23.8957 | 0.88 % | 5.4 % | 9.92 % | 17.32 % | 32.15 % | 44.76 % |
| 2.5 ATR | 11.857 % | 23.2696 | 0.1 % | 2.36 % | 5.01 % | 10.53 % | 22.26 % | 34.97 % |
| 3.0 ATR | 14.229 % | 22.6436 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.12 % | 27.67 % |
| 4.0 ATR | 18.972 % | 21.3914 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 18.98 % |
| 6.0 ATR | 28.458 % | 18.8871 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 9.29 % |

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
- **1 seance(s)** : plage utile 0.455–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.371 %, prix 25.7741), p(touche) 40.88 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (93.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.641–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.557 %, prix 25.461), p(touche) 37.88 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.743 %, prix 25.1478), p(touche) 34.48 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.743 %, prix 25.1478), p(touche) 44.98 % (en stress 97.06 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.114 %, prix 24.5219), p(touche) 43.62 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.99–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.486 %, prix 23.8957), p(touche) 44.76 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.098 | EV/share : €0.123 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 42 % | T3 28 %
- Kelly (position) : f* 0.07 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.6 | bear 5.5 | side 8.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 264.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.025% → cible +1.758% / stop −1.5%, p_fill 78%, n_eff≈34.9) : P(cible|rempli) **45%** · **EV/risk -0.053** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −2.247% → cible +3.931% / stop −4.852%, p_fill 63%, n_eff≈31.2) : P(cible|rempli) **40%** · **EV/risk -0.182** (×p_fill ; si rempli -1.40% du capital)
  - **deep** (entrée dip −3.475% → cible +5.56% / stop −7.371%, p_fill 77%, n_eff≈30.9) : P(cible|rempli) **44%** · **EV/risk -0.119** (×p_fill ; si rempli -1.14% du capital)
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 39.7  _(momentum baissier)_
- **ADX** : 9.9  _(pas de tendance nette)_
- **MACD** : hist 0.219  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 13.0%
- **ATR** : 1.25 (41.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.106  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 62.1  _(marche en range (choppy))_
- **MA** : MA20 27.08 · MA50 28.33 · MA200 26.2  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 -6.8% · MA200 +0.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (795220 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
