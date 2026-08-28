# SOI

**Generated** : 2026-08-28T21:45:21.710540+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €108.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €108.00 (+0.8% vs entrée) · entrée €107.13 · stop €100.80 · T1 €113.80 · R/R 1.05  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.079 _(réel 5 s)_ (GBM 0.158) · ¼-Kelly 0.02 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €106.25–€108.00 (mid €107.13)
- Spot actuel : €108.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €100.80 (stop swing_plan-based (-6.67%))
- Targets : T1 €113.80 · R/R 1.05 | T2 €120.48 · R/R 2.11 | T3 €127.15 · R/R 3.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €100.80


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.67 %)** : le gap seul le franchit 0.547 % des séances (7 fois sur 1280).
   - exécution **2.745 pt plus bas** dans le cas TYPIQUE (médiane), 16.279 au p90, **22.624 au pire**
   - perte réelle **14.154 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 6.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0409 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4196** [0.3479 ; 0.4939] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4058** [0.355 ; 0.4582] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.4288** [0.3774 ; 0.4814] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.2 pt), swing (31.6 pt), deep (30.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.47 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.46 % contre 7.70 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.22 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1201** (β de hausse 1.6206, asymétrie 0.6912) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut -0.02× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 95.3429 sur atr_grid (2.0 ATR, 11.72 %) — p(stop avant cible) 0.4143 [0.36 ; 0.47], R/R 1.116, perte reelle 21.456 % (gap inclus), CVaR 11.743 %, EV -2.9052 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.4 ATR (stop 5.503 %) — p(stop avant cible) 0.6414 [0.59 ; 0.69], R/R 2.143, perte reelle 11.172 % (gap inclus), EV -1.9503 % — **REFUSE**
      - refuse : p_stop_first 0.641, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.12 ATR du spot — compartiment <1, mesure a 45.2 % de casse (IC clusterise [0.423 ; 0.481] sur 1194 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 15.7 % x 23.94 % + P(rien) 20.2 % x 7.22 % ne couvrent pas P(stop) 64.1 % x 11.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.79 %) — p(stop avant cible) 0.5285 [0.48 ; 0.58], R/R 1.563, perte reelle 15.318 % (gap inclus), EV -2.3913 % — **REFUSE**
      - refuse : p_stop_first 0.528, borne haute 0.581 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.39 %) : P(cible) 18.3 % x 23.94 % + P(rien) 28.9 % x 4.62 % ne couvrent pas P(stop) 52.8 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.16 ATR (stop 27.577 %) — p(stop avant cible) 0.0493 [0.03 ; 0.08], R/R 0.817, perte reelle 29.294 % (gap inclus), EV 2.2639 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.58 % > budget 12.00 %
   - 🟢 support a 6.77 ATR (stop 42.854 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.559, perte reelle 42.854 % (gap inclus), EV 2.3543 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.85 % > budget 12.00 %
   - 🔴 grid_snapped a 0.4 ATR (stop 4.073 %) — p(stop avant cible) 0.7056 [0.66 ; 0.75], R/R 3.223, perte reelle 7.428 % (gap inclus), EV -0.6441 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.706, borne haute 0.752 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 13.6 % x 23.94 % + P(rien) 15.8 % x 8.49 % ne couvrent pas P(stop) 70.6 % x 7.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.325 %) — p(stop avant cible) 0.5872 [0.53 ; 0.64], R/R 1.563, perte reelle 15.318 % (gap inclus), EV -3.4398 % — **REFUSE**
      - refuse : p_stop_first 0.587, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.44 %) : P(cible) 17.3 % x 23.94 % + P(rien) 24.0 % x 5.91 % ne couvrent pas P(stop) 58.7 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.255 %) — p(stop avant cible) 0.4529 [0.40 ; 0.51], R/R 1.116, perte reelle 21.456 % (gap inclus), EV -3.681 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.68 %) : P(cible) 20.1 % x 23.94 % + P(rien) 34.6 % x 3.52 % ne couvrent pas P(stop) 45.3 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.72 %) — p(stop avant cible) 0.4143 [0.36 ; 0.47], R/R 1.116, perte reelle 21.456 % (gap inclus), EV -2.9052 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.91 %) : P(cible) 20.4 % x 23.94 % + P(rien) 38.2 % x 2.88 % ne couvrent pas P(stop) 41.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 13.185 %) — p(stop avant cible) 0.3491 [0.30 ; 0.40], R/R 1.116, perte reelle 21.456 % (gap inclus), EV -1.5165 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 21.6 % x 23.94 % + P(rien) 43.5 % x 1.85 % ne couvrent pas P(stop) 34.9 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 14.649 %) — p(stop avant cible) 0.3074 [0.26 ; 0.36], R/R 1.116, perte reelle 21.456 % (gap inclus), EV -0.8841 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 21.6 % x 23.94 % + P(rien) 47.7 % x 1.14 % ne couvrent pas P(stop) 30.7 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 16.114 %) — p(stop avant cible) 0.2465 [0.20 ; 0.29], R/R 1.116, perte reelle 21.456 % (gap inclus), EV 0.5425 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.13 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.579 %) — p(stop avant cible) 0.2026 [0.16 ; 0.25], R/R 0.997, perte reelle 24.006 % (gap inclus), EV 0.719 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.59 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.509 %) — p(stop avant cible) 0.1303 [0.10 ; 0.17], R/R 0.817, perte reelle 29.294 % (gap inclus), EV 1.1695 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.52 % > budget 12.00 %
   - 🟢 grid_snapped a 4.16 ATR (stop 26.147 %) — p(stop avant cible) 0.0556 [0.04 ; 0.08], R/R 0.817, perte reelle 29.294 % (gap inclus), EV 2.2196 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.15 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.299 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 0.817, perte reelle 29.299 % (gap inclus), EV 2.3814 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.30 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.229 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 0.743, perte reelle 32.229 % (gap inclus), EV 2.2844 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.23 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.159 %) — p(stop avant cible) 0.0265 [0.01 ; 0.05], R/R 0.681, perte reelle 35.159 % (gap inclus), EV 2.2569 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.16 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.089 %) — p(stop avant cible) 0.0115 [0.00 ; 0.03], R/R 0.628, perte reelle 38.089 % (gap inclus), EV 2.2981 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.09 % > budget 12.00 %
   - 🟢 grid_snapped a 6.77 ATR (stop 41.425 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.578, perte reelle 41.425 % (gap inclus), EV 2.3385 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.43 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.948 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.545, perte reelle 43.948 % (gap inclus), EV 2.3543 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.95 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.878 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.511, perte reelle 46.878 % (gap inclus), EV 2.3543 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.88 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 108.0, ATR14 6.3286 (5.86 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.36 ATR = 2.11 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.293 % | 107.6836 | 91.08 % | 94.11 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.586 % | 107.3671 | 84.9 % | 89.99 % | 92.04 % | 94.59 % | 96.24 % | 97.4 % |
| 0.15 ATR | 0.879 % | 107.0507 | 77.94 % | 85.08 % | 87.92 % | 91.14 % | 93.77 % | 95.3 % |
| 0.2 ATR | 1.172 % | 106.7343 | 69.51 % | 80.08 % | 83.99 % | 88.39 % | 91.59 % | 93.41 % |
| 0.25 ATR | 1.465 % | 106.4179 | 63.14 % | 76.35 % | 80.75 % | 86.71 % | 90.31 % | 92.81 % |
| 0.35 ATR | 2.051 % | 105.785 | 50.98 % | 67.81 % | 73.77 % | 81.59 % | 86.05 % | 90.21 % |
| 0.5 ATR | 2.93 % | 104.8357 | 36.08 % | 55.54 % | 63.06 % | 73.72 % | 81.4 % | 87.51 % |
| 0.75 ATR | 4.395 % | 103.2536 | 17.06 % | 35.62 % | 47.35 % | 59.25 % | 73.79 % | 81.42 % |
| 1.0 ATR | 5.86 % | 101.6714 | 8.33 % | 24.24 % | 34.38 % | 48.23 % | 65.58 % | 76.12 % |
| 1.25 ATR | 7.325 % | 100.0893 | 4.12 % | 15.8 % | 25.54 % | 37.99 % | 57.27 % | 70.43 % |
| 1.5 ATR | 8.79 % | 98.5071 | 2.35 % | 10.79 % | 18.76 % | 30.31 % | 49.36 % | 64.34 % |
| 2.0 ATR | 11.72 % | 95.3429 | 0.59 % | 4.71 % | 9.04 % | 18.41 % | 35.51 % | 54.05 % |
| 2.5 ATR | 14.649 % | 92.1786 | 0.29 % | 2.45 % | 4.81 % | 11.81 % | 24.63 % | 45.95 % |
| 3.0 ATR | 17.579 % | 89.0143 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 17.11 % | 37.96 % |
| 4.0 ATR | 23.439 % | 82.6857 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.79 % | 24.78 % |
| 6.0 ATR | 35.159 % | 70.0286 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.19 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.63 ATR | 0.81 ATR | 0.98 ATR | 1.13 ATR | 1.56 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.27 ATR | 1.45 ATR | 1.95 ATR | 2.48 ATR |
| **5 s.** | 0.48 ATR | 0.96 ATR | 1.08 ATR | 1.41 ATR | 1.72 ATR | 1.93 ATR | 2.69 ATR | 3.59 ATR |
| **10 s.** | 0.71 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.48 ATR | 2.81 ATR | 3.97 ATR | 5.79 ATR |
| **20 s.** | 1.05 ATR | 2.25 ATR | 2.56 ATR | 3.38 ATR | 3.98 ATR | 4.76 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.632–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.86 %, prix 101.6712), p(touche) 34.38 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.079–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.325 %, prix 100.089), p(touche) 37.99 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.657–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.559–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.158 | EV/share : €1.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 29 % | T3 18 %
- Kelly (position) : f* 0.081 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 68.8 | bear 25.0 | side 6.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 108.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.431% → cible +2.787% / stop −2.5%, p_fill 90%, n_eff≈36.5) : P(cible|rempli) **36%** · **EV/risk -0.081** (×p_fill ; si rempli -0.22% du capital)
  - **swing** (entrée dip −0.81% → cible +6.231% / stop −5.908%, p_fill 89%, n_eff≈35.9) : P(cible|rempli) **46%** · **EV/risk -0.079** (×p_fill ; si rempli -0.52% du capital)
  - **deep** (entrée dip −1.164% → cible +21.502% / stop −10.751%, p_fill 86%, n_eff≈36.5) : P(cible|rempli) **26%** · **EV/risk -0.235** (×p_fill ; si rempli -2.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→66% · +3.0%→51% · +5.0%→32% · +8.0%→10%
- Range intraday médian 7.81% (p90 14.11%) · excursion haute méd. +3.36% / basse méd. −3.33%
- Profil de vol intra : ouverture 4.855% vs midi 1.367% vs clôture 2.119% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑0%/↓2% ; spike-down 74% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.057)_ ; drift intra méd. -0.601% ; recovery-V 34%
- **σ réalisé intraday** 4.458% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 53% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 114.182 (VA 111.23–115.166 ; dernier close 110.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 48% · rebond 85% · **stop −7.73%** sous le fill (sous le bruit) · cible +3.22% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 40% (gap-down >1% 27% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −3.55%) · haut méd +0.96% · range méd 2.7%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −4.93%) · haut méd +1.28% · range méd 3.37%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −5.2%) · haut méd +1.51% · range méd 3.8%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.69%) · haut méd +1.82% · range méd 4.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 110.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 77% (126/159) · gap 35% · délai 0.1min · rebond 70% (89/126) (MFE +1.93%)
   - −1.0% : fill 30min 57% · séance 72% (114/159) · gap 27% · délai 0.2min · rebond 74% (84/114) (MFE +2.02%)
   - −1.5% : fill 30min 50% · séance 64% (106/159) · gap 23% · délai 0.2min · rebond 75% (79/106) (MFE +2.39%)
   - −2.0% : fill 30min 44% · séance 59% (95/159) · gap 20% · délai 0.4min · rebond 72% (73/95) (MFE +2.7%)
   - −3.0% : fill 30min 35% · séance 48% (79/159) · gap 10% · délai 1.2min · rebond 85% (68/79) (MFE +3.22%)
   - −4.0% : fill 30min 26% · séance 40% (64/159) · gap 6% · délai 5.9min · rebond 80% (54/64) (MFE +3.47%)
   - −5.0% : fill 30min 17% · séance 32% (48/159) · gap 2% · délai 26.8min · rebond 70% (38/48) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.85% (p90 −3.55%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.47%) → stop au-delà de −2.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.29%) → stop au-delà de −1.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1341 jambes) : jambe baissière méd −1.31% (p90 −3.17%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 97% (56/58) · rebond 66% (37/56)
      · −2.0% : fill 93% (53/58) · rebond 72% (41/53)
      · −3.0% : fill 85% (48/58) · rebond 82% (41/48)
      · −4.0% : fill 70% (39/58) · rebond 89% (36/39)
      · −5.0% : fill 56% (31/58) · rebond 77% (26/31)
   - **flat** (14 séances) :
      · −1.0% : fill 93% (11/14) · rebond 78% (9/11)
      · −2.0% : fill 73% (10/14) · rebond 79% (9/10)
      · −3.0% : fill 71% (9/14) · rebond 78% (8/9)
      · −4.0% : fill 57% (8/14) · rebond 56% (5/8)
      · −5.0% : fill 56% (7/14) · rebond 72% (6/7)
   - **gap-up** (87 séances) :
      · −1.0% : fill 53% (47/87) · rebond 82% (38/47)
      · −2.0% : fill 36% (32/87) · rebond 70% (23/32)
      · −3.0% : fill 21% (22/87) · rebond 96% (19/22)
      · −4.0% : fill 18% (17/87) · rebond 68% (13/17)
      · −5.0% : fill 13% (10/87) · rebond 48% (6/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 65% si les 15 1res min sont vertes (76 cas) · 32% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 76% si début vert vs 23% si rouge (base 49% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -2.29% (q20 -5.51%) → **SL/trailing à −5.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.33% / q75 +4.65% → **scale +2.33% / runner +4.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **23%** (continue à baisser 57%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.49%** (au-delà de la MAE q10 -7.49%), cible rebond +2.23% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.79% .. +6.15%] · haut q95 +7.6% · bas q05 -6.08%
   - 60min (n=160) : retour [-5.53% .. +6.71%] · haut q95 +7.95% · bas q05 -6.63%
   - 2h (n=160) : retour [-6.35% .. +6.38%] · haut q95 +10.42% · bas q05 -7.61%
   - 4h (n=160) : retour [-7.13% .. +8.48%] · haut q95 +12.15% · bas q05 -8.32%
   - 6h (n=160) : retour [-8.27% .. +9.55%] · haut q95 +12.53% · bas q05 -9.45%
   - session (n=160) : retour [-11.61% .. +11.83%] · haut q95 +14.36% · bas q05 -12.8%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 9% vs absente 4% (base 6%)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 38.9  _(momentum baissier)_
- **ADX** : 13.6  _(pas de tendance nette)_
- **MACD** : hist -1.596  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 31.1%
- **ATR** : 6.33 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 41.3  _(transition)_
- **MA** : MA20 117.39 · MA50 110.45 · MA200 78.75  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -2.2% · MA200 +37.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (924688 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
