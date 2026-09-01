# RHM

**Generated** : 2026-09-01T21:36:10.307788+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1079.80  

> 🟡 **WAIT-FOR-DIP** — spot +8.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1079.80 (+8.1% vs entrée) · entrée €998.78 · stop €960.17 · T1 €1023.96 · R/R 0.65  
> ↳ P(T1 av. stop) 79 % · EV/risk 0.24 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €993.75–€1003.82 (mid €998.78)
- Spot actuel : €1079.80 (+8.1% au-dessus de la zone — repli à attendre)
- Stop : €960.17 (stop swing_plan-based (-11.08%))
- Targets : T1 €1023.96 · R/R 0.65 | T2 €1049.14 · R/R 1.3 | T3 €1074.31 · R/R 1.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €960.17


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.08 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **11.349 pt plus bas** dans le cas TYPIQUE (médiane), 11.349 au p90, **11.349 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 11.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0089 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.327** [0.2604 ; 0.3993] _(largeur 13.9 pt, n_eff 173.1)_
   - swing : **0.3789** [0.329 ; 0.4309] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3681** [0.3185 ; 0.4199] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.86 %** | CVaR **-6.73 %** | vol 2.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.98 % contre 3.27 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.61 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.847 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5069** (β de hausse 0.5828, asymétrie 0.8697) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.294× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 963.9572 sur atr_grid (3.0 ATR, 10.728 %) — p(stop avant cible) 0.2497 [0.21 ; 0.30], R/R 0.896, perte reelle 22.429 % (gap inclus), CVaR 10.737 %, EV -3.0384 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 18 des 18 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 60.2 % de la queue et il ne reste que -755.68 EUR a partager. Prix du risque -0.422 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.364 %) — p(stop avant cible) 0.5625 [0.51 ; 0.61], R/R 1.658, perte reelle 12.114 % (gap inclus), EV -3.6889 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.562, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.69 %) : P(cible) 7.5 % x 20.09 % + P(rien) 36.2 % x 4.46 % ne couvrent pas P(stop) 56.2 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.91 ATR (stop 16.248 %) — p(stop avant cible) 0.1074 [0.08 ; 0.14], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -0.9471 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 8.3 % x 20.09 % + P(rien) 80.9 % x -0.27 % ne couvrent pas P(stop) 10.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.894 %) — p(stop avant cible) 0.9275 [0.90 ; 0.95], R/R 9.148, perte reelle 2.196 % (gap inclus), EV -1.0781 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 9.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.927, borne haute 0.951 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 2.9 % x 20.09 % + P(rien) 4.4 % x 8.73 % ne couvrent pas P(stop) 92.8 % x 2.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.788 %) — p(stop avant cible) 0.8466 [0.81 ; 0.88], R/R 5.945, perte reelle 3.379 % (gap inclus), EV -0.9992 % — **REFUSE**
      - refuse : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 4.7 % x 20.09 % + P(rien) 10.6 % x 8.59 % ne couvrent pas P(stop) 84.7 % x 3.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.682 %) — p(stop avant cible) 0.7887 [0.74 ; 0.83], R/R 4.437, perte reelle 4.528 % (gap inclus), EV -1.1988 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.789, borne haute 0.829 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 5.5 % x 20.09 % + P(rien) 15.6 % x 8.11 % ne couvrent pas P(stop) 78.9 % x 4.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.576 %) — p(stop avant cible) 0.6815 [0.63 ; 0.73], R/R 3.552, perte reelle 5.656 % (gap inclus), EV -1.0304 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 6.5 % x 20.09 % + P(rien) 25.4 % x 6.01 % ne couvrent pas P(stop) 68.2 % x 5.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.47 %) — p(stop avant cible) 0.6174 [0.57 ; 0.67], R/R 2.557, perte reelle 7.856 % (gap inclus), EV -1.7766 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.78 %) : P(cible) 7.4 % x 20.09 % + P(rien) 30.9 % x 5.15 % ne couvrent pas P(stop) 61.7 % x 7.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.258 %) — p(stop avant cible) 0.4929 [0.44 ; 0.55], R/R 1.327, perte reelle 15.141 % (gap inclus), EV -4.3055 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.31 %) : P(cible) 7.8 % x 20.09 % + P(rien) 43.0 % x 3.72 % ne couvrent pas P(stop) 49.3 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.152 %) — p(stop avant cible) 0.4223 [0.37 ; 0.47], R/R 1.327, perte reelle 15.141 % (gap inclus), EV -3.2682 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.27 %) : P(cible) 7.9 % x 20.09 % + P(rien) 49.9 % x 3.09 % ne couvrent pas P(stop) 42.2 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.046 %) — p(stop avant cible) 0.39 [0.34 ; 0.44], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -5.6802 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.68 %) : P(cible) 7.9 % x 20.09 % + P(rien) 53.1 % x 2.79 % ne couvrent pas P(stop) 39.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.94 %) — p(stop avant cible) 0.3423 [0.29 ; 0.39], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -4.72 % — **REFUSE**
      - refuse : cible atteinte seulement 8.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.72 %) : P(cible) 8.1 % x 20.09 % + P(rien) 57.7 % x 2.31 % ne couvrent pas P(stop) 34.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.834 %) — p(stop avant cible) 0.2945 [0.25 ; 0.34], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -3.8562 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.86 %) : P(cible) 8.2 % x 20.09 % + P(rien) 62.4 % x 1.78 % ne couvrent pas P(stop) 29.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.728 %) — p(stop avant cible) 0.2497 [0.21 ; 0.30], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -3.0384 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.04 %) : P(cible) 8.3 % x 20.09 % + P(rien) 66.8 % x 1.35 % ne couvrent pas P(stop) 25.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.516 %) — p(stop avant cible) 0.1982 [0.16 ; 0.24], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -2.1804 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 8.3 % x 20.09 % + P(rien) 71.8 % x 0.82 % ne couvrent pas P(stop) 19.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.91 ATR (stop 15.057 %) — p(stop avant cible) 0.1318 [0.10 ; 0.17], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -1.2173 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 8.3 % x 20.09 % + P(rien) 78.5 % x 0.08 % ne couvrent pas P(stop) 13.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 17.88 %) — p(stop avant cible) 0.0773 [0.05 ; 0.11], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -0.6397 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 8.3 % x 20.09 % + P(rien) 83.9 % x -0.70 % ne couvrent pas P(stop) 7.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 19.668 %) — p(stop avant cible) 0.0577 [0.04 ; 0.09], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -0.4854 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 8.3 % x 20.09 % + P(rien) 85.9 % x -1.01 % ne couvrent pas P(stop) 5.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 21.456 %) — p(stop avant cible) 0.0367 [0.02 ; 0.06], R/R 0.896, perte reelle 22.429 % (gap inclus), EV -0.2844 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 8.3 % x 20.09 % + P(rien) 88.0 % x -1.29 % ne couvrent pas P(stop) 3.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 23.244 %) — p(stop avant cible) 0.015 [0.01 ; 0.03], R/R 0.864, perte reelle 23.244 % (gap inclus), EV -0.1045 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 8.3 % x 20.09 % + P(rien) 90.1 % x -1.59 % ne couvrent pas P(stop) 1.5 % x 23.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 25.032 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 0.803, perte reelle 25.032 % (gap inclus), EV -0.0903 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 8.3 % x 20.09 % + P(rien) 91.0 % x -1.75 % ne couvrent pas P(stop) 0.7 % x 25.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 26.82 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.749, perte reelle 26.82 % (gap inclus), EV -0.0681 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 8.3 % x 20.09 % + P(rien) 91.0 % x -1.74 % ne couvrent pas P(stop) 0.6 % x 26.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 28.608 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.702, perte reelle 28.608 % (gap inclus), EV -0.0511 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 8.3 % x 20.09 % + P(rien) 91.1 % x -1.73 % ne couvrent pas P(stop) 0.5 % x 28.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1079.8, ATR14 38.6143 (3.576 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.392 ATR = 1.402 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.179 % | 1077.8693 | 89.25 % | 92.1 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.358 % | 1075.9386 | 83.23 % | 87.76 % | 89.72 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.536 % | 1074.0079 | 76.23 % | 82.92 % | 85.67 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.715 % | 1072.0772 | 69.72 % | 78.48 % | 81.62 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.894 % | 1070.1465 | 62.23 % | 72.66 % | 76.58 % | 81.09 % | 88.36 % | 91.36 % |
| 0.35 ATR | 1.252 % | 1066.285 | 53.75 % | 65.75 % | 71.05 % | 76.63 % | 85.77 % | 89.25 % |
| 0.5 ATR | 1.788 % | 1060.4929 | 40.24 % | 54.59 % | 61.36 % | 68.91 % | 80.1 % | 83.62 % |
| 0.75 ATR | 2.682 % | 1050.8393 | 23.57 % | 38.89 % | 46.94 % | 57.33 % | 70.25 % | 76.88 % |
| 1.0 ATR | 3.576 % | 1041.1858 | 13.02 % | 26.55 % | 35.97 % | 48.12 % | 62.09 % | 70.35 % |
| 1.25 ATR | 4.47 % | 1031.5322 | 7.4 % | 17.97 % | 26.19 % | 38.71 % | 53.93 % | 63.82 % |
| 1.5 ATR | 5.364 % | 1021.8786 | 3.94 % | 13.03 % | 20.45 % | 31.29 % | 45.67 % | 56.58 % |
| 2.0 ATR | 7.152 % | 1002.5715 | 1.78 % | 6.91 % | 11.96 % | 20.59 % | 33.93 % | 46.73 % |
| 2.5 ATR | 8.94 % | 983.2643 | 0.49 % | 3.36 % | 6.23 % | 12.48 % | 24.68 % | 37.49 % |
| 3.0 ATR | 10.728 % | 963.9572 | 0.1 % | 1.38 % | 3.85 % | 7.52 % | 16.92 % | 30.85 % |
| 4.0 ATR | 14.304 % | 925.3429 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.46 % | 19.8 % |
| 6.0 ATR | 21.456 % | 848.1143 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.57 ATR | 0.65 ATR | 0.87 ATR | 1.04 ATR | 1.19 ATR | 1.75 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.79 ATR | 1.08 ATR | 1.30 ATR | 1.53 ATR | 2.17 ATR | 2.76 ATR |
| **5 s.** | 0.38 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.79 ATR | 2.04 ATR | 2.75 ATR | 3.59 ATR |
| **10 s.** | 0.63 ATR | 1.37 ATR | 1.53 ATR | 2.05 ATR | 2.48 ATR | 2.80 ATR | 3.82 ATR | 4.90 ATR |
| **20 s.** | 0.82 ATR | 1.83 ATR | 2.09 ATR | 2.84 ATR | 3.53 ATR | 3.98 ATR | 5.20 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.447–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.653–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.682 %, prix 1050.8398), p(touche) 38.89 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.794–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.576 %, prix 1041.1864), p(touche) 35.97 % (en stress 95.1 %)  ✅ optimum identifie (68.5 % des re-echantillons)
- **5 seance(s)** : plage utile 1.083–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.47 %, prix 1031.533), p(touche) 38.71 % (en stress 98.02 %)  ✅ optimum identifie (88.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.529–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.152 %, prix 1002.5727), p(touche) 33.93 % (en stress 96.04 %)  ✅ optimum identifie (99.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.094–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.94 %, prix 983.2659), p(touche) 37.49 % (en stress 98.0 %)  ✅ optimum identifie (98.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.03 | EV/share : €-1.170 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 36 % | T3 24 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 78.6 | bear 15.7 | side 5.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=17, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.07% (p90 6.55%) · excursion haute méd. +2.05% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.562% vs midi 0.933% vs clôture 1.056% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.318% ; recovery-V 23%
- **σ réalisé intraday** 2.525% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 58% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 1136.985 (VA 1134.565–1145.455 ; dernier close 1115.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 41% · rebond 61% · **stop −2.91%** sous le fill (sous le bruit) · cible +1.42% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. 0.55% · baisse 28% (gap-down >1% 9% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.74%) · haut méd +0.49% · range méd 1.33%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −1.96%) · haut méd +0.6% · range méd 1.69%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.16%) · haut méd +0.78% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −1.06% (p90 −2.53%) · haut méd +0.89% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1110.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 69% (105/159) · gap 20% · délai 1.0min · rebond 54% (56/105) (MFE +1.07%)
   - −1.0% : fill 30min 39% · séance 62% (93/159) · gap 9% · délai 7.8min · rebond 63% (56/93) (MFE +1.25%)
   - −1.5% : fill 30min 23% · séance 49% (77/159) · gap 6% · délai 30.5min · rebond 59% (44/77) (MFE +1.33%)
   - −2.0% : fill 30min 16% · séance 41% (65/159) · gap 4% · délai 68.0min · rebond 61% (40/65) (MFE +1.42%)
   - −3.0% : fill 30min 6% · séance 22% (33/159) · gap 3% · délai 191.2min · rebond 42% (16/33) (MFE +0.92%)
   - −4.0% : fill 30min 4% · séance 13% (23/159) · gap 2% · délai 174.9min · rebond 69% (14/23) (MFE +1.69%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −1.47%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.7%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.74%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=540 jambes) : jambe baissière méd −1.04% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (34 séances) :
      · −1.0% : fill 96% (33/34) · rebond 80% (25/33)
      · −2.0% : fill 76% (28/34) · rebond 66% (19/28)
      · −3.0% : fill 40% (13/34) · rebond 60% (8/13)
      · −4.0% : fill 34% (11/34) · rebond 72% (8/11)
      · −5.0% : fill 23% (7/34) · rebond 100% (7/7)
   - **flat** (19 séances) :
      · −1.0% : fill 82% (13/19) · rebond 68% (10/13)
      · −2.0% : fill 46% (7/19) · rebond 64% (5/7)
      · −3.0% : fill 20% (3/19) · rebond 0% (0/3)
      · −4.0% : fill 10% (2/19) · rebond 62% (1/2)
      · −5.0% : fill 10% (2/19) · rebond 62% (1/2)
   - **gap-up** (106 séances) :
      · −1.0% : fill 47% (47/106) · rebond 48% (21/47)
      · −2.0% : fill 28% (30/106) · rebond 55% (16/30)
      · −3.0% : fill 17% (17/106) · rebond 41% (8/17)
      · −4.0% : fill 7% (10/106) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/106) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 60% si les 15 1res min sont vertes (74 cas) · 34% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 66% si début vert vs 26% si rouge (base 45% · écart 40 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **66%** · continue >prix actuel 40% ; creux résiduel méd -1.25% (q20 -2.93%) → **SL/trailing à −2.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +1.88% → **scale +1.28% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **26%** (continue à baisser 50%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.19%] · haut q95 +3.59% · bas q05 -2.88%
   - 60min (n=160) : retour [-2.73% .. +3.18%] · haut q95 +4.29% · bas q05 -3.69%
   - 2h (n=160) : retour [-3.14% .. +2.94%] · haut q95 +4.36% · bas q05 -4.28%
   - 4h (n=160) : retour [-3.28% .. +3.08%] · haut q95 +4.83% · bas q05 -4.59%
   - 6h (n=160) : retour [-4.0% .. +3.23%] · haut q95 +4.88% · bas q05 -4.93%
   - session (n=160) : retour [-4.53% .. +3.66%] · haut q95 +5.01% · bas q05 -5.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 35.1  _(momentum baissier)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist -11.453  _(pas de croisement recent)_
- **BB** : %B -0.06 · largeur 12.0%
- **ATR** : 38.61 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.291  _(distribution)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 45.3  _(transition)_
- **MA** : MA20 1157.5 · MA50 1087.96 · MA200 1396.92  _(prix < MA20)_
- **Dist MA** : MA20 -6.7% · MA50 -0.8% · MA200 -22.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (793623 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
