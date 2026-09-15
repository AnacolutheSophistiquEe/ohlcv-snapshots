# SRT3

**Generated** : 2026-09-15T00:03:41.083911+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €227.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €227.00 (+6.3% vs entrée) · entrée €213.53 · stop €206.79 · T1 €219.16 · R/R 0.84  
> ↳ P(T1 av. stop) 55 % · EV/risk -0.07 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €212.40–€214.66 (mid €213.53)
- Spot actuel : €227.00 (+6.3% au-dessus de la zone — repli à attendre)
- Stop : €206.79 (stop swing_plan-based (-8.9%))
- Targets : T1 €219.16 · R/R 0.84 | T2 €224.79 · R/R 1.67 | T3 €230.43 · R/R 2.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €206.79


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.9 %)** : le gap seul le franchit 0.236 % des séances (3 fois sur 1273).
   - exécution **1.072 pt plus bas** dans le cas TYPIQUE (médiane), 4.459 au p90, **5.305 au pire**
   - perte réelle **11.278 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 8.9 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0056 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.625 % | p01 -3.241 % | pire -14.205 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4008** [0.3299 ; 0.475] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4521** [0.4002 ; 0.5048] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4114** [0.3605 ; 0.4638] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.57 %** | vol 2.84 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.2 % si l'on extrapolait par √5 _(rapport 1.087 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0629** (β de hausse 1.1848, asymétrie 0.8971) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.27× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 200.0571 sur atr_grid (4.0 ATR, 11.869 %) — p(stop avant cible) 0.0726 [0.05 ; 0.10], R/R 0.106, perte reelle 14.205 % (gap inclus), CVaR 11.871 %, EV -0.1178 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.451 %) — p(stop avant cible) 0.2538 [0.21 ; 0.30], R/R 0.197, perte reelle 7.669 % (gap inclus), EV -0.8271 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 74.4 % x 1.51 % + P(rien) 0.2 % x -1.13 % ne couvrent pas P(stop) 25.4 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.742 %) — p(stop avant cible) 0.6156 [0.56 ; 0.67], R/R 0.909, perte reelle 1.66 % (gap inclus), EV -0.4418 % — **REFUSE**
      - refuse : p_stop_first 0.616, borne haute 0.666 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 38.4 % x 1.51 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 61.6 % x 1.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.484 %) — p(stop avant cible) 0.5092 [0.46 ; 0.56], R/R 0.534, perte reelle 2.826 % (gap inclus), EV -0.6984 % — **REFUSE**
      - refuse : p_stop_first 0.509, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 49.1 % x 1.51 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 50.9 % x 2.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.225 %) — p(stop avant cible) 0.3992 [0.35 ; 0.45], R/R 0.319, perte reelle 4.737 % (gap inclus), EV -0.9844 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 60.1 % x 1.51 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 39.9 % x 4.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.967 %) — p(stop avant cible) 0.3432 [0.29 ; 0.39], R/R 0.223, perte reelle 6.774 % (gap inclus), EV -1.3337 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.33 %) : P(cible) 65.7 % x 1.51 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 34.3 % x 6.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.709 %) — p(stop avant cible) 0.291 [0.24 ; 0.34], R/R 0.197, perte reelle 7.669 % (gap inclus), EV -1.1684 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 70.7 % x 1.51 % + P(rien) 0.2 % x -1.13 % ne couvrent pas P(stop) 29.1 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.193 %) — p(stop avant cible) 0.2194 [0.18 ; 0.27], R/R 0.183, perte reelle 8.26 % (gap inclus), EV -0.6453 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 77.5 % x 1.51 % + P(rien) 0.6 % x -0.46 % ne couvrent pas P(stop) 21.9 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.935 %) — p(stop avant cible) 0.1988 [0.16 ; 0.24], R/R 0.17, perte reelle 8.862 % (gap inclus), EV -0.577 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 79.0 % x 1.51 % + P(rien) 1.1 % x -0.70 % ne couvrent pas P(stop) 19.9 % x 8.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.676 %) — p(stop avant cible) 0.1812 [0.14 ; 0.22], R/R 0.163, perte reelle 9.276 % (gap inclus), EV -0.4849 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 80.4 % x 1.51 % + P(rien) 1.5 % x -1.17 % ne couvrent pas P(stop) 18.1 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.418 %) — p(stop avant cible) 0.1642 [0.13 ; 0.21], R/R 0.149, perte reelle 10.096 % (gap inclus), EV -0.4694 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 81.4 % x 1.51 % + P(rien) 2.2 % x -1.86 % ne couvrent pas P(stop) 16.4 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.16 %) — p(stop avant cible) 0.1478 [0.11 ; 0.19], R/R 0.149, perte reelle 10.096 % (gap inclus), EV -0.3419 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 82.1 % x 1.51 % + P(rien) 3.1 % x -2.82 % ne couvrent pas P(stop) 14.8 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 8.902 %) — p(stop avant cible) 0.1241 [0.09 ; 0.16], R/R 0.134, perte reelle 11.278 % (gap inclus), EV -0.3246 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 82.8 % x 1.51 % + P(rien) 4.7 % x -3.70 % ne couvrent pas P(stop) 12.4 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.385 %) — p(stop avant cible) 0.0926 [0.07 ; 0.13], R/R 0.106, perte reelle 14.205 % (gap inclus), EV -0.311 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 84.0 % x 1.51 % + P(rien) 6.8 % x -3.88 % ne couvrent pas P(stop) 9.3 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 11.869 %) — p(stop avant cible) 0.0726 [0.05 ; 0.10], R/R 0.106, perte reelle 14.205 % (gap inclus), EV -0.1178 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 84.2 % x 1.51 % + P(rien) 8.5 % x -4.21 % ne couvrent pas P(stop) 7.3 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.353 %) — p(stop avant cible) 0.0539 [0.03 ; 0.08], R/R 0.106, perte reelle 14.205 % (gap inclus), EV -0.0166 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 84.2 % x 1.51 % + P(rien) 10.4 % x -5.03 % ne couvrent pas P(stop) 5.4 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 14.836 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.102, perte reelle 14.836 % (gap inclus), EV 0.082 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.84 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.32 %) — p(stop avant cible) 0.013 [0.00 ; 0.03], R/R 0.092, perte reelle 16.32 % (gap inclus), EV 0.1147 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.32 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.804 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.085, perte reelle 17.804 % (gap inclus), EV 0.1454 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.80 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.287 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.078, perte reelle 19.287 % (gap inclus), EV 0.1372 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 20.771 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.073, perte reelle 20.771 % (gap inclus), EV 0.131 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.77 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.255 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.068, perte reelle 22.255 % (gap inclus), EV 0.1346 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.25 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 23.738 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.064, perte reelle 23.738 % (gap inclus), EV 0.142 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.74 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 227.0, ATR14 6.7357 (2.967 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 1.131 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.148 % | 226.6632 | 89.14 % | 92.98 % | 94.36 % | 96.13 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.297 % | 226.3264 | 82.43 % | 88.34 % | 90.7 % | 93.46 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.445 % | 225.9896 | 75.02 % | 83.89 % | 86.94 % | 90.58 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.593 % | 225.6529 | 68.41 % | 78.95 % | 82.99 % | 87.41 % | 92.23 % | 94.37 % |
| 0.25 ATR | 0.742 % | 225.3161 | 63.18 % | 75.59 % | 79.72 % | 85.03 % | 90.44 % | 93.06 % |
| 0.35 ATR | 1.039 % | 224.6425 | 53.11 % | 69.27 % | 73.99 % | 80.87 % | 87.05 % | 90.95 % |
| 0.5 ATR | 1.484 % | 223.6321 | 38.3 % | 56.72 % | 64.39 % | 74.03 % | 82.57 % | 88.33 % |
| 0.75 ATR | 2.225 % | 221.9482 | 19.45 % | 36.86 % | 47.97 % | 59.27 % | 72.21 % | 81.79 % |
| 1.0 ATR | 2.967 % | 220.2643 | 9.97 % | 24.7 % | 34.82 % | 47.87 % | 62.85 % | 74.75 % |
| 1.25 ATR | 3.709 % | 218.5804 | 4.74 % | 15.02 % | 24.73 % | 38.45 % | 53.29 % | 67.61 % |
| 1.5 ATR | 4.451 % | 216.8964 | 2.27 % | 9.88 % | 17.8 % | 31.12 % | 45.92 % | 61.77 % |
| 2.0 ATR | 5.935 % | 213.5286 | 0.69 % | 4.55 % | 8.21 % | 17.34 % | 34.56 % | 51.91 % |
| 2.5 ATR | 7.418 % | 210.1607 | 0.3 % | 1.98 % | 4.75 % | 10.7 % | 24.4 % | 41.85 % |
| 3.0 ATR | 8.902 % | 206.7929 | 0.2 % | 1.48 % | 2.97 % | 6.34 % | 17.33 % | 34.31 % |
| 4.0 ATR | 11.869 % | 200.0571 | 0.0 % | 0.69 % | 1.78 % | 3.57 % | 8.96 % | 20.22 % |
| 6.0 ATR | 17.804 % | 186.5857 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.46 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.72 ATR | 1.90 ATR | 2.58 ATR | 3.48 ATR |
| **10 s.** | 0.68 ATR | 1.36 ATR | 1.54 ATR | 2.08 ATR | 2.47 ATR | 2.81 ATR | 3.88 ATR | 5.15 ATR |
| **20 s.** | 0.99 ATR | 2.10 ATR | 2.34 ATR | 3.09 ATR | 3.66 ATR | 4.03 ATR | 5.55 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.484 %, prix 223.6313), p(touche) 38.3 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.648–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.225 %, prix 221.9493), p(touche) 36.86 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.806–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.967 %, prix 220.2649), p(touche) 34.82 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.076–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.709 %, prix 218.5806), p(touche) 38.45 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.54–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.935 %, prix 213.5275), p(touche) 34.56 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.343–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.418 %, prix 210.1611), p(touche) 41.85 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.051 | EV/share : €-0.341 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 27 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 26.6 | bear 8.4 | side 65.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→48% · +3.0%→24% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.22% (p90 5.97%) · excursion haute méd. +1.89% / basse méd. −1.26%
- Profil de vol intra : ouverture 1.96% vs midi 0.809% vs clôture 0.978% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.093 ; neutre — autocorr -0.023)_ ; drift intra méd. 0.176% ; recovery-V 26%
- **σ réalisé intraday** 2.303% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 71% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 242.1875 (VA 239.7375–242.8875 ; dernier close 238.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 35% · rebond 66% · **stop −2.22%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.68 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 55% (gap-down >1% 7% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.33% (p90 −1.51%) · haut méd +0.61% · range méd 1.07%
- Excursion ouverture 15min (n=160) : bas méd −0.46% (p90 −1.75%) · haut méd +0.77% · range méd 1.38%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.92%) · haut méd +0.82% · range méd 1.56%
- Excursion ouverture 60min (n=160) : bas méd −0.72% (p90 −2.09%) · haut méd +0.87% · range méd 1.75%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 237.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 78% (121/159) · gap 27% · délai 0.4min · rebond 50% (65/121) (MFE +1.01%)
   - −1.0% : fill 30min 41% · séance 67% (105/159) · gap 7% · délai 8.9min · rebond 59% (61/105) (MFE +1.23%)
   - −1.5% : fill 30min 25% · séance 47% (84/159) · gap 4% · délai 23.6min · rebond 59% (48/84) (MFE +1.33%)
   - −2.0% : fill 30min 9% · séance 35% (65/159) · gap 1% · délai 133.4min · rebond 66% (38/65) (MFE +1.52%)
   - −3.0% : fill 30min 4% · séance 13% (33/159) · gap 1% · délai 99.5min · rebond 67% (20/33) (MFE +1.96%)
   - −4.0% : fill 30min 2% · séance 8% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 5% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.88%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.99%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −2.51%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=453 jambes) : jambe baissière méd −1.01% (p90 −2.24%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 84% (49/58) · rebond 66% (31/49)
      · −2.0% : fill 41% (29/58) · rebond 69% (18/29)
      · −3.0% : fill 14% (18/58) · rebond 62% (11/18)
      · −4.0% : fill 10% (12/58) · rebond 68% (10/12)
      · −5.0% : fill 5% (6/58) · rebond 100% (6/6)
   - **flat** (39 séances) :
      · −1.0% : fill 67% (25/39) · rebond 48% (12/25)
      · −2.0% : fill 36% (17/39) · rebond 55% (9/17)
      · −3.0% : fill 9% (6/39) · rebond 38% (2/6)
      · −4.0% : fill 3% (2/39) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/39) · rebond 0% (0/1)
   - **gap-up** (62 séances) :
      · −1.0% : fill 47% (31/62) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/62) · rebond 72% (11/19)
      · −3.0% : fill 14% (9/62) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/62) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/62) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 54% si les 15 1res min sont vertes (83 cas) · 41% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 63% si début vert vs 31% si rouge (base 48% · écart 32 pts) ; prédictivité sature ensuite (plafond brut 254min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **63%** · continue >prix actuel 47% ; creux résiduel méd -1.47% (q20 -2.17%) → **SL/trailing à −2.17%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.03% / q75 +1.9% → **scale +1.03% / runner +1.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **31%** (continue à baisser 43%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.57%** (au-delà de la MAE q10 -2.57%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.31% .. +2.02%] · haut q95 +2.59% · bas q05 -2.9%
   - 60min (n=160) : retour [-2.31% .. +2.33%] · haut q95 +2.71% · bas q05 -3.26%
   - 2h (n=160) : retour [-2.18% .. +2.26%] · haut q95 +2.94% · bas q05 -3.71%
   - 4h (n=160) : retour [-2.26% .. +2.33%] · haut q95 +3.11% · bas q05 -3.65%
   - 6h (n=160) : retour [-2.48% .. +2.72%] · haut q95 +3.35% · bas q05 -3.82%
   - session (n=160) : retour [-3.37% .. +3.79%] · haut q95 +4.79% · bas q05 -4.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.8  _(momentum baissier)_
- **ADX** : 16.6  _(pas de tendance nette)_
- **MACD** : hist -2.486  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 13.0%
- **ATR** : 6.74 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.036  _(neutre)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 44.3  _(transition)_
- **MA** : MA20 241.06 · MA50 235.33 · MA200 233.04  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -3.5% · MA200 -2.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (753883 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
