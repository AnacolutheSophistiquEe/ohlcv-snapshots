# PLTR

**Generated** : 2026-09-04T22:04:17.594935+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $174.33  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot $174.33 (+9.3% vs entrée) · entrée $159.45 · stop $151.21 · T1 $166.05 · R/R 0.8  
> ↳ P(T1 av. stop) 76 % · EV/risk 0.101 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $158.13–$160.77 (mid $159.45)
- Spot actuel : $174.33 (+9.3% au-dessus de la zone — repli à attendre)
- Stop : $151.21 (stop swing_plan-based (-13.26%))
- Targets : T1 $166.05 · R/R 0.8 | T2 $172.65 · R/R 1.6 | T3 $179.25 · R/R 2.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $151.21


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.26 %)** : le gap seul le franchit 0.159 % des séances (2 fois sur 1254).
   - exécution **3.042 pt plus bas** dans le cas TYPIQUE (médiane), 4.346 au p90, **4.672 au pire**
   - perte réelle **16.302 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 13.26 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0049 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.88 % | p01 -6.138 % | pire -17.932 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3512** [0.283 ; 0.4243] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.3528** [0.3038 ; 0.4042] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.3208** [0.2732 ; 0.3713] _(largeur 9.8 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.973 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7062** (β de hausse 1.4109, asymétrie 1.2093) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 153.7284 sur atr_grid (2.5 ATR, 11.818 %) — p(stop avant cible) 0.2288 [0.19 ; 0.28], R/R 0.62, perte reelle 14.376 % (gap inclus), CVaR 11.826 %, EV 0.0764 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.86 ATR (stop 6.339 %) — p(stop avant cible) 0.4418 [0.39 ; 0.49], R/R 0.866, perte reelle 10.298 % (gap inclus), EV -0.9667 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 37.1 % x 8.91 % + P(rien) 18.8 % x 1.49 % ne couvrent pas P(stop) 44.2 % x 10.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.38 ATR (stop 18.272 %) — p(stop avant cible) 0.0891 [0.06 ; 0.12], R/R 0.488, perte reelle 18.272 % (gap inclus), EV 0.7017 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.27 % > budget 12.00 %
   - 🟢 support a 6.85 ATR (stop 34.654 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.257, perte reelle 34.654 % (gap inclus), EV 1.1647 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.65 % > budget 12.00 %
   - 🟢 support a 8.25 ATR (stop 41.262 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.216, perte reelle 41.262 % (gap inclus), EV 1.1697 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.26 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.182 %) — p(stop avant cible) 0.8701 [0.83 ; 0.90], R/R 3.364, perte reelle 2.65 % (gap inclus), EV -1.1968 % — **REFUSE**
      - refuse : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.870, borne haute 0.902 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 12.2 % x 8.91 % + P(rien) 0.8 % x 3.09 % ne couvrent pas P(stop) 87.0 % x 2.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.364 %) — p(stop avant cible) 0.7533 [0.71 ; 0.80], R/R 2.117, perte reelle 4.211 % (gap inclus), EV -1.0909 % — **REFUSE**
      - refuse : p_stop_first 0.753, borne haute 0.796 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 22.4 % x 8.91 % + P(rien) 2.3 % x 3.82 % ne couvrent pas P(stop) 75.3 % x 4.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.86 ATR (stop 5.478 %) — p(stop avant cible) 0.5022 [0.45 ; 0.55], R/R 0.945, perte reelle 9.434 % (gap inclus), EV -1.3938 % — **REFUSE**
      - refuse : p_stop_first 0.502, borne haute 0.555 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 34.4 % x 8.91 % + P(rien) 15.3 % x 1.78 % ne couvrent pas P(stop) 50.2 % x 9.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 7.091 %) — p(stop avant cible) 0.3904 [0.34 ; 0.44], R/R 0.778, perte reelle 11.461 % (gap inclus), EV -0.6745 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 39.6 % x 8.91 % + P(rien) 21.4 % x 1.27 % ne couvrent pas P(stop) 39.0 % x 11.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.272 %) — p(stop avant cible) 0.3382 [0.29 ; 0.39], R/R 0.712, perte reelle 12.528 % (gap inclus), EV -0.5308 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 40.0 % x 8.91 % + P(rien) 26.2 % x 0.54 % ne couvrent pas P(stop) 33.8 % x 12.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.454 %) — p(stop avant cible) 0.3033 [0.26 ; 0.35], R/R 0.679, perte reelle 13.126 % (gap inclus), EV -0.385 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 40.2 % x 8.91 % + P(rien) 29.5 % x 0.05 % ne couvrent pas P(stop) 30.3 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 10.636 %) — p(stop avant cible) 0.2717 [0.23 ; 0.32], R/R 0.648, perte reelle 13.763 % (gap inclus), EV -0.2997 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 40.4 % x 8.91 % + P(rien) 32.4 % x -0.50 % ne couvrent pas P(stop) 27.2 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.818 %) — p(stop avant cible) 0.2288 [0.19 ; 0.28], R/R 0.62, perte reelle 14.376 % (gap inclus), EV 0.0764 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 12.999 %) — p(stop avant cible) 0.1826 [0.14 ; 0.23], R/R 0.547, perte reelle 16.302 % (gap inclus), EV 0.1117 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.00 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 14.181 %) — p(stop avant cible) 0.1528 [0.12 ; 0.19], R/R 0.547, perte reelle 16.302 % (gap inclus), EV 0.3093 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.18 % > budget 12.00 %
   - ⚪ grid_snapped a 3.38 ATR (stop 17.412 %) — p(stop avant cible) 0.0995 [0.07 ; 0.13], R/R 0.497, perte reelle 17.932 % (gap inclus), EV 0.6637 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.41 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 18.908 %) — p(stop avant cible) 0.0693 [0.05 ; 0.10], R/R 0.471, perte reelle 18.908 % (gap inclus), EV 0.8451 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.91 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.272 %) — p(stop avant cible) 0.0362 [0.02 ; 0.06], R/R 0.419, perte reelle 21.272 % (gap inclus), EV 0.9868 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 23.635 %) — p(stop avant cible) 0.0135 [0.01 ; 0.03], R/R 0.377, perte reelle 23.635 % (gap inclus), EV 1.0969 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.63 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 25.999 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.343, perte reelle 25.999 % (gap inclus), EV 1.1473 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.00 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.362 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.314, perte reelle 28.362 % (gap inclus), EV 1.1594 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.36 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 30.726 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.29, perte reelle 30.726 % (gap inclus), EV 1.1537 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.73 % > budget 12.00 %
   - 🟢 grid_snapped a 6.85 ATR (stop 33.793 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.264, perte reelle 33.793 % (gap inclus), EV 1.1659 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.79 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.453 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.251, perte reelle 35.453 % (gap inclus), EV 1.165 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.45 % > budget 12.00 %
   - 🟢 grid_snapped a 8.25 ATR (stop 40.402 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.221, perte reelle 40.402 % (gap inclus), EV 1.17 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.40 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 174.33, ATR14 8.2406 (4.727 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 1.688 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.236 % | 173.918 | 92.45 % | 94.96 % | 95.77 % | 96.57 % | 97.87 % | 98.56 % |
| 0.1 ATR | 0.473 % | 173.5059 | 84.41 % | 89.12 % | 90.93 % | 93.13 % | 94.82 % | 96.31 % |
| 0.15 ATR | 0.709 % | 173.0939 | 76.96 % | 83.48 % | 85.69 % | 89.49 % | 92.18 % | 94.15 % |
| 0.2 ATR | 0.945 % | 172.6819 | 68.91 % | 78.05 % | 81.35 % | 86.06 % | 89.95 % | 92.31 % |
| 0.25 ATR | 1.182 % | 172.2698 | 61.87 % | 73.51 % | 77.32 % | 82.73 % | 87.61 % | 90.77 % |
| 0.35 ATR | 1.654 % | 171.4458 | 50.7 % | 65.56 % | 71.07 % | 78.08 % | 83.65 % | 87.69 % |
| 0.5 ATR | 2.364 % | 170.2097 | 36.22 % | 53.07 % | 59.88 % | 69.19 % | 77.97 % | 83.18 % |
| 0.75 ATR | 3.545 % | 168.1495 | 19.42 % | 35.35 % | 44.86 % | 55.56 % | 67.01 % | 76.0 % |
| 1.0 ATR | 4.727 % | 166.0894 | 9.05 % | 22.96 % | 32.76 % | 44.14 % | 56.45 % | 67.79 % |
| 1.25 ATR | 5.909 % | 164.0292 | 4.53 % | 15.61 % | 23.49 % | 34.55 % | 46.6 % | 59.08 % |
| 1.5 ATR | 7.091 % | 161.969 | 2.11 % | 10.57 % | 17.54 % | 26.77 % | 39.9 % | 54.26 % |
| 2.0 ATR | 9.454 % | 157.8487 | 0.6 % | 3.73 % | 9.38 % | 15.56 % | 28.93 % | 40.62 % |
| 2.5 ATR | 11.818 % | 153.7284 | 0.1 % | 1.51 % | 3.33 % | 9.09 % | 19.09 % | 30.15 % |
| 3.0 ATR | 14.181 % | 149.6081 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.89 % | 22.56 % |
| 4.0 ATR | 18.908 % | 141.3674 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.79 % |
| 6.0 ATR | 28.362 % | 124.8861 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.75 ATR | 0.99 ATR | 1.21 ATR | 1.40 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.58 ATR | 1.80 ATR | 2.43 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.16 ATR | 1.31 ATR | 1.81 ATR | 2.20 ATR | 2.45 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.78 ATR | 1.66 ATR | 1.84 ATR | 2.36 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.364 %, prix 170.2088), p(touche) 36.22 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.545 %, prix 168.15), p(touche) 35.35 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.545 %, prix 168.15), p(touche) 44.86 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.981–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.727 %, prix 166.0894), p(touche) 44.14 % (en stress 100.0 %)  ✅ optimum identifie (82.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.31–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.091 %, prix 161.9683), p(touche) 39.9 % (en stress 100.0 %)  ✅ optimum identifie (89.8 % des re-echantillons)
- **20 seance(s)** : plage utile 1.839–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (14.181 %, prix 149.6083), p(touche) 22.56 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.038 | EV/share : $-0.310 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 22 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 29.0 | side 66.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 349.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→51% · +3.0%→30% · +5.0%→10% · +8.0%→4%
- Range intraday médian 4.01% (p90 7.17%) · excursion haute méd. +2.11% / basse méd. −1.51%
- Profil de vol intra : ouverture 3.044% vs midi 0.75% vs clôture 0.834% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr -0.01)_ ; drift intra méd. 0.674% ; recovery-V 24%
- **σ réalisé intraday** 2.556% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 47% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 183.1935 (VA 181.3565–184.1955 ; dernier close 179.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 68% · **stop −3.78%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 55% (gap-down >1% 28% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.08%) · haut méd +0.96% · range méd 1.9%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.83%) · haut méd +1.2% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.0% (p90 −3.49%) · haut méd +1.31% · range méd 2.68%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.57%) · haut méd +1.43% · range méd 2.99%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 179.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 77% (118/159) · gap 40% · délai 0.0min · rebond 58% (65/118) (MFE +1.23%)
   - −1.0% : fill 30min 55% · séance 66% (108/159) · gap 28% · délai 0.0min · rebond 66% (65/108) (MFE +1.45%)
   - −1.5% : fill 30min 42% · séance 53% (89/159) · gap 20% · délai 0.1min · rebond 66% (56/89) (MFE +1.49%)
   - −2.0% : fill 30min 37% · séance 48% (78/159) · gap 11% · délai 1.4min · rebond 68% (50/78) (MFE +1.39%)
   - −3.0% : fill 30min 20% · séance 30% (56/159) · gap 6% · délai 4.6min · rebond 55% (27/56) (MFE +1.37%)
   - −4.0% : fill 30min 14% · séance 18% (37/159) · gap 3% · délai 7.7min · rebond 53% (17/37) (MFE +1.07%)
   - −5.0% : fill 30min 8% · séance 13% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.79%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.71%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.35%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.08% (p90 −2.44%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 88% (71/76) · rebond 67% (43/71)
      · −2.0% : fill 70% (57/76) · rebond 71% (36/57)
      · −3.0% : fill 50% (43/76) · rebond 53% (21/43)
      · −4.0% : fill 32% (30/76) · rebond 56% (14/30)
      · −5.0% : fill 24% (23/76) · rebond 58% (12/23)
   - **flat** (24 séances) :
      · −1.0% : fill 72% (20/24) · rebond 41% (9/20)
      · −2.0% : fill 57% (14/24) · rebond 62% (9/14)
      · −3.0% : fill 31% (10/24) · rebond 58% (5/10)
      · −4.0% : fill 18% (6/24) · rebond 41% (3/6)
      · −5.0% : fill 10% (3/24) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 34% (17/59) · rebond 83% (13/17)
      · −2.0% : fill 16% (7/59) · rebond 57% (5/7)
      · −3.0% : fill 4% (3/59) · rebond 71% (1/3)
      · −4.0% : fill 1% (1/59) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/59) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 69% si les 15 1res min sont vertes (83 cas) · 32% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 84% si début vert vs 18% si rouge (base 53% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **84%** · continue >prix actuel 54% ; creux résiduel méd -0.9% (q20 -1.56%) → **SL/trailing à −1.56%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.18% → **scale +1.18% / runner +2.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 47%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.59%** (au-delà de la MAE q10 -2.59%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.43% .. +3.79%] · haut q95 +4.05% · bas q05 -4.01%
   - 60min (n=160) : retour [-3.6% .. +3.93%] · haut q95 +4.78% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.75% .. +5.35%] · haut q95 +5.72% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.03% .. +5.64%] · haut q95 +6.42% · bas q05 -5.15%
   - 6h (n=160) : retour [-4.04% .. +5.75%] · haut q95 +6.82% · bas q05 -5.52%
   - session (n=160) : retour [-4.02% .. +4.89%] · haut q95 +6.82% · bas q05 -5.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 3.1% / strong 4.4%) · base = 12 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 20% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.13% / p90 1.49%) · ~2.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 43.27 min, n=37)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.49%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +4.31% (q75 +7.51% / q95 +12.13%), MFE méd +5.25% / q90 +12.03%
   - Échelle scale-out : +5.25% (33%) / +7.95% (33%) / +12.03% (34%)
- **DÉSARMER** : repli > **−1.49%** depuis le plus-haut = décay → P(retournement) **82%** (préavis méd 214.54 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.03% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 58% du temps (retour médian dernière heure +0.19%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.3  _(neutre)_
- **ADX** : 31.3  _(tendance etablie)_
- **MACD** : hist -1.803  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 11.6%
- **ATR** : 8.24 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.006  _(neutre)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 61.7  _(transition)_
- **MA** : MA20 176.92 · MA50 149.89 · MA200 151.37  _(prix < MA20)_
- **Dist MA** : MA20 -1.5% · MA50 +16.3% · MA200 +15.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (757811 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
