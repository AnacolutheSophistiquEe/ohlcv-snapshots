# ENR

**Generated** : 2026-09-04T21:40:43.951368+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €146.52  

> 🟡 **WAIT-FOR-DIP** — spot +3.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €146.52 (+3.3% vs entrée) · entrée €141.78 · stop €130.44 · T1 €143.51 · R/R 0.15  
> ↳ P(T1 av. stop) 79 % _(réel 5 s)_ · EV/risk 0.017 _(réel 5 s)_ (GBM -0.069) · ¼-Kelly 0.097 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €141.44–€142.13 (mid €141.78)
- Spot actuel : €146.52 (+3.3% au-dessus de la zone — repli à attendre)
- Stop : €130.44 (stop swing_plan-based (-10.76%))
- Targets : T1 €143.51 · R/R 0.15 | T2 €145.23 · R/R 0.3 | T3 €146.95 · R/R 0.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €130.44


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.76 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **5.41 pt plus bas** dans le cas TYPIQUE (médiane), 21.08 au p90, **24.997 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 10.76 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0261 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0094** [0.0016 ; 0.033] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.427** [0.3757 ; 0.4796] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3791** [0.3291 ; 0.4311] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 12.3 observations effectives », dont la borne haute a 95 % vaut environ 24.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.25 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.35 % contre 3.27 % aujourd'hui, rapport 1.63)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.68 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.891 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3617** (β de hausse 1.0928, asymétrie 1.2461) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.399× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 130.4914 sur atr_grid (3.0 ATR, 10.94 %) — p(stop avant cible) 0.2125 [0.17 ; 0.26], R/R 1.285, perte reelle 21.854 % (gap inclus), CVaR 10.966 %, EV -1.8011 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.28 ATR (stop 3.166 %) — p(stop avant cible) 0.7246 [0.68 ; 0.77], R/R 4.33, perte reelle 6.488 % (gap inclus), EV -2.2553 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.725, borne haute 0.770 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 0.5 % x 28.09 % + P(rien) 27.0 % x 8.53 % ne couvrent pas P(stop) 72.5 % x 6.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.47 %) — p(stop avant cible) 0.5526 [0.50 ; 0.60], R/R 2.723, perte reelle 10.316 % (gap inclus), EV -2.5901 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.553, borne haute 0.604 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.59 %) : P(cible) 0.6 % x 28.09 % + P(rien) 44.1 % x 6.66 % ne couvrent pas P(stop) 55.3 % x 10.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.65 ATR (stop 15.439 %) — p(stop avant cible) 0.0551 [0.03 ; 0.08], R/R 1.082, perte reelle 25.963 % (gap inclus), EV 0.658 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.46 % > budget 12.00 %
   - 🟢 support a 6.82 ATR (stop 27.007 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 1.4772 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.01 % > budget 12.00 %
   - 🟢 support a 10.59 ATR (stop 40.769 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.689, perte reelle 40.769 % (gap inclus), EV 1.5217 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.77 % > budget 12.00 %
   - ⚪ grid_snapped a 0.28 ATR (stop 2.124 %) — p(stop avant cible) 0.8202 [0.78 ; 0.86], R/R 6.73, perte reelle 4.174 % (gap inclus), EV -1.7633 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.820, borne haute 0.858 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 0.4 % x 28.09 % + P(rien) 17.6 % x 8.79 % ne couvrent pas P(stop) 82.0 % x 4.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.647 %) — p(stop avant cible) 0.6812 [0.63 ; 0.73], R/R 3.792, perte reelle 7.407 % (gap inclus), EV -2.4137 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.41 %) : P(cible) 0.5 % x 28.09 % + P(rien) 31.4 % x 7.93 % ne couvrent pas P(stop) 68.1 % x 7.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.558 %) — p(stop avant cible) 0.6034 [0.55 ; 0.65], R/R 3.132, perte reelle 8.968 % (gap inclus), EV -2.4555 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.603, borne haute 0.654 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.46 %) : P(cible) 0.6 % x 28.09 % + P(rien) 39.0 % x 7.13 % ne couvrent pas P(stop) 60.3 % x 8.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.381 %) — p(stop avant cible) 0.4874 [0.43 ; 0.54], R/R 1.906, perte reelle 14.737 % (gap inclus), EV -4.0574 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.06 %) : P(cible) 0.6 % x 28.09 % + P(rien) 50.6 % x 5.83 % ne couvrent pas P(stop) 48.7 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.293 %) — p(stop avant cible) 0.4324 [0.38 ; 0.48], R/R 1.512, perte reelle 18.578 % (gap inclus), EV -4.8205 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.82 %) : P(cible) 0.6 % x 28.09 % + P(rien) 56.1 % x 5.41 % ne couvrent pas P(stop) 43.2 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.205 %) — p(stop avant cible) 0.3761 [0.33 ; 0.43], R/R 1.512, perte reelle 18.578 % (gap inclus), EV -3.7533 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.75 %) : P(cible) 0.6 % x 28.09 % + P(rien) 61.8 % x 4.95 % ne couvrent pas P(stop) 37.6 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.116 %) — p(stop avant cible) 0.3151 [0.27 ; 0.37], R/R 1.285, perte reelle 21.854 % (gap inclus), EV -3.7544 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.75 %) : P(cible) 0.6 % x 28.09 % + P(rien) 67.9 % x 4.36 % ne couvrent pas P(stop) 31.5 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.028 %) — p(stop avant cible) 0.2701 [0.23 ; 0.32], R/R 1.285, perte reelle 21.854 % (gap inclus), EV -2.8744 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.87 %) : P(cible) 0.6 % x 28.09 % + P(rien) 72.4 % x 3.94 % ne couvrent pas P(stop) 27.0 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.94 %) — p(stop avant cible) 0.2125 [0.17 ; 0.26], R/R 1.285, perte reelle 21.854 % (gap inclus), EV -1.8011 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.80 %) : P(cible) 0.6 % x 28.09 % + P(rien) 78.1 % x 3.42 % ne couvrent pas P(stop) 21.2 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.65 ATR (stop 14.396 %) — p(stop avant cible) 0.0817 [0.06 ; 0.11], R/R 1.082, perte reelle 25.963 % (gap inclus), EV 0.1504 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.41 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.409 %) — p(stop avant cible) 0.0389 [0.02 ; 0.06], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 0.5731 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.42 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.233 %) — p(stop avant cible) 0.0286 [0.01 ; 0.05], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 0.8504 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.25 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.056 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 1.2177 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.07 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.879 %) — p(stop avant cible) 0.0081 [0.00 ; 0.02], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 1.3255 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.89 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.702 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 1.3939 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.71 % > budget 12.00 %
   - 🟢 grid_snapped a 6.82 ATR (stop 25.964 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 1.4536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.97 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.172 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.786, perte reelle 35.757 % (gap inclus), EV 1.4922 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.18 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 146.52, ATR14 5.3429 (3.647 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.335 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.182 % | 146.2529 | 91.32 % | 94.08 % | 95.55 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.365 % | 145.9857 | 83.73 % | 88.06 % | 90.61 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.547 % | 145.7186 | 76.33 % | 82.43 % | 86.07 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.729 % | 145.4514 | 70.22 % | 79.17 % | 83.2 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.912 % | 145.1843 | 63.81 % | 74.93 % | 79.74 % | 83.66 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.276 % | 144.65 | 51.68 % | 65.05 % | 70.85 % | 76.34 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.823 % | 143.8486 | 36.29 % | 52.12 % | 59.88 % | 66.83 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.735 % | 142.5129 | 19.92 % | 36.23 % | 45.45 % | 54.85 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.647 % | 141.1771 | 11.14 % | 25.57 % | 34.49 % | 44.36 % | 56.72 % | 64.92 % |
| 1.25 ATR | 4.558 % | 139.8414 | 6.11 % | 17.28 % | 25.2 % | 35.94 % | 48.16 % | 57.29 % |
| 1.5 ATR | 5.47 % | 138.5057 | 2.86 % | 11.06 % | 17.89 % | 27.92 % | 41.09 % | 50.95 % |
| 2.0 ATR | 7.293 % | 135.8343 | 0.79 % | 4.05 % | 8.7 % | 16.24 % | 28.16 % | 39.8 % |
| 2.5 ATR | 9.116 % | 133.1629 | 0.3 % | 1.97 % | 4.15 % | 9.5 % | 19.5 % | 30.15 % |
| 3.0 ATR | 10.94 % | 130.4914 | 0.1 % | 0.79 % | 1.88 % | 4.95 % | 12.54 % | 22.51 % |
| 4.0 ATR | 14.586 % | 125.1486 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.67 % | 12.86 % |
| 6.0 ATR | 21.879 % | 114.4628 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 5.53 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.83 ATR | 1.02 ATR | 1.17 ATR | 1.58 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.26 ATR | 1.43 ATR | 1.93 ATR | 2.41 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.34 ATR | 1.62 ATR | 1.84 ATR | 2.46 ATR | 3.00 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.18 ATR | 2.47 ATR | 3.43 ATR | 4.76 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.77 ATR | 2.35 ATR | 2.84 ATR | 3.26 ATR | 4.78 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.415–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.612–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.735 %, prix 142.5127), p(touche) 36.23 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.76–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.647 %, prix 141.1764), p(touche) 34.49 % (en stress 91.18 %)  ✅ optimum identifie (85.2 % des re-echantillons)
- **5 seance(s)** : plage utile 0.985–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.647 %, prix 141.1764), p(touche) 44.36 % (en stress 99.01 %)  ✅ optimum identifie (89.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.47 %, prix 138.5054), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (91.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.767–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.293 %, prix 135.8343), p(touche) 39.8 % (en stress 99.0 %)  ✅ optimum identifie (87.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : €-0.786 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 31 % | T3 14 %
- Kelly (position) : f* 0.388 | ¼-Kelly 0.097 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.3 | bear 9.9 | side 6.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.239% → cible +1.216% / stop −8.0%, p_fill 22%, n_eff≈12.3) : P(cible|rempli) **79%** · **EV/risk +0.017** (×p_fill ; si rempli +0.62% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→57% · +2.0%→38% · +3.0%→20% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.83% (p90 6.15%) · excursion haute méd. +1.29% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.133% vs midi 0.877% vs clôture 1.063% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.739% ; recovery-V 8%
- **σ réalisé intraday** 2.46% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 75% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 141.2948 (VA 140.4263–142.0668 ; dernier close 141.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 66% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.27% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.51% · baisse 33% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.69%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.22%) · haut méd +0.59% · range méd 1.57%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.29%) · haut méd +0.61% · range méd 1.96%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −2.69%) · haut méd +0.73% · range méd 2.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 141.08 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 73% (115/159) · gap 26% · délai 0.4min · rebond 57% (64/115) (MFE +1.17%)
   - −1.0% : fill 30min 46% · séance 69% (107/159) · gap 19% · délai 7.2min · rebond 61% (62/107) (MFE +1.42%)
   - −1.5% : fill 30min 32% · séance 56% (89/159) · gap 15% · délai 10.1min · rebond 62% (53/89) (MFE +1.52%)
   - −2.0% : fill 30min 22% · séance 44% (74/159) · gap 10% · délai 33.3min · rebond 65% (50/74) (MFE +1.49%)
   - −3.0% : fill 30min 11% · séance 29% (52/159) · gap 4% · délai 208.4min · rebond 53% (33/52) (MFE +1.05%)
   - −4.0% : fill 30min 7% · séance 20% (38/159) · gap 2% · délai 129.6min · rebond 66% (27/38) (MFE +1.27%)
   - −5.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 398.5min · rebond 36% (13/25) (MFE +0.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.63%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.84%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.43% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=544 jambes) : jambe baissière méd −1.08% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 98% (50/51) · rebond 55% (27/50)
      · −2.0% : fill 78% (39/51) · rebond 49% (23/39)
      · −3.0% : fill 63% (31/51) · rebond 40% (18/31)
      · −4.0% : fill 51% (26/51) · rebond 71% (20/26)
      · −5.0% : fill 38% (18/51) · rebond 39% (11/18)
   - **flat** (15 séances) :
      · −1.0% : fill 85% (13/15) · rebond 91% (11/13)
      · −2.0% : fill 51% (8/15) · rebond 88% (6/8)
      · −3.0% : fill 25% (5/15) · rebond 76% (3/5)
      · −4.0% : fill 14% (4/15) · rebond 52% (2/4)
      · −5.0% : fill 11% (3/15) · rebond 0% (0/3)
   - **gap-up** (93 séances) :
      · −1.0% : fill 51% (44/93) · rebond 56% (24/44)
      · −2.0% : fill 26% (27/93) · rebond 78% (21/27)
      · −3.0% : fill 13% (16/93) · rebond 74% (12/16)
      · −4.0% : fill 5% (8/93) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/93) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 73% si les 15 1res min sont vertes (74 cas) · 18% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **14min** → P(séance verte=clôture>ouverture) 66% si début vert vs 21% si rouge (base 42% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **66%** · continue >prix actuel 42% ; creux résiduel méd -1.32% (q20 -3.18%) → **SL/trailing à −3.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.48% → **scale +1.5% / runner +2.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **21%** (continue à baisser 61%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.31%** (au-delà de la MAE q10 -4.31%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.07% .. +2.01%] · haut q95 +2.67% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.49% .. +2.33%] · haut q95 +2.7% · bas q05 -3.02%
   - 2h (n=160) : retour [-2.82% .. +2.65%] · haut q95 +2.92% · bas q05 -3.65%
   - 4h (n=160) : retour [-3.17% .. +2.64%] · haut q95 +3.7% · bas q05 -4.07%
   - 6h (n=160) : retour [-3.73% .. +3.32%] · haut q95 +4.15% · bas q05 -4.6%
   - session (n=160) : retour [-4.9% .. +3.96%] · haut q95 +5.2% · bas q05 -6.2%


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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.9  _(survente)_
- **ADX** : 12.2  _(pas de tendance nette)_
- **MACD** : hist -0.89  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 17.4%
- **ATR** : 5.34 (33.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.242  _(distribution)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 46.3  _(transition)_
- **MA** : MA20 152.18 · MA50 152.79 · MA200 150.44  _(prix < MA20)_
- **Dist MA** : MA20 -3.7% · MA50 -4.1% · MA200 -2.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (771347 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
