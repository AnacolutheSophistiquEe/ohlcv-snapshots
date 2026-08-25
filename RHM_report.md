# RHM

**Generated** : 2026-08-25T18:05:29.727513+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1128.60  

> 🟡 **WAIT-FOR-DIP** — spot +4.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1128.60 (+4.5% vs entrée) · entrée €1079.58 · stop €1057.98 · T1 €1093.55 · R/R 0.65  
> ↳ P(T1 av. stop) 65 % · EV/risk 0.341 · ¼-Kelly 0.031 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1076.78–€1082.37 (mid €1079.58)
- Spot actuel : €1128.60 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : €1057.98 (stop swing_plan-based (-13.84%))
- Targets : T1 €1093.55 · R/R 0.65 | T2 €1107.53 · R/R 1.29 | T3 €1121.51 · R/R 1.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1057.98


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (13.84 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **8.589 pt plus bas** dans le cas TYPIQUE (médiane), 8.589 au p90, **8.589 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 13.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0067 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0854** [0.0506 ; 0.1339] _(largeur 8.3 pt, n_eff 173.1)_
   - swing : **0.4052** [0.3544 ; 0.4576] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.5107** [0.4581 ; 0.5631] _(largeur 10.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.06 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 2.06 % contre 3.36 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.6 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.846 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5007** (β de hausse 0.5891, asymétrie 0.85) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.194× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 1044.075 sur atr_grid (1.75 ATR, 7.489 %) — p(stop avant cible) 0.4042 [0.35 ; 0.46], R/R 2.357, perte reelle 15.141 % (gap inclus), CVaR 7.501 %, EV -3.0322 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.37 ATR (stop 3.486 %) — p(stop avant cible) 0.6928 [0.64 ; 0.74], R/R 6.309, perte reelle 5.656 % (gap inclus), EV -1.2163 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.693, borne haute 0.740 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.1 % x 35.69 % + P(rien) 30.6 % x 8.73 % ne couvrent pas P(stop) 69.3 % x 5.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 6.419 %) — p(stop avant cible) 0.4798 [0.43 ; 0.53], R/R 2.357, perte reelle 15.141 % (gap inclus), EV -4.1244 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.12 %) : P(cible) 0.2 % x 35.69 % + P(rien) 51.8 % x 5.91 % ne couvrent pas P(stop) 48.0 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.14 ATR (stop 19.625 %) — p(stop avant cible) 0.0597 [0.04 ; 0.09], R/R 1.591, perte reelle 22.429 % (gap inclus), EV -0.5378 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.2 % x 35.69 % + P(rien) 93.8 % x 0.77 % ne couvrent pas P(stop) 6.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.489 %) — p(stop avant cible) 0.4042 [0.35 ; 0.46], R/R 2.357, perte reelle 15.141 % (gap inclus), EV -3.0322 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.03 %) : P(cible) 0.2 % x 35.69 % + P(rien) 59.4 % x 5.07 % ne couvrent pas P(stop) 40.4 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.629 %) — p(stop avant cible) 0.323 [0.28 ; 0.37], R/R 1.591, perte reelle 22.429 % (gap inclus), EV -4.3162 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.32 %) : P(cible) 0.2 % x 35.69 % + P(rien) 67.5 % x 4.22 % ne couvrent pas P(stop) 32.3 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.699 %) — p(stop avant cible) 0.2615 [0.22 ; 0.31], R/R 1.591, perte reelle 22.429 % (gap inclus), EV -3.2191 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.22 %) : P(cible) 0.2 % x 35.69 % + P(rien) 73.6 % x 3.49 % ne couvrent pas P(stop) 26.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.839 %) — p(stop avant cible) 0.1952 [0.16 ; 0.24], R/R 1.591, perte reelle 22.429 % (gap inclus), EV -2.1652 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.17 %) : P(cible) 0.2 % x 35.69 % + P(rien) 80.3 % x 2.66 % ne couvrent pas P(stop) 19.5 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 14.979 %) — p(stop avant cible) 0.1398 [0.11 ; 0.18], R/R 1.591, perte reelle 22.429 % (gap inclus), EV -1.3712 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 0.2 % x 35.69 % + P(rien) 85.8 % x 1.96 % ne couvrent pas P(stop) 14.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 21.398 %) — p(stop avant cible) 0.038 [0.02 ; 0.06], R/R 1.591, perte reelle 22.429 % (gap inclus), EV -0.3307 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.2 % x 35.69 % + P(rien) 96.0 % x 0.46 % ne couvrent pas P(stop) 3.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 23.538 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 1.516, perte reelle 23.538 % (gap inclus), EV -0.1201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.2 % x 35.69 % + P(rien) 98.6 % x 0.08 % ne couvrent pas P(stop) 1.2 % x 23.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 25.678 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 1.39, perte reelle 25.678 % (gap inclus), EV -0.1331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.2 % x 35.69 % + P(rien) 99.1 % x -0.03 % ne couvrent pas P(stop) 0.7 % x 25.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 27.818 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.283, perte reelle 27.818 % (gap inclus), EV -0.085 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.2 % x 35.69 % + P(rien) 99.2 % x -0.01 % ne couvrent pas P(stop) 0.5 % x 27.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 29.957 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.191, perte reelle 29.957 % (gap inclus), EV -0.0261 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.2 % x 35.69 % + P(rien) 99.5 % x -0.01 % ne couvrent pas P(stop) 0.3 % x 29.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 32.097 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.112, perte reelle 32.097 % (gap inclus), EV 0.0851 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.10 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 34.237 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.042, perte reelle 34.237 % (gap inclus), EV 0.0851 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.24 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1128.6, ATR14 48.3 (4.28 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 5s | p(touche) 20s |
|---|---|---|---|---|---|
| 0.05 ATR | 0.214 % | 1126.185 | 89.25 % | 94.55 % | 97.69 % |
| 0.1 ATR | 0.428 % | 1123.77 | 83.23 % | 91.39 % | 96.28 % |
| 0.15 ATR | 0.642 % | 1121.355 | 76.13 % | 88.22 % | 94.77 % |
| 0.2 ATR | 0.856 % | 1118.94 | 69.63 % | 85.15 % | 93.27 % |
| 0.25 ATR | 1.07 % | 1116.525 | 62.43 % | 80.99 % | 91.46 % |
| 0.35 ATR | 1.498 % | 1111.695 | 53.94 % | 76.63 % | 89.35 % |
| 0.5 ATR | 2.14 % | 1104.45 | 40.34 % | 68.81 % | 83.72 % |
| 0.75 ATR | 3.21 % | 1092.375 | 23.67 % | 57.23 % | 77.09 % |
| 1.0 ATR | 4.28 % | 1080.3 | 13.02 % | 48.12 % | 70.55 % |
| 1.25 ATR | 5.35 % | 1068.225 | 7.5 % | 38.81 % | 64.22 % |
| 1.5 ATR | 6.419 % | 1056.15 | 3.94 % | 31.49 % | 56.88 % |
| 2.0 ATR | 8.559 % | 1032.0 | 1.78 % | 20.79 % | 47.14 % |
| 2.5 ATR | 10.699 % | 1007.85 | 0.49 % | 12.77 % | 37.89 % |
| 3.0 ATR | 12.839 % | 983.7 | 0.1 % | 7.72 % | 31.26 % |
| 4.0 ATR | 17.119 % | 935.4 | 0.0 % | 3.27 % | 20.1 % |
| 6.0 ATR | 25.678 % | 838.7999 | 0.0 % | 0.2 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=50 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|
| **1 s.** | 0.39 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.14 ATR | 1.43 ATR |
| **5 s.** | 0.95 ATR | 1.45 ATR | 1.80 ATR | 2.05 ATR | 2.77 ATR | 3.61 ATR |
| **20 s.** | 1.85 ATR | 2.87 ATR | 3.56 ATR | 4.01 ATR | 5.22 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.05–0.35 ATR — optimum 0.05 ATR (0.214 %, prix 1126.1848), p(touche) 89.25 % (en stress 99.02 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.05–1.5 ATR — optimum 0.15 ATR (0.642 %, prix 1121.3544), p(touche) 88.22 % (en stress 99.01 %)  ✅ optimum identifie (86.8 % des re-echantillons)
- **20 seance(s)** : plage utile 0.05–3.0 ATR — optimum 0.15 ATR (0.642 %, prix 1121.3544), p(touche) 94.77 % (en stress 100.0 %)  ✅ optimum identifie (99.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : €1.856 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 36 % | T3 20 %
- Kelly (position) : f* 0.125 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 45.8 | bear 46.4 | side 7.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.674% vs midi 0.943% vs clôture 1.127% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. -0.194% ; recovery-V 23%
- **σ réalisé intraday** 2.742% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 60% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 1151.1575 (VA 1148.5825–1154.2475 ; dernier close 1152.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 17% · rebond 64% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 31% (gap-down >1% 10% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.74%) · haut méd +0.57% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.0%) · haut méd +0.67% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.19%) · haut méd +0.88% · range méd 2.07%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.62%) · haut méd +1.0% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1152.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 71% (117/159) · gap 21% · délai 0.4min · rebond 53% (61/117) (MFE +1.1%)
   - −1.0% : fill 30min 40% · séance 65% (108/159) · gap 10% · délai 5.9min · rebond 59% (61/108) (MFE +1.27%)
   - −1.5% : fill 30min 28% · séance 54% (88/159) · gap 6% · délai 24.4min · rebond 62% (50/88) (MFE +1.36%)
   - −2.0% : fill 30min 18% · séance 40% (74/159) · gap 5% · délai 33.7min · rebond 66% (46/74) (MFE +1.58%)
   - −3.0% : fill 30min 8% · séance 24% (46/159) · gap 3% · délai 120.4min · rebond 58% (27/46) (MFE +1.31%)
   - −4.0% : fill 30min 3% · séance 17% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 9% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.61%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.76%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.77%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=533 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 94% (46/48) · rebond 65% (27/46)
      · −2.0% : fill 80% (38/48) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/48) · rebond 63% (16/26)
      · −4.0% : fill 41% (16/48) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/48) · rebond 83% (7/9)
   - **flat** (47 séances) :
      · −1.0% : fill 67% (34/47) · rebond 64% (21/34)
      · −2.0% : fill 24% (17/47) · rebond 72% (10/17)
      · −3.0% : fill 16% (10/47) · rebond 55% (5/10)
      · −4.0% : fill 14% (8/47) · rebond 36% (2/8)
      · −5.0% : fill 9% (6/47) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 48% (28/64) · rebond 48% (13/28)
      · −2.0% : fill 30% (19/64) · rebond 63% (11/19)
      · −3.0% : fill 14% (10/64) · rebond 49% (6/10)
      · −4.0% : fill 6% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 2% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 62% si les 15 1res min sont vertes (77 cas) · 33% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:37** → P(séance verte=clôture>ouverture) 73% si début vert vs 19% si rouge (base 47% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 44% ; creux résiduel méd -1.21% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.76% / q75 +1.81% → **scale +0.76% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.7%** (au-delà de la MAE q10 -3.7%), cible rebond +0.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.27%] · haut q95 +3.75% · bas q05 -3.11%
   - 60min (n=160) : retour [-2.78% .. +3.22%] · haut q95 +4.4% · bas q05 -3.85%
   - 2h (n=160) : retour [-3.2% .. +3.04%] · haut q95 +4.4% · bas q05 -4.48%
   - 4h (n=160) : retour [-3.4% .. +3.3%] · haut q95 +4.87% · bas q05 -4.63%
   - 6h (n=160) : retour [-4.15% .. +3.3%] · haut q95 +4.95% · bas q05 -5.04%
   - session (n=160) : retour [-5.21% .. +3.79%] · haut q95 +5.07% · bas q05 -5.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 33.8  _(momentum baissier)_
- **ADX** : 20.4  _(pas de tendance nette)_
- **MACD** : hist -5.128  _(bearish_recent)_
- **BB** : %B 0.23 · largeur 11.0%
- **ATR** : 48.3 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.14  _(distribution)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 64.3  _(marche en range (choppy))_
- **MA** : MA20 1163.68 · MA50 1093.58 · MA200 1414.9  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 +3.2% · MA200 -20.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (974183 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
