# RHM

**Generated** : 2026-09-11T00:02:44.408003+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1019.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €1019.40 (+2.2% vs entrée) · entrée €997.67 · stop €977.72 · T1 €1009.72 · R/R 0.6  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.061 _(réel 5 s)_ (GBM 0.06) · ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €995.27–€1000.08 (mid €997.67)
- Spot actuel : €1019.40 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : €977.72 (stop swing_plan-based (-8.36%))
- Targets : T1 €1009.72 · R/R 0.6 | T2 €1021.76 · R/R 1.21 | T3 €1033.80 · R/R 1.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €977.72


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.36 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1273).
   - exécution **14.069 pt plus bas** dans le cas TYPIQUE (médiane), 14.069 au p90, **14.069 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 8.36 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0111 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.574 % | p01 -3.747 % | pire -22.429 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.351** [0.2828 ; 0.4241] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.3988** [0.3482 ; 0.4511] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3882** [0.3379 ; 0.4403] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.46 %** | vol 2.84 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 1.55 % contre 3.26 % aujourd'hui, rapport 0.47)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.78 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.866 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5171** (β de hausse 0.5891, asymétrie 0.8778) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.304× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 907.6437 sur support (2.42 ATR, 10.963 %) — p(stop avant cible) 0.2446 [0.20 ; 0.29], R/R 2.253, perte reelle 22.429 % (gap inclus), CVaR 10.972 %, EV -3.3689 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.5 %) — p(stop avant cible) 0.5719 [0.52 ; 0.62], R/R 4.172, perte reelle 12.114 % (gap inclus), EV -4.0791 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.572, borne haute 0.623 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.08 %) : P(cible) 0.0 % x 50.54 % + P(rien) 42.8 % x 6.64 % ne couvrent pas P(stop) 57.2 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.42 ATR (stop 10.963 %) — p(stop avant cible) 0.2446 [0.20 ; 0.29], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -3.3689 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.37 %) : P(cible) 0.1 % x 50.54 % + P(rien) 75.5 % x 2.75 % ne couvrent pas P(stop) 24.5 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.917 %) — p(stop avant cible) 0.9303 [0.90 ; 0.95], R/R 22.573, perte reelle 2.239 % (gap inclus), EV -1.3073 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 22.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.930, borne haute 0.954 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 0.0 % x 50.54 % + P(rien) 7.0 % x 11.13 % ne couvrent pas P(stop) 93.0 % x 2.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.833 %) — p(stop avant cible) 0.8503 [0.81 ; 0.88], R/R 14.696, perte reelle 3.439 % (gap inclus), EV -1.2835 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.850, borne haute 0.885 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 0.0 % x 50.54 % + P(rien) 15.0 % x 10.96 % ne couvrent pas P(stop) 85.0 % x 3.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.75 %) — p(stop avant cible) 0.792 [0.75 ; 0.83], R/R 10.829, perte reelle 4.667 % (gap inclus), EV -1.5865 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 0.0 % x 50.54 % + P(rien) 20.8 % x 10.14 % ne couvrent pas P(stop) 79.2 % x 4.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.667 %) — p(stop avant cible) 0.6879 [0.64 ; 0.73], R/R 8.496, perte reelle 5.949 % (gap inclus), EV -1.5172 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.688, borne haute 0.735 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 0.0 % x 50.54 % + P(rien) 31.2 % x 8.25 % ne couvrent pas P(stop) 68.8 % x 5.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.583 %) — p(stop avant cible) 0.6254 [0.57 ; 0.68], R/R 4.886, perte reelle 10.343 % (gap inclus), EV -3.675 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.625, borne haute 0.675 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 0.0 % x 50.54 % + P(rien) 37.5 % x 7.46 % ne couvrent pas P(stop) 62.5 % x 10.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.417 %) — p(stop avant cible) 0.493 [0.44 ; 0.55], R/R 3.338, perte reelle 15.141 % (gap inclus), EV -4.567 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.57 %) : P(cible) 0.1 % x 50.54 % + P(rien) 50.6 % x 5.64 % ne couvrent pas P(stop) 49.3 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.333 %) — p(stop avant cible) 0.4285 [0.38 ; 0.48], R/R 3.338, perte reelle 15.141 % (gap inclus), EV -3.6297 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.63 %) : P(cible) 0.1 % x 50.54 % + P(rien) 57.1 % x 4.94 % ne couvrent pas P(stop) 42.9 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.42 ATR (stop 9.988 %) — p(stop avant cible) 0.2958 [0.25 ; 0.35], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -4.2569 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.26 %) : P(cible) 0.1 % x 50.54 % + P(rien) 70.3 % x 3.32 % ne couvrent pas P(stop) 29.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.834 %) — p(stop avant cible) 0.1821 [0.14 ; 0.23], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -2.419 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 0.1 % x 50.54 % + P(rien) 81.7 % x 1.99 % ne couvrent pas P(stop) 18.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 14.667 %) — p(stop avant cible) 0.1304 [0.10 ; 0.17], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -1.678 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 0.1 % x 50.54 % + P(rien) 86.9 % x 1.39 % ne couvrent pas P(stop) 13.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 16.5 %) — p(stop avant cible) 0.1037 [0.07 ; 0.14], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -1.3472 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 0.1 % x 50.54 % + P(rien) 89.5 % x 1.05 % ne couvrent pas P(stop) 10.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 18.334 %) — p(stop avant cible) 0.0674 [0.04 ; 0.10], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -0.9832 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.1 % x 50.54 % + P(rien) 93.2 % x 0.52 % ne couvrent pas P(stop) 6.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 20.167 %) — p(stop avant cible) 0.0478 [0.03 ; 0.07], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -0.847 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 0.1 % x 50.54 % + P(rien) 95.1 % x 0.19 % ne couvrent pas P(stop) 4.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 22.0 %) — p(stop avant cible) 0.0274 [0.01 ; 0.05], R/R 2.253, perte reelle 22.429 % (gap inclus), EV -0.5947 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.1 % x 50.54 % + P(rien) 97.2 % x -0.02 % ne couvrent pas P(stop) 2.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 23.834 %) — p(stop avant cible) 0.0109 [0.00 ; 0.03], R/R 2.121, perte reelle 23.834 % (gap inclus), EV -0.5144 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.1 % x 50.54 % + P(rien) 98.8 % x -0.30 % ne couvrent pas P(stop) 1.1 % x 23.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 25.667 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 1.969, perte reelle 25.667 % (gap inclus), EV -0.5231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 0.1 % x 50.54 % + P(rien) 99.2 % x -0.40 % ne couvrent pas P(stop) 0.7 % x 25.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 27.5 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 1.838, perte reelle 27.5 % (gap inclus), EV -0.4763 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 0.1 % x 50.54 % + P(rien) 99.4 % x -0.38 % ne couvrent pas P(stop) 0.5 % x 27.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 29.334 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 1.723, perte reelle 29.334 % (gap inclus), EV -0.4692 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 0.1 % x 50.54 % + P(rien) 99.5 % x -0.38 % ne couvrent pas P(stop) 0.4 % x 29.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1019.4, ATR14 37.3786 (3.667 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 1.445 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.183 % | 1017.5311 | 89.44 % | 92.19 % | 93.37 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.367 % | 1015.6622 | 83.42 % | 87.85 % | 89.71 % | 91.38 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.55 % | 1013.7932 | 76.41 % | 83.0 % | 85.66 % | 88.31 % | 92.93 % | 94.77 % |
| 0.2 ATR | 0.733 % | 1011.9243 | 69.79 % | 78.56 % | 81.6 % | 85.23 % | 90.94 % | 93.16 % |
| 0.25 ATR | 0.917 % | 1010.0554 | 62.39 % | 72.83 % | 76.66 % | 81.07 % | 88.35 % | 91.35 % |
| 0.35 ATR | 1.283 % | 1006.3175 | 53.9 % | 65.91 % | 71.22 % | 76.61 % | 85.76 % | 89.24 % |
| 0.5 ATR | 1.833 % | 1000.7107 | 40.47 % | 54.94 % | 61.62 % | 68.98 % | 80.08 % | 83.6 % |
| 0.75 ATR | 2.75 % | 991.3661 | 23.79 % | 39.23 % | 47.28 % | 57.48 % | 70.22 % | 76.86 % |
| 1.0 ATR | 3.667 % | 982.0214 | 13.03 % | 26.68 % | 36.3 % | 48.27 % | 62.05 % | 70.32 % |
| 1.25 ATR | 4.583 % | 972.6768 | 7.4 % | 18.08 % | 26.41 % | 38.85 % | 53.88 % | 63.78 % |
| 1.5 ATR | 5.5 % | 963.3322 | 3.95 % | 13.14 % | 20.67 % | 31.42 % | 45.62 % | 56.54 % |
| 2.0 ATR | 7.333 % | 944.6429 | 1.78 % | 7.02 % | 12.07 % | 20.81 % | 33.86 % | 46.58 % |
| 2.5 ATR | 9.167 % | 925.9536 | 0.49 % | 3.36 % | 6.33 % | 12.49 % | 24.5 % | 37.22 % |
| 3.0 ATR | 11.0 % | 907.2643 | 0.1 % | 1.38 % | 3.86 % | 7.73 % | 16.93 % | 30.89 % |
| 4.0 ATR | 14.667 % | 869.8857 | 0.0 % | 0.3 % | 1.29 % | 3.27 % | 8.47 % | 19.82 % |
| 6.0 ATR | 22.0 % | 795.1286 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.14 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.28 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.54 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.38 ATR | 0.95 ATR | 1.09 ATR | 1.45 ATR | 1.80 ATR | 2.05 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.63 ATR | 1.37 ATR | 1.53 ATR | 2.05 ATR | 2.47 ATR | 2.80 ATR | 3.82 ATR | 4.91 ATR |
| **20 s.** | 0.82 ATR | 1.83 ATR | 2.08 ATR | 2.83 ATR | 3.53 ATR | 3.98 ATR | 5.21 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.449–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.658–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.75 %, prix 991.3665), p(touche) 39.23 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.802–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.667 %, prix 982.0186), p(touche) 36.3 % (en stress 95.1 %)  ✅ optimum identifie (66.6 % des re-echantillons)
- **5 seance(s)** : plage utile 1.087–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.583 %, prix 972.6809), p(touche) 38.85 % (en stress 98.02 %)  ✅ optimum identifie (89.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.526–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.333 %, prix 944.6474), p(touche) 33.86 % (en stress 96.04 %)  ✅ optimum identifie (99.1 % des re-echantillons)
- **20 seance(s)** : plage utile 2.084–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.167 %, prix 925.9516), p(touche) 37.22 % (en stress 98.0 %)  ✅ optimum identifie (98.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.06 | EV/share : €1.207 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 38 % | T3 21 %
- Kelly (position) : f* 0.117 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.8 | bear 5.9 | side 11.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.133% → cible +1.207% / stop −2.0%, p_fill 47%, n_eff≈16.5) : P(cible|rempli) **37%** · **EV/risk -0.061** (×p_fill ; si rempli -0.26% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=6))
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.9  _(survente)_
- **ADX** : 20.6  _(pas de tendance nette)_
- **MACD** : hist -16.599  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 22.5%
- **ATR** : 37.38 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.194  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 37.9  _(marche directionnel)_
- **MA** : MA20 1123.48 · MA50 1096.4 · MA200 1379.21  _(prix < MA20)_
- **Dist MA** : MA20 -9.3% · MA50 -7.0% · MA200 -26.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (763713 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
