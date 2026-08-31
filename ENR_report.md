# ENR

**Generated** : 2026-08-31T21:40:39.264555+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €142.18  

> 🟡 **WAIT-FOR-DIP** — spot +2.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €142.18 (+2.6% vs entrée) · entrée €138.53 · stop €127.44 · T1 €140.23 · R/R 0.15  
> ↳ P(T1 av. stop) 43 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM -0.069) · ¼-Kelly 0.096 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €138.19–€138.87 (mid €138.53)
- Spot actuel : €142.18 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €127.44 (stop swing_plan-based (-9.6%))
- Targets : T1 €140.23 · R/R 0.15 | T2 €141.93 · R/R 0.31 | T3 €143.64 · R/R 0.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.44


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.6 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **6.57 pt plus bas** dans le cas TYPIQUE (médiane), 22.24 au p90, **26.157 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 9.6 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0289 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0098** [0.0018 ; 0.0337] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.4061** [0.3553 ; 0.4585] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.35** [0.3011 ; 0.4014] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 17.4 observations effectives », dont la borne haute a 95 % vaut environ 17.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.6 pt), swing (52.0 pt), deep (48.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 900 séances)** : VaR **-4.37 %** | CVaR **-7.71 %** | vol 3.55 %/j
   - _fenêtre arrêtée : rupture de regime a 960 seances en arriere (volatilite 2.05 % contre 3.32 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3669** (β de hausse 1.0924, asymétrie 1.2513) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.43× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 125.3227 sur grid_snapped (2.71 ATR, 11.856 %) — p(stop avant cible) 0.1578 [0.12 ; 0.20], R/R 1.462, perte reelle 21.854 % (gap inclus), CVaR 11.88 %, EV -0.6304 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 19 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 61.4 % de la queue et il ne reste que 29.65 EUR a partager. Prix du risque 0.019 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.913 %) — p(stop avant cible) 0.5015 [0.45 ; 0.55], R/R 2.691, perte reelle 11.87 % (gap inclus), EV -2.7597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.501, borne haute 0.554 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.76 %) : P(cible) 0.4 % x 31.95 % + P(rien) 49.5 % x 6.22 % ne couvrent pas P(stop) 50.1 % x 11.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.71 ATR (stop 12.739 %) — p(stop avant cible) 0.134 [0.10 ; 0.17], R/R 1.462, perte reelle 21.854 % (gap inclus), EV -0.0898 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.4 % x 31.95 % + P(rien) 86.2 % x 3.16 % ne couvrent pas P(stop) 13.4 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.73 ATR (stop 24.642 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 1.6667 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.65 % > budget 12.00 %
   - 🟢 support a 9.33 ATR (stop 38.824 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.823, perte reelle 38.824 % (gap inclus), EV 1.7639 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.82 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.985 %) — p(stop avant cible) 0.9142 [0.88 ; 0.94], R/R 13.049, perte reelle 2.448 % (gap inclus), EV -1.3523 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.914, borne haute 0.940 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 0.1 % x 31.95 % + P(rien) 8.5 % x 10.04 % ne couvrent pas P(stop) 91.4 % x 2.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.971 %) — p(stop avant cible) 0.8236 [0.78 ; 0.86], R/R 8.143, perte reelle 3.923 % (gap inclus), EV -1.6103 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 8.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.824, borne haute 0.861 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.61 %) : P(cible) 0.3 % x 31.95 % + P(rien) 17.4 % x 8.85 % ne couvrent pas P(stop) 82.4 % x 3.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.956 %) — p(stop avant cible) 0.7465 [0.70 ; 0.79], R/R 5.318, perte reelle 6.007 % (gap inclus), EV -2.1751 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.747, borne haute 0.790 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 0.4 % x 31.95 % + P(rien) 25.0 % x 8.79 % ne couvrent pas P(stop) 74.7 % x 6.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.942 %) — p(stop avant cible) 0.6428 [0.59 ; 0.69], R/R 4.226, perte reelle 7.559 % (gap inclus), EV -2.0739 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.643, borne haute 0.692 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 0.4 % x 31.95 % + P(rien) 35.4 % x 7.56 % ne couvrent pas P(stop) 64.3 % x 7.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.927 %) — p(stop avant cible) 0.5811 [0.53 ; 0.63], R/R 3.334, perte reelle 9.581 % (gap inclus), EV -2.4685 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.581, borne haute 0.632 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 0.4 % x 31.95 % + P(rien) 41.5 % x 7.19 % ne couvrent pas P(stop) 58.1 % x 9.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.898 %) — p(stop avant cible) 0.4478 [0.40 ; 0.50], R/R 2.168, perte reelle 14.737 % (gap inclus), EV -3.3833 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.38 %) : P(cible) 0.4 % x 31.95 % + P(rien) 54.9 % x 5.65 % ne couvrent pas P(stop) 44.8 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.883 %) — p(stop avant cible) 0.3759 [0.33 ; 0.43], R/R 1.72, perte reelle 18.578 % (gap inclus), EV -3.6373 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.64 %) : P(cible) 0.4 % x 31.95 % + P(rien) 62.1 % x 5.21 % ne couvrent pas P(stop) 37.6 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.869 %) — p(stop avant cible) 0.3111 [0.26 ; 0.36], R/R 1.462, perte reelle 21.854 % (gap inclus), EV -3.6317 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.63 %) : P(cible) 0.4 % x 31.95 % + P(rien) 68.5 % x 4.45 % ne couvrent pas P(stop) 31.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.71 ATR (stop 11.856 %) — p(stop avant cible) 0.1578 [0.12 ; 0.20], R/R 1.462, perte reelle 21.854 % (gap inclus), EV -0.6304 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.4 % x 31.95 % + P(rien) 83.9 % x 3.22 % ne couvrent pas P(stop) 15.8 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 13.796 %) — p(stop avant cible) 0.0938 [0.07 ; 0.13], R/R 1.23, perte reelle 25.963 % (gap inclus), EV 0.141 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.82 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 15.767 %) — p(stop avant cible) 0.0456 [0.03 ; 0.07], R/R 1.23, perte reelle 25.963 % (gap inclus), EV 1.0794 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.78 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 17.738 %) — p(stop avant cible) 0.0322 [0.02 ; 0.05], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 0.9957 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.75 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.708 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 1.3765 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.72 % > budget 12.00 %
   - 🟢 grid_snapped a 5.73 ATR (stop 23.759 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 1.6354 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.77 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 25.621 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 1.6953 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 27.592 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 1.7187 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.60 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 29.563 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 1.7372 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.57 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 31.533 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.893, perte reelle 35.757 % (gap inclus), EV 1.765 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.54 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 142.18, ATR14 5.6043 (3.942 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.447 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.197 % | 141.8998 | 91.32 % | 94.08 % | 95.55 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.394 % | 141.6196 | 83.73 % | 88.06 % | 90.61 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.591 % | 141.3393 | 76.33 % | 82.43 % | 86.07 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.788 % | 141.0591 | 70.22 % | 79.17 % | 83.2 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.985 % | 140.7789 | 63.91 % | 75.02 % | 79.74 % | 83.66 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.38 % | 140.2185 | 51.78 % | 65.15 % | 70.95 % | 76.34 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.971 % | 139.3778 | 36.39 % | 52.22 % | 59.98 % | 66.83 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.956 % | 137.9768 | 19.92 % | 36.23 % | 45.45 % | 54.75 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.942 % | 136.5757 | 11.14 % | 25.47 % | 34.39 % | 44.26 % | 56.72 % | 64.92 % |
| 1.25 ATR | 4.927 % | 135.1746 | 6.11 % | 17.18 % | 25.0 % | 35.64 % | 48.16 % | 57.39 % |
| 1.5 ATR | 5.913 % | 133.7736 | 2.86 % | 11.06 % | 17.79 % | 27.62 % | 41.09 % | 51.16 % |
| 2.0 ATR | 7.883 % | 130.9714 | 0.79 % | 4.05 % | 8.5 % | 15.94 % | 28.16 % | 40.1 % |
| 2.5 ATR | 9.854 % | 128.1693 | 0.3 % | 1.97 % | 4.15 % | 9.41 % | 19.7 % | 30.55 % |
| 3.0 ATR | 11.825 % | 125.3671 | 0.1 % | 0.79 % | 1.88 % | 4.95 % | 12.94 % | 22.91 % |
| 4.0 ATR | 15.767 % | 119.7628 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.77 % | 13.27 % |
| 6.0 ATR | 23.65 % | 108.5543 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 5.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.58 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.40 ATR |
| **5 s.** | 0.37 ATR | 0.86 ATR | 0.98 ATR | 1.33 ATR | 1.61 ATR | 1.83 ATR | 2.46 ATR | 2.99 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.19 ATR | 2.48 ATR | 3.48 ATR | 4.79 ATR |
| **20 s.** | 0.69 ATR | 1.55 ATR | 1.78 ATR | 2.37 ATR | 2.86 ATR | 3.30 ATR | 4.86 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.956 %, prix 137.9772), p(touche) 36.23 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.76–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.942 %, prix 136.5753), p(touche) 34.39 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.1 % des re-echantillons)
- **5 seance(s)** : plage utile 0.982–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.942 %, prix 136.5753), p(touche) 44.26 % (en stress 99.01 %)  ✅ optimum identifie (88.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.913 %, prix 133.7729), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (92.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.778–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.883 %, prix 130.9719), p(touche) 40.1 % (en stress 99.0 %)  ✅ optimum identifie (87.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : €-0.759 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 31 % | T3 14 %
- Kelly (position) : f* 0.384 | ¼-Kelly 0.096 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 12.9 | side 82.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.565% → cible +1.23% / stop −8.0%, p_fill 39%, n_eff≈17.4) : P(cible|rempli) **43%** · **EV/risk +0.009** (×p_fill ; si rempli +0.18% du capital)
  - **swing** (entrée dip −5.659% → cible +2.75% / stop −4.178%, p_fill 25%, n_eff≈11.6) : P(cible|rempli) **55%** · **EV/risk +0.024** (×p_fill ; si rempli +0.40% du capital)
  - **deep** (entrée dip −8.737% → cible +3.89% / stop −6.479%, p_fill 15%, n_eff≈8.7) : P(cible|rempli) **80%** · **EV/risk +0.042** (×p_fill ; si rempli +1.85% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→57% · +2.0%→38% · +3.0%→20% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.88% (p90 6.15%) · excursion haute méd. +1.29% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.126% vs midi 0.891% vs clôture 1.082% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑1%/↓0% ; spike-down 59% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr -0.008)_ ; drift intra méd. -0.611% ; recovery-V 8%
- **σ réalisé intraday** 2.46% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 72% / whipsaw 46%
- POC intraday (dernière séance, temps-au-prix) : 150.2585 (VA 149.9025–151.0595 ; dernier close 150.32)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 63% · **stop −3.32%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 32% (gap-down >1% 18% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.57% (p90 −1.67%) · haut méd +0.45% · range méd 1.17%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.2%) · haut méd +0.6% · range méd 1.55%
- Excursion ouverture 30min (n=160) : bas méd −0.84% (p90 −2.26%) · haut méd +0.67% · range méd 1.91%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.57%) · haut méd +0.76% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 149.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 72% (115/159) · gap 25% · délai 0.6min · rebond 57% (64/115) (MFE +1.2%)
   - −1.0% : fill 30min 44% · séance 68% (107/159) · gap 18% · délai 8.8min · rebond 62% (62/107) (MFE +1.42%)
   - −1.5% : fill 30min 30% · séance 54% (89/159) · gap 14% · délai 13.3min · rebond 63% (53/89) (MFE +1.52%)
   - −2.0% : fill 30min 21% · séance 42% (74/159) · gap 9% · délai 32.5min · rebond 66% (51/74) (MFE +1.6%)
   - −3.0% : fill 30min 10% · séance 28% (52/159) · gap 4% · délai 214.2min · rebond 56% (34/52) (MFE +1.39%)
   - −4.0% : fill 30min 5% · séance 19% (38/159) · gap 2% · délai 226.7min · rebond 63% (27/38) (MFE +1.38%)
   - −5.0% : fill 30min 2% · séance 13% (24/159) · gap 0% · délai 389.0min · rebond 41% (13/24) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.63%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.84%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.43% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=544 jambes) : jambe baissière méd −1.06% (p90 −2.65%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 97% (50/51) · rebond 58% (27/50)
      · −2.0% : fill 76% (39/51) · rebond 53% (24/39)
      · −3.0% : fill 61% (31/51) · rebond 45% (19/31)
      · −4.0% : fill 48% (26/51) · rebond 67% (20/26)
      · −5.0% : fill 34% (17/51) · rebond 47% (11/17)
   - **flat** (15 séances) :
      · −1.0% : fill 83% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 43% (8/15) · rebond 84% (6/8)
      · −3.0% : fill 29% (5/15) · rebond 76% (3/5)
      · −4.0% : fill 16% (4/15) · rebond 52% (2/4)
      · −5.0% : fill 13% (3/15) · rebond 0% (0/3)
   - **gap-up** (93 séances) :
      · −1.0% : fill 51% (44/93) · rebond 56% (24/44)
      · −2.0% : fill 26% (27/93) · rebond 78% (21/27)
      · −3.0% : fill 13% (16/93) · rebond 74% (12/16)
      · −4.0% : fill 5% (8/93) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/93) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 73% si les 15 1res min sont vertes (75 cas) · 19% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **14min** → P(séance verte=clôture>ouverture) 66% si début vert vs 23% si rouge (base 44% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **66%** · continue >prix actuel 42% ; creux résiduel méd -1.31% (q20 -3.18%) → **SL/trailing à −3.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.48% → **scale +1.5% / runner +2.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **23%** (continue à baisser 58%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.51%** (au-delà de la MAE q10 -4.51%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.05% .. +2.03%] · haut q95 +2.68% · bas q05 -2.54%
   - 60min (n=160) : retour [-2.49% .. +2.33%] · haut q95 +2.71% · bas q05 -2.84%
   - 2h (n=160) : retour [-2.84% .. +2.65%] · haut q95 +2.93% · bas q05 -3.71%
   - 4h (n=160) : retour [-3.19% .. +2.65%] · haut q95 +3.71% · bas q05 -4.14%
   - 6h (n=160) : retour [-3.75% .. +3.39%] · haut q95 +4.15% · bas q05 -4.62%
   - session (n=160) : retour [-4.9% .. +4.03%] · haut q95 +5.26% · bas q05 -6.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **20 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 27.6  _(survente)_
- **ADX** : 11.3  _(pas de tendance nette)_
- **MACD** : hist -1.11  _(pas de croisement recent)_
- **BB** : %B -0.08 · largeur 13.1%
- **ATR** : 5.6 (36.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.308  _(distribution)_
- **Vol ratio** : 1.71  _(volume au-dessus de la moyenne)_
- **Choppiness** : 45.3  _(transition)_
- **MA** : MA20 153.87 · MA50 154.08 · MA200 149.72  _(prix < MA20)_
- **Dist MA** : MA20 -7.6% · MA50 -7.7% · MA200 -5.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (802071 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
