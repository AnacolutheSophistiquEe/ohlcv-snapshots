# SAF

**Generated** : 2026-09-02T00:07:32.449839+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €330.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €330.70 (+6.7% vs entrée) · entrée €310.01 · stop €302.52 · T1 €314.96 · R/R 0.66  
> ↳ P(T1 av. stop) 59 % · EV/risk -0.008 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €309.02–€311.00 (mid €310.01)
- Spot actuel : €330.70 (+6.7% au-dessus de la zone — repli à attendre)
- Stop : €302.52 (stop swing_plan-based (-8.52%))
- Targets : T1 €314.96 · R/R 0.66 | T2 €319.91 · R/R 1.32 | T3 €324.86 · R/R 1.98
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €302.52


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.52 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.466 pt plus bas** dans le cas TYPIQUE (médiane), 1.466 au p90, **1.466 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.52 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0011 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1734** [0.1226 ; 0.235] _(largeur 11.2 pt, n_eff 173.1)_
   - swing : **0.3475** [0.2987 ; 0.3988] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.306** [0.2592 ; 0.356] _(largeur 9.7 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.07 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.24 % contre 2.48 % aujourd'hui, rapport 0.50)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3703** (β de hausse 1.336, asymétrie 1.0256) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.258× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 296.9821 sur atr_grid (4.5 ATR, 10.196 %) — p(stop avant cible) 0.0758 [0.05 ; 0.11], R/R 0.911, perte reelle 10.196 % (gap inclus), CVaR 10.196 %, EV 1.2104 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.399 %) — p(stop avant cible) 0.4249 [0.37 ; 0.48], R/R 1.629, perte reelle 5.698 % (gap inclus), EV 0.1264 % — **REFUSE**
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 5.12 ATR (stop 13.028 %) — p(stop avant cible) 0.0438 [0.03 ; 0.07], R/R 0.713, perte reelle 13.028 % (gap inclus), EV 1.1578 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.03 % > budget 12.00 %
   - 🟢 support a 9.48 ATR (stop 22.902 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.405, perte reelle 22.902 % (gap inclus), EV 1.1646 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.90 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.566 %) — p(stop avant cible) 0.8877 [0.85 ; 0.92], R/R 7.109, perte reelle 1.306 % (gap inclus), EV -0.4231 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 5.1 % x 9.28 % + P(rien) 6.1 % x 4.24 % ne couvrent pas P(stop) 88.8 % x 1.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.133 %) — p(stop avant cible) 0.768 [0.72 ; 0.81], R/R 4.71, perte reelle 1.971 % (gap inclus), EV -0.1784 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.768, borne haute 0.810 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 7.8 % x 9.28 % + P(rien) 15.3 % x 3.95 % ne couvrent pas P(stop) 76.8 % x 1.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.699 %) — p(stop avant cible) 0.676 [0.63 ; 0.72], R/R 3.446, perte reelle 2.694 % (gap inclus), EV -0.0054 % — **REFUSE**
      - refuse : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 10.8 % x 9.28 % + P(rien) 21.6 % x 3.77 % ne couvrent pas P(stop) 67.6 % x 2.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.266 %) — p(stop avant cible) 0.5945 [0.54 ; 0.65], R/R 2.4, perte reelle 3.868 % (gap inclus), EV -0.2099 % — **REFUSE**
      - refuse : cible atteinte seulement 12.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.595, borne haute 0.645 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 12.4 % x 9.28 % + P(rien) 28.2 % x 3.34 % ne couvrent pas P(stop) 59.5 % x 3.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.832 %) — p(stop avant cible) 0.5037 [0.45 ; 0.56], R/R 2.017, perte reelle 4.602 % (gap inclus), EV 0.0514 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.504, borne haute 0.556 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 3.965 %) — p(stop avant cible) 0.362 [0.31 ; 0.41], R/R 1.506, perte reelle 6.163 % (gap inclus), EV 0.4697 % — **REFUSE**
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.532 %) — p(stop avant cible) 0.3171 [0.27 ; 0.37], R/R 1.365, perte reelle 6.799 % (gap inclus), EV 0.5489 % — **REFUSE**
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 5.098 %) — p(stop avant cible) 0.2708 [0.23 ; 0.32], R/R 1.208, perte reelle 7.683 % (gap inclus), EV 0.7328 % — **REFUSE**
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.664 %) — p(stop avant cible) 0.246 [0.20 ; 0.29], R/R 0.93, perte reelle 9.986 % (gap inclus), EV 0.3387 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 6.231 %) — p(stop avant cible) 0.2268 [0.19 ; 0.27], R/R 0.93, perte reelle 9.986 % (gap inclus), EV 0.5405 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.797 %) — p(stop avant cible) 0.1758 [0.14 ; 0.22], R/R 0.93, perte reelle 9.986 % (gap inclus), EV 0.7948 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.93 %) — p(stop avant cible) 0.1376 [0.10 ; 0.18], R/R 0.93, perte reelle 9.986 % (gap inclus), EV 1.0211 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 9.063 %) — p(stop avant cible) 0.1034 [0.07 ; 0.14], R/R 0.93, perte reelle 9.986 % (gap inclus), EV 1.1555 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 10.196 %) — p(stop avant cible) 0.0758 [0.05 ; 0.11], R/R 0.911, perte reelle 10.196 % (gap inclus), EV 1.2104 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 5.12 ATR (stop 12.281 %) — p(stop avant cible) 0.0439 [0.03 ; 0.07], R/R 0.756, perte reelle 12.281 % (gap inclus), EV 1.1899 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.28 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 13.595 %) — p(stop avant cible) 0.0341 [0.02 ; 0.06], R/R 0.683, perte reelle 13.595 % (gap inclus), EV 1.1452 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.60 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.727 %) — p(stop avant cible) 0.0199 [0.01 ; 0.04], R/R 0.63, perte reelle 14.727 % (gap inclus), EV 1.1478 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.73 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 15.86 %) — p(stop avant cible) 0.0099 [0.00 ; 0.02], R/R 0.585, perte reelle 15.86 % (gap inclus), EV 1.1546 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.86 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 16.993 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 0.546, perte reelle 16.993 % (gap inclus), EV 1.1619 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.99 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 18.126 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.512, perte reelle 18.126 % (gap inclus), EV 1.1604 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.13 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 330.7, ATR14 7.4929 (2.266 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 0.782 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.113 % | 330.3254 | 89.12 % | 92.44 % | 93.61 % | 95.57 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.227 % | 329.9507 | 81.27 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.34 % | 329.5761 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.453 % | 329.2014 | 68.24 % | 78.12 % | 82.51 % | 85.24 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.566 % | 328.8268 | 61.27 % | 73.41 % | 78.88 % | 83.17 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.793 % | 328.0775 | 49.41 % | 63.0 % | 69.45 % | 76.57 % | 82.59 % | 87.01 % |
| 0.5 ATR | 1.133 % | 326.9536 | 35.49 % | 51.62 % | 59.04 % | 68.31 % | 75.77 % | 81.32 % |
| 0.75 ATR | 1.699 % | 325.0804 | 20.49 % | 35.53 % | 42.93 % | 52.95 % | 63.11 % | 70.73 % |
| 1.0 ATR | 2.266 % | 323.2072 | 9.71 % | 23.65 % | 32.42 % | 41.73 % | 53.31 % | 61.24 % |
| 1.25 ATR | 2.832 % | 321.3339 | 4.31 % | 15.41 % | 23.97 % | 33.07 % | 45.99 % | 54.45 % |
| 1.5 ATR | 3.399 % | 319.4607 | 2.25 % | 10.01 % | 16.5 % | 25.0 % | 37.78 % | 46.45 % |
| 2.0 ATR | 4.532 % | 315.7143 | 0.98 % | 4.42 % | 7.47 % | 15.35 % | 26.81 % | 36.76 % |
| 2.5 ATR | 5.664 % | 311.9679 | 0.2 % | 1.47 % | 3.54 % | 8.96 % | 18.6 % | 27.97 % |
| 3.0 ATR | 6.797 % | 308.2214 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.46 % | 21.78 % |
| 4.0 ATR | 9.063 % | 300.7286 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.04 % | 11.29 % |
| 6.0 ATR | 13.595 % | 285.7429 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.1 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.22 ATR | 1.38 ATR | 1.86 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.25 ATR | 1.50 ATR | 1.76 ATR | 2.42 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.11 ATR | 1.28 ATR | 1.72 ATR | 2.11 ATR | 2.42 ATR | 3.33 ATR | 4.02 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.21 ATR | 2.74 ATR | 3.17 ATR | 4.32 ATR | 5.54 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.699 %, prix 325.0814), p(touche) 35.53 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.718–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.699 %, prix 325.0814), p(touche) 42.93 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.927–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.266 %, prix 323.2063), p(touche) 41.73 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.28–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.399 %, prix 319.4595), p(touche) 37.78 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.575–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.532 %, prix 315.7127), p(touche) 36.76 % (en stress 99.01 %)  ✅ optimum identifie (63.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : €-0.057 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 36 % | T3 23 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.2 | bear 9.7 | side 85.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→51% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.48% (p90 3.72%) · excursion haute méd. +1.05% / basse méd. −0.86%
- Profil de vol intra : ouverture 1.466% vs midi 0.525% vs clôture 0.665% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 42% · recovery-V 17%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.074)_ ; drift intra méd. -0.318% ; recovery-V 13%
- **σ réalisé intraday** 1.544% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 58% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 341.7912 (VA 340.6287–342.4887 ; dernier close 336.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 39% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.72% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. 0.32% · baisse 31% (gap-down >1% 2% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.49%) · haut méd +0.18% · range méd 0.88%
- Excursion ouverture 15min (n=160) : bas méd −0.48% (p90 −1.69%) · haut méd +0.31% · range méd 1.03%
- Excursion ouverture 30min (n=160) : bas méd −0.49% (p90 −1.7%) · haut méd +0.44% · range méd 1.25%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.85%) · haut méd +0.53% · range méd 1.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 337.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 44% · séance 59% (85/159) · gap 9% · délai 0.5min · rebond 36% (33/85) (MFE +0.81%)
   - −1.0% : fill 30min 25% · séance 50% (71/159) · gap 2% · délai 29.3min · rebond 44% (33/71) (MFE +0.86%)
   - −1.5% : fill 30min 10% · séance 29% (45/159) · gap 1% · délai 198.3min · rebond 33% (19/45) (MFE +0.45%)
   - −2.0% : fill 30min 5% · séance 23% (37/159) · gap 0% · délai 288.2min · rebond 39% (17/37) (MFE +0.72%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.66% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.12% (p90 −0.77%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=210 jambes) : jambe baissière méd −1.03% (p90 −2.27%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (21 séances) :
      · −1.0% : fill 85% (18/21) · rebond 29% (7/18)
      · −2.0% : fill 53% (12/21) · rebond 42% (6/12)
      · −3.0% : fill 18% (5/21) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/21) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/21) · rebond 0% (0/0)
   - **flat** (35 séances) :
      · −1.0% : fill 52% (19/35) · rebond 44% (10/19)
      · −2.0% : fill 24% (8/35) · rebond 15% (1/8)
      · −3.0% : fill 6% (3/35) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/35) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (103 séances) :
      · −1.0% : fill 38% (34/103) · rebond 53% (16/34)
      · −2.0% : fill 13% (17/103) · rebond 60% (10/17)
      · −3.0% : fill 5% (6/103) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/103) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/103) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 67% si les 15 1res min sont vertes (72 cas) · 25% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 75% si début vert vs 20% si rouge (base 46% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 288min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **75%** · continue >prix actuel 54% ; creux résiduel méd -0.7% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.47% → **scale +0.97% / runner +1.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 60%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.32%** (au-delà de la MAE q10 -2.32%), cible rebond +0.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.5% .. +1.55%] · haut q95 +1.95% · bas q05 -2.1%
   - 60min (n=160) : retour [-1.63% .. +2.04%] · haut q95 +2.04% · bas q05 -2.35%
   - 2h (n=160) : retour [-1.85% .. +2.14%] · haut q95 +2.52% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.8% .. +2.18%] · haut q95 +2.73% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.1% .. +2.33%] · haut q95 +2.8% · bas q05 -3.03%
   - session (n=160) : retour [-2.71% .. +2.42%] · haut q95 +3.35% · bas q05 -3.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 23.5  _(survente)_
- **ADX** : 14.8  _(pas de tendance nette)_
- **MACD** : hist -2.95  _(pas de croisement recent)_
- **BB** : %B -0.02 · largeur 11.0%
- **ATR** : 7.49 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.324  _(distribution)_
- **Vol ratio** : 0.34  _(volume atone)_
- **Choppiness** : 40.6  _(transition)_
- **MA** : MA20 350.88 · MA50 343.25 · MA200 310.65  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -3.7% · MA200 +6.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (772760 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
