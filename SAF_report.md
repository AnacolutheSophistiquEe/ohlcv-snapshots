# SAF

**Generated** : 2026-09-29T00:10:09.978955+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €333.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €333.00 (+6.6% vs entrée) · entrée €312.35 · stop €304.34 · T1 €318.46 · R/R 0.76  
> ↳ P(T1 av. stop) 53 % · EV/risk -0.029 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €311.12–€313.57 (mid €312.35)
- Spot actuel : €333.00 (+6.6% au-dessus de la zone — repli à attendre)
- Stop : €304.34 (plancher anti-bruit (R/R<2) ; -2.56 % depuis l'entree)
- Targets : T1 €318.46 · R/R 0.76 | T2 €324.57 · R/R 1.53 | T3 €330.68 · R/R 2.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €304.34


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.61 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.376 pt plus bas** dans le cas TYPIQUE (médiane), 1.376 au p90, **1.376 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.61 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0011 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1869** [0.1343 ; 0.2499] _(largeur 11.6 pt, n_eff 173.1)_
   - swing : **0.3781** [0.3282 ; 0.4301] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.332** [0.2839 ; 0.3829] _(largeur 9.9 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.08 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.26 % contre 2.21 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.06 % si l'on extrapolait par √5 _(rapport 0.934 ; < 1 = le √5 surestime)_
- **β de baisse : 1.386** (β de hausse 1.35, asymétrie 1.0267) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 296.9678 sur atr_grid (4.5 ATR, 10.82 %) — p(stop avant cible) 0.0617 [0.04 ; 0.09], R/R 0.784, perte reelle 10.82 % (gap inclus), CVaR 10.82 %, EV 0.7594 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.607 %) — p(stop avant cible) 0.4197 [0.37 ; 0.47], R/R 1.489, perte reelle 5.698 % (gap inclus), EV -0.0933 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 16.6 % x 8.48 % + P(rien) 41.5 % x 2.15 % ne couvrent pas P(stop) 42.0 % x 5.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.96 ATR (stop 6.295 %) — p(stop avant cible) 0.2206 [0.18 ; 0.27], R/R 0.849, perte reelle 9.986 % (gap inclus), EV 0.1227 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 4.79 ATR (stop 13.097 %) — p(stop avant cible) 0.0306 [0.02 ; 0.05], R/R 0.648, perte reelle 13.097 % (gap inclus), EV 0.7319 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.10 % > budget 12.00 %
   - 🟢 support a 9.16 ATR (stop 23.597 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.359, perte reelle 23.597 % (gap inclus), EV 0.7431 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.60 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.601 %) — p(stop avant cible) 0.8931 [0.86 ; 0.92], R/R 6.34, perte reelle 1.338 % (gap inclus), EV -0.5223 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.893, borne haute 0.922 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 5.5 % x 8.48 % + P(rien) 5.2 % x 3.94 % ne couvrent pas P(stop) 89.3 % x 1.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.202 %) — p(stop avant cible) 0.776 [0.73 ; 0.82], R/R 4.11, perte reelle 2.064 % (gap inclus), EV -0.3127 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.776, borne haute 0.818 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 9.2 % x 8.48 % + P(rien) 13.2 % x 3.84 % ne couvrent pas P(stop) 77.6 % x 2.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 1.803 %) — p(stop avant cible) 0.6813 [0.63 ; 0.73], R/R 2.951, perte reelle 2.875 % (gap inclus), EV -0.3079 % — **REFUSE**
      - refuse : cible atteinte seulement 11.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 11.1 % x 8.48 % + P(rien) 20.8 % x 3.42 % ne couvrent pas P(stop) 68.1 % x 2.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 2.405 %) — p(stop avant cible) 0.604 [0.55 ; 0.65], R/R 2.06, perte reelle 4.117 % (gap inclus), EV -0.5325 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.604, borne haute 0.654 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 13.4 % x 8.48 % + P(rien) 26.2 % x 3.12 % ne couvrent pas P(stop) 60.4 % x 4.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 3.006 %) — p(stop avant cible) 0.5081 [0.46 ; 0.56], R/R 1.764, perte reelle 4.809 % (gap inclus), EV -0.2448 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.508, borne haute 0.560 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 14.9 % x 8.48 % + P(rien) 34.3 % x 2.72 % ne couvrent pas P(stop) 50.8 % x 4.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.96 ATR (stop 5.436 %) — p(stop avant cible) 0.2584 [0.21 ; 0.31], R/R 0.849, perte reelle 9.986 % (gap inclus), EV -0.2315 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 18.8 % x 8.48 % + P(rien) 55.4 % x 1.37 % ne couvrent pas P(stop) 25.8 % x 9.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 6.613 %) — p(stop avant cible) 0.1937 [0.15 ; 0.24], R/R 0.849, perte reelle 9.986 % (gap inclus), EV 0.2476 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 7.214 %) — p(stop avant cible) 0.1502 [0.12 ; 0.19], R/R 0.849, perte reelle 9.986 % (gap inclus), EV 0.5077 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 8.416 %) — p(stop avant cible) 0.1108 [0.08 ; 0.15], R/R 0.849, perte reelle 9.986 % (gap inclus), EV 0.6587 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 9.618 %) — p(stop avant cible) 0.0785 [0.05 ; 0.11], R/R 0.849, perte reelle 9.986 % (gap inclus), EV 0.7556 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 10.82 %) — p(stop avant cible) 0.0617 [0.04 ; 0.09], R/R 0.784, perte reelle 10.82 % (gap inclus), EV 0.7594 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.79 ATR (stop 12.239 %) — p(stop avant cible) 0.0393 [0.02 ; 0.06], R/R 0.693, perte reelle 12.239 % (gap inclus), EV 0.7593 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 14.427 %) — p(stop avant cible) 0.0179 [0.01 ; 0.04], R/R 0.588, perte reelle 14.427 % (gap inclus), EV 0.7239 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.43 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 15.63 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 0.543, perte reelle 15.63 % (gap inclus), EV 0.7273 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 16.832 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.504, perte reelle 16.832 % (gap inclus), EV 0.733 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 18.034 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.47, perte reelle 18.034 % (gap inclus), EV 0.7324 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.03 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 19.236 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.441, perte reelle 19.236 % (gap inclus), EV 0.7333 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.24 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 333.0, ATR14 8.0071 (2.405 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 0.827 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.12 % | 332.5996 | 89.22 % | 92.54 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.24 % | 332.1993 | 81.37 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.361 % | 331.7989 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.481 % | 331.3986 | 67.94 % | 77.92 % | 82.42 % | 85.14 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.601 % | 330.9982 | 60.98 % | 73.41 % | 78.78 % | 83.07 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.842 % | 330.1975 | 49.31 % | 63.3 % | 69.65 % | 76.77 % | 82.69 % | 87.01 % |
| 0.5 ATR | 1.202 % | 328.9964 | 35.2 % | 51.62 % | 58.84 % | 68.41 % | 75.87 % | 81.42 % |
| 0.75 ATR | 1.803 % | 326.9946 | 20.49 % | 35.33 % | 42.53 % | 52.95 % | 63.11 % | 70.83 % |
| 1.0 ATR | 2.405 % | 324.9929 | 9.8 % | 23.55 % | 32.22 % | 41.83 % | 53.51 % | 61.44 % |
| 1.25 ATR | 3.006 % | 322.9911 | 4.41 % | 15.21 % | 23.67 % | 32.87 % | 46.09 % | 54.65 % |
| 1.5 ATR | 3.607 % | 320.9893 | 2.25 % | 9.91 % | 16.4 % | 24.7 % | 37.88 % | 46.75 % |
| 2.0 ATR | 4.809 % | 316.9857 | 0.98 % | 4.42 % | 7.47 % | 15.16 % | 26.71 % | 37.06 % |
| 2.5 ATR | 6.011 % | 312.9821 | 0.2 % | 1.47 % | 3.63 % | 8.56 % | 18.2 % | 28.47 % |
| 3.0 ATR | 7.214 % | 308.9786 | 0.0 % | 0.88 % | 2.06 % | 5.71 % | 12.07 % | 22.28 % |
| 4.0 ATR | 9.618 % | 300.9714 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.89 % |
| 6.0 ATR | 14.427 % | 284.9571 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.71 ATR | 0.98 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.25 ATR | 1.49 ATR | 1.75 ATR | 2.39 ATR | 3.15 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.28 ATR | 1.72 ATR | 2.10 ATR | 2.39 ATR | 3.27 ATR | 3.94 ATR |
| **20 s.** | 0.65 ATR | 1.40 ATR | 1.59 ATR | 2.24 ATR | 2.78 ATR | 3.20 ATR | 4.23 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.602–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.803 %, prix 326.996), p(touche) 35.33 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.712–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.803 %, prix 326.996), p(touche) 42.53 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.929–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.405 %, prix 324.9914), p(touche) 41.83 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.283–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.607 %, prix 320.9887), p(touche) 37.88 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.59–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.809 %, prix 316.986), p(touche) 37.06 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.029 | EV/share : €-0.232 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 29 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 46.6 | bear 47.1 | side 6.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 333.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→52% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.45% (p90 3.72%) · excursion haute méd. +1.09% / basse méd. −0.77%
- Profil de vol intra : ouverture 1.461% vs midi 0.5% vs clôture 0.665% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.3% ; recovery-V 12%
- **σ réalisé intraday** 1.544% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 331.8075 (VA 331.3325–332.7575 ; dernier close 333.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 36% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 31% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.56%) · haut méd +0.18% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.48% (p90 −1.76%) · haut méd +0.31% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.49% (p90 −1.78%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.84%) · haut méd +0.53% · range méd 1.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 333.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 60% (86/159) · gap 10% · délai 0.4min · rebond 38% (34/86) (MFE +0.84%)
   - −1.0% : fill 30min 25% · séance 48% (71/159) · gap 1% · délai 25.1min · rebond 42% (33/71) (MFE +0.79%)
   - −1.5% : fill 30min 11% · séance 29% (45/159) · gap 1% · délai 67.5min · rebond 31% (19/45) (MFE +0.52%)
   - −2.0% : fill 30min 4% · séance 23% (37/159) · gap 0% · délai 240.5min · rebond 36% (16/37) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −0.77%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.77%) → stop au-delà de −0.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=205 jambes) : jambe baissière méd −1.05% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 76% (18/22) · rebond 29% (7/18)
      · −2.0% : fill 48% (12/22) · rebond 42% (6/12)
      · −3.0% : fill 16% (5/22) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/22) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **flat** (38 séances) :
      · −1.0% : fill 49% (20/38) · rebond 40% (10/20)
      · −2.0% : fill 26% (9/38) · rebond 12% (1/9)
      · −3.0% : fill 5% (3/38) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/38) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/38) · rebond 0% (0/0)
   - **gap-up** (99 séances) :
      · −1.0% : fill 39% (33/99) · rebond 53% (16/33)
      · −2.0% : fill 13% (16/99) · rebond 59% (9/16)
      · −3.0% : fill 5% (6/99) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/99) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/99) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 70% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -0.71% (q20 -1.34%) → **SL/trailing à −1.34%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.96% / q75 +1.45% → **scale +0.96% / runner +1.45%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.29%** (au-delà de la MAE q10 -2.29%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.54%] · haut q95 +1.94% · bas q05 -2.06%
   - 60min (n=160) : retour [-1.63% .. +1.81%] · haut q95 +1.99% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.32% .. +2.06%] · haut q95 +2.49% · bas q05 -2.92%
   - 4h (n=160) : retour [-1.87% .. +2.1%] · haut q95 +2.7% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.98%
   - session (n=160) : retour [-2.7% .. +2.39%] · haut q95 +3.33% · bas q05 -3.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 49.6  _(neutre)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist 1.406  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 6.0%
- **ATR** : 8.01 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.12  _(distribution)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 62.7  _(marche en range (choppy))_
- **MA** : MA20 329.71 · MA50 339.7 · MA200 314.52  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 -2.0% · MA200 +5.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (850477 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
