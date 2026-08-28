# SAF

**Generated** : 2026-08-28T21:42:06.958660+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €344.20  

> 🟡 **WAIT-FOR-DIP** — spot +8.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €344.20 (+8.9% vs entrée) · entrée €316.09 · stop €309.04 · T1 €321.91 · R/R 0.83  
> ↳ P(T1 av. stop) 54 % · EV/risk 0.019 · ¼-Kelly 0.005 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €314.92–€317.25 (mid €316.09)
- Spot actuel : €344.20 (+8.9% au-dessus de la zone — repli à attendre)
- Stop : €309.04 (stop swing_plan-based (-10.21%))
- Targets : T1 €321.91 · R/R 0.83 | T2 €327.73 · R/R 1.65 | T3 €333.56 · R/R 2.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €309.04


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (10.21 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.21 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.405 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1734** [0.1226 ; 0.235] _(largeur 11.2 pt, n_eff 173.1)_
   - swing : **0.4117** [0.3607 ; 0.4641] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3412** [0.2927 ; 0.3923] _(largeur 10.0 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.06 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.29 % contre 2.48 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3698** (β de hausse 1.3365, asymétrie 1.0249) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.255× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 308.9857 sur atr_grid (5.0 ATR, 10.231 %) — p(stop avant cible) 0.0731 [0.05 ; 0.10], R/R 0.492, perte reelle 10.231 % (gap inclus), CVaR 10.231 %, EV 0.7153 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.95 ATR (stop 3.246 %) — p(stop avant cible) 0.428 [0.38 ; 0.48], R/R 1.047, perte reelle 4.809 % (gap inclus), EV -0.0084 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 36.9 % x 5.04 % + P(rien) 20.3 % x 0.94 % ne couvrent pas P(stop) 42.8 % x 4.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 7.36 ATR (stop 16.352 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 0.308, perte reelle 16.352 % (gap inclus), EV 0.667 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.35 % > budget 12.00 %
   - 🟢 support a 12.0 ATR (stop 25.852 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.195, perte reelle 25.852 % (gap inclus), EV 0.6823 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.85 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.512 %) — p(stop avant cible) 0.8732 [0.84 ; 0.91], R/R 4.023, perte reelle 1.252 % (gap inclus), EV -0.4998 % — **REFUSE**
      - refuse : cible atteinte seulement 11.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.873, borne haute 0.905 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 11.1 % x 5.04 % + P(rien) 1.6 % x 2.23 % ne couvrent pas P(stop) 87.3 % x 1.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.023 %) — p(stop avant cible) 0.7651 [0.72 ; 0.81], R/R 2.676, perte reelle 1.882 % (gap inclus), EV -0.3884 % — **REFUSE**
      - refuse : p_stop_first 0.765, borne haute 0.807 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 19.1 % x 5.04 % + P(rien) 4.3 % x 2.01 % ne couvrent pas P(stop) 76.5 % x 1.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.95 ATR (stop 2.563 %) — p(stop avant cible) 0.5157 [0.46 ; 0.57], R/R 1.183, perte reelle 4.259 % (gap inclus), EV -0.339 % — **REFUSE**
      - refuse : p_stop_first 0.516, borne haute 0.568 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 33.0 % x 5.04 % + P(rien) 15.5 % x 1.27 % ne couvrent pas P(stop) 51.6 % x 4.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.581 %) — p(stop avant cible) 0.3766 [0.33 ; 0.43], R/R 0.884, perte reelle 5.698 % (gap inclus), EV -0.027 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 38.8 % x 5.04 % + P(rien) 23.5 % x 0.70 % ne couvrent pas P(stop) 37.7 % x 5.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 4.092 %) — p(stop avant cible) 0.3256 [0.28 ; 0.38], R/R 0.817, perte reelle 6.163 % (gap inclus), EV 0.1895 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.604 %) — p(stop avant cible) 0.293 [0.25 ; 0.34], R/R 0.741, perte reelle 6.799 % (gap inclus), EV 0.1966 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.115 %) — p(stop avant cible) 0.2546 [0.21 ; 0.30], R/R 0.656, perte reelle 7.683 % (gap inclus), EV 0.2724 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 5.627 %) — p(stop avant cible) 0.2308 [0.19 ; 0.28], R/R 0.504, perte reelle 9.986 % (gap inclus), EV -0.0985 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 43.4 % x 5.04 % + P(rien) 33.5 % x 0.06 % ne couvrent pas P(stop) 23.1 % x 9.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 6.138 %) — p(stop avant cible) 0.2171 [0.18 ; 0.26], R/R 0.504, perte reelle 9.986 % (gap inclus), EV 0.0649 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.162 %) — p(stop avant cible) 0.1486 [0.11 ; 0.19], R/R 0.504, perte reelle 9.986 % (gap inclus), EV 0.4151 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.185 %) — p(stop avant cible) 0.1192 [0.09 ; 0.16], R/R 0.504, perte reelle 9.986 % (gap inclus), EV 0.5874 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 9.208 %) — p(stop avant cible) 0.0978 [0.07 ; 0.13], R/R 0.504, perte reelle 9.986 % (gap inclus), EV 0.6666 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 10.231 %) — p(stop avant cible) 0.0731 [0.05 ; 0.10], R/R 0.492, perte reelle 10.231 % (gap inclus), EV 0.7153 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 11.254 %) — p(stop avant cible) 0.0598 [0.04 ; 0.09], R/R 0.448, perte reelle 11.254 % (gap inclus), EV 0.6853 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.0 ATR (stop 12.277 %) — p(stop avant cible) 0.0444 [0.03 ; 0.07], R/R 0.41, perte reelle 12.277 % (gap inclus), EV 0.6911 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.28 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 13.3 %) — p(stop avant cible) 0.0345 [0.02 ; 0.06], R/R 0.379, perte reelle 13.3 % (gap inclus), EV 0.6557 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.30 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 14.323 %) — p(stop avant cible) 0.0202 [0.01 ; 0.04], R/R 0.352, perte reelle 14.323 % (gap inclus), EV 0.6555 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.32 % > budget 12.00 %
   - ⚪ grid_snapped a 7.36 ATR (stop 15.669 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 0.321, perte reelle 15.669 % (gap inclus), EV 0.6574 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.67 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 344.2, ATR14 7.0429 (2.046 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 0.706 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.102 % | 343.8479 | 89.12 % | 92.44 % | 93.61 % | 95.57 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.205 % | 343.4957 | 81.27 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.307 % | 343.1436 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.409 % | 342.7914 | 68.24 % | 78.12 % | 82.51 % | 85.24 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.512 % | 342.4393 | 61.27 % | 73.41 % | 78.88 % | 83.17 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.716 % | 341.735 | 49.41 % | 63.0 % | 69.45 % | 76.57 % | 82.59 % | 87.01 % |
| 0.5 ATR | 1.023 % | 340.6786 | 35.49 % | 51.62 % | 59.04 % | 68.31 % | 75.77 % | 81.32 % |
| 0.75 ATR | 1.535 % | 338.9179 | 20.59 % | 35.53 % | 43.03 % | 53.05 % | 63.11 % | 70.83 % |
| 1.0 ATR | 2.046 % | 337.1572 | 9.8 % | 23.65 % | 32.51 % | 41.83 % | 53.31 % | 61.34 % |
| 1.25 ATR | 2.558 % | 335.3964 | 4.31 % | 15.41 % | 23.97 % | 33.17 % | 45.9 % | 54.55 % |
| 1.5 ATR | 3.069 % | 333.6357 | 2.25 % | 10.01 % | 16.5 % | 25.1 % | 37.69 % | 46.55 % |
| 2.0 ATR | 4.092 % | 330.1143 | 0.98 % | 4.51 % | 7.47 % | 15.45 % | 26.71 % | 36.86 % |
| 2.5 ATR | 5.115 % | 326.5929 | 0.2 % | 1.47 % | 3.54 % | 8.96 % | 18.4 % | 28.17 % |
| 3.0 ATR | 6.138 % | 323.0714 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.36 % | 21.98 % |
| 4.0 ATR | 8.185 % | 316.0286 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.04 % | 11.49 % |
| 6.0 ATR | 12.277 % | 301.9428 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.1 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.96 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.22 ATR | 1.38 ATR | 1.86 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.25 ATR | 1.50 ATR | 1.76 ATR | 2.42 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.11 ATR | 1.28 ATR | 1.71 ATR | 2.10 ATR | 2.40 ATR | 3.32 ATR | 4.02 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.58 ATR | 2.22 ATR | 2.76 ATR | 3.19 ATR | 4.36 ATR | 5.55 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.535 %, prix 338.9165), p(touche) 35.53 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.719–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.535 %, prix 338.9165), p(touche) 43.03 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.929–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.046 %, prix 337.1577), p(touche) 41.83 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.277–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.069 %, prix 333.6365), p(touche) 37.69 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.58–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.092 %, prix 330.1153), p(touche) 36.86 % (en stress 100.0 %)  ✅ optimum identifie (65.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.019 | EV/share : €0.132 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 31 % | T3 18 %
- Kelly (position) : f* 0.018 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.1 | bear 9.7 | side 85.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 344.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→51% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.48% (p90 3.72%) · excursion haute méd. +1.05% / basse méd. −0.86%
- Profil de vol intra : ouverture 1.49% vs midi 0.532% vs clôture 0.674% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 42% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.083)_ ; drift intra méd. -0.192% ; recovery-V 16%
- **σ réalisé intraday** 1.591% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 54% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 349.3513 (VA 348.0888–351.1187 ; dernier close 343.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 22% · rebond 42% · **stop −1.37%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.32% · baisse 30% (gap-down >1% 2% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.5%) · haut méd +0.18% · range méd 0.91%
- Excursion ouverture 15min (n=160) : bas méd −0.48% (p90 −1.71%) · haut méd +0.31% · range méd 1.09%
- Excursion ouverture 30min (n=160) : bas méd −0.49% (p90 −1.72%) · haut méd +0.51% · range méd 1.28%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.88%) · haut méd +0.56% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 343.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 44% · séance 59% (85/159) · gap 9% · délai 0.4min · rebond 37% (34/85) (MFE +0.84%)
   - −1.0% : fill 30min 26% · séance 50% (70/159) · gap 2% · délai 25.6min · rebond 46% (33/70) (MFE +0.87%)
   - −1.5% : fill 30min 10% · séance 28% (44/159) · gap 1% · délai 70.9min · rebond 35% (19/44) (MFE +0.53%)
   - −2.0% : fill 30min 5% · séance 22% (36/159) · gap 0% · délai 249.7min · rebond 42% (17/36) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 8% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.65% (survit 80% du bruit)
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
   - **flat** (36 séances) :
      · −1.0% : fill 48% (18/36) · rebond 50% (10/18)
      · −2.0% : fill 19% (7/36) · rebond 20% (1/7)
      · −3.0% : fill 7% (3/36) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/36) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (102 séances) :
      · −1.0% : fill 40% (34/102) · rebond 53% (16/34)
      · −2.0% : fill 14% (17/102) · rebond 60% (10/17)
      · −3.0% : fill 5% (6/102) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/102) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/102) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 67% si les 15 1res min sont vertes (74 cas) · 27% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 75% si début vert vs 21% si rouge (base 47% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 288min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **75%** · continue >prix actuel 54% ; creux résiduel méd -0.62% (q20 -1.46%) → **SL/trailing à −1.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.9% / q75 +1.5% → **scale +0.9% / runner +1.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **21%** (continue à baisser 53%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.26%** (au-delà de la MAE q10 -2.26%), cible rebond +0.84% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.51% .. +1.56%] · haut q95 +1.96% · bas q05 -2.13%
   - 60min (n=160) : retour [-1.64% .. +2.08%] · haut q95 +2.08% · bas q05 -2.4%
   - 2h (n=160) : retour [-1.95% .. +2.14%] · haut q95 +2.53% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.82% .. +2.18%] · haut q95 +2.75% · bas q05 -2.95%
   - 6h (n=160) : retour [-2.12% .. +2.35%] · haut q95 +2.91% · bas q05 -3.03%
   - session (n=160) : retour [-2.71% .. +2.45%] · haut q95 +3.36% · bas q05 -3.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 31.9  _(momentum baissier)_
- **ADX** : 13.7  _(pas de tendance nette)_
- **MACD** : hist -2.172  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 8.8%
- **ATR** : 7.04 (40.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.193  _(distribution)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 48.2  _(transition)_
- **MA** : MA20 352.88 · MA50 343.14 · MA200 310.33  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 +0.3% · MA200 +10.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (905510 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
