# SRT3

**Generated** : 2026-09-01T00:04:07.099262+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €251.10  

> 🟡 **WAIT-FOR-DIP** — spot +5.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €251.10 (+5.5% vs entrée) · entrée €237.99 · stop €230.83 · T1 €243.52 · R/R 0.77  
> ↳ P(T1 av. stop) 62 % · EV/risk 0.047 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €236.89–€239.10 (mid €237.99)
- Spot actuel : €251.10 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : €230.83 (stop swing_plan-based (-8.07%))
- Targets : T1 €243.52 · R/R 0.77 | T2 €249.05 · R/R 1.54 | T3 €254.58 · R/R 2.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €230.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.07 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **1.587 pt plus bas** dans le cas TYPIQUE (médiane), 4.442 au p90, **6.135 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 8.07 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0079 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3694** [0.3001 ; 0.443] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4189** [0.3678 ; 0.4714] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4399** [0.3883 ; 0.4925] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (49.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0687** (β de hausse 1.1747, asymétrie 0.9098) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.317× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 222.195 sur sr_based (3.43 ATR, 11.511 %) — p(stop avant cible) 0.0644 [0.04 ; 0.09], R/R 0.098, perte reelle 14.205 % (gap inclus), CVaR 11.513 %, EV -0.0854 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.28 %) — p(stop avant cible) 0.2508 [0.21 ; 0.30], R/R 0.181, perte reelle 7.669 % (gap inclus), EV -0.8917 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 74.7 % x 1.39 % + P(rien) 0.3 % x -1.13 % ne couvrent pas P(stop) 25.1 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.65 ATR (stop 6.447 %) — p(stop avant cible) 0.1765 [0.14 ; 0.22], R/R 0.149, perte reelle 9.276 % (gap inclus), EV -0.5348 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 80.8 % x 1.39 % + P(rien) 1.5 % x -1.14 % ne couvrent pas P(stop) 17.6 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.43 ATR (stop 11.511 %) — p(stop avant cible) 0.0644 [0.04 ; 0.09], R/R 0.098, perte reelle 14.205 % (gap inclus), EV -0.0854 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 85.0 % x 1.39 % + P(rien) 8.5 % x -4.09 % ne couvrent pas P(stop) 6.4 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 8.63 ATR (stop 26.367 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.053, perte reelle 26.367 % (gap inclus), EV 0.1525 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.37 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.713 %) — p(stop avant cible) 0.6119 [0.56 ; 0.66], R/R 0.857, perte reelle 1.617 % (gap inclus), EV -0.4515 % — **REFUSE**
      - refuse : p_stop_first 0.612, borne haute 0.662 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 38.8 % x 1.39 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 61.2 % x 1.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.427 %) — p(stop avant cible) 0.5102 [0.46 ; 0.56], R/R 0.511, perte reelle 2.714 % (gap inclus), EV -0.7058 % — **REFUSE**
      - refuse : p_stop_first 0.510, borne haute 0.563 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 49.0 % x 1.39 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 51.0 % x 2.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.14 %) — p(stop avant cible) 0.4065 [0.36 ; 0.46], R/R 0.313, perte reelle 4.426 % (gap inclus), EV -0.9766 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 59.4 % x 1.39 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 40.6 % x 4.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.853 %) — p(stop avant cible) 0.3371 [0.29 ; 0.39], R/R 0.212, perte reelle 6.529 % (gap inclus), EV -1.2821 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 66.3 % x 1.39 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 33.7 % x 6.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.566 %) — p(stop avant cible) 0.2916 [0.25 ; 0.34], R/R 0.181, perte reelle 7.669 % (gap inclus), EV -1.2544 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 70.8 % x 1.39 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 29.2 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.65 ATR (stop 5.568 %) — p(stop avant cible) 0.1979 [0.16 ; 0.24], R/R 0.168, perte reelle 8.26 % (gap inclus), EV -0.5466 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 79.1 % x 1.39 % + P(rien) 1.1 % x -0.70 % ne couvrent pas P(stop) 19.8 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.133 %) — p(stop avant cible) 0.1622 [0.13 ; 0.20], R/R 0.144, perte reelle 9.643 % (gap inclus), EV -0.4735 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 81.6 % x 1.39 % + P(rien) 2.2 % x -1.84 % ne couvrent pas P(stop) 16.2 % x 9.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.846 %) — p(stop avant cible) 0.1431 [0.11 ; 0.18], R/R 0.137, perte reelle 10.096 % (gap inclus), EV -0.3764 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 82.7 % x 1.39 % + P(rien) 3.0 % x -2.62 % ne couvrent pas P(stop) 14.3 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 8.559 %) — p(stop avant cible) 0.1265 [0.09 ; 0.16], R/R 0.123, perte reelle 11.278 % (gap inclus), EV -0.3981 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 83.3 % x 1.39 % + P(rien) 4.0 % x -3.11 % ne couvrent pas P(stop) 12.7 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.43 ATR (stop 10.633 %) — p(stop avant cible) 0.0785 [0.05 ; 0.11], R/R 0.098, perte reelle 14.205 % (gap inclus), EV -0.2272 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 84.8 % x 1.39 % + P(rien) 7.4 % x -3.87 % ne couvrent pas P(stop) 7.8 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 12.839 %) — p(stop avant cible) 0.0491 [0.03 ; 0.08], R/R 0.098, perte reelle 14.205 % (gap inclus), EV -0.0045 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 85.0 % x 1.39 % + P(rien) 10.1 % x -4.83 % ne couvrent pas P(stop) 4.9 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 14.266 %) — p(stop avant cible) 0.027 [0.01 ; 0.05], R/R 0.097, perte reelle 14.266 % (gap inclus), EV 0.1113 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 15.692 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.088, perte reelle 15.692 % (gap inclus), EV 0.1195 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.69 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.119 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.081, perte reelle 17.119 % (gap inclus), EV 0.1654 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.12 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 18.546 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.075, perte reelle 18.546 % (gap inclus), EV 0.1593 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.55 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 19.972 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.069, perte reelle 19.972 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.97 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.399 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.065, perte reelle 21.399 % (gap inclus), EV 0.1479 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.40 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.825 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.061, perte reelle 22.825 % (gap inclus), EV 0.1525 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 251.1, ATR14 7.1643 (2.853 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 1.087 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.143 % | 250.7418 | 88.95 % | 92.89 % | 94.37 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.285 % | 250.3836 | 82.45 % | 88.35 % | 90.71 % | 93.37 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.428 % | 250.0254 | 74.95 % | 83.81 % | 86.96 % | 90.5 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.571 % | 249.6671 | 68.34 % | 78.87 % | 83.0 % | 87.33 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.713 % | 249.3089 | 63.21 % | 75.52 % | 79.74 % | 84.95 % | 90.55 % | 93.07 % |
| 0.35 ATR | 0.999 % | 248.5925 | 53.06 % | 69.1 % | 74.11 % | 80.99 % | 87.16 % | 91.16 % |
| 0.5 ATR | 1.427 % | 247.5179 | 38.07 % | 56.56 % | 64.43 % | 74.26 % | 82.79 % | 88.64 % |
| 0.75 ATR | 2.14 % | 245.7268 | 19.63 % | 36.82 % | 47.92 % | 59.31 % | 72.44 % | 82.31 % |
| 1.0 ATR | 2.853 % | 243.9357 | 10.26 % | 24.68 % | 34.68 % | 47.72 % | 63.18 % | 75.28 % |
| 1.25 ATR | 3.566 % | 242.1446 | 4.83 % | 15.0 % | 24.7 % | 38.32 % | 53.83 % | 68.34 % |
| 1.5 ATR | 4.28 % | 240.3536 | 2.37 % | 10.07 % | 18.08 % | 31.09 % | 46.57 % | 62.71 % |
| 2.0 ATR | 5.706 % | 236.7714 | 0.79 % | 4.74 % | 8.5 % | 17.62 % | 35.32 % | 52.86 % |
| 2.5 ATR | 7.133 % | 233.1893 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 25.17 % | 42.81 % |
| 3.0 ATR | 8.559 % | 229.6071 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 18.21 % | 35.28 % |
| 4.0 ATR | 11.413 % | 222.4429 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.55 % | 21.21 % |
| 6.0 ATR | 17.119 % | 208.1143 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.24 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.73 ATR | 1.91 ATR | 2.63 ATR | 3.64 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.57 ATR | 2.11 ATR | 2.51 ATR | 2.87 ATR | 3.95 ATR | 5.24 ATR |
| **20 s.** | 1.01 ATR | 2.14 ATR | 2.39 ATR | 3.16 ATR | 3.73 ATR | 4.17 ATR | 5.62 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.427 %, prix 247.5168), p(touche) 38.07 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.14 %, prix 245.7265), p(touche) 36.82 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.853 %, prix 243.9361), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.566 %, prix 242.1458), p(touche) 38.32 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.57–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.706 %, prix 236.7722), p(touche) 35.32 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.391–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.133 %, prix 233.189), p(touche) 42.81 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.004 | EV/share : €-0.031 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 35 % | T3 21 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 20.0 | bear 8.5 | side 71.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 502.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.376% → cible +1.039% / stop −1.5%, p_fill 19%, n_eff≈12.6) : P(cible|rempli) **62%** · **EV/risk +0.026** (×p_fill ; si rempli +0.20% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→45% · +3.0%→24% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.23% (p90 6.3%) · excursion haute méd. +1.79% / basse méd. −1.26%
- Profil de vol intra : ouverture 1.989% vs midi 0.826% vs clôture 0.984% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.099 ; mean-reverting — autocorr -0.031)_ ; drift intra méd. 0.366% ; recovery-V 26%
- **σ réalisé intraday** 2.368% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 64% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 251.5506 (VA 250.8231–252.1569 ; dernier close 254.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 32% · rebond 66% · **stop −2.49%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.08% · baisse 52% (gap-down >1% 8% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.68%) · haut méd +0.57% · range méd 1.19%
- Excursion ouverture 15min (n=160) : bas méd −0.53% (p90 −1.86%) · haut méd +0.66% · range méd 1.46%
- Excursion ouverture 30min (n=160) : bas méd −0.58% (p90 −1.97%) · haut méd +0.83% · range méd 1.66%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.25%) · haut méd +0.9% · range méd 1.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 253.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 75% (120/159) · gap 24% · délai 0.4min · rebond 51% (66/120) (MFE +1.05%)
   - −1.0% : fill 30min 41% · séance 64% (104/159) · gap 8% · délai 4.5min · rebond 62% (62/104) (MFE +1.33%)
   - −1.5% : fill 30min 25% · séance 46% (84/159) · gap 4% · délai 14.6min · rebond 59% (49/84) (MFE +1.43%)
   - −2.0% : fill 30min 10% · séance 32% (64/159) · gap 1% · délai 106.1min · rebond 66% (38/64) (MFE +1.39%)
   - −3.0% : fill 30min 4% · séance 14% (33/159) · gap 1% · délai 99.5min · rebond 67% (20/33) (MFE +1.96%)
   - −4.0% : fill 30min 3% · séance 8% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 6% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.97%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −2.15%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −2.51%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=448 jambes) : jambe baissière méd −1.02% (p90 −2.28%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 80% (48/57) · rebond 70% (32/48)
      · −2.0% : fill 34% (28/57) · rebond 71% (18/28)
      · −3.0% : fill 17% (18/57) · rebond 62% (11/18)
      · −4.0% : fill 13% (12/57) · rebond 68% (10/12)
      · −5.0% : fill 6% (6/57) · rebond 100% (6/6)
   - **flat** (39 séances) :
      · −1.0% : fill 65% (25/39) · rebond 53% (12/25)
      · −2.0% : fill 38% (17/39) · rebond 55% (9/17)
      · −3.0% : fill 9% (6/39) · rebond 38% (2/6)
      · −4.0% : fill 3% (2/39) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/39) · rebond 0% (0/1)
   - **gap-up** (63 séances) :
      · −1.0% : fill 47% (31/63) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/63) · rebond 72% (11/19)
      · −3.0% : fill 14% (9/63) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/63) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/63) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 58% si les 15 1res min sont vertes (85 cas) · 42% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 64% si début vert vs 35% si rouge (base 50% · écart 29 pts) ; prédictivité sature ensuite (plafond brut 254min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **64%** · continue >prix actuel 46% ; creux résiduel méd -1.43% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.03% / q75 +1.78% → **scale +1.03% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **35%** (continue à baisser 44%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.69% .. +2.09%] · haut q95 +2.63% · bas q05 -3.05%
   - 60min (n=160) : retour [-2.46% .. +2.34%] · haut q95 +2.76% · bas q05 -3.47%
   - 2h (n=160) : retour [-2.18% .. +2.33%] · haut q95 +2.94% · bas q05 -3.8%
   - 4h (n=160) : retour [-2.3% .. +2.44%] · haut q95 +3.21% · bas q05 -3.82%
   - 6h (n=160) : retour [-2.53% .. +2.85%] · haut q95 +3.48% · bas q05 -3.83%
   - session (n=160) : retour [-3.47% .. +3.94%] · haut q95 +5.14% · bas q05 -4.35%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 61.2  _(momentum haussier)_
- **ADX** : 18.3  _(pas de tendance nette)_
- **MACD** : hist 1.516  _(pas de croisement recent)_
- **BB** : %B 0.86 · largeur 13.8%
- **ATR** : 7.16 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.115  _(accumulation)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 47.8  _(transition)_
- **MA** : MA20 239.29 · MA50 233.08 · MA200 232.61  _(prix > MA20)_
- **Dist MA** : MA20 +4.9% · MA50 +7.7% · MA200 +8.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (782957 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
