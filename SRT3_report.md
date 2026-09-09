# SRT3

**Generated** : 2026-09-09T00:04:59.949142+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €238.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €238.40 (+1.1% vs entrée) · entrée €235.85 · stop €232.31 · T1 €238.59 · R/R 0.77  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.005 _(réel 5 s)_ (GBM 0.062) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €235.30–€236.40 (mid €235.85)
- Spot actuel : €238.40 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : €232.31 (stop swing_plan-based (-5.58%))
- Targets : T1 €238.59 · R/R 0.77 | T2 €241.34 · R/R 1.55 | T3 €244.08 · R/R 2.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €232.31


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.58 %)** : le gap seul le franchit 0.785 % des séances (10 fois sur 1274).
   - exécution **2.23 pt plus bas** dans le cas TYPIQUE (médiane), 4.815 au p90, **8.625 au pire**
   - perte réelle **8.26 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 5.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.021 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.403** [0.332 ; 0.4772] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4157** [0.3646 ; 0.4682] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4091** [0.3582 ; 0.4615] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.7 pt), swing (41.5 pt), deep (44.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.11 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0642** (β de hausse 1.1837, asymétrie 0.899) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.273× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 211.5 sur atr_grid (3.5 ATR, 11.284 %) — p(stop avant cible) 0.1404 [0.11 ; 0.18], R/R 0.371, perte reelle 14.205 % (gap inclus), CVaR 11.286 %, EV -0.0233 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.836 %) — p(stop avant cible) 0.4657 [0.41 ; 0.52], R/R 0.637, perte reelle 8.26 % (gap inclus), EV -1.5667 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 43.8 % x 5.26 % + P(rien) 9.6 % x -0.27 % ne couvrent pas P(stop) 46.6 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.43 ATR (stop 6.654 %) — p(stop avant cible) 0.3196 [0.27 ; 0.37], R/R 0.567, perte reelle 9.276 % (gap inclus), EV -0.3955 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 51.1 % x 5.26 % + P(rien) 16.9 % x -0.72 % ne couvrent pas P(stop) 32.0 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.4 ATR (stop 22.674 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.232, perte reelle 22.674 % (gap inclus), EV 0.6314 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.67 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.806 %) — p(stop avant cible) 0.8494 [0.81 ; 0.88], R/R 3.032, perte reelle 1.736 % (gap inclus), EV -0.682 % — **REFUSE**
      - refuse : p_stop_first 0.849, borne haute 0.884 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 15.1 % x 5.26 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 84.9 % x 1.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.612 %) — p(stop avant cible) 0.7797 [0.73 ; 0.82], R/R 1.656, perte reelle 3.178 % (gap inclus), EV -1.3296 % — **REFUSE**
      - refuse : p_stop_first 0.780, borne haute 0.821 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.33 %) : P(cible) 21.8 % x 5.26 % + P(rien) 0.2 % x 0.40 % ne couvrent pas P(stop) 78.0 % x 3.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.418 %) — p(stop avant cible) 0.6893 [0.64 ; 0.74], R/R 1.027, perte reelle 5.125 % (gap inclus), EV -1.9451 % — **REFUSE**
      - refuse : p_stop_first 0.689, borne haute 0.736 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 30.0 % x 5.26 % + P(rien) 1.1 % x 0.94 % ne couvrent pas P(stop) 68.9 % x 5.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.224 %) — p(stop avant cible) 0.5989 [0.55 ; 0.65], R/R 0.748, perte reelle 7.038 % (gap inclus), EV -2.2546 % — **REFUSE**
      - refuse : p_stop_first 0.599, borne haute 0.650 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 36.8 % x 5.26 % + P(rien) 3.3 % x 0.73 % ne couvrent pas P(stop) 59.9 % x 7.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.43 ATR (stop 5.565 %) — p(stop avant cible) 0.382 [0.33 ; 0.43], R/R 0.637, perte reelle 8.26 % (gap inclus), EV -0.6382 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 49.2 % x 5.26 % + P(rien) 12.6 % x -0.58 % ne couvrent pas P(stop) 38.2 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.254 %) — p(stop avant cible) 0.29 [0.24 ; 0.34], R/R 0.546, perte reelle 9.643 % (gap inclus), EV -0.2449 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 52.0 % x 5.26 % + P(rien) 18.9 % x -0.99 % ne couvrent pas P(stop) 29.0 % x 9.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.06 %) — p(stop avant cible) 0.2518 [0.21 ; 0.30], R/R 0.521, perte reelle 10.096 % (gap inclus), EV -0.1523 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 52.2 % x 5.26 % + P(rien) 22.6 % x -1.59 % ne couvrent pas P(stop) 25.2 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.866 %) — p(stop avant cible) 0.2177 [0.18 ; 0.26], R/R 0.467, perte reelle 11.278 % (gap inclus), EV -0.1914 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 52.6 % x 5.26 % + P(rien) 25.7 % x -1.96 % ne couvrent pas P(stop) 21.8 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 9.672 %) — p(stop avant cible) 0.1847 [0.15 ; 0.23], R/R 0.435, perte reelle 12.088 % (gap inclus), EV -0.024 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 53.1 % x 5.26 % + P(rien) 28.4 % x -2.06 % ne couvrent pas P(stop) 18.5 % x 12.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.284 %) — p(stop avant cible) 0.1404 [0.11 ; 0.18], R/R 0.371, perte reelle 14.205 % (gap inclus), EV -0.0233 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 53.2 % x 5.26 % + P(rien) 32.8 % x -2.53 % ne couvrent pas P(stop) 14.0 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.895 %) — p(stop avant cible) 0.0888 [0.06 ; 0.12], R/R 0.371, perte reelle 14.205 % (gap inclus), EV 0.3278 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.90 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.507 %) — p(stop avant cible) 0.0538 [0.03 ; 0.08], R/R 0.363, perte reelle 14.507 % (gap inclus), EV 0.4827 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.51 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.119 %) — p(stop avant cible) 0.0227 [0.01 ; 0.04], R/R 0.327, perte reelle 16.119 % (gap inclus), EV 0.5783 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.12 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.731 %) — p(stop avant cible) 0.0143 [0.01 ; 0.03], R/R 0.297, perte reelle 17.731 % (gap inclus), EV 0.6139 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.73 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.343 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 0.272, perte reelle 19.343 % (gap inclus), EV 0.6022 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.34 % > budget 12.00 %
   - 🟢 grid_snapped a 6.4 ATR (stop 21.585 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 0.244, perte reelle 21.585 % (gap inclus), EV 0.6253 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.59 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.179 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.218, perte reelle 24.179 % (gap inclus), EV 0.6458 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.18 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 25.791 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.204, perte reelle 25.791 % (gap inclus), EV 0.6479 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.79 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 238.4, ATR14 7.6857 (3.224 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.383 ATR = 1.235 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.161 % | 238.0157 | 89.05 % | 92.99 % | 94.37 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.322 % | 237.6314 | 82.54 % | 88.45 % | 90.71 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.484 % | 237.2471 | 75.15 % | 84.01 % | 86.96 % | 90.59 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.645 % | 236.8629 | 68.54 % | 79.07 % | 83.0 % | 87.43 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.806 % | 236.4786 | 63.31 % | 75.72 % | 79.74 % | 85.05 % | 90.45 % | 93.07 % |
| 0.35 ATR | 1.128 % | 235.71 | 53.25 % | 69.4 % | 74.11 % | 80.89 % | 87.06 % | 90.95 % |
| 0.5 ATR | 1.612 % | 234.5571 | 38.46 % | 56.86 % | 64.53 % | 74.06 % | 82.59 % | 88.34 % |
| 0.75 ATR | 2.418 % | 232.6357 | 19.72 % | 37.02 % | 48.12 % | 59.31 % | 72.24 % | 81.81 % |
| 1.0 ATR | 3.224 % | 230.7143 | 10.26 % | 24.98 % | 35.08 % | 47.92 % | 62.89 % | 74.77 % |
| 1.25 ATR | 4.03 % | 228.7929 | 4.83 % | 15.2 % | 25.0 % | 38.51 % | 53.33 % | 67.74 % |
| 1.5 ATR | 4.836 % | 226.8714 | 2.37 % | 10.17 % | 18.18 % | 31.19 % | 46.07 % | 62.11 % |
| 2.0 ATR | 6.448 % | 223.0286 | 0.79 % | 4.74 % | 8.5 % | 17.72 % | 34.83 % | 52.26 % |
| 2.5 ATR | 8.06 % | 219.1857 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 24.68 % | 42.21 % |
| 3.0 ATR | 9.672 % | 215.3428 | 0.2 % | 1.68 % | 3.16 % | 6.73 % | 17.71 % | 34.67 % |
| 4.0 ATR | 12.895 % | 207.6571 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.35 % | 20.6 % |
| 6.0 ATR | 19.343 % | 192.2857 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.24 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.59 ATR | 0.65 ATR | 0.83 ATR | 1.00 ATR | 1.13 ATR | 1.52 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.05 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.73 ATR | 1.92 ATR | 2.62 ATR | 3.62 ATR |
| **10 s.** | 0.68 ATR | 1.36 ATR | 1.55 ATR | 2.09 ATR | 2.48 ATR | 2.84 ATR | 3.92 ATR | 5.21 ATR |
| **20 s.** | 0.99 ATR | 2.11 ATR | 2.36 ATR | 3.12 ATR | 3.69 ATR | 4.09 ATR | 5.59 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.434–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.612 %, prix 234.557), p(touche) 38.46 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.649–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.418 %, prix 232.6355), p(touche) 37.02 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.81–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.224 %, prix 230.714), p(touche) 35.08 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.078–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.03 %, prix 228.7925), p(touche) 38.51 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.548–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.448 %, prix 223.028), p(touche) 34.83 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.361–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.06 %, prix 219.185), p(touche) 42.21 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.062 | EV/share : €0.219 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 63 % | T2 34 % | T3 16 %
- Kelly (position) : f* 0.135 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.3 | bear 5.8 | side 77.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 238.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.066% → cible +1.162% / stop −1.5%, p_fill 56%, n_eff≈23.0) : P(cible|rempli) **36%** · **EV/risk -0.005** (×p_fill ; si rempli -0.01% du capital)
  - **swing** (entrée dip −2.356% → cible +2.599% / stop −3.301%, p_fill 33%, n_eff≈15.9) : P(cible|rempli) **72%** · **EV/risk +0.081** (×p_fill ; si rempli +0.80% du capital)
  - **deep** (entrée dip −3.634% → cible +3.676% / stop −5.018%, p_fill 28%, n_eff≈14.7) : P(cible|rempli) **68%** · **EV/risk +0.047** (×p_fill ; si rempli +0.84% du capital)
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

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.1  _(neutre)_
- **ADX** : 16.6  _(pas de tendance nette)_
- **MACD** : hist -1.506  _(bearish_recent)_
- **BB** : %B 0.38 · largeur 11.5%
- **ATR** : 7.69 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.065  _(distribution)_
- **Vol ratio** : 0.32  _(volume atone)_
- **Choppiness** : 54.9  _(transition)_
- **MA** : MA20 241.77 · MA50 235.18 · MA200 233.06  _(prix < MA20)_
- **Dist MA** : MA20 -1.4% · MA50 +1.4% · MA200 +2.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (762281 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
