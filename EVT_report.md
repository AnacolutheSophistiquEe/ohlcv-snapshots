# EVT

**Generated** : 2026-09-03T00:04:58.271440+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.30  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.30 (+0.9% vs entrée) · entrée €3.27 · stop €3.14 · T1 €3.38 · R/R 0.85  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.096 _(réel 5 s)_ (GBM -0.081) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.26–€3.28 (mid €3.27)
- Spot actuel : €3.30 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : €3.14 (stop swing_plan-based (-5.66%))
- Targets : T1 €3.38 · R/R 0.85 | T2 €3.41 · R/R 1.08 | T3 €3.44 · R/R 1.31
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.66 %)** : le gap seul le franchit 0.863 % des séances (11 fois sur 1274).
   - exécution **1.452 pt plus bas** dans le cas TYPIQUE (médiane), 15.951 au p90, **26.753 au pire**
   - perte réelle **11.717 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 5.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0523 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1117** [0.0713 ; 0.165] _(largeur 9.4 pt, n_eff 173.1)_
   - swing : **0.4519** [0.4 ; 0.5046] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4612** [0.4092 ; 0.5139] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (40.8 pt), deep (40.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.89 %** | CVaR **-9.26 %** | vol 3.66 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 6.08 % contre 3.76 % aujourd'hui, rapport 1.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1138** (β de hausse 0.9425, asymétrie 1.1817) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.9735 sur atr_grid (2.75 ATR, 9.893 %) — p(stop avant cible) 0.3179 [0.27 ; 0.37], R/R 1.916, perte reelle 18.001 % (gap inclus), CVaR 9.925 %, EV -3.3084 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.71 ATR (stop 4.652 %) — p(stop avant cible) 0.625 [0.57 ; 0.67], R/R 2.944, perte reelle 11.717 % (gap inclus), EV -4.4884 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.625, borne haute 0.675 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.49 %) : P(cible) 0.4 % x 34.50 % + P(rien) 37.0 % x 7.23 % ne couvrent pas P(stop) 62.5 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.04 ATR (stop 5.873 %) — p(stop avant cible) 0.533 [0.48 ; 0.59], R/R 2.944, perte reelle 11.717 % (gap inclus), EV -3.2455 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.533, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.25 %) : P(cible) 0.6 % x 34.50 % + P(rien) 46.1 % x 6.07 % ne couvrent pas P(stop) 53.3 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.899 %) — p(stop avant cible) 0.9058 [0.87 ; 0.93], R/R 14.94, perte reelle 2.309 % (gap inclus), EV -1.0821 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 14.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.906, borne haute 0.933 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 0.2 % x 34.50 % + P(rien) 9.3 % x 10.30 % ne couvrent pas P(stop) 90.6 % x 2.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.71 ATR (stop 3.616 %) — p(stop avant cible) 0.6919 [0.64 ; 0.74], R/R 4.088, perte reelle 8.438 % (gap inclus), EV -3.4178 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.692, borne haute 0.739 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.42 %) : P(cible) 0.3 % x 34.50 % + P(rien) 30.5 % x 7.57 % ne couvrent pas P(stop) 69.2 % x 8.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 5.396 %) — p(stop avant cible) 0.5616 [0.51 ; 0.61], R/R 2.944, perte reelle 11.717 % (gap inclus), EV -3.5847 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.562, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.58 %) : P(cible) 0.5 % x 34.50 % + P(rien) 43.3 % x 6.50 % ne couvrent pas P(stop) 56.2 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.195 %) — p(stop avant cible) 0.4354 [0.38 ; 0.49], R/R 1.916, perte reelle 18.001 % (gap inclus), EV -5.0637 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.06 %) : P(cible) 0.7 % x 34.50 % + P(rien) 55.8 % x 4.56 % ne couvrent pas P(stop) 43.5 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.094 %) — p(stop avant cible) 0.3916 [0.34 ; 0.44], R/R 1.916, perte reelle 18.001 % (gap inclus), EV -4.3799 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.38 %) : P(cible) 0.7 % x 34.50 % + P(rien) 60.2 % x 4.06 % ne couvrent pas P(stop) 39.2 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.994 %) — p(stop avant cible) 0.3497 [0.30 ; 0.40], R/R 1.916, perte reelle 18.001 % (gap inclus), EV -3.7587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.76 %) : P(cible) 0.7 % x 34.50 % + P(rien) 64.4 % x 3.59 % ne couvrent pas P(stop) 35.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.893 %) — p(stop avant cible) 0.3179 [0.27 ; 0.37], R/R 1.916, perte reelle 18.001 % (gap inclus), EV -3.3084 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.31 %) : P(cible) 0.7 % x 34.50 % + P(rien) 67.5 % x 3.24 % ne couvrent pas P(stop) 31.8 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.792 %) — p(stop avant cible) 0.2911 [0.25 ; 0.34], R/R 1.731, perte reelle 19.926 % (gap inclus), EV -3.5277 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.53 %) : P(cible) 0.7 % x 34.50 % + P(rien) 70.2 % x 2.91 % ne couvrent pas P(stop) 29.1 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.591 %) — p(stop avant cible) 0.2279 [0.19 ; 0.27], R/R 1.525, perte reelle 22.616 % (gap inclus), EV -3.2955 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.30 %) : P(cible) 0.7 % x 34.50 % + P(rien) 76.6 % x 2.13 % ne couvrent pas P(stop) 22.8 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 14.39 %) — p(stop avant cible) 0.1745 [0.14 ; 0.22], R/R 1.277, perte reelle 27.012 % (gap inclus), EV -3.3062 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.31 %) : P(cible) 0.7 % x 34.50 % + P(rien) 81.9 % x 1.44 % ne couvrent pas P(stop) 17.4 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 16.188 %) — p(stop avant cible) 0.1416 [0.11 ; 0.18], R/R 1.277, perte reelle 27.012 % (gap inclus), EV -2.6922 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.69 %) : P(cible) 0.7 % x 34.50 % + P(rien) 85.2 % x 1.06 % ne couvrent pas P(stop) 14.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 17.987 %) — p(stop avant cible) 0.1181 [0.09 ; 0.16], R/R 1.277, perte reelle 27.012 % (gap inclus), EV -2.2692 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.27 %) : P(cible) 0.7 % x 34.50 % + P(rien) 87.5 % x 0.79 % ne couvrent pas P(stop) 11.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 19.786 %) — p(stop avant cible) 0.1082 [0.08 ; 0.14], R/R 1.277, perte reelle 27.012 % (gap inclus), EV -2.1276 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 0.7 % x 34.50 % + P(rien) 88.5 % x 0.64 % ne couvrent pas P(stop) 10.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 21.584 %) — p(stop avant cible) 0.1028 [0.07 ; 0.14], R/R 1.277, perte reelle 27.012 % (gap inclus), EV -2.0505 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 0.7 % x 34.50 % + P(rien) 89.1 % x 0.56 % ne couvrent pas P(stop) 10.3 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 23.383 %) — p(stop avant cible) 0.0949 [0.07 ; 0.13], R/R 1.064, perte reelle 32.413 % (gap inclus), EV -2.4919 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.49 %) : P(cible) 0.7 % x 34.50 % + P(rien) 89.9 % x 0.40 % ne couvrent pas P(stop) 9.5 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 25.182 %) — p(stop avant cible) 0.0835 [0.06 ; 0.12], R/R 1.064, perte reelle 32.413 % (gap inclus), EV -2.3521 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 0.7 % x 34.50 % + P(rien) 91.0 % x 0.14 % ne couvrent pas P(stop) 8.3 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 26.981 %) — p(stop avant cible) 0.0742 [0.05 ; 0.11], R/R 1.064, perte reelle 32.413 % (gap inclus), EV -2.2645 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 0.7 % x 34.50 % + P(rien) 91.9 % x -0.09 % ne couvrent pas P(stop) 7.4 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 28.779 %) — p(stop avant cible) 0.0586 [0.04 ; 0.09], R/R 1.064, perte reelle 32.413 % (gap inclus), EV -2.1438 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 0.7 % x 34.50 % + P(rien) 93.5 % x -0.51 % ne couvrent pas P(stop) 5.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.3, ATR14 0.1187 (3.597 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.317 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.18 % | 3.2941 | 88.86 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.36 % | 3.2881 | 81.56 % | 86.97 % | 89.72 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.54 % | 3.2822 | 75.25 % | 83.12 % | 86.66 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.719 % | 3.2763 | 68.84 % | 78.97 % | 83.3 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 0.899 % | 3.2703 | 63.12 % | 75.72 % | 80.24 % | 84.75 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.259 % | 3.2584 | 51.78 % | 67.52 % | 73.81 % | 79.8 % | 86.17 % | 91.56 % |
| 0.5 ATR | 1.799 % | 3.2406 | 35.4 % | 54.79 % | 62.75 % | 70.69 % | 80.1 % | 88.24 % |
| 0.75 ATR | 2.698 % | 3.211 | 19.13 % | 37.81 % | 47.63 % | 59.31 % | 71.74 % | 81.91 % |
| 1.0 ATR | 3.597 % | 3.1813 | 10.16 % | 24.78 % | 35.87 % | 47.43 % | 62.39 % | 75.28 % |
| 1.25 ATR | 4.497 % | 3.1516 | 4.83 % | 17.47 % | 27.47 % | 39.41 % | 55.62 % | 70.05 % |
| 1.5 ATR | 5.396 % | 3.1219 | 3.06 % | 11.35 % | 19.86 % | 31.39 % | 48.56 % | 64.72 % |
| 2.0 ATR | 7.195 % | 3.0626 | 1.48 % | 5.23 % | 9.98 % | 19.41 % | 35.12 % | 52.46 % |
| 2.5 ATR | 8.994 % | 3.0032 | 0.49 % | 2.76 % | 5.83 % | 12.48 % | 27.96 % | 44.62 % |
| 3.0 ATR | 10.792 % | 2.9439 | 0.39 % | 1.68 % | 3.75 % | 9.01 % | 21.09 % | 37.69 % |
| 4.0 ATR | 14.39 % | 2.8251 | 0.2 % | 0.89 % | 1.98 % | 4.55 % | 11.94 % | 24.82 % |
| 6.0 ATR | 21.584 % | 2.5877 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.57 % | 14.27 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.61 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.08 ATR | 1.33 ATR | 1.50 ATR | 2.00 ATR | 2.70 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.86 ATR | 3.90 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.15 ATR | 2.71 ATR | 3.12 ATR | 4.61 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.16 ATR | 2.48 ATR | 3.36 ATR | 3.99 ATR | 4.91 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (62.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.644–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.698 %, prix 3.211), p(touche) 37.81 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.2 % des re-echantillons)
- **3 seance(s)** : plage utile 0.806–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.597 %, prix 3.1813), p(touche) 35.87 % (en stress 96.08 %)  ✅ optimum identifie (64.4 % des re-echantillons)
- **5 seance(s)** : plage utile 1.076–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.497 %, prix 3.1516), p(touche) 39.41 % (en stress 95.05 %)  ✅ optimum identifie (74.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.632–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.195 %, prix 3.0626), p(touche) 35.12 % (en stress 98.02 %)  ✅ optimum identifie (73.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.476–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.994 %, prix 3.0032), p(touche) 44.62 % (en stress 98.0 %)  ✅ optimum identifie (85.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : €-0.011 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 6 % | T3 5 %
- Kelly (position) : f* 0.023 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 29.7 | bear 5.0 | side 65.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.936% → cible +3.396% / stop −4.001%, p_fill 78%, n_eff≈31.5) : P(cible|rempli) **7%** · **EV/risk -0.096** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −2.063% → cible +3.958% / stop −3.673%, p_fill 54%, n_eff≈20.5) : P(cible|rempli) **45%** · **EV/risk -0.035** (×p_fill ; si rempli -0.23% du capital)
  - **deep** (entrée dip −3.193% → cible +5.6% / stop −5.575%, p_fill 53%, n_eff≈20.5) : P(cible|rempli) **20%** · **EV/risk -0.225** (×p_fill ; si rempli -2.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→68% · +2.0%→40% · +3.0%→21% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.26%) · excursion haute méd. +1.53% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.484% vs midi 1.192% vs clôture 1.156% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.091 ; mean-reverting — autocorr -0.18)_ ; drift intra méd. -0.791% ; recovery-V 20%
- **σ réalisé intraday** 2.934% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 76% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 3.2093 (VA 3.2031–3.2341 ; dernier close 3.166)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 56% · rebond 66% · **stop −2.56%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 41% (gap-down >1% 9% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −2.25%) · haut méd +0.44% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.68%) · haut méd +0.67% · range méd 1.73%
- Excursion ouverture 30min (n=160) : bas méd −0.91% (p90 −2.78%) · haut méd +0.77% · range méd 1.97%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −3.02%) · haut méd +0.93% · range méd 2.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.15 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 78% (130/159) · gap 23% · délai 0.5min · rebond 67% (88/130) (MFE +1.42%)
   - −1.0% : fill 30min 39% · séance 67% (112/159) · gap 9% · délai 6.9min · rebond 64% (74/112) (MFE +1.44%)
   - −1.5% : fill 30min 30% · séance 56% (95/159) · gap 5% · délai 23.5min · rebond 66% (62/95) (MFE +1.4%)
   - −2.0% : fill 30min 20% · séance 44% (78/159) · gap 5% · délai 39.1min · rebond 52% (44/78) (MFE +1.29%)
   - −3.0% : fill 30min 10% · séance 24% (49/159) · gap 3% · délai 59.4min · rebond 66% (35/49) (MFE +1.5%)
   - −4.0% : fill 30min 4% · séance 11% (26/159) · gap 1% · délai 46.7min · rebond 53% (16/26) (MFE +1.13%)
   - −5.0% : fill 30min 3% · séance 7% (15/159) · gap 1% · délai 30.3min · rebond 59% (10/15) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.45%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.31% (p90 −1.66%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.85%) → stop au-delà de −1.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=810 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 81% (47/55) · rebond 69% (32/47)
      · −2.0% : fill 59% (36/55) · rebond 53% (21/36)
      · −3.0% : fill 37% (25/55) · rebond 68% (18/25)
      · −4.0% : fill 22% (18/55) · rebond 42% (11/18)
      · −5.0% : fill 16% (12/55) · rebond 40% (7/12)
   - **flat** (36 séances) :
      · −1.0% : fill 85% (29/36) · rebond 49% (17/29)
      · −2.0% : fill 62% (21/36) · rebond 44% (9/21)
      · −3.0% : fill 35% (13/36) · rebond 79% (10/13)
      · −4.0% : fill 7% (3/36) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/36) · rebond 100% (1/1)
   - **gap-up** (68 séances) :
      · −1.0% : fill 49% (36/68) · rebond 71% (25/36)
      · −2.0% : fill 26% (21/68) · rebond 60% (14/21)
      · −3.0% : fill 10% (11/68) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/68) · rebond 95% (4/5)
      · −5.0% : fill 4% (2/68) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 58% si les 15 1res min sont vertes (73 cas) · 35% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 57% si début vert vs 36% si rouge (base 46% · écart 21 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **57%** · continue >prix actuel 39% ; creux résiduel méd -1.83% (q20 -2.79%) → **SL/trailing à −2.79%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.27% / q75 +2.35% → **scale +1.27% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **36%** (continue à baisser 48%) → **RÉDUIRE ~64%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.47%** (au-delà de la MAE q10 -4.47%), cible rebond +1.72% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +2.27%] · haut q95 +3.04% · bas q05 -3.92%
   - 60min (n=160) : retour [-3.1% .. +2.54%] · haut q95 +3.27% · bas q05 -4.08%
   - 2h (n=160) : retour [-3.48% .. +2.4%] · haut q95 +3.75% · bas q05 -4.25%
   - 4h (n=160) : retour [-3.35% .. +3.74%] · haut q95 +4.43% · bas q05 -4.48%
   - 6h (n=160) : retour [-3.34% .. +4.49%] · haut q95 +5.26% · bas q05 -5.28%
   - session (n=160) : retour [-4.19% .. +4.05%] · haut q95 +5.8% · bas q05 -5.68%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.3  _(momentum baissier)_
- **ADX** : 30.4  _(tendance etablie)_
- **MACD** : hist 0.015  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 19.7%
- **ATR** : 0.12 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.285  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 47.7  _(transition)_
- **MA** : MA20 3.41 · MA50 3.85 · MA200 4.95  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 -14.3% · MA200 -33.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (493677 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
