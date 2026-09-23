# RHM

**Generated** : 2026-09-23T21:36:32.412470+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1025.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1025.00 (+1.9% vs entrée) · entrée €1005.50 · stop €985.39 · T1 €1018.45 · R/R 0.64  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.144 _(réel 5 s)_ (GBM 0.064) · ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1002.91–€1008.09 (mid €1005.50)
- Spot actuel : €1025.00 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €985.39 (stop swing_plan-based (-7.6%))
- Targets : T1 €1018.45 · R/R 0.64 | T2 €1031.40 · R/R 1.29 | T3 €1044.35 · R/R 1.93
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €985.39


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.6 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **7.541 pt plus bas** dans le cas TYPIQUE (médiane), 13.372 au p90, **14.829 au pire**
   - perte réelle **15.141 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 7.6 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0118 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.574 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3364** [0.2692 ; 0.409] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.4433** [0.3916 ; 0.496] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4529** [0.401 ; 0.5056] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 9.0 observations effectives », dont la borne haute a 95 % vaut environ 33.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.7 pt), swing (54.6 pt), deep (57.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.07 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.95 % contre 3.14 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5319** (β de hausse 0.5811, asymétrie 0.9153) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.142× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 905.9637 sur support (2.75 ATR, 11.613 %) — p(stop avant cible) 0.237 [0.19 ; 0.28], R/R 1.187, perte reelle 22.429 % (gap inclus), CVaR 11.621 %, EV -3.5372 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 46.9 % de la queue et il ne reste que -384.52 EUR a partager. Prix du risque -0.123 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.118 %) — p(stop avant cible) 0.6197 [0.57 ; 0.67], R/R 2.197, perte reelle 12.114 % (gap inclus), EV -4.8177 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.620, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.82 %) : P(cible) 0.6 % x 26.62 % + P(rien) 37.4 % x 6.74 % ne couvrent pas P(stop) 62.0 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.6 ATR (stop 7.691 %) — p(stop avant cible) 0.4357 [0.38 ; 0.49], R/R 1.758, perte reelle 15.141 % (gap inclus), EV -3.956 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.96 %) : P(cible) 1.0 % x 26.62 % + P(rien) 55.4 % x 4.27 % ne couvrent pas P(stop) 43.6 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.33 ATR (stop 10.179 %) — p(stop avant cible) 0.2999 [0.25 ; 0.35], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -4.6447 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.64 %) : P(cible) 1.1 % x 26.62 % + P(rien) 68.9 % x 2.58 % ne couvrent pas P(stop) 30.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.75 ATR (stop 11.613 %) — p(stop avant cible) 0.237 [0.19 ; 0.28], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -3.5372 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.54 %) : P(cible) 1.1 % x 26.62 % + P(rien) 75.1 % x 1.96 % ne couvrent pas P(stop) 23.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.853 %) — p(stop avant cible) 0.9349 [0.91 ; 0.96], R/R 12.555, perte reelle 2.12 % (gap inclus), EV -1.2394 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 12.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.935, borne haute 0.957 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 0.3 % x 26.62 % + P(rien) 6.2 % x 10.67 % ne couvrent pas P(stop) 93.5 % x 2.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.706 %) — p(stop avant cible) 0.8705 [0.83 ; 0.90], R/R 8.149, perte reelle 3.266 % (gap inclus), EV -1.3551 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.871, borne haute 0.903 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 0.4 % x 26.62 % + P(rien) 12.5 % x 10.98 % ne couvrent pas P(stop) 87.1 % x 3.27 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.559 %) — p(stop avant cible) 0.8086 [0.76 ; 0.85], R/R 5.962, perte reelle 4.464 % (gap inclus), EV -1.6186 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.809, borne haute 0.847 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.62 %) : P(cible) 0.6 % x 26.62 % + P(rien) 18.6 % x 9.88 % ne couvrent pas P(stop) 80.9 % x 4.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.412 %) — p(stop avant cible) 0.7248 [0.68 ; 0.77], R/R 4.706, perte reelle 5.656 % (gap inclus), EV -1.7374 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.725, borne haute 0.770 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 0.6 % x 26.62 % + P(rien) 26.9 % x 8.19 % ne couvrent pas P(stop) 72.5 % x 5.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.265 %) — p(stop avant cible) 0.6662 [0.62 ; 0.71], R/R 3.765, perte reelle 7.069 % (gap inclus), EV -2.1376 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.666, borne haute 0.714 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 0.6 % x 26.62 % + P(rien) 32.8 % x 7.36 % ne couvrent pas P(stop) 66.6 % x 7.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.6 ATR (stop 6.486 %) — p(stop avant cible) 0.5026 [0.45 ; 0.56], R/R 1.758, perte reelle 15.141 % (gap inclus), EV -4.9353 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.503, borne haute 0.555 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.94 %) : P(cible) 1.0 % x 26.62 % + P(rien) 48.7 % x 4.92 % ne couvrent pas P(stop) 50.3 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.33 ATR (stop 8.974 %) — p(stop avant cible) 0.3668 [0.32 ; 0.42], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -5.8104 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.81 %) : P(cible) 1.1 % x 26.62 % + P(rien) 62.2 % x 3.42 % ne couvrent pas P(stop) 36.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.647 %) — p(stop avant cible) 0.1569 [0.12 ; 0.20], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -2.3837 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.38 %) : P(cible) 1.1 % x 26.62 % + P(rien) 83.2 % x 1.00 % ne couvrent pas P(stop) 15.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.353 %) — p(stop avant cible) 0.1312 [0.10 ; 0.17], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -2.0272 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.03 %) : P(cible) 1.1 % x 26.62 % + P(rien) 85.7 % x 0.71 % ne couvrent pas P(stop) 13.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 17.059 %) — p(stop avant cible) 0.0894 [0.06 ; 0.12], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -1.5783 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 1.1 % x 26.62 % + P(rien) 89.9 % x 0.13 % ne couvrent pas P(stop) 8.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 18.765 %) — p(stop avant cible) 0.0584 [0.04 ; 0.09], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -1.3064 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 1.1 % x 26.62 % + P(rien) 93.0 % x -0.33 % ne couvrent pas P(stop) 5.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 20.471 %) — p(stop avant cible) 0.0417 [0.02 ; 0.07], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -1.1997 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 1.1 % x 26.62 % + P(rien) 94.7 % x -0.60 % ne couvrent pas P(stop) 4.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 22.177 %) — p(stop avant cible) 0.0218 [0.01 ; 0.04], R/R 1.187, perte reelle 22.429 % (gap inclus), EV -0.9666 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 1.1 % x 26.62 % + P(rien) 96.7 % x -0.81 % ne couvrent pas P(stop) 2.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 23.883 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.114, perte reelle 23.883 % (gap inclus), EV -0.8994 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 1.1 % x 26.62 % + P(rien) 97.8 % x -0.98 % ne couvrent pas P(stop) 1.0 % x 23.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 25.589 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 1.04, perte reelle 25.589 % (gap inclus), EV -0.9081 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 1.1 % x 26.62 % + P(rien) 98.2 % x -1.07 % ne couvrent pas P(stop) 0.6 % x 25.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 27.295 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 0.975, perte reelle 27.295 % (gap inclus), EV -0.8642 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 1.1 % x 26.62 % + P(rien) 98.4 % x -1.05 % ne couvrent pas P(stop) 0.5 % x 27.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1025.0, ATR14 34.9714 (3.412 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.393 ATR = 1.341 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 1023.2514 | 89.55 % | 92.2 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.341 % | 1021.5029 | 83.53 % | 87.96 % | 89.82 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.512 % | 1019.7543 | 76.53 % | 83.12 % | 85.77 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.682 % | 1018.0057 | 69.92 % | 78.68 % | 81.72 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.853 % | 1016.2571 | 62.43 % | 72.95 % | 76.78 % | 81.19 % | 88.46 % | 91.36 % |
| 0.35 ATR | 1.194 % | 1012.76 | 53.85 % | 66.04 % | 71.34 % | 76.73 % | 85.87 % | 89.25 % |
| 0.5 ATR | 1.706 % | 1007.5143 | 40.43 % | 54.99 % | 61.76 % | 69.21 % | 80.3 % | 83.82 % |
| 0.75 ATR | 2.559 % | 998.7714 | 23.57 % | 39.09 % | 47.33 % | 57.62 % | 70.65 % | 77.09 % |
| 1.0 ATR | 3.412 % | 990.0286 | 13.02 % | 26.55 % | 36.36 % | 48.61 % | 62.59 % | 70.55 % |
| 1.25 ATR | 4.265 % | 981.2857 | 7.4 % | 17.87 % | 26.28 % | 39.21 % | 54.53 % | 64.22 % |
| 1.5 ATR | 5.118 % | 972.5429 | 3.94 % | 13.13 % | 20.65 % | 31.88 % | 46.27 % | 57.09 % |
| 2.0 ATR | 6.824 % | 955.0572 | 1.78 % | 7.01 % | 12.15 % | 20.99 % | 34.53 % | 47.24 % |
| 2.5 ATR | 8.53 % | 937.5714 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 25.07 % | 37.79 % |
| 3.0 ATR | 10.236 % | 920.0857 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 31.86 % |
| 4.0 ATR | 13.647 % | 885.1143 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.2 % |
| 6.0 ATR | 20.471 % | 815.1715 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.04 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.54 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.39 ATR | 0.96 ATR | 1.10 ATR | 1.46 ATR | 1.82 ATR | 2.06 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.64 ATR | 1.39 ATR | 1.55 ATR | 2.08 ATR | 2.50 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.12 ATR | 2.90 ATR | 3.59 ATR | 4.02 ATR | 5.22 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.449–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.657–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.559 %, prix 998.7703), p(touche) 39.09 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.412 %, prix 990.027), p(touche) 36.36 % (en stress 95.1 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.096–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.265 %, prix 981.2838), p(touche) 39.21 % (en stress 98.02 %)  ✅ optimum identifie (87.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.554–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.824 %, prix 955.054), p(touche) 34.53 % (en stress 96.04 %)  ✅ optimum identifie (99.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.119–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.53 %, prix 937.5675), p(touche) 37.79 % (en stress 98.0 %)  ✅ optimum identifie (99.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.064 | EV/share : €1.293 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 35 % | T3 17 %
- Kelly (position) : f* 0.108 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.7 | bear 7.1 | side 8.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.898% → cible +1.288% / stop −2.0%, p_fill 52%, n_eff≈18.7) : P(cible|rempli) **28%** · **EV/risk -0.144** (×p_fill ; si rempli -0.56% du capital)
  - **swing** (entrée dip −4.188% → cible +2.88% / stop −3.561%, p_fill 24%, n_eff≈9.0) : P(cible|rempli) **33%** · **EV/risk -0.108** (×p_fill ; si rempli -1.60% du capital)
  - **deep** (entrée dip −6.472% → cible +4.072% / stop −5.472%, p_fill 22%, n_eff≈9.0) : P(cible|rempli) **31%** · **EV/risk -0.079** (×p_fill ; si rempli -2.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→69% · +2.0%→48% · +3.0%→30% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.92% (p90 6.55%) · excursion haute méd. +1.95% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.505% vs midi 0.939% vs clôture 1.046% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. -0.593% ; recovery-V 19%
- **σ réalisé intraday** 2.514% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 61% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 1053.3925 (VA 1037.4725–1057.3725 ; dernier close 1033.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 26% · rebond 47% · **stop −2.28%** sous le fill (sous le bruit) · cible +0.96% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 30% (gap-down >1% 8% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −1.97%) · haut méd +0.43% · range méd 1.33%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.06%) · haut méd +0.57% · range méd 1.69%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −2.22%) · haut méd +0.72% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −2.63%) · haut méd +0.86% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1034.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 71% (105/159) · gap 18% · délai 0.9min · rebond 51% (54/105) (MFE +1.01%)
   - −1.0% : fill 30min 42% · séance 65% (93/159) · gap 8% · délai 5.7min · rebond 59% (55/93) (MFE +1.18%)
   - −1.5% : fill 30min 23% · séance 50% (76/159) · gap 6% · délai 33.2min · rebond 53% (42/76) (MFE +1.15%)
   - −2.0% : fill 30min 16% · séance 43% (65/159) · gap 3% · délai 65.8min · rebond 57% (38/65) (MFE +1.2%)
   - −3.0% : fill 30min 6% · séance 26% (35/159) · gap 3% · délai 224.3min · rebond 47% (17/35) (MFE +0.96%)
   - −4.0% : fill 30min 3% · séance 12% (22/159) · gap 2% · délai 170.8min · rebond 69% (13/22) (MFE +1.66%)
   - −5.0% : fill 30min 1% · séance 7% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −1.47%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.71%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.74%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=539 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~7.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 96% (32/33) · rebond 73% (23/32)
      · −2.0% : fill 78% (27/33) · rebond 58% (17/27)
      · −3.0% : fill 45% (13/33) · rebond 48% (7/13)
      · −4.0% : fill 31% (10/33) · rebond 72% (7/10)
      · −5.0% : fill 21% (7/33) · rebond 100% (7/7)
   - **flat** (21 séances) :
      · −1.0% : fill 86% (15/21) · rebond 64% (11/15)
      · −2.0% : fill 47% (8/21) · rebond 71% (6/8)
      · −3.0% : fill 26% (4/21) · rebond 37% (1/4)
      · −4.0% : fill 8% (2/21) · rebond 62% (1/2)
      · −5.0% : fill 8% (2/21) · rebond 62% (1/2)
   - **gap-up** (105 séances) :
      · −1.0% : fill 48% (46/105) · rebond 46% (21/46)
      · −2.0% : fill 30% (30/105) · rebond 49% (15/30)
      · −3.0% : fill 19% (18/105) · rebond 50% (9/18)
      · −4.0% : fill 7% (10/105) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/105) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 57% si les 15 1res min sont vertes (73 cas) · 34% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **47min** → P(séance verte=clôture>ouverture) 66% si début vert vs 25% si rouge (base 44% · écart 41 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **66%** · continue >prix actuel 45% ; creux résiduel méd -1.28% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +2.23% → **scale +1.65% / runner +2.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **25%** (continue à baisser 58%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.83%** (au-delà de la MAE q10 -3.83%), cible rebond +1.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.58% .. +3.13%] · haut q95 +3.42% · bas q05 -2.96%
   - 60min (n=160) : retour [-2.7% .. +3.15%] · haut q95 +4.2% · bas q05 -3.67%
   - 2h (n=160) : retour [-3.26% .. +2.84%] · haut q95 +4.34% · bas q05 -4.04%
   - 4h (n=160) : retour [-3.25% .. +2.99%] · haut q95 +4.73% · bas q05 -4.52%
   - 6h (n=160) : retour [-3.97% .. +3.17%] · haut q95 +4.8% · bas q05 -4.76%
   - session (n=160) : retour [-4.23% .. +3.53%] · haut q95 +4.94% · bas q05 -5.45%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 41.5  _(momentum baissier)_
- **ADX** : 24.6  _(pas de tendance nette)_
- **MACD** : hist -0.276  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 20.1%
- **ATR** : 34.97 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.241  _(distribution)_
- **Vol ratio** : 1.0  _(volume normal)_
- **Choppiness** : 61.9  _(marche en range (choppy))_
- **MA** : MA20 1044.92 · MA50 1089.45 · MA200 1355.82  _(prix < MA20)_
- **Dist MA** : MA20 -1.9% · MA50 -5.9% · MA200 -24.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (884849 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
