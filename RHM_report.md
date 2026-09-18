# RHM

**Generated** : 2026-09-18T21:36:30.759774+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1011.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1011.80 (+2.0% vs entrée) · entrée €991.98 · stop €972.14 · T1 €1004.25 · R/R 0.62  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.109 _(réel 5 s)_ (GBM 0.062) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €989.52–€994.43 (mid €991.98)
- Spot actuel : €1011.80 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €972.14 (stop swing_plan-based (-8.08%))
- Targets : T1 €1004.25 · R/R 0.62 | T2 €1016.52 · R/R 1.24 | T3 €1028.80 · R/R 1.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €972.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.08 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1273).
   - exécution **14.349 pt plus bas** dans le cas TYPIQUE (médiane), 14.349 au p90, **14.349 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 8.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0113 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.574 % | p01 -3.747 % | pire -22.429 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3521** [0.2839 ; 0.4252] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.4029** [0.3522 ; 0.4552] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.4057** [0.3549 ; 0.4581] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 8.2 observations effectives », dont la borne haute a 95 % vaut environ 36.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.6 pt), swing (55.1 pt), deep (56.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.07 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.94 % contre 3.26 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5321** (β de hausse 0.5812, asymétrie 0.9155) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.22× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 901.4032 sur support (2.18 ATR, 10.911 %) — p(stop avant cible) 0.2588 [0.21 ; 0.31], R/R 2.303, perte reelle 22.429 % (gap inclus), CVaR 10.92 %, EV -3.8215 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 42.1 % de la queue et il ne reste que -112.43 EUR a partager. Prix du risque -0.036 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.657 %) — p(stop avant cible) 0.5826 [0.53 ; 0.63], R/R 4.264, perte reelle 12.114 % (gap inclus), EV -4.2706 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.583, borne haute 0.634 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.27 %) : P(cible) 0.0 % x 51.65 % + P(rien) 41.7 % x 6.66 % ne couvrent pas P(stop) 58.3 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.14 ATR (stop 7.0 %) — p(stop avant cible) 0.4761 [0.42 ; 0.53], R/R 3.411, perte reelle 15.141 % (gap inclus), EV -4.3929 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.39 %) : P(cible) 0.0 % x 51.65 % + P(rien) 52.4 % x 5.37 % ne couvrent pas P(stop) 47.6 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.18 ATR (stop 10.911 %) — p(stop avant cible) 0.2588 [0.21 ; 0.31], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -3.8215 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.82 %) : P(cible) 0.0 % x 51.65 % + P(rien) 74.1 % x 2.67 % ne couvrent pas P(stop) 25.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.943 %) — p(stop avant cible) 0.9326 [0.90 ; 0.96], R/R 22.763, perte reelle 2.269 % (gap inclus), EV -1.3667 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 22.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.933, borne haute 0.956 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 0.0 % x 51.65 % + P(rien) 6.7 % x 11.12 % ne couvrent pas P(stop) 93.3 % x 2.27 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.886 %) — p(stop avant cible) 0.8526 [0.81 ; 0.89], R/R 14.88, perte reelle 3.471 % (gap inclus), EV -1.3579 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.853, borne haute 0.887 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 0.0 % x 51.65 % + P(rien) 14.7 % x 10.87 % ne couvrent pas P(stop) 85.3 % x 3.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.828 %) — p(stop avant cible) 0.7833 [0.74 ; 0.82], R/R 10.89, perte reelle 4.743 % (gap inclus), EV -1.6537 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 0.0 % x 51.65 % + P(rien) 21.7 % x 9.52 % ne couvrent pas P(stop) 78.3 % x 4.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.18 ATR (stop 9.335 %) — p(stop avant cible) 0.3474 [0.30 ; 0.40], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -5.3602 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.36 %) : P(cible) 0.0 % x 51.65 % + P(rien) 65.2 % x 3.72 % ne couvrent pas P(stop) 34.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.371 %) — p(stop avant cible) 0.2945 [0.25 ; 0.34], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -4.467 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.47 %) : P(cible) 0.0 % x 51.65 % + P(rien) 70.5 % x 3.02 % ne couvrent pas P(stop) 29.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 13.199 %) — p(stop avant cible) 0.1777 [0.14 ; 0.22], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -2.6576 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.66 %) : P(cible) 0.0 % x 51.65 % + P(rien) 82.2 % x 1.61 % ne couvrent pas P(stop) 17.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 15.085 %) — p(stop avant cible) 0.1343 [0.10 ; 0.17], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -1.992 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 0.0 % x 51.65 % + P(rien) 86.6 % x 1.17 % ne couvrent pas P(stop) 13.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 16.97 %) — p(stop avant cible) 0.0939 [0.07 ; 0.13], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -1.5544 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.55 %) : P(cible) 0.0 % x 51.65 % + P(rien) 90.6 % x 0.60 % ne couvrent pas P(stop) 9.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 18.856 %) — p(stop avant cible) 0.0598 [0.04 ; 0.09], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -1.2543 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.0 % x 51.65 % + P(rien) 94.0 % x 0.09 % ne couvrent pas P(stop) 6.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 20.742 %) — p(stop avant cible) 0.0427 [0.03 ; 0.07], R/R 2.303, perte reelle 22.429 % (gap inclus), EV -1.1448 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.0 % x 51.65 % + P(rien) 95.7 % x -0.20 % ne couvrent pas P(stop) 4.3 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 22.627 %) — p(stop avant cible) 0.0181 [0.01 ; 0.04], R/R 2.283, perte reelle 22.627 % (gap inclus), EV -0.8526 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 0.0 % x 51.65 % + P(rien) 98.2 % x -0.46 % ne couvrent pas P(stop) 1.8 % x 22.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 24.513 %) — p(stop avant cible) 0.0105 [0.00 ; 0.03], R/R 2.107, perte reelle 24.513 % (gap inclus), EV -0.8427 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 0.0 % x 51.65 % + P(rien) 98.9 % x -0.60 % ne couvrent pas P(stop) 1.1 % x 24.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 26.398 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 1.957, perte reelle 26.398 % (gap inclus), EV -0.8499 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 0.0 % x 51.65 % + P(rien) 99.4 % x -0.69 % ne couvrent pas P(stop) 0.6 % x 26.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 28.284 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 1.826, perte reelle 28.284 % (gap inclus), EV -0.8055 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.0 % x 51.65 % + P(rien) 99.5 % x -0.67 % ne couvrent pas P(stop) 0.5 % x 28.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 30.17 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.712, perte reelle 30.17 % (gap inclus), EV -0.7304 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 0.0 % x 51.65 % + P(rien) 99.8 % x -0.67 % ne couvrent pas P(stop) 0.2 % x 30.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1011.8, ATR14 38.1571 (3.771 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.393 ATR = 1.482 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 1009.8921 | 89.54 % | 92.19 % | 93.37 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.377 % | 1007.9843 | 83.51 % | 87.94 % | 89.81 % | 91.38 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.566 % | 1006.0764 | 76.51 % | 83.1 % | 85.76 % | 88.31 % | 92.93 % | 94.77 % |
| 0.2 ATR | 0.754 % | 1004.1686 | 69.79 % | 78.56 % | 81.6 % | 85.23 % | 90.94 % | 93.16 % |
| 0.25 ATR | 0.943 % | 1002.2607 | 62.29 % | 72.83 % | 76.76 % | 81.27 % | 88.45 % | 91.35 % |
| 0.35 ATR | 1.32 % | 998.445 | 53.8 % | 65.91 % | 71.32 % | 76.81 % | 85.86 % | 89.24 % |
| 0.5 ATR | 1.886 % | 992.7214 | 40.47 % | 55.04 % | 61.82 % | 69.28 % | 80.28 % | 83.8 % |
| 0.75 ATR | 2.828 % | 983.1821 | 23.69 % | 39.13 % | 47.38 % | 57.68 % | 70.52 % | 77.06 % |
| 1.0 ATR | 3.771 % | 973.6428 | 13.13 % | 26.68 % | 36.5 % | 48.56 % | 62.45 % | 70.52 % |
| 1.25 ATR | 4.714 % | 964.1036 | 7.4 % | 17.98 % | 26.41 % | 39.25 % | 54.38 % | 64.19 % |
| 1.5 ATR | 5.657 % | 954.5643 | 3.95 % | 13.14 % | 20.67 % | 31.91 % | 46.12 % | 56.94 % |
| 2.0 ATR | 7.542 % | 935.4857 | 1.78 % | 7.02 % | 12.17 % | 21.01 % | 34.46 % | 47.08 % |
| 2.5 ATR | 9.428 % | 916.4071 | 0.49 % | 3.36 % | 6.33 % | 12.49 % | 25.0 % | 37.63 % |
| 3.0 ATR | 11.314 % | 897.3286 | 0.1 % | 1.38 % | 3.86 % | 7.73 % | 17.43 % | 31.49 % |
| 4.0 ATR | 15.085 % | 859.1714 | 0.0 % | 0.3 % | 1.29 % | 3.27 % | 8.67 % | 20.22 % |
| 6.0 ATR | 22.627 % | 782.8572 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.14 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.28 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.81 ATR | 1.09 ATR | 1.31 ATR | 1.54 ATR | 2.19 ATR | 2.77 ATR |
| **5 s.** | 0.39 ATR | 0.96 ATR | 1.10 ATR | 1.46 ATR | 1.82 ATR | 2.06 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.64 ATR | 1.38 ATR | 1.55 ATR | 2.08 ATR | 2.50 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.83 ATR | 1.85 ATR | 2.11 ATR | 2.88 ATR | 3.58 ATR | 4.03 ATR | 5.22 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.449–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.658–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.828 %, prix 983.1863), p(touche) 39.13 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.771 %, prix 973.645), p(touche) 36.5 % (en stress 95.1 %)  ✅ optimum identifie (63.8 % des re-echantillons)
- **5 seance(s)** : plage utile 1.096–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.714 %, prix 964.1037), p(touche) 39.25 % (en stress 98.02 %)  ✅ optimum identifie (88.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.548–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.542 %, prix 935.49), p(touche) 34.46 % (en stress 96.04 %)  ✅ optimum identifie (99.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.11–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.428 %, prix 916.4075), p(touche) 37.63 % (en stress 98.0 %)  ✅ optimum identifie (99.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.062 | EV/share : €1.232 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 37 % | T3 19 %
- Kelly (position) : f* 0.113 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.6 | bear 7.2 | side 8.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.959% → cible +1.237% / stop −2.0%, p_fill 51%, n_eff≈18.5) : P(cible|rempli) **31%** · **EV/risk -0.109** (×p_fill ; si rempli -0.42% du capital)
  - **swing** (entrée dip −4.309% → cible +2.767% / stop −3.941%, p_fill 23%, n_eff≈8.2) : P(cible|rempli) **29%** · **EV/risk -0.122** (×p_fill ; si rempli -2.12% du capital)
  - **deep** (entrée dip −6.663% → cible +3.913% / stop −6.061%, p_fill 20%, n_eff≈8.3) : P(cible|rempli) **66%** · **EV/risk +0.025** (×p_fill ; si rempli +0.75% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 27.0  _(survente)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist -6.374  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 22.3%
- **ATR** : 38.16 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.23  _(distribution)_
- **Vol ratio** : 1.97  _(volume au-dessus de la moyenne)_
- **Choppiness** : 41.0  _(transition)_
- **MA** : MA20 1069.64 · MA50 1087.13 · MA200 1365.7  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 -6.9% · MA200 -25.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843152 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
