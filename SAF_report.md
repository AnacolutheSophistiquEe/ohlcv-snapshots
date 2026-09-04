# SAF

**Generated** : 2026-09-04T21:42:20.205402+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €333.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €333.50 (+3.1% vs entrée) · entrée €323.61 · stop €317.14 · T1 €325.91 · R/R 0.36  
> ↳ P(T1 av. stop) 51 % · EV/risk -0.018 · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €323.15–€324.07 (mid €323.61)
- Spot actuel : €333.50 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : €317.14 (stop swing_plan-based (-8.74%))
- Targets : T1 €325.91 · R/R 0.36 | T2 €328.21 · R/R 0.71 | T3 €330.51 · R/R 1.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €317.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.74 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.246 pt plus bas** dans le cas TYPIQUE (médiane), 1.246 au p90, **1.246 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.74 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.001 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1787** [0.1272 ; 0.2408] _(largeur 11.4 pt, n_eff 173.1)_
   - swing : **0.3559** [0.3068 ; 0.4074] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.316** [0.2687 ; 0.3664] _(largeur 9.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.06 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.28 % contre 2.48 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3675** (β de hausse 1.3318, asymétrie 1.0268) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.261× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 300.3286 sur atr_grid (4.5 ATR, 9.946 %) — p(stop avant cible) 0.0824 [0.06 ; 0.11], R/R 0.839, perte reelle 9.986 % (gap inclus), CVaR 9.946 %, EV 0.9868 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.315 %) — p(stop avant cible) 0.4504 [0.40 ; 0.50], R/R 1.578, perte reelle 5.309 % (gap inclus), EV -0.0105 % — **REFUSE**
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 17.4 % x 8.38 % + P(rien) 37.6 % x 2.46 % ne couvrent pas P(stop) 45.0 % x 5.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 5.47 ATR (stop 13.38 %) — p(stop avant cible) 0.0335 [0.02 ; 0.06], R/R 0.626, perte reelle 13.38 % (gap inclus), EV 0.943 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.38 % > budget 12.00 %
   - 🟢 support a 10.01 ATR (stop 23.43 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.358, perte reelle 23.43 % (gap inclus), EV 0.9625 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.43 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.553 %) — p(stop avant cible) 0.8905 [0.85 ; 0.92], R/R 6.469, perte reelle 1.295 % (gap inclus), EV -0.4661 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.890, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 5.7 % x 8.38 % + P(rien) 5.3 % x 4.02 % ne couvrent pas P(stop) 89.0 % x 1.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.105 %) — p(stop avant cible) 0.7809 [0.74 ; 0.82], R/R 4.314, perte reelle 1.942 % (gap inclus), EV -0.2734 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.781, borne haute 0.822 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 8.8 % x 8.38 % + P(rien) 13.1 % x 3.84 % ne couvrent pas P(stop) 78.1 % x 1.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.658 %) — p(stop avant cible) 0.6842 [0.63 ; 0.73], R/R 3.172, perte reelle 2.641 % (gap inclus), EV -0.086 % — **REFUSE**
      - refuse : cible atteinte seulement 12.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.684, borne haute 0.732 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 12.1 % x 8.38 % + P(rien) 19.5 % x 3.64 % ne couvrent pas P(stop) 68.4 % x 2.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.21 %) — p(stop avant cible) 0.607 [0.55 ; 0.66], R/R 2.338, perte reelle 3.583 % (gap inclus), EV -0.1846 % — **REFUSE**
      - refuse : cible atteinte seulement 14.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.607, borne haute 0.657 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 14.0 % x 8.38 % + P(rien) 25.3 % x 3.23 % ne couvrent pas P(stop) 60.7 % x 3.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.763 %) — p(stop avant cible) 0.5177 [0.47 ; 0.57], R/R 1.894, perte reelle 4.424 % (gap inclus), EV -0.0382 % — **REFUSE**
      - refuse : p_stop_first 0.518, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 16.3 % x 8.38 % + P(rien) 32.0 % x 2.78 % ne couvrent pas P(stop) 51.8 % x 4.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.868 %) — p(stop avant cible) 0.3738 [0.32 ; 0.43], R/R 1.359, perte reelle 6.163 % (gap inclus), EV 0.2509 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.421 %) — p(stop avant cible) 0.3331 [0.28 ; 0.38], R/R 1.232, perte reelle 6.799 % (gap inclus), EV 0.2566 % — **REFUSE**
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.973 %) — p(stop avant cible) 0.2862 [0.24 ; 0.34], R/R 1.232, perte reelle 6.799 % (gap inclus), EV 0.6821 % — **REFUSE**
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.526 %) — p(stop avant cible) 0.2551 [0.21 ; 0.30], R/R 0.839, perte reelle 9.986 % (gap inclus), EV 0.0761 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 6.078 %) — p(stop avant cible) 0.2312 [0.19 ; 0.28], R/R 0.839, perte reelle 9.986 % (gap inclus), EV 0.3053 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.631 %) — p(stop avant cible) 0.1947 [0.16 ; 0.24], R/R 0.839, perte reelle 9.986 % (gap inclus), EV 0.4869 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.736 %) — p(stop avant cible) 0.1382 [0.10 ; 0.18], R/R 0.839, perte reelle 9.986 % (gap inclus), EV 0.8001 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.841 %) — p(stop avant cible) 0.1102 [0.08 ; 0.15], R/R 0.839, perte reelle 9.986 % (gap inclus), EV 0.9267 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 9.946 %) — p(stop avant cible) 0.0824 [0.06 ; 0.11], R/R 0.839, perte reelle 9.986 % (gap inclus), EV 0.9868 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 11.052 %) — p(stop avant cible) 0.0646 [0.04 ; 0.09], R/R 0.758, perte reelle 11.052 % (gap inclus), EV 0.9696 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 5.47 ATR (stop 12.748 %) — p(stop avant cible) 0.0431 [0.03 ; 0.07], R/R 0.657, perte reelle 12.748 % (gap inclus), EV 0.9596 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.75 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.367 %) — p(stop avant cible) 0.0196 [0.01 ; 0.04], R/R 0.583, perte reelle 14.367 % (gap inclus), EV 0.9448 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.37 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 15.472 %) — p(stop avant cible) 0.0097 [0.00 ; 0.02], R/R 0.541, perte reelle 15.472 % (gap inclus), EV 0.9493 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.47 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 16.577 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 0.505, perte reelle 16.577 % (gap inclus), EV 0.9546 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.58 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 17.683 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.474, perte reelle 17.683 % (gap inclus), EV 0.9531 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.68 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 333.5, ATR14 7.3714 (2.21 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 0.765 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.111 % | 333.1314 | 89.22 % | 92.54 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.221 % | 332.7629 | 81.37 % | 87.24 % | 89.19 % | 91.44 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.332 % | 332.3943 | 75.1 % | 83.32 % | 86.25 % | 88.68 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.442 % | 332.0257 | 68.43 % | 78.21 % | 82.61 % | 85.33 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.553 % | 331.6571 | 61.27 % | 73.5 % | 78.98 % | 83.27 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.774 % | 330.92 | 49.51 % | 63.3 % | 69.74 % | 76.87 % | 82.69 % | 87.01 % |
| 0.5 ATR | 1.105 % | 329.8143 | 35.59 % | 51.82 % | 59.33 % | 68.6 % | 75.87 % | 81.32 % |
| 0.75 ATR | 1.658 % | 327.9714 | 20.59 % | 35.72 % | 43.22 % | 53.25 % | 63.2 % | 70.73 % |
| 1.0 ATR | 2.21 % | 326.1286 | 9.71 % | 23.75 % | 32.71 % | 42.03 % | 53.51 % | 61.24 % |
| 1.25 ATR | 2.763 % | 324.2857 | 4.31 % | 15.51 % | 24.17 % | 33.37 % | 46.19 % | 54.45 % |
| 1.5 ATR | 3.315 % | 322.4429 | 2.25 % | 10.11 % | 16.7 % | 25.3 % | 38.08 % | 46.45 % |
| 2.0 ATR | 4.421 % | 318.7571 | 0.98 % | 4.42 % | 7.56 % | 15.65 % | 27.1 % | 36.76 % |
| 2.5 ATR | 5.526 % | 315.0714 | 0.2 % | 1.47 % | 3.63 % | 9.15 % | 18.79 % | 27.97 % |
| 3.0 ATR | 6.631 % | 311.3857 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.56 % | 21.78 % |
| 4.0 ATR | 8.841 % | 304.0143 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.04 % | 10.99 % |
| 6.0 ATR | 13.262 % | 289.2714 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.1 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.11 ATR | 1.51 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.65 ATR | 0.72 ATR | 0.99 ATR | 1.23 ATR | 1.39 ATR | 1.87 ATR | 2.33 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.26 ATR | 1.52 ATR | 1.77 ATR | 2.44 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.29 ATR | 1.73 ATR | 2.13 ATR | 2.43 ATR | 3.34 ATR | 4.02 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.21 ATR | 2.74 ATR | 3.17 ATR | 4.25 ATR | 5.52 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.658 %, prix 327.9706), p(touche) 35.72 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.722–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.658 %, prix 327.9706), p(touche) 43.22 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.934–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.21 %, prix 326.1296), p(touche) 42.03 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.287–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.315 %, prix 322.4445), p(touche) 38.08 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.575–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.421 %, prix 318.756), p(touche) 36.76 % (en stress 99.01 %)  ✅ optimum identifie (61.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.018 | EV/share : €-0.119 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 43 % | T3 25 %
- Kelly (position) : f* 0.056 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.7 | bear 65.6 | side 5.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→51% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.52% (p90 3.72%) · excursion haute méd. +1.05% / basse méd. −0.86%
- Profil de vol intra : ouverture 1.472% vs midi 0.522% vs clôture 0.665% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 43% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.084)_ ; drift intra méd. -0.4% ; recovery-V 12%
- **σ réalisé intraday** 1.576% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 331.4575 (VA 330.5975–332.5325 ; dernier close 330.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 24% · rebond 36% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.32% · baisse 30% (gap-down >1% 2% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.71%) · haut méd +0.17% · range méd 0.9%
- Excursion ouverture 15min (n=160) : bas méd −0.5% (p90 −1.8%) · haut méd +0.31% · range méd 1.04%
- Excursion ouverture 30min (n=160) : bas méd −0.5% (p90 −1.81%) · haut méd +0.44% · range méd 1.28%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.85%) · haut méd +0.52% · range méd 1.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 331.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 60% (86/159) · gap 9% · délai 0.4min · rebond 34% (33/86) (MFE +0.79%)
   - −1.0% : fill 30min 27% · séance 51% (72/159) · gap 2% · délai 25.5min · rebond 42% (33/72) (MFE +0.78%)
   - −1.5% : fill 30min 12% · séance 31% (46/159) · gap 1% · délai 70.2min · rebond 31% (19/46) (MFE +0.53%)
   - −2.0% : fill 30min 5% · séance 24% (38/159) · gap 0% · délai 247.8min · rebond 36% (17/38) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.65% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.12% (p90 −0.77%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=212 jambes) : jambe baissière méd −1.04% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (21 séances) :
      · −1.0% : fill 85% (18/21) · rebond 29% (7/18)
      · −2.0% : fill 53% (12/21) · rebond 42% (6/12)
      · −3.0% : fill 18% (5/21) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/21) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/21) · rebond 0% (0/0)
   - **flat** (36 séances) :
      · −1.0% : fill 55% (20/36) · rebond 40% (10/20)
      · −2.0% : fill 29% (9/36) · rebond 12% (1/9)
      · −3.0% : fill 6% (3/36) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/36) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (102 séances) :
      · −1.0% : fill 39% (34/102) · rebond 53% (16/34)
      · −2.0% : fill 13% (17/102) · rebond 60% (10/17)
      · −3.0% : fill 5% (6/102) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/102) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/102) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 67% si les 15 1res min sont vertes (72 cas) · 24% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 75% si début vert vs 19% si rouge (base 45% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 288min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **75%** · continue >prix actuel 54% ; creux résiduel méd -0.7% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.47% → **scale +0.97% / runner +1.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **19%** (continue à baisser 62%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.3%** (au-delà de la MAE q10 -2.3%), cible rebond +0.73% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.5% .. +1.55%] · haut q95 +1.95% · bas q05 -2.09%
   - 60min (n=160) : retour [-1.63% .. +1.99%] · haut q95 +2.02% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.35% .. +2.14%] · haut q95 +2.51% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.87% .. +2.17%] · haut q95 +2.73% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.09% .. +2.33%] · haut q95 +2.79% · bas q05 -3.03%
   - session (n=160) : retour [-2.7% .. +2.41%] · haut q95 +3.35% · bas q05 -3.88%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.1  _(survente)_
- **ADX** : 17.1  _(pas de tendance nette)_
- **MACD** : hist -2.697  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 13.2%
- **ATR** : 7.37 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.279  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 347.06 · MA50 342.85 · MA200 311.18  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 -2.7% · MA200 +7.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (756498 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
