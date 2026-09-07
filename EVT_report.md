# EVT

**Generated** : 2026-09-07T21:42:30.409109+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.21  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.21 (+0.3% vs entrée) · entrée €3.20 · stop €3.08 · T1 €3.26 · R/R 0.5  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.125 _(réel 5 s)_ (GBM -0.031) · ¼-Kelly 0.044 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.19–€3.21 (mid €3.20)
- Spot actuel : €3.21 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €3.08 (stop swing_plan-based (-4.04%))
- Targets : T1 €3.26 · R/R 0.5 | T2 €3.31 · R/R 0.92 | T3 €3.36 · R/R 1.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.08


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.04 %)** : le gap seul le franchit 1.02 % des séances (13 fois sur 1274).
   - exécution **2.871 pt plus bas** dans le cas TYPIQUE (médiane), 16.013 au p90, **28.373 au pire**
   - perte réelle **10.56 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 4.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0665 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1004** [0.0623 ; 0.1518] _(largeur 9.0 pt, n_eff 173.1)_
   - swing : **0.4722** [0.42 ; 0.5249] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4776** [0.4253 ; 0.5302] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.3 pt), swing (31.6 pt), deep (33.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.89 %** | CVaR **-9.26 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 6.11 % contre 3.75 % aujourd'hui, rapport 1.63)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1194** (β de hausse 0.9465, asymétrie 1.1826) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.8365 sur atr_grid (3.5 ATR, 11.745 %) — p(stop avant cible) 0.2577 [0.21 ; 0.31], R/R 1.917, perte reelle 19.926 % (gap inclus), CVaR 11.771 %, EV -3.1399 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.35 ATR (stop 3.258 %) — p(stop avant cible) 0.7137 [0.66 ; 0.76], R/R 5.393, perte reelle 7.083 % (gap inclus), EV -2.7452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.714, borne haute 0.759 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.75 %) : P(cible) 0.2 % x 38.20 % + P(rien) 28.4 % x 7.81 % ne couvrent pas P(stop) 71.4 % x 7.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.09 ATR (stop 5.734 %) — p(stop avant cible) 0.55 [0.50 ; 0.60], R/R 3.26, perte reelle 11.717 % (gap inclus), EV -3.5021 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.550, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.50 %) : P(cible) 0.3 % x 38.20 % + P(rien) 44.7 % x 6.31 % ne couvrent pas P(stop) 55.0 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 0.35 ATR (stop 2.189 %) — p(stop avant cible) 0.823 [0.78 ; 0.86], R/R 7.734, perte reelle 4.939 % (gap inclus), EV -2.4534 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.823, borne haute 0.861 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 0.2 % x 38.20 % + P(rien) 17.5 % x 8.77 % ne couvrent pas P(stop) 82.3 % x 4.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.09 ATR (stop 4.666 %) — p(stop avant cible) 0.6314 [0.58 ; 0.68], R/R 3.26, perte reelle 11.717 % (gap inclus), EV -4.6224 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.631, borne haute 0.681 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.62 %) : P(cible) 0.3 % x 38.20 % + P(rien) 36.6 % x 7.30 % ne couvrent pas P(stop) 63.1 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.712 %) — p(stop avant cible) 0.4727 [0.42 ; 0.53], R/R 2.57, perte reelle 14.861 % (gap inclus), EV -4.214 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.21 %) : P(cible) 0.3 % x 38.20 % + P(rien) 52.4 % x 5.13 % ne couvrent pas P(stop) 47.3 % x 14.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.551 %) — p(stop avant cible) 0.4128 [0.36 ; 0.47], R/R 2.122, perte reelle 18.001 % (gap inclus), EV -4.7656 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.77 %) : P(cible) 0.3 % x 38.20 % + P(rien) 58.4 % x 4.35 % ne couvrent pas P(stop) 41.3 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.39 %) — p(stop avant cible) 0.3762 [0.33 ; 0.43], R/R 2.122, perte reelle 18.001 % (gap inclus), EV -4.2331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.23 %) : P(cible) 0.3 % x 38.20 % + P(rien) 62.1 % x 3.89 % ne couvrent pas P(stop) 37.6 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.229 %) — p(stop avant cible) 0.3302 [0.28 ; 0.38], R/R 2.122, perte reelle 18.001 % (gap inclus), EV -3.5931 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.59 %) : P(cible) 0.3 % x 38.20 % + P(rien) 66.7 % x 3.34 % ne couvrent pas P(stop) 33.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.068 %) — p(stop avant cible) 0.3104 [0.26 ; 0.36], R/R 2.122, perte reelle 18.001 % (gap inclus), EV -3.3014 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.30 %) : P(cible) 0.3 % x 38.20 % + P(rien) 68.6 % x 3.15 % ne couvrent pas P(stop) 31.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.745 %) — p(stop avant cible) 0.2577 [0.21 ; 0.31], R/R 1.917, perte reelle 19.926 % (gap inclus), EV -3.1399 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.14 %) : P(cible) 0.3 % x 38.20 % + P(rien) 73.9 % x 2.53 % ne couvrent pas P(stop) 25.8 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.423 %) — p(stop avant cible) 0.1911 [0.15 ; 0.23], R/R 1.689, perte reelle 22.616 % (gap inclus), EV -2.8546 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.85 %) : P(cible) 0.3 % x 38.20 % + P(rien) 80.6 % x 1.67 % ne couvrent pas P(stop) 19.1 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.101 %) — p(stop avant cible) 0.1533 [0.12 ; 0.19], R/R 1.414, perte reelle 27.012 % (gap inclus), EV -3.0089 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.01 %) : P(cible) 0.3 % x 38.20 % + P(rien) 84.3 % x 1.20 % ne couvrent pas P(stop) 15.3 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 16.779 %) — p(stop avant cible) 0.135 [0.10 ; 0.17], R/R 1.414, perte reelle 27.012 % (gap inclus), EV -2.6314 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.63 %) : P(cible) 0.3 % x 38.20 % + P(rien) 86.2 % x 1.04 % ne couvrent pas P(stop) 13.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 18.457 %) — p(stop avant cible) 0.1091 [0.08 ; 0.15], R/R 1.414, perte reelle 27.012 % (gap inclus), EV -2.1973 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 0.3 % x 38.20 % + P(rien) 88.8 % x 0.71 % ne couvrent pas P(stop) 10.9 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 20.135 %) — p(stop avant cible) 0.1018 [0.07 ; 0.14], R/R 1.414, perte reelle 27.012 % (gap inclus), EV -2.0969 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.10 %) : P(cible) 0.3 % x 38.20 % + P(rien) 89.5 % x 0.59 % ne couvrent pas P(stop) 10.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 21.813 %) — p(stop avant cible) 0.0993 [0.07 ; 0.13], R/R 1.178, perte reelle 32.413 % (gap inclus), EV -2.6085 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.3 % x 38.20 % + P(rien) 89.7 % x 0.54 % ne couvrent pas P(stop) 9.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 23.491 %) — p(stop avant cible) 0.0932 [0.07 ; 0.13], R/R 1.178, perte reelle 32.413 % (gap inclus), EV -2.5185 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.52 %) : P(cible) 0.3 % x 38.20 % + P(rien) 90.3 % x 0.42 % ne couvrent pas P(stop) 9.3 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 25.169 %) — p(stop avant cible) 0.082 [0.06 ; 0.11], R/R 1.178, perte reelle 32.413 % (gap inclus), EV -2.3812 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.38 %) : P(cible) 0.3 % x 38.20 % + P(rien) 91.5 % x 0.17 % ne couvrent pas P(stop) 8.2 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 26.847 %) — p(stop avant cible) 0.0729 [0.05 ; 0.10], R/R 1.178, perte reelle 32.413 % (gap inclus), EV -2.2963 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.30 %) : P(cible) 0.3 % x 38.20 % + P(rien) 92.4 % x -0.06 % ne couvrent pas P(stop) 7.3 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.214, ATR14 0.1079 (3.356 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.228 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.168 % | 3.2086 | 88.95 % | 91.81 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.336 % | 3.2032 | 81.56 % | 86.97 % | 89.62 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.503 % | 3.1978 | 75.25 % | 83.12 % | 86.56 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.671 % | 3.1924 | 68.93 % | 79.07 % | 83.3 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 0.839 % | 3.187 | 63.21 % | 75.81 % | 80.24 % | 84.85 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.175 % | 3.1762 | 51.78 % | 67.62 % | 73.81 % | 79.9 % | 86.17 % | 91.56 % |
| 0.5 ATR | 1.678 % | 3.1601 | 35.5 % | 54.99 % | 62.85 % | 70.79 % | 80.1 % | 88.24 % |
| 0.75 ATR | 2.517 % | 3.1331 | 19.13 % | 38.01 % | 47.73 % | 59.41 % | 71.74 % | 81.91 % |
| 1.0 ATR | 3.356 % | 3.1061 | 10.16 % | 24.98 % | 35.97 % | 47.52 % | 62.39 % | 75.28 % |
| 1.25 ATR | 4.195 % | 3.0792 | 4.83 % | 17.47 % | 27.57 % | 39.6 % | 55.62 % | 70.05 % |
| 1.5 ATR | 5.034 % | 3.0522 | 3.06 % | 11.35 % | 19.86 % | 31.49 % | 48.46 % | 64.72 % |
| 2.0 ATR | 6.712 % | 2.9983 | 1.48 % | 5.23 % | 9.98 % | 19.5 % | 34.83 % | 52.46 % |
| 2.5 ATR | 8.39 % | 2.9444 | 0.49 % | 2.76 % | 5.83 % | 12.48 % | 27.66 % | 44.62 % |
| 3.0 ATR | 10.068 % | 2.8904 | 0.39 % | 1.68 % | 3.75 % | 9.01 % | 20.8 % | 37.49 % |
| 4.0 ATR | 13.423 % | 2.7826 | 0.2 % | 0.89 % | 1.98 % | 4.55 % | 11.74 % | 24.52 % |
| 6.0 ATR | 20.135 % | 2.5669 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.57 % | 14.17 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.50 ATR | 2.00 ATR | 2.70 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.86 ATR | 3.90 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.13 ATR | 2.69 ATR | 3.09 ATR | 4.56 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.16 ATR | 2.48 ATR | 3.35 ATR | 3.96 ATR | 4.87 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.647–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.517 %, prix 3.1331), p(touche) 38.01 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.1 % des re-echantillons)
- **3 seance(s)** : plage utile 0.808–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.356 %, prix 3.1061), p(touche) 35.97 % (en stress 96.08 %)  ✅ optimum identifie (63.9 % des re-echantillons)
- **5 seance(s)** : plage utile 1.08–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.195 %, prix 3.0792), p(touche) 39.6 % (en stress 95.05 %)  ✅ optimum identifie (75.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.627–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.712 %, prix 2.9983), p(touche) 34.83 % (en stress 98.02 %)  ✅ optimum identifie (72.9 % des re-echantillons)
- **20 seance(s)** : plage utile 2.476–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.39 %, prix 2.9443), p(touche) 44.62 % (en stress 98.0 %)  ✅ optimum identifie (84.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : €-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 18 % | T3 6 %
- Kelly (position) : f* 0.175 | ¼-Kelly 0.044 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.7 | bear 5.0 | side 77.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.311% → cible +1.623% / stop −4.001%, p_fill 90%, n_eff≈36.6) : P(cible|rempli) **31%** · **EV/risk -0.125** (×p_fill ; si rempli -0.56% du capital)
  - **swing** (entrée dip −0.686% → cible +3.634% / stop −3.377%, p_fill 88%, n_eff≈35.8) : P(cible|rempli) **40%** · **EV/risk -0.052** (×p_fill ; si rempli -0.20% du capital)
  - **deep** (entrée dip −1.019% → cible +5.139% / stop −5.083%, p_fill 83%, n_eff≈31.8) : P(cible|rempli) **42%** · **EV/risk -0.124** (×p_fill ; si rempli -0.76% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→69% · +2.0%→41% · +3.0%→21% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.26%) · excursion haute méd. +1.57% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.39% vs midi 1.183% vs clôture 1.156% _(ouverture ~2.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.092 ; mean-reverting — autocorr -0.184)_ ; drift intra méd. -0.657% ; recovery-V 22%
- **σ réalisé intraday** 2.883% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 75% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 3.2156 (VA 3.191–3.2341 ; dernier close 3.203)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 55% · rebond 63% · **stop −2.51%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 40% (gap-down >1% 9% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.2%) · haut méd +0.37% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.65%) · haut méd +0.56% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.77%) · haut méd +0.71% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.93%) · haut méd +0.88% · range méd 2.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.212 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 79% (131/159) · gap 22% · délai 1.0min · rebond 65% (88/131) (MFE +1.39%)
   - −1.0% : fill 30min 38% · séance 67% (112/159) · gap 9% · délai 6.9min · rebond 63% (74/112) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 55% (95/159) · gap 5% · délai 25.1min · rebond 63% (61/95) (MFE +1.33%)
   - −2.0% : fill 30min 19% · séance 44% (79/159) · gap 5% · délai 43.0min · rebond 50% (44/79) (MFE +0.99%)
   - −3.0% : fill 30min 9% · séance 23% (49/159) · gap 3% · délai 59.4min · rebond 66% (35/49) (MFE +1.5%)
   - −4.0% : fill 30min 4% · séance 10% (26/159) · gap 1% · délai 46.7min · rebond 53% (16/26) (MFE +1.13%)
   - −5.0% : fill 30min 3% · séance 6% (15/159) · gap 1% · délai 30.3min · rebond 59% (10/15) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −2.19%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.83%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −1.85%) → stop au-delà de −1.58% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=808 jambes) : jambe baissière méd −1.07% (p90 −2.28%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (47/55) · rebond 64% (32/47)
      · −2.0% : fill 62% (37/55) · rebond 48% (21/37)
      · −3.0% : fill 35% (25/55) · rebond 68% (18/25)
      · −4.0% : fill 21% (18/55) · rebond 42% (11/18)
      · −5.0% : fill 15% (12/55) · rebond 40% (7/12)
   - **flat** (35 séances) :
      · −1.0% : fill 85% (28/35) · rebond 49% (16/28)
      · −2.0% : fill 62% (21/35) · rebond 44% (9/21)
      · −3.0% : fill 35% (13/35) · rebond 79% (10/13)
      · −4.0% : fill 7% (3/35) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/35) · rebond 100% (1/1)
   - **gap-up** (69 séances) :
      · −1.0% : fill 49% (37/69) · rebond 73% (26/37)
      · −2.0% : fill 24% (21/69) · rebond 60% (14/21)
      · −3.0% : fill 9% (11/69) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/69) · rebond 95% (4/5)
      · −5.0% : fill 3% (2/69) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 62% si début vert vs 33% si rouge (base 45% · écart 29 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **62%** · continue >prix actuel 35% ; creux résiduel méd -1.77% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.42% → **scale +1.38% / runner +2.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **33%** (continue à baisser 55%) → **RÉDUIRE ~67%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.16%** (au-delà de la MAE q10 -4.16%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +2.07%] · haut q95 +2.96% · bas q05 -3.91%
   - 60min (n=160) : retour [-2.99% .. +2.44%] · haut q95 +3.08% · bas q05 -3.96%
   - 2h (n=160) : retour [-3.46% .. +2.37%] · haut q95 +3.72% · bas q05 -4.16%
   - 4h (n=160) : retour [-3.35% .. +3.62%] · haut q95 +4.28% · bas q05 -4.28%
   - 6h (n=160) : retour [-3.3% .. +3.75%] · haut q95 +5.24% · bas q05 -4.99%
   - session (n=160) : retour [-4.11% .. +4.05%] · haut q95 +5.66% · bas q05 -5.54%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.8  _(momentum baissier)_
- **ADX** : 30.0  _(tendance etablie)_
- **MACD** : hist 0.015  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 20.0%
- **ATR** : 0.11 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.276  _(distribution)_
- **Vol ratio** : 0.33  _(volume atone)_
- **Choppiness** : 56.1  _(transition)_
- **MA** : MA20 3.37 · MA50 3.75 · MA200 4.92  _(prix < MA20)_
- **Dist MA** : MA20 -4.7% · MA50 -14.3% · MA200 -34.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (757980 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
