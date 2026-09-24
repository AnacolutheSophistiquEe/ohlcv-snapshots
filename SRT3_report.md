# SRT3

**Generated** : 2026-09-24T00:04:36.104803+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €252.70  

> 🟡 **WAIT-FOR-DIP** — spot +5.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €252.70 (+5.5% vs entrée) · entrée €239.48 · stop €232.44 · T1 €245.17 · R/R 0.81  
> ↳ P(T1 av. stop) 62 % · EV/risk 0.023 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €238.34–€240.62 (mid €239.48)
- Spot actuel : €252.70 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : €232.44 (stop swing_plan-based (-8.02%))
- Targets : T1 €245.17 · R/R 0.81 | T2 €250.86 · R/R 1.62 | T3 €256.56 · R/R 2.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €232.44


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.02 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **1.637 pt plus bas** dans le cas TYPIQUE (médiane), 4.492 au p90, **6.185 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 8.02 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0081 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3693** [0.3 ; 0.4429] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4341** [0.3826 ; 0.4867] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.439** [0.3874 ; 0.4916] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (49.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.57 %** | vol 2.84 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.2 % si l'on extrapolait par √5 _(rapport 1.087 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0722** (β de hausse 1.1745, asymétrie 0.9129) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.27× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 222.6822 sur grid_snapped (3.97 ATR, 11.879 %) — p(stop avant cible) 0.0693 [0.05 ; 0.10], R/R 0.107, perte reelle 14.205 % (gap inclus), CVaR 11.881 %, EV -0.1448 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.176 %) — p(stop avant cible) 0.2793 [0.23 ; 0.33], R/R 0.199, perte reelle 7.669 % (gap inclus), EV -1.0485 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 71.8 % x 1.53 % + P(rien) 0.2 % x -1.13 % ne couvrent pas P(stop) 27.9 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.52 ATR (stop 11.489 %) — p(stop avant cible) 0.072 [0.05 ; 0.10], R/R 0.107, perte reelle 14.205 % (gap inclus), EV -0.1584 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 83.8 % x 1.53 % + P(rien) 9.0 % x -4.60 % ne couvrent pas P(stop) 7.2 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.97 ATR (stop 12.742 %) — p(stop avant cible) 0.0555 [0.04 ; 0.08], R/R 0.107, perte reelle 14.205 % (gap inclus), EV -0.0718 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 83.8 % x 1.53 % + P(rien) 10.7 % x -5.28 % ne couvrent pas P(stop) 5.5 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 9.02 ATR (stop 26.808 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.057, perte reelle 26.808 % (gap inclus), EV 0.1021 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.81 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.696 %) — p(stop avant cible) 0.636 [0.58 ; 0.69], R/R 0.965, perte reelle 1.581 % (gap inclus), EV -0.4501 % — **REFUSE**
      - refuse : p_stop_first 0.636, borne haute 0.685 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 36.4 % x 1.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 63.6 % x 1.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.392 %) — p(stop avant cible) 0.5349 [0.48 ; 0.59], R/R 0.583, perte reelle 2.619 % (gap inclus), EV -0.6912 % — **REFUSE**
      - refuse : p_stop_first 0.535, borne haute 0.587 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 46.5 % x 1.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 53.5 % x 2.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.088 %) — p(stop avant cible) 0.4504 [0.40 ; 0.50], R/R 0.345, perte reelle 4.426 % (gap inclus), EV -1.1548 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 55.0 % x 1.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 45.0 % x 4.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.784 %) — p(stop avant cible) 0.3687 [0.32 ; 0.42], R/R 0.242, perte reelle 6.31 % (gap inclus), EV -1.3631 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 63.1 % x 1.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 36.9 % x 6.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.48 %) — p(stop avant cible) 0.321 [0.27 ; 0.37], R/R 0.199, perte reelle 7.669 % (gap inclus), EV -1.4256 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.43 %) : P(cible) 67.9 % x 1.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 32.1 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 4.872 %) — p(stop avant cible) 0.2426 [0.20 ; 0.29], R/R 0.185, perte reelle 8.26 % (gap inclus), EV -0.8586 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 75.2 % x 1.53 % + P(rien) 0.5 % x -0.46 % ne couvrent pas P(stop) 24.3 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.568 %) — p(stop avant cible) 0.2129 [0.17 ; 0.26], R/R 0.185, perte reelle 8.26 % (gap inclus), EV -0.5803 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 77.7 % x 1.53 % + P(rien) 1.0 % x -0.70 % ne couvrent pas P(stop) 21.3 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.264 %) — p(stop avant cible) 0.1985 [0.16 ; 0.24], R/R 0.165, perte reelle 9.276 % (gap inclus), EV -0.6534 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 78.8 % x 1.53 % + P(rien) 1.4 % x -1.04 % ne couvrent pas P(stop) 19.9 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 6.961 %) — p(stop avant cible) 0.1828 [0.14 ; 0.23], R/R 0.165, perte reelle 9.276 % (gap inclus), EV -0.5068 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 80.0 % x 1.53 % + P(rien) 1.8 % x -1.76 % ne couvrent pas P(stop) 18.3 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.657 %) — p(stop avant cible) 0.1638 [0.13 ; 0.21], R/R 0.151, perte reelle 10.096 % (gap inclus), EV -0.4632 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 81.3 % x 1.53 % + P(rien) 2.3 % x -2.18 % ne couvrent pas P(stop) 16.4 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 8.353 %) — p(stop avant cible) 0.141 [0.11 ; 0.18], R/R 0.145, perte reelle 10.559 % (gap inclus), EV -0.3431 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 82.3 % x 1.53 % + P(rien) 3.6 % x -3.03 % ne couvrent pas P(stop) 14.1 % x 10.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.52 ATR (stop 10.626 %) — p(stop avant cible) 0.0839 [0.06 ; 0.12], R/R 0.107, perte reelle 14.205 % (gap inclus), EV -0.2817 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 83.5 % x 1.53 % + P(rien) 8.1 % x -4.52 % ne couvrent pas P(stop) 8.4 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.97 ATR (stop 11.879 %) — p(stop avant cible) 0.0693 [0.05 ; 0.10], R/R 0.107, perte reelle 14.205 % (gap inclus), EV -0.1448 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 83.8 % x 1.53 % + P(rien) 9.3 % x -4.74 % ne couvrent pas P(stop) 6.9 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 13.921 %) — p(stop avant cible) 0.0403 [0.02 ; 0.07], R/R 0.107, perte reelle 14.205 % (gap inclus), EV 0.0221 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.92 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 15.313 %) — p(stop avant cible) 0.0253 [0.01 ; 0.05], R/R 0.1, perte reelle 15.313 % (gap inclus), EV 0.0359 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.31 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.705 %) — p(stop avant cible) 0.0057 [0.00 ; 0.02], R/R 0.091, perte reelle 16.705 % (gap inclus), EV 0.1122 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.70 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 18.097 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.084, perte reelle 18.097 % (gap inclus), EV 0.106 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.10 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 19.49 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 0.078, perte reelle 19.49 % (gap inclus), EV 0.0988 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 20.882 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 0.073, perte reelle 20.882 % (gap inclus), EV 0.0914 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.88 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.274 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.069, perte reelle 22.274 % (gap inclus), EV 0.0952 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.27 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 252.7, ATR14 7.0357 (2.784 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.38 ATR = 1.058 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.139 % | 252.3482 | 89.25 % | 92.99 % | 94.37 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.278 % | 251.9964 | 82.54 % | 88.45 % | 90.71 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.418 % | 251.6446 | 74.85 % | 83.61 % | 86.66 % | 90.4 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.557 % | 251.2929 | 68.24 % | 78.68 % | 82.71 % | 87.23 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.696 % | 250.9411 | 62.92 % | 75.32 % | 79.45 % | 84.85 % | 90.45 % | 93.07 % |
| 0.35 ATR | 0.974 % | 250.2375 | 52.96 % | 69.1 % | 73.81 % | 80.69 % | 87.06 % | 90.95 % |
| 0.5 ATR | 1.392 % | 249.1821 | 38.17 % | 56.56 % | 64.23 % | 73.86 % | 82.59 % | 88.24 % |
| 0.75 ATR | 2.088 % | 247.4232 | 19.13 % | 36.62 % | 47.63 % | 59.11 % | 72.44 % | 81.71 % |
| 1.0 ATR | 2.784 % | 245.6643 | 9.76 % | 24.38 % | 34.58 % | 47.72 % | 63.18 % | 74.67 % |
| 1.25 ATR | 3.48 % | 243.9054 | 4.73 % | 14.91 % | 24.6 % | 38.42 % | 53.53 % | 67.54 % |
| 1.5 ATR | 4.176 % | 242.1464 | 2.27 % | 9.87 % | 17.69 % | 30.89 % | 46.27 % | 61.71 % |
| 2.0 ATR | 5.568 % | 238.6286 | 0.69 % | 4.54 % | 8.2 % | 17.23 % | 34.83 % | 51.76 % |
| 2.5 ATR | 6.961 % | 235.1107 | 0.3 % | 1.97 % | 4.74 % | 10.69 % | 24.48 % | 41.71 % |
| 3.0 ATR | 8.353 % | 231.5929 | 0.2 % | 1.48 % | 2.96 % | 6.34 % | 17.51 % | 34.17 % |
| 4.0 ATR | 11.137 % | 224.5571 | 0.0 % | 0.69 % | 1.78 % | 3.56 % | 8.96 % | 20.2 % |
| 6.0 ATR | 16.705 % | 210.4857 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.82 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.46 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.72 ATR | 1.90 ATR | 2.58 ATR | 3.48 ATR |
| **10 s.** | 0.69 ATR | 1.37 ATR | 1.56 ATR | 2.09 ATR | 2.48 ATR | 2.82 ATR | 3.88 ATR | 5.15 ATR |
| **20 s.** | 0.99 ATR | 2.09 ATR | 2.34 ATR | 3.08 ATR | 3.66 ATR | 4.03 ATR | 5.55 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.392 %, prix 249.1824), p(touche) 38.17 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.088 %, prix 247.4236), p(touche) 36.62 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.8–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.784 %, prix 245.6648), p(touche) 34.58 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.073–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.48 %, prix 243.906), p(touche) 38.42 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.556–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.568 %, prix 238.6297), p(touche) 34.83 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.336–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.961 %, prix 235.1096), p(touche) 41.71 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.007 | EV/share : €-0.052 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 33 % | T3 19 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.3 | bear 8.7 | side 72.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 505.0 (= 2 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.376% → cible +1.063% / stop −1.5%, p_fill 15%, n_eff≈12.3) : P(cible|rempli) **60%** · **EV/risk +0.021** (×p_fill ; si rempli +0.20% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=6))
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 56.9  _(momentum haussier)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist 1.388  _(bullish_recent)_
- **BB** : %B 0.81 · largeur 13.0%
- **ATR** : 7.04 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.084  _(accumulation)_
- **Vol ratio** : 0.26  _(volume atone)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 242.98 · MA50 236.55 · MA200 232.88  _(prix > MA20)_
- **Dist MA** : MA20 +4.0% · MA50 +6.8% · MA200 +8.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (848450 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
