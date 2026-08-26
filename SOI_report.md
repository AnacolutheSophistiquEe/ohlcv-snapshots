# SOI

**Generated** : 2026-08-26T00:09:19.971732+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €108.95  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €108.95 (+0.5% vs entrée) · entrée €108.42 · stop €103.75 · T1 €117.75 · R/R 2.0  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.163 _(réel 5 s)_ (GBM -0.016) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.3% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €107.89–€108.95 (mid €108.42)
- Spot actuel : €108.95 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €103.75 (stop swing_plan-based (-10.37%))
- Targets : T1 €117.75 · R/R 2.0 | T2 €117.90 · R/R 2.03 | T3 €118.05 · R/R 2.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €103.75


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.37 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **8.349 pt plus bas** dans le cas TYPIQUE (médiane), 16.809 au p90, **18.924 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.026 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3236** [0.2573 ; 0.3958] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.3255** [0.2777 ; 0.3762] _(largeur 9.8 pt, n_eff 345.8)_
   - deep : **0.3418** [0.2933 ; 0.3929] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.1 pt), swing (31.6 pt), deep (31.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.48 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.43 % contre 7.71 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.22 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1271** (β de hausse 1.6164, asymétrie 0.6973) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.051× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 98.75 sur atr_based (1.5 ATR, 9.362 %) — p(stop avant cible) 0.4827 [0.43 ; 0.54], R/R 1.232, perte reelle 18.446 % (gap inclus), CVaR 9.39 %, EV -2.9159 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.51 ATR (stop 6.0 %) — p(stop avant cible) 0.6161 [0.56 ; 0.67], R/R 1.722, perte reelle 13.196 % (gap inclus), EV -2.6966 % — **REFUSE**
      - refuse : p_stop_first 0.616, borne haute 0.666 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.25 ATR du spot — compartiment <1, mesure a 47.7 % de casse (IC clusterise [0.443 ; 0.512] sur 1016 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.70 %) : P(cible) 17.8 % x 22.73 % + P(rien) 20.6 % x 6.73 % ne couvrent pas P(stop) 61.6 % x 13.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 9.362 %) — p(stop avant cible) 0.4827 [0.43 ; 0.54], R/R 1.232, perte reelle 18.446 % (gap inclus), EV -2.9159 % — **REFUSE**
      - refuse : R/R 1.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.92 %) : P(cible) 20.8 % x 22.73 % + P(rien) 30.9 % x 4.05 % ne couvrent pas P(stop) 48.3 % x 18.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.48 ATR (stop 18.336 %) — p(stop avant cible) 0.1893 [0.15 ; 0.23], R/R 0.947, perte reelle 24.006 % (gap inclus), EV 1.0909 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
   - 🟢 support a 4.01 ATR (stop 27.882 %) — p(stop avant cible) 0.049 [0.03 ; 0.08], R/R 0.776, perte reelle 29.294 % (gap inclus), EV 2.4516 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.88 % > budget 12.00 %
   - 🔴 support a 6.44 ATR (stop 43.026 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.528, perte reelle 43.026 % (gap inclus), EV 2.5327 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.03 % > budget 12.00 %
      - ⚠ support DETECTE a 6.44 ATR du spot — compartiment >=6, mesure a 46.5 % de casse (IC clusterise [0.333 ; 0.591] sur 43 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 1.56 %) — p(stop avant cible) 0.8708 [0.83 ; 0.90], R/R 6.782, perte reelle 3.351 % (gap inclus), EV -0.6451 % — **REFUSE**
      - refuse : cible atteinte seulement 7.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.871, borne haute 0.903 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 7.6 % x 22.73 % + P(rien) 5.3 % x 10.19 % ne couvrent pas P(stop) 87.1 % x 3.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.51 ATR (stop 5.039 %) — p(stop avant cible) 0.6572 [0.61 ; 0.71], R/R 2.218, perte reelle 10.247 % (gap inclus), EV -1.7257 % — **REFUSE**
      - refuse : p_stop_first 0.657, borne haute 0.706 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 16.0 % x 22.73 % + P(rien) 18.3 % x 7.51 % ne couvrent pas P(stop) 65.7 % x 10.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.802 %) — p(stop avant cible) 0.5523 [0.50 ; 0.60], R/R 1.484, perte reelle 15.318 % (gap inclus), EV -2.885 % — **REFUSE**
      - refuse : p_stop_first 0.552, borne haute 0.604 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.48 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 18.9 % x 22.73 % + P(rien) 25.9 % x 4.95 % ne couvrent pas P(stop) 55.2 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.922 %) — p(stop avant cible) 0.4223 [0.37 ; 0.47], R/R 1.059, perte reelle 21.456 % (gap inclus), EV -3.0041 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.00 %) : P(cible) 22.3 % x 22.73 % + P(rien) 35.4 % x 2.77 % ne couvrent pas P(stop) 42.2 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.483 %) — p(stop avant cible) 0.3653 [0.32 ; 0.42], R/R 1.059, perte reelle 21.456 % (gap inclus), EV -1.9018 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 23.3 % x 22.73 % + P(rien) 40.2 % x 1.59 % ne couvrent pas P(stop) 36.5 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.48 ATR (stop 17.375 %) — p(stop avant cible) 0.2104 [0.17 ; 0.26], R/R 0.947, perte reelle 24.006 % (gap inclus), EV 0.6065 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.39 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.845 %) — p(stop avant cible) 0.113 [0.08 ; 0.15], R/R 0.776, perte reelle 29.294 % (gap inclus), EV 1.616 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.85 % > budget 12.00 %
   - 🟢 grid_snapped a 4.01 ATR (stop 26.921 %) — p(stop avant cible) 0.052 [0.03 ; 0.08], R/R 0.776, perte reelle 29.294 % (gap inclus), EV 2.4267 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.92 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.207 %) — p(stop avant cible) 0.0337 [0.02 ; 0.06], R/R 0.728, perte reelle 31.207 % (gap inclus), EV 2.4951 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.21 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 34.328 %) — p(stop avant cible) 0.0282 [0.01 ; 0.05], R/R 0.662, perte reelle 34.328 % (gap inclus), EV 2.4471 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.33 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.448 %) — p(stop avant cible) 0.016 [0.01 ; 0.03], R/R 0.607, perte reelle 37.448 % (gap inclus), EV 2.4618 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.45 % > budget 12.00 %
   - 🔴 grid_snapped a 6.44 ATR (stop 42.065 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.54, perte reelle 42.065 % (gap inclus), EV 2.5125 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.81 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.485, perte reelle 46.81 % (gap inclus), EV 2.5327 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.81 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 49.931 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.455, perte reelle 49.931 % (gap inclus), EV 2.5327 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.93 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 108.95, ATR14 6.8 (6.241 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.361 ATR = 2.253 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.312 % | 108.61 | 91.08 % | 94.11 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.624 % | 108.27 | 84.9 % | 89.99 % | 92.04 % | 94.59 % | 96.24 % | 97.4 % |
| 0.15 ATR | 0.936 % | 107.93 | 77.84 % | 85.08 % | 87.92 % | 91.14 % | 93.77 % | 95.3 % |
| 0.2 ATR | 1.248 % | 107.59 | 69.41 % | 80.18 % | 84.09 % | 88.39 % | 91.59 % | 93.51 % |
| 0.25 ATR | 1.56 % | 107.25 | 63.04 % | 76.45 % | 80.84 % | 86.71 % | 90.31 % | 93.01 % |
| 0.35 ATR | 2.184 % | 106.57 | 51.08 % | 67.81 % | 73.87 % | 81.59 % | 86.05 % | 90.41 % |
| 0.5 ATR | 3.121 % | 105.55 | 36.18 % | 55.64 % | 63.16 % | 73.72 % | 81.4 % | 87.71 % |
| 0.75 ATR | 4.681 % | 103.85 | 17.16 % | 35.82 % | 47.64 % | 59.55 % | 73.79 % | 81.62 % |
| 1.0 ATR | 6.241 % | 102.15 | 8.43 % | 24.34 % | 34.58 % | 48.52 % | 65.58 % | 76.42 % |
| 1.25 ATR | 7.802 % | 100.45 | 4.12 % | 15.9 % | 25.74 % | 38.29 % | 57.27 % | 70.73 % |
| 1.5 ATR | 9.362 % | 98.75 | 2.35 % | 10.89 % | 18.96 % | 30.61 % | 49.36 % | 64.64 % |
| 2.0 ATR | 12.483 % | 95.35 | 0.59 % | 4.81 % | 9.23 % | 18.6 % | 35.61 % | 54.35 % |
| 2.5 ATR | 15.603 % | 91.95 | 0.29 % | 2.45 % | 4.91 % | 11.91 % | 24.73 % | 46.25 % |
| 3.0 ATR | 18.724 % | 88.55 | 0.2 % | 0.79 % | 2.55 % | 7.19 % | 17.01 % | 38.26 % |
| 4.0 ATR | 24.966 % | 81.75 | 0.1 % | 0.59 % | 1.38 % | 3.64 % | 9.89 % | 25.07 % |
| 6.0 ATR | 37.448 % | 68.15 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.29 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.63 ATR | 0.81 ATR | 0.99 ATR | 1.13 ATR | 1.57 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.28 ATR | 1.46 ATR | 1.96 ATR | 2.49 ATR |
| **5 s.** | 0.48 ATR | 0.97 ATR | 1.09 ATR | 1.42 ATR | 1.73 ATR | 1.94 ATR | 2.70 ATR | 3.62 ATR |
| **10 s.** | 0.71 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.49 ATR | 2.81 ATR | 3.98 ATR | 5.80 ATR |
| **20 s.** | 1.06 ATR | 2.27 ATR | 2.58 ATR | 3.40 ATR | 4.01 ATR | 4.79 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.634–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.241 %, prix 102.1504), p(touche) 34.58 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.086–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.802 %, prix 100.4497), p(touche) 38.29 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.659–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.578–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : €-0.076 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.134 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 69.5 | bear 16.2 | side 14.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 109.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.487% → cible +8.608% / stop −4.304%, p_fill 89%, n_eff≈36.3) : P(cible|rempli) **3%** · **EV/risk -0.163** (×p_fill ; si rempli -0.79% du capital)
  - **swing** (entrée dip −1.086% → cible +18.771% / stop −9.386%, p_fill 87%, n_eff≈35.9) : P(cible|rempli) **14%** · **EV/risk +0.040** (×p_fill ; si rempli +0.43% du capital)
  - **deep** (entrée dip −1.579% → cible +26.602% / stop −13.301%, p_fill 88%, n_eff≈37.4) : P(cible|rempli) **27%** · **EV/risk -0.076** (×p_fill ; si rempli -1.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→65% · +3.0%→51% · +5.0%→34% · +8.0%→11%
- Range intraday médian 8.23% (p90 14.47%) · excursion haute méd. +3.37% / basse méd. −3.46%
- Profil de vol intra : ouverture 5.163% vs midi 1.446% vs clôture 2.296% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑0%/↓3% ; spike-down 76% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.078)_ ; drift intra méd. -0.684% ; recovery-V 32%
- **σ réalisé intraday** 4.759% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 53% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 111.478 (VA 110.49–111.934 ; dernier close 109.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 50% · rebond 84% · **stop −8.21%** sous le fill (sous le bruit) · cible +3.13% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. 0.5% · baisse 41% (gap-down >1% 27% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.1% (p90 −3.73%) · haut méd +0.89% · range méd 2.73%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −5.04%) · haut méd +1.24% · range méd 3.47%
- Excursion ouverture 30min (n=160) : bas méd −1.49% (p90 −5.35%) · haut méd +1.5% · range méd 3.83%
- Excursion ouverture 60min (n=160) : bas méd −1.7% (p90 −5.86%) · haut méd +1.58% · range méd 4.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 109.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 79% (127/159) · gap 36% · délai 0.1min · rebond 69% (88/127) (MFE +1.87%)
   - −1.0% : fill 30min 59% · séance 73% (115/159) · gap 27% · délai 0.2min · rebond 72% (84/115) (MFE +2.02%)
   - −1.5% : fill 30min 52% · séance 65% (106/159) · gap 23% · délai 0.2min · rebond 73% (78/106) (MFE +2.34%)
   - −2.0% : fill 30min 45% · séance 60% (95/159) · gap 19% · délai 0.4min · rebond 70% (73/95) (MFE +2.4%)
   - −3.0% : fill 30min 36% · séance 50% (80/159) · gap 11% · délai 1.5min · rebond 84% (69/80) (MFE +3.13%)
   - −4.0% : fill 30min 26% · séance 41% (65/159) · gap 6% · délai 11.4min · rebond 79% (55/65) (MFE +3.3%)
   - −5.0% : fill 30min 18% · séance 34% (48/159) · gap 2% · délai 26.8min · rebond 70% (38/48) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −3.58%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.9%) → stop au-delà de −2.14% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.37%) → stop au-delà de −1.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1359 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 97% (55/57) · rebond 64% (36/55)
      · −2.0% : fill 93% (52/57) · rebond 70% (40/52)
      · −3.0% : fill 84% (47/57) · rebond 80% (40/47)
      · −4.0% : fill 68% (38/57) · rebond 88% (35/38)
      · −5.0% : fill 58% (31/57) · rebond 77% (26/31)
   - **flat** (14 séances) :
      · −1.0% : fill 93% (11/14) · rebond 78% (9/11)
      · −2.0% : fill 73% (10/14) · rebond 79% (9/10)
      · −3.0% : fill 71% (9/14) · rebond 78% (8/9)
      · −4.0% : fill 57% (8/14) · rebond 56% (5/8)
      · −5.0% : fill 56% (7/14) · rebond 72% (6/7)
   - **gap-up** (88 séances) :
      · −1.0% : fill 55% (49/88) · rebond 80% (39/49)
      · −2.0% : fill 36% (33/88) · rebond 68% (24/33)
      · −3.0% : fill 23% (24/88) · rebond 96% (21/24)
      · −4.0% : fill 20% (19/88) · rebond 68% (15/19)
      · −5.0% : fill 14% (10/88) · rebond 48% (6/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 66% si les 15 1res min sont vertes (75 cas) · 30% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:08** → P(séance verte=clôture>ouverture) 76% si début vert vs 25% si rouge (base 48% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **76%** · continue >prix actuel 58% ; creux résiduel méd -2.31% (q20 -5.6%) → **SL/trailing à −5.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.43% / q75 +4.57% → **scale +2.43% / runner +4.57%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **25%** (continue à baisser 54%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.33%** (au-delà de la MAE q10 -7.33%), cible rebond +2.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.04% .. +6.39%] · haut q95 +7.84% · bas q05 -6.21%
   - 60min (n=160) : retour [-5.66% .. +6.76%] · haut q95 +8.11% · bas q05 -6.7%
   - 2h (n=160) : retour [-6.77% .. +6.49%] · haut q95 +11.63% · bas q05 -7.74%
   - 4h (n=160) : retour [-7.21% .. +9.21%] · haut q95 +12.35% · bas q05 -8.5%
   - 6h (n=160) : retour [-8.67% .. +10.05%] · haut q95 +12.88% · bas q05 -9.45%
   - session (n=160) : retour [-12.01% .. +12.42%] · haut q95 +14.53% · bas q05 -12.9%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 6%)
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

- **RSI** : 40.5  _(momentum baissier)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist -1.801  _(bearish_recent)_
- **BB** : %B 0.33 · largeur 36.4%
- **ATR** : 6.8 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.173  _(distribution)_
- **Vol ratio** : 0.28  _(volume atone)_
- **Choppiness** : 44.0  _(transition)_
- **MA** : MA20 116.29 · MA50 111.11 · MA200 77.69  _(prix < MA20)_
- **Dist MA** : MA20 -6.3% · MA50 -1.9% · MA200 +40.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (817583 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
