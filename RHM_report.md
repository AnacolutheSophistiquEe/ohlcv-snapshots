# RHM

**Generated** : 2026-09-02T21:36:12.099803+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1090.40  

> 🟡 **WAIT-FOR-DIP** — spot +3.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1090.40 (+3.8% vs entrée) · entrée €1050.92 · stop €1029.91 · T1 €1062.92 · R/R 0.57  
> ↳ P(T1 av. stop) 65 % · EV/risk 0.197 · ¼-Kelly 0.04 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1048.53–€1053.32 (mid €1050.92)
- Spot actuel : €1090.40 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : €1029.91 (stop swing_plan-based (-11.44%))
- Targets : T1 €1062.92 · R/R 0.57 | T2 €1074.91 · R/R 1.14 | T3 €1086.90 · R/R 1.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1029.91


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.44 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **10.989 pt plus bas** dans le cas TYPIQUE (médiane), 10.989 au p90, **10.989 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 11.44 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0086 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3347** [0.2676 ; 0.4073] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.3868** [0.3366 ; 0.4389] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3778** [0.3279 ; 0.4297] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (60.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.86 %** | CVaR **-6.73 %** | vol 2.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.97 % contre 3.26 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.61 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.847 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5079** (β de hausse 0.5813, asymétrie 0.8737) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.307× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 1005.125 sur atr_grid (2.25 ATR, 7.821 %) — p(stop avant cible) 0.4004 [0.35 ; 0.45], R/R 1.251, perte reelle 15.141 % (gap inclus), CVaR 7.832 %, EV -3.0618 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.214 %) — p(stop avant cible) 0.5762 [0.52 ; 0.63], R/R 1.564, perte reelle 12.114 % (gap inclus), EV -3.9425 % — **REFUSE**
      - refuse : cible atteinte seulement 8.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.576, borne haute 0.627 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.94 %) : P(cible) 8.1 % x 18.94 % + P(rien) 34.3 % x 4.38 % ne couvrent pas P(stop) 57.6 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.26 ATR (stop 17.083 %) — p(stop avant cible) 0.0975 [0.07 ; 0.13], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -0.969 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 9.0 % x 18.94 % + P(rien) 81.3 % x -0.60 % ne couvrent pas P(stop) 9.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.869 %) — p(stop avant cible) 0.929 [0.90 ; 0.95], R/R 8.793, perte reelle 2.154 % (gap inclus), EV -1.0792 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.929, borne haute 0.953 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 3.0 % x 18.94 % + P(rien) 4.1 % x 8.55 % ne couvrent pas P(stop) 92.9 % x 2.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.738 %) — p(stop avant cible) 0.8571 [0.82 ; 0.89], R/R 5.75, perte reelle 3.294 % (gap inclus), EV -1.0759 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.857, borne haute 0.891 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 5.4 % x 18.94 % + P(rien) 8.9 % x 8.16 % ne couvrent pas P(stop) 85.7 % x 3.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.607 %) — p(stop avant cible) 0.7909 [0.75 ; 0.83], R/R 4.243, perte reelle 4.464 % (gap inclus), EV -1.2306 % — **REFUSE**
      - refuse : cible atteinte seulement 6.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.791, borne haute 0.831 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 6.1 % x 18.94 % + P(rien) 14.8 % x 7.72 % ne couvrent pas P(stop) 79.1 % x 4.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.476 %) — p(stop avant cible) 0.6934 [0.64 ; 0.74], R/R 3.349, perte reelle 5.656 % (gap inclus), EV -1.2187 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.693, borne haute 0.740 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 7.0 % x 18.94 % + P(rien) 23.7 % x 5.84 % ne couvrent pas P(stop) 69.3 % x 5.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.345 %) — p(stop avant cible) 0.6267 [0.57 ; 0.68], R/R 2.411, perte reelle 7.856 % (gap inclus), EV -1.9344 % — **REFUSE**
      - refuse : cible atteinte seulement 8.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.627, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 8.0 % x 18.94 % + P(rien) 29.3 % x 5.01 % ne couvrent pas P(stop) 62.7 % x 7.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.083 %) — p(stop avant cible) 0.5097 [0.46 ; 0.56], R/R 1.251, perte reelle 15.141 % (gap inclus), EV -4.6306 % — **REFUSE**
      - refuse : cible atteinte seulement 8.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.510, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.63 %) : P(cible) 8.4 % x 18.94 % + P(rien) 40.6 % x 3.68 % ne couvrent pas P(stop) 51.0 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.952 %) — p(stop avant cible) 0.4417 [0.39 ; 0.49], R/R 1.251, perte reelle 15.141 % (gap inclus), EV -3.622 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.62 %) : P(cible) 8.5 % x 18.94 % + P(rien) 47.3 % x 3.07 % ne couvrent pas P(stop) 44.2 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.821 %) — p(stop avant cible) 0.4004 [0.35 ; 0.45], R/R 1.251, perte reelle 15.141 % (gap inclus), EV -3.0618 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.06 %) : P(cible) 8.5 % x 18.94 % + P(rien) 51.4 % x 2.69 % ne couvrent pas P(stop) 40.0 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.689 %) — p(stop avant cible) 0.3648 [0.32 ; 0.42], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -5.2652 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.27 %) : P(cible) 8.6 % x 18.94 % + P(rien) 54.9 % x 2.35 % ne couvrent pas P(stop) 36.5 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.558 %) — p(stop avant cible) 0.3184 [0.27 ; 0.37], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -4.3635 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.36 %) : P(cible) 8.8 % x 18.94 % + P(rien) 59.4 % x 1.87 % ne couvrent pas P(stop) 31.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.427 %) — p(stop avant cible) 0.2778 [0.23 ; 0.33], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -3.6631 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.66 %) : P(cible) 8.8 % x 18.94 % + P(rien) 63.4 % x 1.42 % ne couvrent pas P(stop) 27.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.165 %) — p(stop avant cible) 0.2041 [0.16 ; 0.25], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -2.4197 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 9.0 % x 18.94 % + P(rien) 70.6 % x 0.64 % ne couvrent pas P(stop) 20.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.903 %) — p(stop avant cible) 0.1477 [0.11 ; 0.19], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -1.5917 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 9.0 % x 18.94 % + P(rien) 76.2 % x 0.02 % ne couvrent pas P(stop) 14.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.26 ATR (stop 15.863 %) — p(stop avant cible) 0.1177 [0.09 ; 0.15], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -1.1964 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 9.0 % x 18.94 % + P(rien) 79.2 % x -0.33 % ne couvrent pas P(stop) 11.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 19.117 %) — p(stop avant cible) 0.0592 [0.04 ; 0.09], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -0.6319 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 9.0 % x 18.94 % + P(rien) 85.1 % x -1.18 % ne couvrent pas P(stop) 5.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 20.855 %) — p(stop avant cible) 0.0455 [0.03 ; 0.07], R/R 0.844, perte reelle 22.429 % (gap inclus), EV -0.5565 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 9.0 % x 18.94 % + P(rien) 86.5 % x -1.43 % ne couvrent pas P(stop) 4.5 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 22.593 %) — p(stop avant cible) 0.0238 [0.01 ; 0.04], R/R 0.838, perte reelle 22.593 % (gap inclus), EV -0.3061 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 9.0 % x 18.94 % + P(rien) 88.6 % x -1.66 % ne couvrent pas P(stop) 2.4 % x 22.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 24.331 %) — p(stop avant cible) 0.0112 [0.00 ; 0.03], R/R 0.778, perte reelle 24.331 % (gap inclus), EV -0.2327 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 9.0 % x 18.94 % + P(rien) 89.9 % x -1.85 % ne couvrent pas P(stop) 1.1 % x 24.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 26.068 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 0.727, perte reelle 26.068 % (gap inclus), EV -0.2394 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 9.0 % x 18.94 % + P(rien) 90.3 % x -1.95 % ne couvrent pas P(stop) 0.7 % x 26.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 27.806 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.681, perte reelle 27.806 % (gap inclus), EV -0.1915 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 9.0 % x 18.94 % + P(rien) 90.5 % x -1.93 % ne couvrent pas P(stop) 0.5 % x 27.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1090.4, ATR14 37.9 (3.476 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.393 ATR = 1.366 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.174 % | 1088.505 | 89.25 % | 92.1 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.348 % | 1086.61 | 83.23 % | 87.76 % | 89.72 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.521 % | 1084.715 | 76.23 % | 82.92 % | 85.67 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.695 % | 1082.82 | 69.72 % | 78.48 % | 81.62 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.869 % | 1080.925 | 62.23 % | 72.66 % | 76.58 % | 81.09 % | 88.36 % | 91.36 % |
| 0.35 ATR | 1.217 % | 1077.135 | 53.85 % | 65.75 % | 71.05 % | 76.63 % | 85.77 % | 89.25 % |
| 0.5 ATR | 1.738 % | 1071.45 | 40.34 % | 54.59 % | 61.36 % | 68.91 % | 80.1 % | 83.62 % |
| 0.75 ATR | 2.607 % | 1061.975 | 23.67 % | 38.99 % | 47.04 % | 57.43 % | 70.25 % | 76.88 % |
| 1.0 ATR | 3.476 % | 1052.5 | 13.02 % | 26.65 % | 36.07 % | 48.22 % | 62.09 % | 70.35 % |
| 1.25 ATR | 4.345 % | 1043.025 | 7.4 % | 18.07 % | 26.28 % | 38.71 % | 53.93 % | 63.82 % |
| 1.5 ATR | 5.214 % | 1033.55 | 3.94 % | 13.13 % | 20.55 % | 31.29 % | 45.67 % | 56.58 % |
| 2.0 ATR | 6.952 % | 1014.6 | 1.78 % | 7.01 % | 12.06 % | 20.59 % | 33.93 % | 46.73 % |
| 2.5 ATR | 8.689 % | 995.65 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 24.68 % | 37.49 % |
| 3.0 ATR | 10.427 % | 976.7 | 0.1 % | 1.38 % | 3.85 % | 7.52 % | 16.92 % | 30.85 % |
| 4.0 ATR | 13.903 % | 938.8 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.46 % | 19.8 % |
| 6.0 ATR | 20.855 % | 863.0 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.57 ATR | 0.65 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.53 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.38 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.79 ATR | 2.04 ATR | 2.75 ATR | 3.59 ATR |
| **10 s.** | 0.63 ATR | 1.37 ATR | 1.53 ATR | 2.05 ATR | 2.48 ATR | 2.80 ATR | 3.82 ATR | 4.90 ATR |
| **20 s.** | 0.82 ATR | 1.83 ATR | 2.09 ATR | 2.84 ATR | 3.53 ATR | 3.98 ATR | 5.20 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.448–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.654–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.607 %, prix 1061.9733), p(touche) 38.99 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.796–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.476 %, prix 1052.4977), p(touche) 36.07 % (en stress 95.1 %)  ✅ optimum identifie (68.2 % des re-echantillons)
- **5 seance(s)** : plage utile 1.085–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.345 %, prix 1043.0221), p(touche) 38.71 % (en stress 98.02 %)  ✅ optimum identifie (88.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.529–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.952 %, prix 1014.5954), p(touche) 33.93 % (en stress 96.04 %)  ✅ optimum identifie (99.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.094–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.689 %, prix 995.6552), p(touche) 37.49 % (en stress 98.0 %)  ✅ optimum identifie (99.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.088 | EV/share : €1.843 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 64 % | T2 43 % | T3 26 %
- Kelly (position) : f* 0.159 | ¼-Kelly 0.04 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.0 | bear 7.0 | side 11.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.622% → cible +1.141% / stop −2.0%, p_fill 24%, n_eff≈8.0) : P(cible|rempli) **44%** · **EV/risk +0.039** (×p_fill ; si rempli +0.33% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.03% (p90 6.55%) · excursion haute méd. +2.05% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.584% vs midi 0.93% vs clôture 1.052% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.438% ; recovery-V 22%
- **σ réalisé intraday** 2.549% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 1077.4625 (VA 1075.4125–1087.7125 ; dernier close 1079.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 62% · **stop −2.78%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.53% · baisse 28% (gap-down >1% 9% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.75% (p90 −1.76%) · haut méd +0.49% · range méd 1.34%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.04%) · haut méd +0.58% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.99% (p90 −2.24%) · haut méd +0.77% · range méd 1.98%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −2.64%) · haut méd +0.88% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1079.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 69% (105/159) · gap 19% · délai 1.0min · rebond 52% (55/105) (MFE +1.05%)
   - −1.0% : fill 30min 40% · séance 63% (93/159) · gap 9% · délai 6.3min · rebond 61% (56/93) (MFE +1.19%)
   - −1.5% : fill 30min 25% · séance 50% (77/159) · gap 6% · délai 28.2min · rebond 57% (44/77) (MFE +1.19%)
   - −2.0% : fill 30min 18% · séance 42% (65/159) · gap 4% · délai 53.3min · rebond 62% (40/65) (MFE +1.3%)
   - −3.0% : fill 30min 6% · séance 24% (34/159) · gap 3% · délai 225.8min · rebond 46% (17/34) (MFE +0.93%)
   - −4.0% : fill 30min 4% · séance 13% (23/159) · gap 2% · délai 174.9min · rebond 69% (14/23) (MFE +1.69%)
   - −5.0% : fill 30min 1% · séance 7% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −1.47%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.7%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.74%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=542 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (34 séances) :
      · −1.0% : fill 96% (33/34) · rebond 80% (25/33)
      · −2.0% : fill 76% (28/34) · rebond 66% (19/28)
      · −3.0% : fill 40% (13/34) · rebond 60% (8/13)
      · −4.0% : fill 34% (11/34) · rebond 72% (8/11)
      · −5.0% : fill 23% (7/34) · rebond 100% (7/7)
   - **flat** (20 séances) :
      · −1.0% : fill 84% (14/20) · rebond 60% (10/14)
      · −2.0% : fill 52% (8/20) · rebond 71% (6/8)
      · −3.0% : fill 29% (4/20) · rebond 37% (1/4)
      · −4.0% : fill 9% (2/20) · rebond 62% (1/2)
      · −5.0% : fill 9% (2/20) · rebond 62% (1/2)
   - **gap-up** (105 séances) :
      · −1.0% : fill 47% (46/105) · rebond 48% (21/46)
      · −2.0% : fill 28% (29/105) · rebond 54% (15/29)
      · −3.0% : fill 17% (17/105) · rebond 41% (8/17)
      · −4.0% : fill 7% (10/105) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/105) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 60% si les 15 1res min sont vertes (74 cas) · 33% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 66% si début vert vs 25% si rouge (base 44% · écart 40 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **66%** · continue >prix actuel 40% ; creux résiduel méd -1.25% (q20 -2.93%) → **SL/trailing à −2.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +1.88% → **scale +1.28% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **25%** (continue à baisser 52%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.11%** (au-delà de la MAE q10 -4.11%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.6% .. +3.18%] · haut q95 +3.56% · bas q05 -3.0%
   - 60min (n=160) : retour [-2.72% .. +3.16%] · haut q95 +4.28% · bas q05 -3.69%
   - 2h (n=160) : retour [-3.14% .. +2.91%] · haut q95 +4.35% · bas q05 -4.21%
   - 4h (n=160) : retour [-3.27% .. +3.05%] · haut q95 +4.82% · bas q05 -4.57%
   - 6h (n=160) : retour [-4.0% .. +3.22%] · haut q95 +4.87% · bas q05 -4.89%
   - session (n=160) : retour [-4.46% .. +3.65%] · haut q95 +4.99% · bas q05 -5.62%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 37.8  _(momentum baissier)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist -12.315  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 12.6%
- **ATR** : 37.9 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.232  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 43.9  _(transition)_
- **MA** : MA20 1151.99 · MA50 1090.79 · MA200 1393.82  _(prix < MA20)_
- **Dist MA** : MA20 -5.3% · MA50 -0.0% · MA200 -21.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (494822 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
