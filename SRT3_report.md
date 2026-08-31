# SRT3

**Generated** : 2026-08-31T21:37:41.154218+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €249.20  

> 🟡 **WAIT-FOR-DIP** — spot +5.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €249.20 (+5.1% vs entrée) · entrée €237.14 · stop €229.97 · T1 €242.76 · R/R 0.78  
> ↳ P(T1 av. stop) 63 % · EV/risk 0.099 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €236.01–€238.26 (mid €237.14)
- Spot actuel : €249.20 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : €229.97 (stop swing_plan-based (-7.72%))
- Targets : T1 €242.76 · R/R 0.78 | T2 €248.38 · R/R 1.57 | T3 €254.00 · R/R 2.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €229.97


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.72 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **1.937 pt plus bas** dans le cas TYPIQUE (médiane), 4.792 au p90, **6.485 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 7.72 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0093 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3696** [0.3003 ; 0.4432] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4194** [0.3682 ; 0.4719] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4446** [0.3929 ; 0.4973] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0691** (β de hausse 1.1747, asymétrie 0.9101) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.32× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 220.5429 sur atr_grid (4.0 ATR, 11.5 %) — p(stop avant cible) 0.0929 [0.07 ; 0.13], R/R 0.136, perte reelle 14.205 % (gap inclus), CVaR 11.502 %, EV -0.2216 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.312 %) — p(stop avant cible) 0.325 [0.28 ; 0.38], R/R 0.251, perte reelle 7.669 % (gap inclus), EV -1.2044 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 67.0 % x 1.93 % + P(rien) 0.5 % x -0.70 % ne couvrent pas P(stop) 32.5 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.39 ATR (stop 5.492 %) — p(stop avant cible) 0.2622 [0.22 ; 0.31], R/R 0.233, perte reelle 8.26 % (gap inclus), EV -0.7798 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 72.4 % x 1.93 % + P(rien) 1.4 % x -0.62 % ne couvrent pas P(stop) 26.2 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.16 ATR (stop 10.595 %) — p(stop avant cible) 0.1133 [0.08 ; 0.15], R/R 0.136, perte reelle 14.205 % (gap inclus), EV -0.4152 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 79.7 % x 1.93 % + P(rien) 9.0 % x -3.80 % ne couvrent pas P(stop) 11.3 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 8.37 ATR (stop 25.564 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.075, perte reelle 25.564 % (gap inclus), EV 0.1625 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.56 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.719 %) — p(stop avant cible) 0.6748 [0.62 ; 0.72], R/R 1.184, perte reelle 1.628 % (gap inclus), EV -0.4716 % — **REFUSE**
      - refuse : p_stop_first 0.675, borne haute 0.723 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 32.5 % x 1.93 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 67.5 % x 1.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.437 %) — p(stop avant cible) 0.5863 [0.53 ; 0.64], R/R 0.699, perte reelle 2.759 % (gap inclus), EV -0.82 % — **REFUSE**
      - refuse : p_stop_first 0.586, borne haute 0.637 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 41.4 % x 1.93 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 58.6 % x 2.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.156 %) — p(stop avant cible) 0.4968 [0.44 ; 0.55], R/R 0.422, perte reelle 4.572 % (gap inclus), EV -1.3012 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 50.3 % x 1.93 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 49.7 % x 4.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.875 %) — p(stop avant cible) 0.411 [0.36 ; 0.46], R/R 0.285, perte reelle 6.774 % (gap inclus), EV -1.6485 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 58.9 % x 1.93 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 41.1 % x 6.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.39 ATR (stop 4.848 %) — p(stop avant cible) 0.2957 [0.25 ; 0.35], R/R 0.233, perte reelle 8.26 % (gap inclus), EV -1.1042 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 69.6 % x 1.93 % + P(rien) 0.9 % x -0.35 % ne couvrent pas P(stop) 29.6 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.469 %) — p(stop avant cible) 0.216 [0.18 ; 0.26], R/R 0.208, perte reelle 9.276 % (gap inclus), EV -0.57 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 76.0 % x 1.93 % + P(rien) 2.4 % x -1.29 % ne couvrent pas P(stop) 21.6 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.187 %) — p(stop avant cible) 0.1937 [0.15 ; 0.24], R/R 0.2, perte reelle 9.643 % (gap inclus), EV -0.4292 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 77.5 % x 1.93 % + P(rien) 3.1 % x -1.77 % ne couvrent pas P(stop) 19.4 % x 9.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.906 %) — p(stop avant cible) 0.1725 [0.14 ; 0.21], R/R 0.191, perte reelle 10.096 % (gap inclus), EV -0.3661 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 78.3 % x 1.93 % + P(rien) 4.5 % x -2.97 % ne couvrent pas P(stop) 17.2 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.16 ATR (stop 9.951 %) — p(stop avant cible) 0.1244 [0.09 ; 0.16], R/R 0.159, perte reelle 12.088 % (gap inclus), EV -0.2492 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 79.4 % x 1.93 % + P(rien) 8.1 % x -3.41 % ne couvrent pas P(stop) 12.4 % x 12.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 11.5 %) — p(stop avant cible) 0.0929 [0.07 ; 0.13], R/R 0.136, perte reelle 14.205 % (gap inclus), EV -0.2216 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 80.0 % x 1.93 % + P(rien) 10.8 % x -4.13 % ne couvrent pas P(stop) 9.3 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 12.937 %) — p(stop avant cible) 0.0638 [0.04 ; 0.09], R/R 0.136, perte reelle 14.205 % (gap inclus), EV -0.0353 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 80.0 % x 1.93 % + P(rien) 13.7 % x -4.91 % ne couvrent pas P(stop) 6.4 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 14.375 %) — p(stop avant cible) 0.0358 [0.02 ; 0.06], R/R 0.134, perte reelle 14.375 % (gap inclus), EV 0.0961 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.38 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 15.812 %) — p(stop avant cible) 0.0255 [0.01 ; 0.05], R/R 0.122, perte reelle 15.812 % (gap inclus), EV 0.1029 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.81 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.249 %) — p(stop avant cible) 0.0085 [0.00 ; 0.02], R/R 0.112, perte reelle 17.249 % (gap inclus), EV 0.1584 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 18.687 %) — p(stop avant cible) 0.008 [0.00 ; 0.02], R/R 0.103, perte reelle 18.687 % (gap inclus), EV 0.148 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.69 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 20.124 %) — p(stop avant cible) 0.008 [0.00 ; 0.02], R/R 0.096, perte reelle 20.124 % (gap inclus), EV 0.1356 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.12 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.562 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.089, perte reelle 21.562 % (gap inclus), EV 0.1469 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.56 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.999 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.084, perte reelle 22.999 % (gap inclus), EV 0.1517 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.00 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 249.2, ATR14 7.1643 (2.875 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 1.095 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.144 % | 248.8418 | 88.95 % | 92.89 % | 94.37 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.287 % | 248.4836 | 82.45 % | 88.35 % | 90.71 % | 93.37 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.431 % | 248.1254 | 74.95 % | 83.81 % | 86.96 % | 90.5 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.575 % | 247.7671 | 68.34 % | 78.87 % | 83.0 % | 87.33 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.719 % | 247.4089 | 63.21 % | 75.52 % | 79.74 % | 84.95 % | 90.55 % | 93.07 % |
| 0.35 ATR | 1.006 % | 246.6925 | 53.06 % | 69.1 % | 74.11 % | 80.99 % | 87.16 % | 91.16 % |
| 0.5 ATR | 1.437 % | 245.6179 | 38.07 % | 56.56 % | 64.43 % | 74.26 % | 82.79 % | 88.64 % |
| 0.75 ATR | 2.156 % | 243.8268 | 19.63 % | 36.82 % | 47.92 % | 59.31 % | 72.44 % | 82.31 % |
| 1.0 ATR | 2.875 % | 242.0357 | 10.26 % | 24.68 % | 34.68 % | 47.72 % | 63.18 % | 75.28 % |
| 1.25 ATR | 3.594 % | 240.2446 | 4.83 % | 15.0 % | 24.7 % | 38.32 % | 53.83 % | 68.34 % |
| 1.5 ATR | 4.312 % | 238.4536 | 2.37 % | 10.07 % | 18.08 % | 31.09 % | 46.57 % | 62.71 % |
| 2.0 ATR | 5.75 % | 234.8714 | 0.79 % | 4.74 % | 8.5 % | 17.62 % | 35.32 % | 52.86 % |
| 2.5 ATR | 7.187 % | 231.2893 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 25.17 % | 42.81 % |
| 3.0 ATR | 8.625 % | 227.7071 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 18.21 % | 35.28 % |
| 4.0 ATR | 11.5 % | 220.5429 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.55 % | 21.21 % |
| 6.0 ATR | 17.249 % | 206.2143 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

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
- **1 seance(s)** : plage utile 0.431–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.437 %, prix 245.619), p(touche) 38.07 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.156 %, prix 243.8272), p(touche) 36.82 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.875 %, prix 242.0355), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.594 %, prix 240.2437), p(touche) 38.32 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.57–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.75 %, prix 234.871), p(touche) 35.32 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.391–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.187 %, prix 231.29), p(touche) 42.81 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : €-0.068 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 33 % | T3 20 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.3 | bear 8.4 | side 72.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 498.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.203% → cible +1.06% / stop −1.5%, p_fill 21%, n_eff≈14.3) : P(cible|rempli) **56%** · **EV/risk +0.011** (×p_fill ; si rempli +0.08% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 59.3  _(momentum haussier)_
- **ADX** : 18.3  _(pas de tendance nette)_
- **MACD** : hist 1.395  _(pas de croisement recent)_
- **BB** : %B 0.81 · largeur 13.5%
- **ATR** : 7.16 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.094  _(accumulation)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 47.8  _(transition)_
- **MA** : MA20 239.2 · MA50 233.05 · MA200 232.6  _(prix > MA20)_
- **Dist MA** : MA20 +4.2% · MA50 +6.9% · MA200 +7.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (788456 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
