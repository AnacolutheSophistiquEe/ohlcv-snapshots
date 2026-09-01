# SOI

**Generated** : 2026-09-01T21:45:23.892529+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €110.55  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €110.55 (+2.0% vs entrée) · entrée €108.35 · stop €101.74 · T1 €114.65 · R/R 0.95  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.156 _(réel 5 s)_ (GBM 0.167) · ¼-Kelly 0.026 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 122 % hors [0,100] (R² max 0.59). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.310 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €107.09–€109.61 (mid €108.35)
- Spot actuel : €110.55 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €101.74 (stop swing_plan-based (-7.97%))
- Targets : T1 €114.65 · R/R 0.95 | T2 €120.95 · R/R 1.91 | T3 €127.26 · R/R 2.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €101.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.97 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **4.915 pt plus bas** dans le cas TYPIQUE (médiane), 16.036 au p90, **21.324 au pire**
   - perte réelle **15.318 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 7.97 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0344 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3522** [0.284 ; 0.4253] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.387** [0.3368 ; 0.4391] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.4113** [0.3604 ; 0.4637] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 30.7 observations effectives », dont la borne haute a 95 % vaut environ 9.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.3 pt), swing (35.8 pt), deep (33.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.49 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.12 % contre 7.53 % aujourd'hui, rapport 0.41)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.22 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1217** (β de hausse 1.6219, asymétrie 0.6916) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut -0.048× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 97.3429 sur atr_grid (2.0 ATR, 11.947 %) — p(stop avant cible) 0.4025 [0.35 ; 0.45], R/R 0.979, perte reelle 21.456 % (gap inclus), CVaR 11.969 %, EV -3.1068 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.76 ATR (stop 7.28 %) — p(stop avant cible) 0.5911 [0.54 ; 0.64], R/R 1.371, perte reelle 15.318 % (gap inclus), EV -3.8857 % — **REFUSE**
      - refuse : p_stop_first 0.591, borne haute 0.642 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.61 ATR du spot — compartiment <1, mesure a 46.6 % de casse (IC clusterise [0.432 ; 0.497] sur 1116 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.89 %) : P(cible) 19.3 % x 21.00 % + P(rien) 21.6 % x 5.15 % ne couvrent pas P(stop) 59.1 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.96 %) — p(stop avant cible) 0.5222 [0.47 ; 0.57], R/R 1.266, perte reelle 16.593 % (gap inclus), EV -3.3263 % — **REFUSE**
      - refuse : p_stop_first 0.522, borne haute 0.575 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.33 %) : P(cible) 21.0 % x 21.00 % + P(rien) 26.8 % x 3.48 % ne couvrent pas P(stop) 52.2 % x 16.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.37 ATR (stop 28.845 %) — p(stop avant cible) 0.0327 [0.02 ; 0.06], R/R 0.717, perte reelle 29.294 % (gap inclus), EV 1.8162 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.85 % > budget 12.00 %
   - 🟢 support a 6.87 ATR (stop 43.77 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.48, perte reelle 43.77 % (gap inclus), EV 1.7886 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.77 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.493 %) — p(stop avant cible) 0.8874 [0.85 ; 0.92], R/R 6.58, perte reelle 3.192 % (gap inclus), EV -0.9694 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.887, borne haute 0.917 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 7.0 % x 21.00 % + P(rien) 4.3 % x 9.28 % ne couvrent pas P(stop) 88.7 % x 3.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.987 %) — p(stop avant cible) 0.7807 [0.73 ; 0.82], R/R 3.845, perte reelle 5.463 % (gap inclus), EV -0.7515 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.781, borne haute 0.822 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 13.3 % x 21.00 % + P(rien) 8.7 % x 8.36 % ne couvrent pas P(stop) 78.1 % x 5.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.76 ATR (stop 6.36 %) — p(stop avant cible) 0.6161 [0.56 ; 0.67], R/R 1.592, perte reelle 13.196 % (gap inclus), EV -3.0051 % — **REFUSE**
      - refuse : p_stop_first 0.616, borne haute 0.666 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.01 %) : P(cible) 18.9 % x 21.00 % + P(rien) 19.5 % x 5.94 % ne couvrent pas P(stop) 61.6 % x 13.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.453 %) — p(stop avant cible) 0.4468 [0.40 ; 0.50], R/R 0.979, perte reelle 21.456 % (gap inclus), EV -3.9794 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.98 %) : P(cible) 23.4 % x 21.00 % + P(rien) 31.9 % x 2.18 % ne couvrent pas P(stop) 44.7 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.947 %) — p(stop avant cible) 0.4025 [0.35 ; 0.45], R/R 0.979, perte reelle 21.456 % (gap inclus), EV -3.1068 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.11 %) : P(cible) 24.2 % x 21.00 % + P(rien) 35.6 % x 1.27 % ne couvrent pas P(stop) 40.2 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 13.44 %) — p(stop avant cible) 0.3448 [0.30 ; 0.40], R/R 0.979, perte reelle 21.456 % (gap inclus), EV -1.933 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 25.4 % x 21.00 % + P(rien) 40.2 % x 0.35 % ne couvrent pas P(stop) 34.5 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 14.933 %) — p(stop avant cible) 0.302 [0.26 ; 0.35], R/R 0.979, perte reelle 21.456 % (gap inclus), EV -1.1846 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 25.4 % x 21.00 % + P(rien) 44.4 % x -0.07 % ne couvrent pas P(stop) 30.2 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 16.427 %) — p(stop avant cible) 0.2442 [0.20 ; 0.29], R/R 0.875, perte reelle 24.006 % (gap inclus), EV -0.5285 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 27.0 % x 21.00 % + P(rien) 48.6 % x -0.68 % ne couvrent pas P(stop) 24.4 % x 24.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 17.92 %) — p(stop avant cible) 0.2076 [0.17 ; 0.25], R/R 0.875, perte reelle 24.006 % (gap inclus), EV 0.2235 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.93 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.907 %) — p(stop avant cible) 0.1153 [0.08 ; 0.15], R/R 0.717, perte reelle 29.294 % (gap inclus), EV 0.8177 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.91 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.894 %) — p(stop avant cible) 0.0675 [0.04 ; 0.10], R/R 0.717, perte reelle 29.294 % (gap inclus), EV 1.5378 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.90 % > budget 12.00 %
   - 🟢 grid_snapped a 4.37 ATR (stop 27.925 %) — p(stop avant cible) 0.0476 [0.03 ; 0.07], R/R 0.717, perte reelle 29.294 % (gap inclus), EV 1.7104 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.93 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.867 %) — p(stop avant cible) 0.0327 [0.02 ; 0.06], R/R 0.703, perte reelle 29.867 % (gap inclus), EV 1.7974 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.854 %) — p(stop avant cible) 0.0327 [0.02 ; 0.06], R/R 0.639, perte reelle 32.854 % (gap inclus), EV 1.6997 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.85 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.84 %) — p(stop avant cible) 0.0223 [0.01 ; 0.04], R/R 0.586, perte reelle 35.84 % (gap inclus), EV 1.7067 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.84 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.827 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 0.541, perte reelle 38.827 % (gap inclus), EV 1.7237 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.83 % > budget 12.00 %
   - 🟢 grid_snapped a 6.87 ATR (stop 42.85 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.49, perte reelle 42.85 % (gap inclus), EV 1.7886 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.85 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 44.8 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.469, perte reelle 44.8 % (gap inclus), EV 1.7886 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.80 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.787 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.44, perte reelle 47.787 % (gap inclus), EV 1.7886 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.79 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 110.55, ATR14 6.6036 (5.973 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 2.138 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.299 % | 110.2198 | 91.08 % | 94.11 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.597 % | 109.8896 | 84.9 % | 89.99 % | 92.04 % | 94.59 % | 96.24 % | 97.4 % |
| 0.15 ATR | 0.896 % | 109.5595 | 77.94 % | 85.08 % | 87.92 % | 91.14 % | 93.77 % | 95.3 % |
| 0.2 ATR | 1.195 % | 109.2293 | 69.51 % | 80.08 % | 83.99 % | 88.29 % | 91.59 % | 93.41 % |
| 0.25 ATR | 1.493 % | 108.8991 | 63.04 % | 76.25 % | 80.75 % | 86.61 % | 90.31 % | 92.81 % |
| 0.35 ATR | 2.091 % | 108.2388 | 50.78 % | 67.71 % | 73.77 % | 81.5 % | 86.05 % | 90.21 % |
| 0.5 ATR | 2.987 % | 107.2482 | 35.88 % | 55.45 % | 62.97 % | 73.62 % | 81.4 % | 87.51 % |
| 0.75 ATR | 4.48 % | 105.5973 | 16.96 % | 35.53 % | 47.15 % | 59.06 % | 73.79 % | 81.32 % |
| 1.0 ATR | 5.973 % | 103.9464 | 8.24 % | 24.14 % | 34.28 % | 48.03 % | 65.58 % | 75.92 % |
| 1.25 ATR | 7.467 % | 102.2955 | 4.12 % | 15.7 % | 25.44 % | 37.8 % | 57.27 % | 70.23 % |
| 1.5 ATR | 8.96 % | 100.6446 | 2.35 % | 10.7 % | 18.66 % | 30.22 % | 49.46 % | 64.14 % |
| 2.0 ATR | 11.947 % | 97.3429 | 0.59 % | 4.61 % | 8.94 % | 18.31 % | 35.61 % | 53.85 % |
| 2.5 ATR | 14.933 % | 94.0411 | 0.29 % | 2.45 % | 4.81 % | 11.71 % | 24.73 % | 45.75 % |
| 3.0 ATR | 17.92 % | 90.7393 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 17.21 % | 37.76 % |
| 4.0 ATR | 23.894 % | 84.1357 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.79 % | 24.58 % |
| 6.0 ATR | 35.84 % | 70.9286 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.19 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.63 ATR | 0.81 ATR | 0.98 ATR | 1.12 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.27 ATR | 1.45 ATR | 1.95 ATR | 2.48 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.41 ATR | 1.72 ATR | 1.93 ATR | 2.69 ATR | 3.59 ATR |
| **10 s.** | 0.71 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.49 ATR | 2.81 ATR | 3.97 ATR | 5.79 ATR |
| **20 s.** | 1.04 ATR | 2.24 ATR | 2.55 ATR | 3.36 ATR | 3.97 ATR | 4.74 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.631–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.792–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.973 %, prix 103.9469), p(touche) 34.28 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.074–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.467 %, prix 102.2952), p(touche) 37.8 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.661–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.547–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.167 | EV/share : €1.105 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 31 % | T3 21 %
- Kelly (position) : f* 0.104 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 74.5 | bear 19.5 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 221.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.911% → cible +7.487% / stop −3.743%, p_fill 75%, n_eff≈33.8) : P(cible|rempli) **9%** · **EV/risk -0.045** (×p_fill ; si rempli -0.23% du capital)
  - **swing** (entrée dip −1.997% → cible +5.818% / stop −6.095%, p_fill 66%, n_eff≈27.3) : P(cible|rempli) **40%** · **EV/risk -0.156** (×p_fill ; si rempli -1.43% du capital)
  - **deep** (entrée dip −3.08% → cible +8.227% / stop −9.245%, p_fill 72%, n_eff≈30.7) : P(cible|rempli) **39%** · **EV/risk -0.227** (×p_fill ; si rempli -2.92% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→65% · +3.0%→50% · +5.0%→31% · +8.0%→9%
- Range intraday médian 7.72% (p90 13.93%) · excursion haute méd. +3.14% / basse méd. −3.25%
- Profil de vol intra : ouverture 4.727% vs midi 1.336% vs clôture 2.087% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.062)_ ; drift intra méd. -0.394% ; recovery-V 38%
- **σ réalisé intraday** 4.322% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 52% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 111.7212 (VA 109.7812–116.5712 ; dernier close 115.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 46% · rebond 85% · **stop −7.75%** sous le fill (sous le bruit) · cible +3.22% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 40% (gap-down >1% 28% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −3.5%) · haut méd +0.89% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −4.81%) · haut méd +1.25% · range méd 3.22%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −5.13%) · haut méd +1.35% · range méd 3.5%
- Excursion ouverture 60min (n=160) : bas méd −1.54% (p90 −5.54%) · haut méd +1.58% · range méd 3.92%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 114.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 76% (125/159) · gap 36% · délai 0.1min · rebond 69% (88/125) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 71% (113/159) · gap 28% · délai 0.2min · rebond 74% (84/113) (MFE +1.99%)
   - −1.5% : fill 30min 50% · séance 63% (105/159) · gap 22% · délai 0.3min · rebond 75% (78/105) (MFE +2.33%)
   - −2.0% : fill 30min 42% · séance 59% (94/159) · gap 19% · délai 0.4min · rebond 70% (71/94) (MFE +2.45%)
   - −3.0% : fill 30min 34% · séance 46% (77/159) · gap 10% · délai 1.2min · rebond 85% (66/77) (MFE +3.22%)
   - −4.0% : fill 30min 25% · séance 38% (64/159) · gap 6% · délai 5.9min · rebond 80% (54/64) (MFE +3.47%)
   - −5.0% : fill 30min 16% · séance 30% (48/159) · gap 2% · délai 26.8min · rebond 70% (38/48) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.85% (p90 −3.5%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.45%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.28%) → stop au-delà de −1.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1336 jambes) : jambe baissière méd −1.31% (p90 −3.15%) · ~16.0 jambes/séance
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
      · −1.0% : fill 51% (47/88) · rebond 82% (38/47)
      · −2.0% : fill 34% (32/88) · rebond 70% (23/32)
      · −3.0% : fill 20% (22/88) · rebond 96% (19/22)
      · −4.0% : fill 17% (17/88) · rebond 68% (13/17)
      · −5.0% : fill 13% (10/88) · rebond 48% (6/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 63% si les 15 1res min sont vertes (77 cas) · 35% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 73% si début vert vs 24% si rouge (base 49% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **73%** · continue >prix actuel 53% ; creux résiduel méd -1.81% (q20 -5.04%) → **SL/trailing à −5.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.35% / q75 +4.7% → **scale +2.35% / runner +4.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 66%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.67%** (au-delà de la MAE q10 -8.67%), cible rebond +2.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.68% .. +6.14%] · haut q95 +7.43% · bas q05 -6.01%
   - 60min (n=160) : retour [-5.47% .. +6.71%] · haut q95 +7.9% · bas q05 -6.6%
   - 2h (n=160) : retour [-6.06% .. +6.23%] · haut q95 +9.84% · bas q05 -7.55%
   - 4h (n=160) : retour [-7.02% .. +8.29%] · haut q95 +11.85% · bas q05 -8.23%
   - 6h (n=160) : retour [-8.01% .. +9.34%] · haut q95 +12.47% · bas q05 -9.44%
   - session (n=160) : retour [-11.43% .. +11.49%] · haut q95 +14.27% · bas q05 -12.75%


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

- **RSI** : 30.8  _(momentum baissier)_
- **ADX** : 13.0  _(pas de tendance nette)_
- **MACD** : hist -0.927  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 30.9%
- **ATR** : 6.6 (61.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.313  _(distribution)_
- **Vol ratio** : 1.12  _(volume normal)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 117.19 · MA50 109.96 · MA200 79.5  _(prix < MA20)_
- **Dist MA** : MA20 -5.7% · MA50 +0.5% · MA200 +39.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (800715 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
