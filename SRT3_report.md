# SRT3

**Generated** : 2026-09-09T21:39:43.732489+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €236.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €236.80 (+2.0% vs entrée) · entrée €232.07 · stop €224.47 · T1 €237.82 · R/R 0.76  
> ↳ P(T1 av. stop) 87 % _(réel 5 s)_ · EV/risk 0.236 _(réel 5 s)_ (GBM -0.017) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €230.93–€233.22 (mid €232.07)
- Spot actuel : €236.80 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €224.47 (stop swing_plan-based (-5.2%))
- Targets : T1 €237.82 · R/R 0.76 | T2 €243.56 · R/R 1.51 | T3 €249.30 · R/R 2.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €224.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.2 %)** : le gap seul le franchit 0.786 % des séances (10 fois sur 1273).
   - exécution **2.61 pt plus bas** dans le cas TYPIQUE (médiane), 5.195 au p90, **9.005 au pire**
   - perte réelle **8.26 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 5.2 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.024 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.625 % | p01 -3.241 % | pire -14.205 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3833** [0.3133 ; 0.4572] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.4119** [0.3609 ; 0.4643] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.4042** [0.3535 ; 0.4565] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.3 pt), swing (28.8 pt), deep (38.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.11 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.26 % si l'on extrapolait par √5 _(rapport 1.08 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0646** (β de hausse 1.1823, asymétrie 0.9005) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.258× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 214.0 sur atr_grid (3.0 ATR, 9.628 %) — p(stop avant cible) 0.1857 [0.15 ; 0.23], R/R 0.468, perte reelle 11.278 % (gap inclus), CVaR 9.632 %, EV 0.1221 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.814 %) — p(stop avant cible) 0.4661 [0.41 ; 0.52], R/R 0.664, perte reelle 7.948 % (gap inclus), EV -1.4202 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 43.8 % x 5.28 % + P(rien) 9.6 % x -0.27 % ne couvrent pas P(stop) 46.6 % x 7.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.23 ATR (stop 5.997 %) — p(stop avant cible) 0.3522 [0.30 ; 0.40], R/R 0.569, perte reelle 9.276 % (gap inclus), EV -0.7234 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 50.1 % x 5.28 % + P(rien) 14.7 % x -0.67 % ne couvrent pas P(stop) 35.2 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.26 ATR (stop 22.129 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.239, perte reelle 22.129 % (gap inclus), EV 0.6392 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.13 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.802 %) — p(stop avant cible) 0.8499 [0.81 ; 0.88], R/R 3.041, perte reelle 1.736 % (gap inclus), EV -0.683 % — **REFUSE**
      - refuse : p_stop_first 0.850, borne haute 0.885 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 15.0 % x 5.28 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 85.0 % x 1.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.605 %) — p(stop avant cible) 0.7801 [0.73 ; 0.82], R/R 1.685, perte reelle 3.133 % (gap inclus), EV -1.2949 % — **REFUSE**
      - refuse : p_stop_first 0.780, borne haute 0.821 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 21.8 % x 5.28 % + P(rien) 0.2 % x 0.40 % ne couvrent pas P(stop) 78.0 % x 3.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.407 %) — p(stop avant cible) 0.6898 [0.64 ; 0.74], R/R 1.03, perte reelle 5.125 % (gap inclus), EV -1.9449 % — **REFUSE**
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 29.9 % x 5.28 % + P(rien) 1.1 % x 0.94 % ne couvrent pas P(stop) 69.0 % x 5.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.419 %) — p(stop avant cible) 0.326 [0.28 ; 0.38], R/R 0.569, perte reelle 9.276 % (gap inclus), EV -0.471 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 50.7 % x 5.28 % + P(rien) 16.7 % x -0.73 % ne couvrent pas P(stop) 32.6 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.221 %) — p(stop avant cible) 0.2925 [0.25 ; 0.34], R/R 0.547, perte reelle 9.643 % (gap inclus), EV -0.2574 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 51.9 % x 5.28 % + P(rien) 18.8 % x -0.95 % ne couvrent pas P(stop) 29.2 % x 9.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.024 %) — p(stop avant cible) 0.2532 [0.21 ; 0.30], R/R 0.523, perte reelle 10.096 % (gap inclus), EV -0.1591 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 52.1 % x 5.28 % + P(rien) 22.6 % x -1.57 % ne couvrent pas P(stop) 25.3 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.826 %) — p(stop avant cible) 0.2177 [0.18 ; 0.26], R/R 0.468, perte reelle 11.278 % (gap inclus), EV -0.1866 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 52.5 % x 5.28 % + P(rien) 25.8 % x -1.95 % ne couvrent pas P(stop) 21.8 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 9.628 %) — p(stop avant cible) 0.1857 [0.15 ; 0.23], R/R 0.468, perte reelle 11.278 % (gap inclus), EV 0.1221 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.233 %) — p(stop avant cible) 0.1404 [0.11 ; 0.18], R/R 0.372, perte reelle 14.205 % (gap inclus), EV -0.0182 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 53.1 % x 5.28 % + P(rien) 32.9 % x -2.51 % ne couvrent pas P(stop) 14.0 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.838 %) — p(stop avant cible) 0.0931 [0.07 ; 0.13], R/R 0.372, perte reelle 14.205 % (gap inclus), EV 0.2967 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.443 %) — p(stop avant cible) 0.0542 [0.03 ; 0.08], R/R 0.366, perte reelle 14.443 % (gap inclus), EV 0.4907 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.44 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.047 %) — p(stop avant cible) 0.0227 [0.01 ; 0.04], R/R 0.329, perte reelle 16.047 % (gap inclus), EV 0.5852 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.652 %) — p(stop avant cible) 0.0143 [0.01 ; 0.03], R/R 0.299, perte reelle 17.652 % (gap inclus), EV 0.6198 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.65 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.257 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 0.274, perte reelle 19.257 % (gap inclus), EV 0.6088 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.26 % > budget 12.00 %
   - 🟢 grid_snapped a 6.26 ATR (stop 21.044 %) — p(stop avant cible) 0.0097 [0.00 ; 0.02], R/R 0.251, perte reelle 21.044 % (gap inclus), EV 0.6057 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.04 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.071 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.219, perte reelle 24.071 % (gap inclus), EV 0.6507 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.07 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 25.676 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.206, perte reelle 25.676 % (gap inclus), EV 0.6527 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.68 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 236.8, ATR14 7.6 (3.209 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 1.223 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.16 % | 236.42 | 89.04 % | 92.98 % | 94.36 % | 96.13 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.321 % | 236.04 | 82.43 % | 88.44 % | 90.7 % | 93.46 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.481 % | 235.66 | 75.02 % | 83.99 % | 86.94 % | 90.58 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.642 % | 235.28 | 68.41 % | 79.05 % | 82.99 % | 87.41 % | 92.23 % | 94.37 % |
| 0.25 ATR | 0.802 % | 234.9 | 63.18 % | 75.69 % | 79.72 % | 85.03 % | 90.44 % | 93.06 % |
| 0.35 ATR | 1.123 % | 234.14 | 53.11 % | 69.37 % | 74.09 % | 80.87 % | 87.05 % | 90.95 % |
| 0.5 ATR | 1.605 % | 233.0 | 38.3 % | 56.82 % | 64.49 % | 74.03 % | 82.57 % | 88.33 % |
| 0.75 ATR | 2.407 % | 231.1 | 19.64 % | 36.96 % | 48.07 % | 59.27 % | 72.21 % | 81.79 % |
| 1.0 ATR | 3.209 % | 229.2 | 10.17 % | 24.9 % | 35.01 % | 47.87 % | 62.85 % | 74.75 % |
| 1.25 ATR | 4.012 % | 227.3 | 4.84 % | 15.22 % | 24.93 % | 38.45 % | 53.29 % | 67.71 % |
| 1.5 ATR | 4.814 % | 225.4 | 2.37 % | 10.08 % | 18.1 % | 31.12 % | 45.92 % | 62.07 % |
| 2.0 ATR | 6.419 % | 221.6 | 0.79 % | 4.74 % | 8.51 % | 17.64 % | 34.76 % | 52.21 % |
| 2.5 ATR | 8.024 % | 217.8 | 0.3 % | 2.17 % | 5.04 % | 11.0 % | 24.6 % | 42.15 % |
| 3.0 ATR | 9.628 % | 214.0 | 0.2 % | 1.68 % | 3.17 % | 6.64 % | 17.63 % | 34.61 % |
| 4.0 ATR | 12.838 % | 206.4 | 0.0 % | 0.69 % | 1.88 % | 3.87 % | 9.26 % | 20.52 % |
| 6.0 ATR | 19.257 % | 191.2 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.14 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.59 ATR | 0.65 ATR | 0.83 ATR | 1.00 ATR | 1.13 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.05 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.73 ATR | 1.91 ATR | 2.62 ATR | 3.59 ATR |
| **10 s.** | 0.68 ATR | 1.36 ATR | 1.54 ATR | 2.09 ATR | 2.48 ATR | 2.83 ATR | 3.91 ATR | 5.19 ATR |
| **20 s.** | 0.99 ATR | 2.11 ATR | 2.36 ATR | 3.11 ATR | 3.68 ATR | 4.08 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.605 %, prix 232.9994), p(touche) 38.3 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.649–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.407 %, prix 231.1002), p(touche) 36.96 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.809–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.209 %, prix 229.2011), p(touche) 35.01 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.076–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.012 %, prix 227.2996), p(touche) 38.45 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.541–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.419 %, prix 221.5998), p(touche) 34.76 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.358–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.024 %, prix 217.7992), p(touche) 42.15 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : €-0.132 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 31 % | T3 18 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 25.1 | bear 8.0 | side 66.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 237.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.904% → cible +1.106% / stop −1.5%, p_fill 62%, n_eff≈25.0) : P(cible|rempli) **49%** · **EV/risk +0.013** (×p_fill ; si rempli +0.03% du capital)
  - **swing** (entrée dip −1.99% → cible +2.474% / stop −3.275%, p_fill 46%, n_eff≈20.0) : P(cible|rempli) **87%** · **EV/risk +0.236** (×p_fill ; si rempli +1.68% du capital)
  - **deep** (entrée dip −3.086% → cible +3.499% / stop −4.967%, p_fill 34%, n_eff≈17.7) : P(cible|rempli) **74%** · **EV/risk +0.081** (×p_fill ; si rempli +1.18% du capital)
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
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 52.0  _(neutre)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist -1.422  _(bearish_recent)_
- **BB** : %B 0.31 · largeur 11.1%
- **ATR** : 7.6 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.015  _(neutre)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 57.7  _(transition)_
- **MA** : MA20 241.95 · MA50 235.25 · MA200 233.08  _(prix < MA20)_
- **Dist MA** : MA20 -2.1% · MA50 +0.7% · MA200 +1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (757958 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
