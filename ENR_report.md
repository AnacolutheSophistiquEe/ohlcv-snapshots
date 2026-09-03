# ENR

**Generated** : 2026-09-03T21:40:56.439265+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €145.40  

> 🟡 **WAIT-FOR-DIP** — spot +3.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €145.40 (+3.2% vs entrée) · entrée €140.94 · stop €129.67 · T1 €142.65 · R/R 0.15  
> ↳ P(T1 av. stop) 64 % _(réel 5 s)_ · EV/risk 0.02 _(réel 5 s)_ (GBM -0.069) · ¼-Kelly 0.097 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €140.60–€141.28 (mid €140.94)
- Spot actuel : €145.40 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : €129.67 (stop swing_plan-based (-10.43%))
- Targets : T1 €142.65 · R/R 0.15 | T2 €144.35 · R/R 0.3 | T3 €146.06 · R/R 0.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.67


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.43 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **5.74 pt plus bas** dans le cas TYPIQUE (médiane), 21.41 au p90, **25.327 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 10.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0269 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0095** [0.0017 ; 0.0332] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.4175** [0.3664 ; 0.47] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3755** [0.3257 ; 0.4274] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.2 observations effectives », dont la borne haute a 95 % vaut environ 22.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.25 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.36 % contre 3.28 % aujourd'hui, rapport 1.63)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.75 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.898 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3617** (β de hausse 1.0915, asymétrie 1.2476) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.399× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 129.3414 sur atr_grid (3.0 ATR, 11.044 %) — p(stop avant cible) 0.2067 [0.17 ; 0.25], R/R 1.33, perte reelle 21.854 % (gap inclus), CVaR 11.069 %, EV -1.6653 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.4 % de la queue et il ne reste que -955.87 EUR a partager. Prix du risque -0.692 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.07 ATR (stop 2.485 %) — p(stop avant cible) 0.7847 [0.74 ; 0.83], R/R 5.995, perte reelle 4.85 % (gap inclus), EV -1.8526 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.785, borne haute 0.826 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.85 %) : P(cible) 0.5 % x 29.07 % + P(rien) 21.1 % x 8.61 % ne couvrent pas P(stop) 78.5 % x 4.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.522 %) — p(stop avant cible) 0.5454 [0.49 ; 0.60], R/R 2.704, perte reelle 10.753 % (gap inclus), EV -2.7397 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.74 %) : P(cible) 0.6 % x 29.07 % + P(rien) 44.9 % x 6.58 % ne couvrent pas P(stop) 54.5 % x 10.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.43 ATR (stop 14.851 %) — p(stop avant cible) 0.0747 [0.05 ; 0.11], R/R 1.12, perte reelle 25.963 % (gap inclus), EV 0.3488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 12.00 %
   - 🟢 support a 6.6 ATR (stop 26.507 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 1.5189 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.51 % > budget 12.00 %
   - 🔴 support a 10.37 ATR (stop 40.375 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.72, perte reelle 40.375 % (gap inclus), EV 1.5624 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.38 % > budget 12.00 %
      - ⚠ support DETECTE a 9.40 ATR du spot — compartiment >=6, mesure a 45.5 % de casse (IC clusterise [0.340 ; 0.585] sur 55 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ grid_snapped a 0.07 ATR (stop 1.373 %) — p(stop avant cible) 0.8959 [0.86 ; 0.92], R/R 8.99, perte reelle 3.234 % (gap inclus), EV -1.8391 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 8.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.896, borne haute 0.925 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 0.3 % x 29.07 % + P(rien) 10.1 % x 9.64 % ne couvrent pas P(stop) 89.6 % x 3.23 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.841 %) — p(stop avant cible) 0.8463 [0.81 ; 0.88], R/R 7.583, perte reelle 3.834 % (gap inclus), EV -1.7698 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 7.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.846, borne haute 0.881 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.77 %) : P(cible) 0.3 % x 29.07 % + P(rien) 15.0 % x 9.18 % ne couvrent pas P(stop) 84.6 % x 3.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.681 %) — p(stop avant cible) 0.6716 [0.62 ; 0.72], R/R 3.925, perte reelle 7.407 % (gap inclus), EV -2.2951 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.672, borne haute 0.720 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.30 %) : P(cible) 0.5 % x 29.07 % + P(rien) 32.3 % x 7.83 % ne couvrent pas P(stop) 67.2 % x 7.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.602 %) — p(stop avant cible) 0.5976 [0.55 ; 0.65], R/R 3.242, perte reelle 8.968 % (gap inclus), EV -2.3835 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.598, borne haute 0.648 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.38 %) : P(cible) 0.6 % x 29.07 % + P(rien) 39.7 % x 7.08 % ne couvrent pas P(stop) 59.8 % x 8.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.443 %) — p(stop avant cible) 0.4835 [0.43 ; 0.54], R/R 1.973, perte reelle 14.737 % (gap inclus), EV -3.9801 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.98 %) : P(cible) 0.6 % x 29.07 % + P(rien) 51.1 % x 5.82 % ne couvrent pas P(stop) 48.4 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.363 %) — p(stop avant cible) 0.4161 [0.36 ; 0.47], R/R 1.565, perte reelle 18.578 % (gap inclus), EV -4.5098 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.51 %) : P(cible) 0.6 % x 29.07 % + P(rien) 57.8 % x 5.28 % ne couvrent pas P(stop) 41.6 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.283 %) — p(stop avant cible) 0.3649 [0.32 ; 0.42], R/R 1.565, perte reelle 18.578 % (gap inclus), EV -3.551 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.55 %) : P(cible) 0.6 % x 29.07 % + P(rien) 62.9 % x 4.86 % ne couvrent pas P(stop) 36.5 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.204 %) — p(stop avant cible) 0.3056 [0.26 ; 0.36], R/R 1.33, perte reelle 21.854 % (gap inclus), EV -3.4984 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.50 %) : P(cible) 0.6 % x 29.07 % + P(rien) 68.8 % x 4.37 % ne couvrent pas P(stop) 30.6 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.124 %) — p(stop avant cible) 0.2655 [0.22 ; 0.31], R/R 1.33, perte reelle 21.854 % (gap inclus), EV -2.7213 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.72 %) : P(cible) 0.6 % x 29.07 % + P(rien) 72.9 % x 3.99 % ne couvrent pas P(stop) 26.6 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.044 %) — p(stop avant cible) 0.2067 [0.17 ; 0.25], R/R 1.33, perte reelle 21.854 % (gap inclus), EV -1.6653 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.67 %) : P(cible) 0.6 % x 29.07 % + P(rien) 78.7 % x 3.40 % ne couvrent pas P(stop) 20.7 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.43 ATR (stop 13.739 %) — p(stop avant cible) 0.0973 [0.07 ; 0.13], R/R 1.12, perte reelle 25.963 % (gap inclus), EV -0.1424 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.6 % x 29.07 % + P(rien) 89.7 % x 2.47 % ne couvrent pas P(stop) 9.7 % x 25.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 16.567 %) — p(stop avant cible) 0.0362 [0.02 ; 0.06], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 0.6802 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.58 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.407 %) — p(stop avant cible) 0.0288 [0.01 ; 0.05], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 0.8865 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.42 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.248 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 1.2601 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.26 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.089 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 1.3638 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.10 % > budget 12.00 %
   - 🟢 grid_snapped a 6.6 ATR (stop 25.396 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 1.4955 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.611 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 1.5189 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.62 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.452 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.813, perte reelle 35.757 % (gap inclus), EV 1.534 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.46 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 145.4, ATR14 5.3529 (3.681 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.351 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.184 % | 145.1324 | 91.42 % | 94.08 % | 95.55 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.368 % | 144.8647 | 83.83 % | 88.06 % | 90.61 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.552 % | 144.5971 | 76.43 % | 82.43 % | 86.07 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.736 % | 144.3294 | 70.32 % | 79.17 % | 83.2 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.92 % | 144.0618 | 63.91 % | 75.02 % | 79.74 % | 83.66 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.289 % | 143.5265 | 51.78 % | 65.15 % | 70.95 % | 76.34 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.841 % | 142.7236 | 36.39 % | 52.22 % | 59.98 % | 66.83 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.761 % | 141.3853 | 20.02 % | 36.33 % | 45.55 % | 54.85 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.681 % | 140.0471 | 11.14 % | 25.57 % | 34.49 % | 44.36 % | 56.72 % | 64.92 % |
| 1.25 ATR | 4.602 % | 138.7089 | 6.11 % | 17.28 % | 25.2 % | 35.84 % | 48.16 % | 57.29 % |
| 1.5 ATR | 5.522 % | 137.3707 | 2.86 % | 11.06 % | 17.89 % | 27.82 % | 41.09 % | 50.95 % |
| 2.0 ATR | 7.363 % | 134.6943 | 0.79 % | 4.05 % | 8.7 % | 16.14 % | 28.16 % | 39.9 % |
| 2.5 ATR | 9.204 % | 132.0178 | 0.3 % | 1.97 % | 4.15 % | 9.5 % | 19.6 % | 30.25 % |
| 3.0 ATR | 11.044 % | 129.3414 | 0.1 % | 0.79 % | 1.88 % | 4.95 % | 12.64 % | 22.61 % |
| 4.0 ATR | 14.726 % | 123.9886 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.67 % | 12.96 % |
| 6.0 ATR | 22.089 % | 113.2828 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 5.53 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.83 ATR | 1.02 ATR | 1.17 ATR | 1.58 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.26 ATR | 1.43 ATR | 1.93 ATR | 2.41 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.34 ATR | 1.62 ATR | 1.83 ATR | 2.46 ATR | 3.00 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.19 ATR | 2.48 ATR | 3.44 ATR | 4.76 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.77 ATR | 2.36 ATR | 2.84 ATR | 3.27 ATR | 4.80 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.761 %, prix 141.3855), p(touche) 36.33 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.762–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.681 %, prix 140.0478), p(touche) 34.49 % (en stress 91.18 %)  ✅ optimum identifie (85.5 % des re-echantillons)
- **5 seance(s)** : plage utile 0.985–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.681 %, prix 140.0478), p(touche) 44.36 % (en stress 99.01 %)  ✅ optimum identifie (89.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.522 %, prix 137.371), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (91.8 % des re-echantillons)
- **20 seance(s)** : plage utile 1.769–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.363 %, prix 134.6942), p(touche) 39.9 % (en stress 99.0 %)  ✅ optimum identifie (87.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : €-0.781 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 31 % | T3 15 %
- Kelly (position) : f* 0.39 | ¼-Kelly 0.097 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.2 | bear 9.8 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.065% → cible +1.21% / stop −8.0%, p_fill 31%, n_eff≈13.2) : P(cible|rempli) **64%** · **EV/risk +0.020** (×p_fill ; si rempli +0.53% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.8  _(survente)_
- **ADX** : 12.9  _(pas de tendance nette)_
- **MACD** : hist -1.202  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 17.0%
- **ATR** : 5.35 (33.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.237  _(distribution)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 40.2  _(transition)_
- **MA** : MA20 152.53 · MA50 152.94 · MA200 150.24  _(prix < MA20)_
- **Dist MA** : MA20 -4.7% · MA50 -4.9% · MA200 -3.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (773093 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
