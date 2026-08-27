# CEG

**Generated** : 2026-08-27T00:32:47.992939+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $279.52  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $279.52 (+1.3% vs entrée) · entrée $275.93 · stop $271.79 · T1 $278.99 · R/R 0.74  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.155 _(réel 5 s)_ (GBM -0.021) · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -95 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $275.32–$276.55 (mid $275.93)
- Spot actuel : $279.52 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $271.79 (stop swing_plan-based (-5.84%))
- Targets : T1 $278.99 · R/R 0.74 | T2 $282.05 · R/R 1.48 | T3 $285.11 · R/R 2.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $271.79


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.99 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.84 %)** : le gap seul le franchit 0.433 % des séances (5 fois sur 1154).
   - exécution **2.05 pt plus bas** dans le cas TYPIQUE (médiane), 7.622 au p90, **9.984 au pire**
   - perte réelle **9.329 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 5.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0151 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.822 % | p01 -4.437 % | pire -15.824 % _(sur 1154 séances)_
- **P(stop avant cible)** _(source : daily, 1155 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.403** [0.332 ; 0.4772] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4316** [0.3801 ; 0.4842] _(largeur 10.4 pt, n_eff 345.3)_
   - deep : **0.4354** [0.3838 ; 0.4881] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.5 observations effectives », dont la borne haute a 95 % vaut environ 18.2 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 17.0 observations effectives », dont la borne haute a 95 % vaut environ 17.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.6 pt), swing (45.0 pt), deep (40.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.11 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.66 % contre 2.87 % aujourd'hui, rapport 1.97)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.63 % vs -9.59 % si l'on extrapolait par √5 _(rapport 1.005 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1874** (β de hausse 1.1919, asymétrie 0.9962) vs SPY — 529 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 254.1908 sur atr_grid (3.0 ATR, 9.062 %) — p(stop avant cible) 0.3343 [0.29 ; 0.39], R/R 2.662, perte reelle 12.871 % (gap inclus), CVaR 9.069 %, EV -1.4784 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.531 %) — p(stop avant cible) 0.6066 [0.55 ; 0.66], R/R 4.695, perte reelle 7.297 % (gap inclus), EV -1.5101 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.607, borne haute 0.657 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.51 %) : P(cible) 0.9 % x 34.26 % + P(rien) 38.5 % x 6.82 % ne couvrent pas P(stop) 60.7 % x 7.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.94 ATR (stop 7.567 %) — p(stop avant cible) 0.4044 [0.35 ; 0.46], R/R 3.056, perte reelle 11.211 % (gap inclus), EV -1.5975 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 0.9 % x 34.26 % + P(rien) 58.7 % x 4.51 % ne couvrent pas P(stop) 40.4 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.07 ATR (stop 20.035 %) — p(stop avant cible) 0.0211 [0.01 ; 0.04], R/R 1.71, perte reelle 20.035 % (gap inclus), EV 0.0987 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.04 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.755 %) — p(stop avant cible) 0.9434 [0.92 ; 0.96], R/R 17.984, perte reelle 1.905 % (gap inclus), EV -1.1765 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 17.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.943, borne haute 0.964 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.2 % x 34.26 % + P(rien) 5.5 % x 10.07 % ne couvrent pas P(stop) 94.3 % x 1.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.51 %) — p(stop avant cible) 0.8541 [0.81 ; 0.89], R/R 11.617, perte reelle 2.949 % (gap inclus), EV -1.107 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 11.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.854, borne haute 0.888 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 0.5 % x 34.26 % + P(rien) 14.1 % x 8.76 % ne couvrent pas P(stop) 85.4 % x 2.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.265 %) — p(stop avant cible) 0.7532 [0.71 ; 0.80], R/R 8.514, perte reelle 4.024 % (gap inclus), EV -0.8586 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 8.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.753, borne haute 0.796 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.7 % x 34.26 % + P(rien) 24.0 % x 8.06 % ne couvrent pas P(stop) 75.3 % x 4.02 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.021 %) — p(stop avant cible) 0.6859 [0.64 ; 0.73], R/R 6.405, perte reelle 5.349 % (gap inclus), EV -1.1114 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.686, borne haute 0.733 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 0.9 % x 34.26 % + P(rien) 30.6 % x 7.42 % ne couvrent pas P(stop) 68.6 % x 5.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.776 %) — p(stop avant cible) 0.6449 [0.59 ; 0.69], R/R 5.77, perte reelle 5.938 % (gap inclus), EV -1.0491 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.645, borne haute 0.694 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.9 % x 34.26 % + P(rien) 34.7 % x 7.18 % ne couvrent pas P(stop) 64.5 % x 5.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.94 ATR (stop 6.769 %) — p(stop avant cible) 0.463 [0.41 ; 0.52], R/R 3.056, perte reelle 11.211 % (gap inclus), EV -2.1558 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.16 %) : P(cible) 0.9 % x 34.26 % + P(rien) 52.8 % x 5.19 % ne couvrent pas P(stop) 46.3 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.307 %) — p(stop avant cible) 0.3637 [0.31 ; 0.42], R/R 2.662, perte reelle 12.871 % (gap inclus), EV -1.8269 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.9 % x 34.26 % + P(rien) 62.8 % x 4.08 % ne couvrent pas P(stop) 36.4 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 9.062 %) — p(stop avant cible) 0.3343 [0.29 ; 0.39], R/R 2.662, perte reelle 12.871 % (gap inclus), EV -1.4784 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.48 %) : P(cible) 0.9 % x 34.26 % + P(rien) 65.7 % x 3.85 % ne couvrent pas P(stop) 33.4 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.572 %) — p(stop avant cible) 0.2732 [0.23 ; 0.32], R/R 2.165, perte reelle 15.824 % (gap inclus), EV -1.6495 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 0.9 % x 34.26 % + P(rien) 71.8 % x 3.32 % ne couvrent pas P(stop) 27.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.082 %) — p(stop avant cible) 0.2164 [0.18 ; 0.26], R/R 2.165, perte reelle 15.824 % (gap inclus), EV -1.0061 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 0.9 % x 34.26 % + P(rien) 77.5 % x 2.72 % ne couvrent pas P(stop) 21.6 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.592 %) — p(stop avant cible) 0.178 [0.14 ; 0.22], R/R 2.165, perte reelle 15.824 % (gap inclus), EV -0.6084 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 0.9 % x 34.26 % + P(rien) 81.3 % x 2.34 % ne couvrent pas P(stop) 17.8 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 15.103 %) — p(stop avant cible) 0.1156 [0.09 ; 0.15], R/R 2.165, perte reelle 15.824 % (gap inclus), EV -0.174 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.9 % x 34.26 % + P(rien) 87.5 % x 1.54 % ne couvrent pas P(stop) 11.6 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 16.613 %) — p(stop avant cible) 0.0661 [0.04 ; 0.10], R/R 2.062, perte reelle 16.613 % (gap inclus), EV 0.0158 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.61 % > budget 12.00 %
   - 🟢 grid_snapped a 6.07 ATR (stop 19.238 %) — p(stop avant cible) 0.0333 [0.02 ; 0.06], R/R 1.781, perte reelle 19.238 % (gap inclus), EV 0.066 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.634 %) — p(stop avant cible) 0.0297 [0.02 ; 0.05], R/R 1.745, perte reelle 19.634 % (gap inclus), EV 0.0826 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.144 %) — p(stop avant cible) 0.0148 [0.01 ; 0.03], R/R 1.62, perte reelle 21.144 % (gap inclus), EV 0.1407 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.654 %) — p(stop avant cible) 0.0106 [0.00 ; 0.03], R/R 1.512, perte reelle 22.654 % (gap inclus), EV 0.153 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.65 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.164 %) — p(stop avant cible) 0.0084 [0.00 ; 0.02], R/R 1.418, perte reelle 24.164 % (gap inclus), EV 0.1779 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.16 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 279.52, ATR14 8.4431 (3.021 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.387 ATR = 1.169 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.151 % | 279.0978 | 91.61 % | 94.62 % | 95.52 % | 96.63 % | 97.51 % | 97.94 % |
| 0.1 ATR | 0.302 % | 278.6757 | 85.57 % | 90.37 % | 92.26 % | 93.93 % | 95.59 % | 96.69 % |
| 0.15 ATR | 0.453 % | 278.2535 | 79.08 % | 86.0 % | 88.23 % | 90.34 % | 93.67 % | 95.31 % |
| 0.2 ATR | 0.604 % | 277.8314 | 72.15 % | 80.74 % | 83.97 % | 86.63 % | 91.19 % | 93.94 % |
| 0.25 ATR | 0.755 % | 277.4092 | 65.21 % | 75.14 % | 79.26 % | 83.03 % | 88.36 % | 92.11 % |
| 0.35 ATR | 1.057 % | 276.5649 | 53.69 % | 65.51 % | 71.3 % | 76.52 % | 83.73 % | 88.46 % |
| 0.5 ATR | 1.51 % | 275.2985 | 38.59 % | 52.3 % | 59.08 % | 65.84 % | 76.38 % | 82.74 % |
| 0.75 ATR | 2.265 % | 273.1877 | 20.25 % | 36.06 % | 44.51 % | 52.81 % | 65.99 % | 75.77 % |
| 1.0 ATR | 3.021 % | 271.0769 | 11.19 % | 23.74 % | 32.74 % | 42.81 % | 56.84 % | 69.37 % |
| 1.25 ATR | 3.776 % | 268.9662 | 5.82 % | 16.13 % | 23.88 % | 35.17 % | 50.85 % | 63.09 % |
| 1.5 ATR | 4.531 % | 266.8554 | 2.8 % | 10.64 % | 17.15 % | 28.76 % | 44.18 % | 57.37 % |
| 2.0 ATR | 6.041 % | 262.6339 | 0.89 % | 4.37 % | 9.19 % | 17.87 % | 31.53 % | 46.51 % |
| 2.5 ATR | 7.551 % | 258.4124 | 0.45 % | 2.24 % | 4.71 % | 10.9 % | 21.02 % | 36.57 % |
| 3.0 ATR | 9.062 % | 254.1908 | 0.0 % | 1.12 % | 2.8 % | 6.74 % | 15.48 % | 28.57 % |
| 4.0 ATR | 12.082 % | 245.7478 | 0.0 % | 0.22 % | 0.9 % | 2.58 % | 6.78 % | 14.29 % |
| 6.0 ATR | 18.123 % | 228.8617 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.79 % | 2.74 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.90 ATR | 2.61 ATR | 3.42 ATR |
| **10 s.** | 0.53 ATR | 1.28 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.59 ATR | 3.63 ATR | 4.59 ATR |
| **20 s.** | 0.78 ATR | 1.84 ATR | 2.08 ATR | 2.72 ATR | 3.25 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.436–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.51 %, prix 275.2992), p(touche) 38.59 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.612–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.265 %, prix 273.1889), p(touche) 36.06 % (en stress 88.89 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.742–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.265 %, prix 273.1889), p(touche) 44.51 % (en stress 97.78 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.945–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.021 %, prix 271.0757), p(touche) 42.81 % (en stress 96.63 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.469–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.531 %, prix 266.8549), p(touche) 44.18 % (en stress 98.88 %)  ✅ optimum identifie (73.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.076–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.551 %, prix 258.4134), p(touche) 36.57 % (en stress 95.45 %)  ✅ optimum identifie (87.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : $-0.088 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 31 % | T3 9 %
- Kelly (position) : f* 0.057 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 81.0 | bear 6.0 | side 12.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 280.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.279% → cible +1.108% / stop −1.5%, p_fill 47%, n_eff≈19.4) : P(cible|rempli) **35%** · **EV/risk -0.155** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −2.819% → cible +2.477% / stop −3.108%, p_fill 41%, n_eff≈16.5) : P(cible|rempli) **50%** · **EV/risk -0.052** (×p_fill ; si rempli -0.40% du capital)
  - **deep** (entrée dip −4.359% → cible +3.503% / stop −4.737%, p_fill 37%, n_eff≈17.0) : P(cible|rempli) **72%** · **EV/risk +0.085** (×p_fill ; si rempli +1.08% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→68% · +2.0%→38% · +3.0%→16% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.36% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.41%
- Profil de vol intra : ouverture 2.487% vs midi 0.665% vs clôture 0.785% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. -0.434% ; recovery-V 7%
- **σ réalisé intraday** 2.331% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 275.8521 (VA 273.1364–276.4911 ; dernier close 272.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 41% · **stop −2.26%** sous le fill (sous le bruit) · cible +0.7% · R/R 0.31 (high win-rate)
- Gaps overnight (n=159) : méd. 0.64% · baisse 31% (gap-down >1% 11% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.86%) · haut méd +0.86% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −0.66% (p90 −2.25%) · haut méd +1.02% · range méd 2.01%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.8%) · haut méd +1.1% · range méd 2.25%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −3.05%) · haut méd +1.3% · range méd 2.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 272.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 47% · séance 63% (107/159) · gap 19% · délai 1.4min · rebond 56% (61/107) (MFE +1.09%)
   - −1.0% : fill 30min 34% · séance 51% (91/159) · gap 11% · délai 3.7min · rebond 47% (49/91) (MFE +0.9%)
   - −1.5% : fill 30min 27% · séance 39% (72/159) · gap 7% · délai 8.1min · rebond 42% (37/72) (MFE +0.82%)
   - −2.0% : fill 30min 22% · séance 34% (59/159) · gap 4% · délai 12.8min · rebond 56% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 7% · séance 19% (33/159) · gap 2% · délai 46.4min · rebond 41% (13/33) (MFE +0.7%)
   - −4.0% : fill 30min 4% · séance 10% (20/159) · gap 1% · délai 42.9min · rebond 61% (11/20) (MFE +1.17%)
   - −5.0% : fill 30min 2% · séance 5% (13/159) · gap 0% · délai 46.1min · rebond 86% (10/13) (MFE +1.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.16%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.38%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=469 jambes) : jambe baissière méd −1.09% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 94% (40/42) · rebond 61% (25/40)
      · −2.0% : fill 79% (32/42) · rebond 51% (18/32)
      · −3.0% : fill 43% (18/42) · rebond 26% (6/18)
      · −4.0% : fill 38% (15/42) · rebond 63% (8/15)
      · −5.0% : fill 20% (11/42) · rebond 85% (8/11)
   - **flat** (24 séances) :
      · −1.0% : fill 70% (19/24) · rebond 14% (5/19)
      · −2.0% : fill 40% (11/24) · rebond 63% (6/11)
      · −3.0% : fill 25% (7/24) · rebond 22% (2/7)
      · −4.0% : fill 8% (3/24) · rebond 42% (2/3)
      · −5.0% : fill 2% (1/24) · rebond 100% (1/1)
   - **gap-up** (93 séances) :
      · −1.0% : fill 31% (32/93) · rebond 47% (19/32)
      · −2.0% : fill 16% (16/93) · rebond 61% (9/16)
      · −3.0% : fill 8% (8/93) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/93) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/93) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 63% si les 15 1res min sont vertes (93 cas) · 24% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 46% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **82%** · continue >prix actuel 45% ; creux résiduel méd -1.01% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.82% / q75 +1.41% → **scale +0.82% / runner +1.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **8%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.11% .. +2.29%] · haut q95 +2.63% · bas q05 -3.47%
   - 60min (n=160) : retour [-3.68% .. +2.57%] · haut q95 +3.28% · bas q05 -4.68%
   - 2h (n=160) : retour [-3.72% .. +2.9%] · haut q95 +3.97% · bas q05 -4.78%
   - 4h (n=160) : retour [-3.56% .. +3.35%] · haut q95 +4.16% · bas q05 -4.83%
   - 6h (n=160) : retour [-4.25% .. +3.15%] · haut q95 +4.47% · bas q05 -4.87%
   - session (n=160) : retour [-3.99% .. +3.29%] · haut q95 +4.5% · bas q05 -4.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 68.1  _(momentum haussier)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist 0.156  _(pas de croisement recent)_
- **BB** : %B 0.79 · largeur 9.4%
- **ATR** : 8.44 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.24  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 58.0  _(transition)_
- **MA** : MA20 272.15 · MA50 264.14 · MA200 297.66  _(prix > MA20)_
- **Dist MA** : MA20 +2.7% · MA50 +5.8% · MA200 -6.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (815668 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
