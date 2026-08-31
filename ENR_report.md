# ENR

**Generated** : 2026-08-31T00:06:43.643672+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €150.32  

> 🟡 **WAIT-FOR-DIP** — spot +9.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €150.32 (+9.1% vs entrée) · entrée €137.80 · stop €132.36 · T1 €141.03 · R/R 0.59  
> ↳ P(T1 av. stop) 84 % · EV/risk 0.392 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €137.16–€138.45 (mid €137.80)
- Spot actuel : €150.32 (+9.1% au-dessus de la zone — repli à attendre)
- Stop : €132.36 (stop swing_plan-based (-11.94%))
- Targets : T1 €141.03 · R/R 0.59 | T2 €144.26 · R/R 1.19 | T3 €147.49 · R/R 1.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €132.36


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.94 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **4.23 pt plus bas** dans le cas TYPIQUE (médiane), 19.9 au p90, **23.817 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 11.94 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0233 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0099** [0.0018 ; 0.0338] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.4002** [0.3496 ; 0.4525] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3441** [0.2955 ; 0.3953] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.5 observations effectives », dont la borne haute a 95 % vaut environ 26.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (51.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.6 %** | vol 3.21 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 6.23 % contre 3.29 % aujourd'hui, rapport 1.89)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3631** (β de hausse 1.0924, asymétrie 1.2478) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.416× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 134.0 sur atr_grid (3.0 ATR, 10.857 %) — p(stop avant cible) 0.2106 [0.17 ; 0.26], R/R 1.136, perte reelle 21.854 % (gap inclus), CVaR 10.883 %, EV -1.581 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.98 ATR (stop 5.542 %) — p(stop avant cible) 0.5347 [0.48 ; 0.59], R/R 2.309, perte reelle 10.753 % (gap inclus), EV -2.5669 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.535, borne haute 0.587 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.57 %) : P(cible) 1.1 % x 24.83 % + P(rien) 45.4 % x 6.38 % ne couvrent pas P(stop) 53.5 % x 10.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 4.28 ATR (stop 17.498 %) — p(stop avant cible) 0.0337 [0.02 ; 0.06], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 0.9957 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.51 % > budget 12.00 %
   - 🟢 support a 7.4 ATR (stop 28.767 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 1.7746 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.77 % > budget 12.00 %
   - 🟢 support a 11.1 ATR (stop 42.181 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.589, perte reelle 42.181 % (gap inclus), EV 1.8115 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.18 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.905 %) — p(stop avant cible) 0.927 [0.90 ; 0.95], R/R 11.12, perte reelle 2.233 % (gap inclus), EV -1.2778 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 11.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.927, borne haute 0.951 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 0.3 % x 24.83 % + P(rien) 7.0 % x 10.29 % ne couvrent pas P(stop) 92.7 % x 2.23 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.809 %) — p(stop avant cible) 0.8437 [0.80 ; 0.88], R/R 6.48, perte reelle 3.832 % (gap inclus), EV -1.7404 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.844, borne haute 0.879 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 0.5 % x 24.83 % + P(rien) 15.1 % x 9.00 % ne couvrent pas P(stop) 84.4 % x 3.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.98 ATR (stop 4.63 %) — p(stop avant cible) 0.5882 [0.54 ; 0.64], R/R 2.682, perte reelle 9.258 % (gap inclus), EV -2.4152 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 1.1 % x 24.83 % + P(rien) 40.1 % x 6.90 % ne couvrent pas P(stop) 58.8 % x 9.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.333 %) — p(stop avant cible) 0.477 [0.42 ; 0.53], R/R 1.835, perte reelle 13.536 % (gap inclus), EV -3.2796 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 1.1 % x 24.83 % + P(rien) 51.1 % x 5.65 % ne couvrent pas P(stop) 47.7 % x 13.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.238 %) — p(stop avant cible) 0.4158 [0.36 ; 0.47], R/R 1.337, perte reelle 18.578 % (gap inclus), EV -4.4337 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.43 %) : P(cible) 1.2 % x 24.83 % + P(rien) 57.2 % x 5.24 % ne couvrent pas P(stop) 41.6 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.143 %) — p(stop avant cible) 0.3594 [0.31 ; 0.41], R/R 1.337, perte reelle 18.578 % (gap inclus), EV -3.3667 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.37 %) : P(cible) 1.2 % x 24.83 % + P(rien) 62.9 % x 4.80 % ne couvrent pas P(stop) 35.9 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.047 %) — p(stop avant cible) 0.2952 [0.25 ; 0.34], R/R 1.136, perte reelle 21.854 % (gap inclus), EV -3.2427 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.24 %) : P(cible) 1.2 % x 24.83 % + P(rien) 69.3 % x 4.21 % ne couvrent pas P(stop) 29.5 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.952 %) — p(stop avant cible) 0.2605 [0.22 ; 0.31], R/R 1.136, perte reelle 21.854 % (gap inclus), EV -2.5082 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 1.2 % x 24.83 % + P(rien) 72.8 % x 3.97 % ne couvrent pas P(stop) 26.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.857 %) — p(stop avant cible) 0.2106 [0.17 ; 0.26], R/R 1.136, perte reelle 21.854 % (gap inclus), EV -1.581 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 1.2 % x 24.83 % + P(rien) 77.8 % x 3.51 % ne couvrent pas P(stop) 21.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.666 %) — p(stop avant cible) 0.1396 [0.11 ; 0.18], R/R 1.136, perte reelle 21.854 % (gap inclus), EV -0.1932 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 1.2 % x 24.83 % + P(rien) 84.9 % x 3.02 % ne couvrent pas P(stop) 14.0 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 14.476 %) — p(stop avant cible) 0.0841 [0.06 ; 0.12], R/R 0.956, perte reelle 25.963 % (gap inclus), EV 0.3921 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.49 % > budget 12.00 %
   - ⚪ grid_snapped a 4.28 ATR (stop 16.586 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 0.8983 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.60 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.095 %) — p(stop avant cible) 0.0295 [0.02 ; 0.05], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 1.1103 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.11 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.904 %) — p(stop avant cible) 0.0145 [0.01 ; 0.03], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 1.4932 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.92 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.714 %) — p(stop avant cible) 0.0084 [0.00 ; 0.02], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 1.6013 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.73 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.523 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 1.6765 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.333 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 1.7365 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.34 % > budget 12.00 %
   - 🟢 grid_snapped a 7.4 ATR (stop 27.855 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.694, perte reelle 35.757 % (gap inclus), EV 1.7599 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.86 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 150.32, ATR14 5.44 (3.619 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.328 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.181 % | 150.048 | 91.32 % | 94.08 % | 95.55 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.362 % | 149.776 | 83.73 % | 88.06 % | 90.61 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.543 % | 149.504 | 76.33 % | 82.43 % | 86.07 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.724 % | 149.232 | 70.22 % | 79.17 % | 83.2 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.905 % | 148.96 | 63.91 % | 75.02 % | 79.74 % | 83.66 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.267 % | 148.416 | 51.78 % | 65.15 % | 70.95 % | 76.34 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.809 % | 147.6 | 36.39 % | 52.22 % | 59.98 % | 66.83 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.714 % | 146.24 | 20.02 % | 36.23 % | 45.55 % | 54.85 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.619 % | 144.88 | 11.14 % | 25.47 % | 34.49 % | 44.36 % | 56.72 % | 65.03 % |
| 1.25 ATR | 4.524 % | 143.52 | 6.11 % | 17.08 % | 25.0 % | 35.74 % | 48.16 % | 57.49 % |
| 1.5 ATR | 5.428 % | 142.16 | 2.86 % | 11.06 % | 17.79 % | 27.72 % | 41.09 % | 51.26 % |
| 2.0 ATR | 7.238 % | 139.44 | 0.79 % | 4.05 % | 8.5 % | 16.04 % | 28.16 % | 40.2 % |
| 2.5 ATR | 9.047 % | 136.72 | 0.3 % | 1.97 % | 4.15 % | 9.41 % | 19.7 % | 30.65 % |
| 3.0 ATR | 10.857 % | 134.0 | 0.1 % | 0.79 % | 1.88 % | 4.95 % | 12.94 % | 23.02 % |
| 4.0 ATR | 14.476 % | 128.56 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.77 % | 13.37 % |
| 6.0 ATR | 21.714 % | 117.68 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 5.73 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.16 ATR | 1.58 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.40 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.33 ATR | 1.62 ATR | 1.83 ATR | 2.46 ATR | 2.99 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.19 ATR | 2.48 ATR | 3.48 ATR | 4.79 ATR |
| **20 s.** | 0.69 ATR | 1.56 ATR | 1.78 ATR | 2.38 ATR | 2.87 ATR | 3.31 ATR | 4.88 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.714 %, prix 146.2403), p(touche) 36.23 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.762–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.619 %, prix 144.8799), p(touche) 34.49 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.4 % des re-echantillons)
- **5 seance(s)** : plage utile 0.985–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.619 %, prix 144.8799), p(touche) 44.36 % (en stress 99.01 %)  ✅ optimum identifie (89.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.428 %, prix 142.1606), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (91.0 % des re-echantillons)
- **20 seance(s)** : plage utile 1.783–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.238 %, prix 139.4398), p(touche) 40.2 % (en stress 99.0 %)  ✅ optimum identifie (88.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.017 | EV/share : €0.092 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 62 % | T2 42 % | T3 32 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 14.1 | side 80.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.783% → cible +1.048% / stop −8.0%, p_fill 20%, n_eff≈11.5) : P(cible|rempli) **62%** · **EV/risk +0.004** (×p_fill ; si rempli +0.14% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=1))
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
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 150.32 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
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

- **RSI** : 43.4  _(momentum baissier)_
- **ADX** : 10.8  _(pas de tendance nette)_
- **MACD** : hist -0.582  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 11.6%
- **ATR** : 5.44 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.225  _(distribution)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 51.1  _(transition)_
- **MA** : MA20 154.17 · MA50 154.63 · MA200 149.55  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 -2.8% · MA200 +0.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (905233 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
