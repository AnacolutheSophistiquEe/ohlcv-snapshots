# EVT

**Generated** : 2026-09-21T00:06:24.535512+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · €2.94  

> 🟡 **WAIT-FOR-DIP** — spot +3.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €2.94 (+3.9% vs entrée) · entrée €2.83 · stop €2.71 · T1 €2.86 · R/R 0.25  
> ↳ P(T1 av. stop) 71 % · EV/risk 0.005 · ¼-Kelly 0.059 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €2.82–€2.83 (mid €2.83)
- Spot actuel : €2.94 (+3.9% au-dessus de la zone — repli à attendre)
- Stop : €2.71 (stop swing_plan-based (-11.76%))
- Targets : T1 €2.86 · R/R 0.25 | T2 €2.90 · R/R 0.58 | T3 €2.93 · R/R 0.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €2.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.76 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1274).
   - exécution **5.957 pt plus bas** dans le cas TYPIQUE (médiane), 17.412 au p90, **20.653 au pire**
   - perte réelle **19.926 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 11.76 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0256 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.096** [0.0588 ; 0.1466] _(largeur 8.8 pt, n_eff 173.1)_
   - swing : **0.3975** [0.3469 ; 0.4498] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3702** [0.3206 ; 0.422] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.89 %** | CVaR **-9.26 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 6.00 % contre 3.75 % aujourd'hui, rapport 1.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1116** (β de hausse 0.9571, asymétrie 1.1615) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.5961 sur atr_grid (3.0 ATR, 11.756 %) — p(stop avant cible) 0.2674 [0.22 ; 0.32], R/R 1.68, perte reelle 19.926 % (gap inclus), CVaR 11.782 %, EV -3.6077 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.877 %) — p(stop avant cible) 0.5533 [0.50 ; 0.61], R/R 2.858, perte reelle 11.717 % (gap inclus), EV -3.7179 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.553, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.72 %) : P(cible) 0.7 % x 33.48 % + P(rien) 44.0 % x 5.79 % ne couvrent pas P(stop) 55.3 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.73 ATR (stop 9.324 %) — p(stop avant cible) 0.3468 [0.30 ; 0.40], R/R 1.86, perte reelle 18.001 % (gap inclus), EV -4.0729 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.07 %) : P(cible) 0.7 % x 33.48 % + P(rien) 64.6 % x 2.98 % ne couvrent pas P(stop) 34.7 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.98 %) — p(stop avant cible) 0.9101 [0.88 ; 0.94], R/R 13.389, perte reelle 2.501 % (gap inclus), EV -1.3208 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.910, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.1 % x 33.48 % + P(rien) 8.8 % x 10.24 % ne couvrent pas P(stop) 91.0 % x 2.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.959 %) — p(stop avant cible) 0.8443 [0.80 ; 0.88], R/R 8.359, perte reelle 4.006 % (gap inclus), EV -1.9076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.844, borne haute 0.880 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 0.2 % x 33.48 % + P(rien) 15.3 % x 9.11 % ne couvrent pas P(stop) 84.4 % x 4.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.939 %) — p(stop avant cible) 0.76 [0.71 ; 0.80], R/R 5.108, perte reelle 6.555 % (gap inclus), EV -2.917 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.760, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.92 %) : P(cible) 0.3 % x 33.48 % + P(rien) 23.7 % x 8.29 % ne couvrent pas P(stop) 76.0 % x 6.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.919 %) — p(stop avant cible) 0.703 [0.65 ; 0.75], R/R 3.46, perte reelle 9.679 % (gap inclus), EV -4.5087 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.703, borne haute 0.749 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.51 %) : P(cible) 0.3 % x 33.48 % + P(rien) 29.4 % x 7.43 % ne couvrent pas P(stop) 70.3 % x 9.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.898 %) — p(stop avant cible) 0.6292 [0.58 ; 0.68], R/R 2.858, perte reelle 11.717 % (gap inclus), EV -4.7114 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.629, borne haute 0.679 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.71 %) : P(cible) 0.5 % x 33.48 % + P(rien) 36.5 % x 6.79 % ne couvrent pas P(stop) 62.9 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.73 ATR (stop 7.943 %) — p(stop avant cible) 0.4122 [0.36 ; 0.46], R/R 1.86, perte reelle 18.001 % (gap inclus), EV -5.0124 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.01 %) : P(cible) 0.7 % x 33.48 % + P(rien) 58.1 % x 3.73 % ne couvrent pas P(stop) 41.2 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.817 %) — p(stop avant cible) 0.3791 [0.33 ; 0.43], R/R 1.86, perte reelle 18.001 % (gap inclus), EV -4.5226 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.52 %) : P(cible) 0.7 % x 33.48 % + P(rien) 61.4 % x 3.35 % ne couvrent pas P(stop) 37.9 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.776 %) — p(stop avant cible) 0.3035 [0.26 ; 0.35], R/R 1.68, perte reelle 19.926 % (gap inclus), EV -4.0916 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.09 %) : P(cible) 0.7 % x 33.48 % + P(rien) 68.9 % x 2.48 % ne couvrent pas P(stop) 30.3 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.756 %) — p(stop avant cible) 0.2674 [0.22 ; 0.32], R/R 1.68, perte reelle 19.926 % (gap inclus), EV -3.6077 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.61 %) : P(cible) 0.7 % x 33.48 % + P(rien) 72.5 % x 2.03 % ne couvrent pas P(stop) 26.7 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 13.715 %) — p(stop avant cible) 0.1849 [0.15 ; 0.23], R/R 1.481, perte reelle 22.616 % (gap inclus), EV -3.1591 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.16 %) : P(cible) 0.7 % x 33.48 % + P(rien) 80.8 % x 0.96 % ne couvrent pas P(stop) 18.5 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 15.674 %) — p(stop avant cible) 0.1423 [0.11 ; 0.18], R/R 1.24, perte reelle 27.012 % (gap inclus), EV -3.1836 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.18 %) : P(cible) 0.7 % x 33.48 % + P(rien) 85.0 % x 0.49 % ne couvrent pas P(stop) 14.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 17.634 %) — p(stop avant cible) 0.1138 [0.08 ; 0.15], R/R 1.24, perte reelle 27.012 % (gap inclus), EV -2.6899 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.69 %) : P(cible) 0.7 % x 33.48 % + P(rien) 87.9 % x 0.16 % ne couvrent pas P(stop) 11.4 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 19.593 %) — p(stop avant cible) 0.1014 [0.07 ; 0.14], R/R 1.24, perte reelle 27.012 % (gap inclus), EV -2.5118 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 0.7 % x 33.48 % + P(rien) 89.1 % x -0.02 % ne couvrent pas P(stop) 10.1 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 21.552 %) — p(stop avant cible) 0.0959 [0.07 ; 0.13], R/R 1.24, perte reelle 27.012 % (gap inclus), EV -2.4343 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.43 %) : P(cible) 0.7 % x 33.48 % + P(rien) 89.7 % x -0.10 % ne couvrent pas P(stop) 9.6 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 23.512 %) — p(stop avant cible) 0.0885 [0.06 ; 0.12], R/R 1.033, perte reelle 32.413 % (gap inclus), EV -2.8452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.85 %) : P(cible) 0.7 % x 33.48 % + P(rien) 90.4 % x -0.24 % ne couvrent pas P(stop) 8.8 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 25.471 %) — p(stop avant cible) 0.0771 [0.05 ; 0.11], R/R 1.033, perte reelle 32.413 % (gap inclus), EV -2.7079 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.71 %) : P(cible) 0.7 % x 33.48 % + P(rien) 91.6 % x -0.50 % ne couvrent pas P(stop) 7.7 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 27.43 %) — p(stop avant cible) 0.0658 [0.04 ; 0.10], R/R 1.033, perte reelle 32.413 % (gap inclus), EV -2.6087 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.7 % x 33.48 % + P(rien) 92.7 % x -0.78 % ne couvrent pas P(stop) 6.6 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 29.39 %) — p(stop avant cible) 0.0475 [0.03 ; 0.07], R/R 1.033, perte reelle 32.413 % (gap inclus), EV -2.4643 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.46 %) : P(cible) 0.7 % x 33.48 % + P(rien) 94.5 % x -1.24 % ne couvrent pas P(stop) 4.8 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 31.349 %) — p(stop avant cible) 0.0446 [0.03 ; 0.07], R/R 1.033, perte reelle 32.413 % (gap inclus), EV -2.4447 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.44 %) : P(cible) 0.7 % x 33.48 % + P(rien) 94.8 % x -1.31 % ne couvrent pas P(stop) 4.5 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.942, ATR14 0.1153 (3.919 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.434 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.196 % | 2.9362 | 89.05 % | 91.81 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.392 % | 2.9305 | 81.66 % | 86.97 % | 89.62 % | 92.67 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.588 % | 2.9247 | 75.35 % | 83.12 % | 86.56 % | 89.9 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.784 % | 2.9189 | 69.03 % | 79.07 % | 83.3 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 0.98 % | 2.9132 | 63.31 % | 75.81 % | 80.24 % | 84.75 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.372 % | 2.9016 | 51.78 % | 67.62 % | 73.81 % | 79.8 % | 86.17 % | 91.56 % |
| 0.5 ATR | 1.959 % | 2.8844 | 35.5 % | 54.99 % | 62.85 % | 70.69 % | 80.1 % | 88.24 % |
| 0.75 ATR | 2.939 % | 2.8555 | 19.13 % | 37.81 % | 47.63 % | 59.31 % | 71.74 % | 81.91 % |
| 1.0 ATR | 3.919 % | 2.8267 | 9.96 % | 24.68 % | 35.77 % | 47.43 % | 62.29 % | 75.28 % |
| 1.25 ATR | 4.898 % | 2.7979 | 4.73 % | 17.18 % | 27.27 % | 39.41 % | 55.42 % | 70.05 % |
| 1.5 ATR | 5.878 % | 2.7691 | 2.96 % | 11.15 % | 19.57 % | 31.39 % | 48.36 % | 64.72 % |
| 2.0 ATR | 7.837 % | 2.7114 | 1.28 % | 4.94 % | 9.49 % | 19.41 % | 34.73 % | 52.46 % |
| 2.5 ATR | 9.797 % | 2.6538 | 0.49 % | 2.67 % | 5.63 % | 12.28 % | 27.46 % | 44.62 % |
| 3.0 ATR | 11.756 % | 2.5961 | 0.39 % | 1.68 % | 3.66 % | 8.61 % | 20.5 % | 37.69 % |
| 4.0 ATR | 15.674 % | 2.4809 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.44 % | 24.22 % |
| 6.0 ATR | 23.512 % | 2.2503 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 0.99 ATR | 1.16 ATR | 1.59 ATR | 2.00 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.08 ATR | 1.32 ATR | 1.49 ATR | 1.98 ATR | 2.66 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.81 ATR | 3.81 ATR |
| **10 s.** | 0.65 ATR | 1.44 ATR | 1.62 ATR | 2.12 ATR | 2.68 ATR | 3.06 ATR | 4.46 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.16 ATR | 2.48 ATR | 3.35 ATR | 3.94 ATR | 4.80 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.939 %, prix 2.8555), p(touche) 37.81 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.919 %, prix 2.8267), p(touche) 35.77 % (en stress 96.08 %)  ✅ optimum identifie (62.5 % des re-echantillons)
- **5 seance(s)** : plage utile 1.076–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.898 %, prix 2.7979), p(touche) 39.41 % (en stress 95.05 %)  ✅ optimum identifie (74.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.623–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.837 %, prix 2.7114), p(touche) 34.73 % (en stress 97.03 %)  ✅ optimum identifie (75.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.476–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.797 %, prix 2.6538), p(touche) 44.62 % (en stress 98.0 %)  ✅ optimum identifie (85.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : €-0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 27 % | T3 12 %
- Kelly (position) : f* 0.235 | ¼-Kelly 0.059 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 77.9 | bear 5.0 | side 17.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→69% · +2.0%→41% · +3.0%→21% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.26%) · excursion haute méd. +1.57% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.39% vs midi 1.183% vs clôture 1.156% _(ouverture ~2.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.092 ; mean-reverting — autocorr -0.184)_ ; drift intra méd. -0.657% ; recovery-V 22%
- **σ réalisé intraday** 2.883% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 75% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 3.2156 (VA 3.191–3.2341 ; dernier close 3.203)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 55% · rebond 63% · **stop −2.51%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 40% (gap-down >1% 9% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.2%) · haut méd +0.37% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.65%) · haut méd +0.56% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.77%) · haut méd +0.71% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.93%) · haut méd +0.88% · range méd 2.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.212 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 79% (131/159) · gap 22% · délai 1.0min · rebond 65% (88/131) (MFE +1.39%)
   - −1.0% : fill 30min 38% · séance 67% (112/159) · gap 9% · délai 6.9min · rebond 63% (74/112) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 55% (95/159) · gap 5% · délai 25.1min · rebond 63% (61/95) (MFE +1.33%)
   - −2.0% : fill 30min 19% · séance 44% (79/159) · gap 5% · délai 43.0min · rebond 50% (44/79) (MFE +0.99%)
   - −3.0% : fill 30min 9% · séance 23% (49/159) · gap 3% · délai 59.4min · rebond 66% (35/49) (MFE +1.5%)
   - −4.0% : fill 30min 4% · séance 10% (26/159) · gap 1% · délai 46.7min · rebond 53% (16/26) (MFE +1.13%)
   - −5.0% : fill 30min 3% · séance 6% (15/159) · gap 1% · délai 30.3min · rebond 59% (10/15) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −2.19%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.83%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −1.85%) → stop au-delà de −1.58% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=808 jambes) : jambe baissière méd −1.07% (p90 −2.28%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (47/55) · rebond 64% (32/47)
      · −2.0% : fill 62% (37/55) · rebond 48% (21/37)
      · −3.0% : fill 35% (25/55) · rebond 68% (18/25)
      · −4.0% : fill 21% (18/55) · rebond 42% (11/18)
      · −5.0% : fill 15% (12/55) · rebond 40% (7/12)
   - **flat** (35 séances) :
      · −1.0% : fill 85% (28/35) · rebond 49% (16/28)
      · −2.0% : fill 62% (21/35) · rebond 44% (9/21)
      · −3.0% : fill 35% (13/35) · rebond 79% (10/13)
      · −4.0% : fill 7% (3/35) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/35) · rebond 100% (1/1)
   - **gap-up** (69 séances) :
      · −1.0% : fill 49% (37/69) · rebond 73% (26/37)
      · −2.0% : fill 24% (21/69) · rebond 60% (14/21)
      · −3.0% : fill 9% (11/69) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/69) · rebond 95% (4/5)
      · −5.0% : fill 3% (2/69) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 62% si début vert vs 33% si rouge (base 45% · écart 29 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **62%** · continue >prix actuel 35% ; creux résiduel méd -1.77% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.42% → **scale +1.38% / runner +2.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **33%** (continue à baisser 55%) → **RÉDUIRE ~67%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.16%** (au-delà de la MAE q10 -4.16%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +2.07%] · haut q95 +2.96% · bas q05 -3.91%
   - 60min (n=160) : retour [-2.99% .. +2.44%] · haut q95 +3.08% · bas q05 -3.96%
   - 2h (n=160) : retour [-3.46% .. +2.37%] · haut q95 +3.72% · bas q05 -4.16%
   - 4h (n=160) : retour [-3.35% .. +3.62%] · haut q95 +4.28% · bas q05 -4.28%
   - 6h (n=160) : retour [-3.3% .. +3.75%] · haut q95 +5.24% · bas q05 -4.99%
   - session (n=160) : retour [-4.11% .. +4.05%] · haut q95 +5.66% · bas q05 -5.54%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 33.0  _(momentum baissier)_
- **ADX** : 36.9  _(tendance etablie)_
- **MACD** : hist -0.009  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 24.3%
- **ATR** : 0.12 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.398  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 37.0  _(marche directionnel)_
- **MA** : MA20 3.13 · MA50 3.38 · MA200 4.81  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -12.9% · MA200 -38.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (815739 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
