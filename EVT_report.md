# EVT

**Generated** : 2026-08-24T00:05:03.235596+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.36  

> 🟡 **WAIT-FOR-DIP** — spot +1.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.36 (+1.5% vs entrée) · entrée €3.31 · stop €3.26 · T1 €3.38 · R/R 1.4  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk 0.068 _(réel 5 s)_ (GBM -0.017) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.30–€3.32 (mid €3.31)
- Spot actuel : €3.36 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €3.26 (stop swing_plan-based (-7.67%))
- Targets : T1 €3.38 · R/R 1.4 | T2 €3.42 · R/R 2.2 | T3 €3.47 · R/R 3.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.26


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.67 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **6.154 pt plus bas** dans le cas TYPIQUE (médiane), 20.422 au p90, **24.743 au pire**
   - perte réelle **18.001 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 7.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0405 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0657** [0.0358 ; 0.1099] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.4215** [0.3703 ; 0.474] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4868** [0.4344 ; 0.5394] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.1 pt), swing (45.9 pt), deep (44.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-5.11 %** | CVaR **-9.26 %** | vol 3.81 %/j
   - _fenêtre arrêtée : rupture de regime a 1260 seances en arriere (volatilite 2.12 % contre 3.96 % aujourd'hui, rapport 0.53)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1125** (β de hausse 0.9496, asymétrie 1.1715) vs GDAXI — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.9599 sur atr_grid (2.5 ATR, 11.802 %) — p(stop avant cible) 0.2584 [0.21 ; 0.31], R/R 1.601, perte reelle 19.926 % (gap inclus), CVaR 11.828 %, EV -2.7936 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.05 ATR (stop 2.709 %) — p(stop avant cible) 0.7567 [0.71 ; 0.80], R/R 5.459, perte reelle 5.843 % (gap inclus), EV -2.2249 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.757, borne haute 0.800 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 1.0 % x 31.90 % + P(rien) 23.4 % x 8.07 % ne couvrent pas P(stop) 75.7 % x 5.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.14 ATR (stop 7.843 %) — p(stop avant cible) 0.3963 [0.35 ; 0.45], R/R 1.772, perte reelle 18.001 % (gap inclus), EV -4.1941 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.19 %) : P(cible) 1.5 % x 31.90 % + P(rien) 58.9 % x 4.20 % ne couvrent pas P(stop) 39.6 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.442 %) — p(stop avant cible) 0.32 [0.27 ; 0.37], R/R 1.772, perte reelle 18.001 % (gap inclus), EV -3.084 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.08 %) : P(cible) 1.5 % x 31.90 % + P(rien) 66.5 % x 3.33 % ne couvrent pas P(stop) 32.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.802 %) — p(stop avant cible) 0.2584 [0.21 ; 0.31], R/R 1.601, perte reelle 19.926 % (gap inclus), EV -2.7936 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.79 %) : P(cible) 1.5 % x 31.90 % + P(rien) 72.7 % x 2.60 % ne couvrent pas P(stop) 25.8 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 14.162 %) — p(stop avant cible) 0.1774 [0.14 ; 0.22], R/R 1.181, perte reelle 27.012 % (gap inclus), EV -3.0367 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.04 %) : P(cible) 1.5 % x 31.90 % + P(rien) 80.8 % x 1.60 % ne couvrent pas P(stop) 17.7 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 16.523 %) — p(stop avant cible) 0.1458 [0.11 ; 0.19], R/R 1.181, perte reelle 27.012 % (gap inclus), EV -2.4229 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 1.5 % x 31.90 % + P(rien) 84.0 % x 1.25 % ne couvrent pas P(stop) 14.6 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 18.883 %) — p(stop avant cible) 0.1159 [0.09 ; 0.15], R/R 1.181, perte reelle 27.012 % (gap inclus), EV -1.9135 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 1.5 % x 31.90 % + P(rien) 87.0 % x 0.87 % ne couvrent pas P(stop) 11.6 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 21.243 %) — p(stop avant cible) 0.1076 [0.08 ; 0.14], R/R 1.181, perte reelle 27.012 % (gap inclus), EV -1.798 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.80 %) : P(cible) 1.5 % x 31.90 % + P(rien) 87.8 % x 0.74 % ne couvrent pas P(stop) 10.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 23.604 %) — p(stop avant cible) 0.0987 [0.07 ; 0.13], R/R 0.984, perte reelle 32.413 % (gap inclus), EV -2.2557 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 1.5 % x 31.90 % + P(rien) 88.7 % x 0.54 % ne couvrent pas P(stop) 9.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 25.964 %) — p(stop avant cible) 0.0816 [0.06 ; 0.11], R/R 0.984, perte reelle 32.413 % (gap inclus), EV -2.0489 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 1.5 % x 31.90 % + P(rien) 90.4 % x 0.15 % ne couvrent pas P(stop) 8.2 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 28.325 %) — p(stop avant cible) 0.0613 [0.04 ; 0.09], R/R 0.984, perte reelle 32.413 % (gap inclus), EV -1.8952 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 1.5 % x 31.90 % + P(rien) 92.4 % x -0.40 % ne couvrent pas P(stop) 6.1 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 30.685 %) — p(stop avant cible) 0.0501 [0.03 ; 0.08], R/R 0.984, perte reelle 32.413 % (gap inclus), EV -1.8121 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.81 %) : P(cible) 1.5 % x 31.90 % + P(rien) 93.5 % x -0.70 % ne couvrent pas P(stop) 5.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 33.045 %) — p(stop avant cible) 0.0501 [0.03 ; 0.08], R/R 0.965, perte reelle 33.045 % (gap inclus), EV -1.8438 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 1.5 % x 31.90 % + P(rien) 93.5 % x -0.70 % ne couvrent pas P(stop) 5.0 % x 33.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 35.406 %) — p(stop avant cible) 0.0442 [0.03 ; 0.07], R/R 0.901, perte reelle 35.406 % (gap inclus), EV -1.9221 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 1.5 % x 31.90 % + P(rien) 94.1 % x -0.87 % ne couvrent pas P(stop) 4.4 % x 35.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 37.766 %) — p(stop avant cible) 0.023 [0.01 ; 0.04], R/R 0.845, perte reelle 37.766 % (gap inclus), EV -1.838 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 1.5 % x 31.90 % + P(rien) 96.2 % x -1.49 % ne couvrent pas P(stop) 2.3 % x 37.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 16 % | T3 6 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.0 | bear 7.4 | side 14.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.339% → cible +2.084% / stop −1.501%, p_fill 68%, n_eff≈25.3) : P(cible|rempli) **27%** · **EV/risk +0.068** (×p_fill ; si rempli +0.15% du capital)
  - **swing** (entrée dip −2.95% → cible +3.516% / stop −4.863%, p_fill 42%, n_eff≈15.7) : P(cible|rempli) **46%** · **EV/risk -0.069** (×p_fill ; si rempli -0.79% du capital)
  - **deep** (entrée dip −4.56% → cible +4.973% / stop −7.418%, p_fill 25%, n_eff≈17.0) : P(cible|rempli) **21%** · **EV/risk -0.116** (×p_fill ; si rempli -3.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→69% · +2.0%→44% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.57%) · excursion haute méd. +1.74% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.692% vs midi 1.22% vs clôture 1.193% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; mean-reverting — autocorr -0.134)_ ; drift intra méd. -0.771% ; recovery-V 27%
- **σ réalisé intraday** 3.137% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 72% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 3.3443 (VA 3.3227–3.3569 ; dernier close 3.348)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 71% · rebond 71% · **stop −3.14%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 38% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.34%) · haut méd +0.49% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.83%) · haut méd +0.75% · range méd 1.78%
- Excursion ouverture 30min (n=160) : bas méd −1.05% (p90 −2.83%) · haut méd +0.81% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.26%) · haut méd +0.95% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.348 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 83% (134/159) · gap 22% · délai 0.4min · rebond 71% (89/134) (MFE +1.59%)
   - −1.0% : fill 30min 47% · séance 71% (117/159) · gap 16% · délai 2.5min · rebond 71% (75/117) (MFE +1.6%)
   - −1.5% : fill 30min 35% · séance 54% (95/159) · gap 11% · délai 7.8min · rebond 66% (60/95) (MFE +1.79%)
   - −2.0% : fill 30min 22% · séance 43% (80/159) · gap 7% · délai 23.5min · rebond 58% (50/80) (MFE +1.32%)
   - −3.0% : fill 30min 11% · séance 26% (55/159) · gap 4% · délai 51.4min · rebond 66% (40/55) (MFE +1.36%)
   - −4.0% : fill 30min 6% · séance 16% (32/159) · gap 2% · délai 53.0min · rebond 60% (20/32) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 8% (18/159) · gap 1% · délai 56.0min · rebond 60% (12/18) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.49%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.72%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.89%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=813 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 95% (54/57) · rebond 70% (31/54)
      · −2.0% : fill 65% (41/57) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/57) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/57) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/57) · rebond 57% (9/13)
   - **flat** (43 séances) :
      · −1.0% : fill 65% (30/43) · rebond 73% (23/30)
      · −2.0% : fill 48% (20/43) · rebond 64% (13/20)
      · −3.0% : fill 34% (13/43) · rebond 77% (10/13)
      · −4.0% : fill 17% (6/43) · rebond 46% (2/6)
      · −5.0% : fill 6% (3/43) · rebond 27% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 58% (33/59) · rebond 69% (21/33)
      · −2.0% : fill 24% (19/59) · rebond 46% (12/19)
      · −3.0% : fill 13% (13/59) · rebond 40% (9/13)
      · −4.0% : fill 8% (6/59) · rebond 90% (4/6)
      · −5.0% : fill 5% (2/59) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 35% si rouge (base 48% · écart 31 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.75% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.43% → **scale +1.56% / runner +2.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **35%** (continue à baisser 51%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.58%** (au-delà de la MAE q10 -4.58%), cible rebond +1.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +2.3%] · haut q95 +3.38% · bas q05 -3.94%
   - 60min (n=160) : retour [-3.32% .. +2.7%] · haut q95 +3.45% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.68% .. +2.64%] · haut q95 +3.9% · bas q05 -4.81%
   - 4h (n=160) : retour [-3.48% .. +3.03%] · haut q95 +3.94% · bas q05 -6.47%
   - 6h (n=160) : retour [-3.71% .. +3.37%] · haut q95 +4.79% · bas q05 -6.47%
   - session (n=160) : retour [-4.59% .. +4.21%] · haut q95 +6.42% · bas q05 -7.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 44.2  _(momentum baissier)_
- **ADX** : 32.2  _(tendance etablie)_
- **MACD** : hist 0.024  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 14.6%
- **ATR** : 0.16 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.353  _(distribution)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 48.2  _(transition)_
- **MA** : MA20 3.48 · MA50 4.08 · MA200 5.03  _(prix < MA20)_
- **Dist MA** : MA20 -3.6% · MA50 -17.7% · MA200 -33.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (823070 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
