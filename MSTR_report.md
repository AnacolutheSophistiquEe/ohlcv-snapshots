# MSTR

**Generated** : 2026-08-27T00:25:05.964875+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $123.19  

> 🟡 **WAIT-FOR-DIP** — spot +2.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $123.19 (+2.6% vs entrée) · entrée $120.01 · stop $112.89 · T1 $126.57 · R/R 0.92  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk 0.014 _(réel 5 s)_ (GBM -0.062) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 124 % hors [0,100] (R² max 0.70). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $118.69–$121.32 (mid $120.01)
- Spot actuel : $123.19 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : $112.89 (stop swing_plan-based (-8.36%))
- Targets : T1 $126.57 · R/R 0.92 | T2 $133.14 · R/R 1.84 | T3 $139.71 · R/R 2.77
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $112.89


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.36 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **3.039 pt plus bas** dans le cas TYPIQUE (médiane), 18.377 au p90, **19.012 au pire**
   - perte réelle **14.455 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 8.36 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0438 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.222** [0.165 ; 0.2882] _(largeur 12.3 pt, n_eff 173.1)_
   - swing : **0.4583** [0.4063 ; 0.511] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4245** [0.3732 ; 0.4771] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.8 pt), swing (36.5 pt), deep (34.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.92 %** | CVaR **-10.5 %** | vol 5.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.31 % contre 4.69 % aujourd'hui, rapport 1.77)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.77 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3288** (β de hausse 1.8725, asymétrie 1.2436) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 110.7312 sur atr_grid (1.75 ATR, 10.113 %) — p(stop avant cible) 0.4688 [0.42 ; 0.52], R/R 1.338, perte reelle 17.215 % (gap inclus), CVaR 10.147 %, EV -4.3056 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 24 des 24 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 55.6 % de la queue et il ne reste que -172.39 EUR a partager. Prix du risque -0.087 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.95 ATR (stop 8.043 %) — p(stop avant cible) 0.5544 [0.50 ; 0.61], R/R 1.665, perte reelle 13.835 % (gap inclus), EV -3.9095 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.554, borne haute 0.606 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.81 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.451 ; 0.510] sur 1199 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.91 %) : P(cible) 9.4 % x 23.03 % + P(rien) 35.1 % x 4.53 % ne couvrent pas P(stop) 55.4 % x 13.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.67 ATR (stop 17.971 %) — p(stop avant cible) 0.2158 [0.17 ; 0.26], R/R 0.854, perte reelle 26.975 % (gap inclus), EV -3.7402 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.74 %) : P(cible) 10.0 % x 23.03 % + P(rien) 68.4 % x -0.32 % ne couvrent pas P(stop) 21.6 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.77 ATR (stop 30.115 %) — p(stop avant cible) 0.0483 [0.03 ; 0.07], R/R 0.765, perte reelle 30.115 % (gap inclus), EV -2.0086 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.01 %) : P(cible) 10.0 % x 23.03 % + P(rien) 85.2 % x -3.36 % ne couvrent pas P(stop) 4.8 % x 30.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.445 %) — p(stop avant cible) 0.9465 [0.92 ; 0.97], R/R 6.831, perte reelle 3.372 % (gap inclus), EV -2.5429 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.947, borne haute 0.967 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.54 %) : P(cible) 1.5 % x 23.03 % + P(rien) 3.9 % x 7.94 % ne couvrent pas P(stop) 94.7 % x 3.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.89 %) — p(stop avant cible) 0.8585 [0.82 ; 0.89], R/R 4.501, perte reelle 5.117 % (gap inclus), EV -2.6394 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.859, borne haute 0.892 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.64 %) : P(cible) 4.9 % x 23.03 % + P(rien) 9.3 % x 6.84 % ne couvrent pas P(stop) 85.9 % x 5.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.95 ATR (stop 7.246 %) — p(stop avant cible) 0.5995 [0.55 ; 0.65], R/R 2.075, perte reelle 11.102 % (gap inclus), EV -3.1088 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.600, borne haute 0.650 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.11 %) : P(cible) 9.2 % x 23.03 % + P(rien) 30.8 % x 4.61 % ne couvrent pas P(stop) 60.0 % x 11.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.113 %) — p(stop avant cible) 0.4688 [0.42 ; 0.52], R/R 1.338, perte reelle 17.215 % (gap inclus), EV -4.3056 % — **REFUSE**
      - refuse : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.31 %) : P(cible) 9.6 % x 23.03 % + P(rien) 43.5 % x 3.56 % ne couvrent pas P(stop) 46.9 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.558 %) — p(stop avant cible) 0.4055 [0.35 ; 0.46], R/R 1.143, perte reelle 20.144 % (gap inclus), EV -4.5122 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.51 %) : P(cible) 9.7 % x 23.03 % + P(rien) 49.7 % x 2.85 % ne couvrent pas P(stop) 40.6 % x 20.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 13.003 %) — p(stop avant cible) 0.3614 [0.31 ; 0.41], R/R 1.004, perte reelle 22.94 % (gap inclus), EV -4.9303 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.93 %) : P(cible) 9.8 % x 23.03 % + P(rien) 54.1 % x 2.05 % ne couvrent pas P(stop) 36.1 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.67 ATR (stop 17.173 %) — p(stop avant cible) 0.2271 [0.19 ; 0.27], R/R 0.854, perte reelle 26.975 % (gap inclus), EV -3.936 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.94 %) : P(cible) 10.0 % x 23.03 % + P(rien) 67.3 % x -0.17 % ne couvrent pas P(stop) 22.7 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 20.227 %) — p(stop avant cible) 0.1757 [0.14 ; 0.22], R/R 0.854, perte reelle 26.975 % (gap inclus), EV -3.135 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.14 %) : P(cible) 10.0 % x 23.03 % + P(rien) 72.4 % x -0.96 % ne couvrent pas P(stop) 17.6 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 23.116 %) — p(stop avant cible) 0.1379 [0.10 ; 0.18], R/R 0.854, perte reelle 26.975 % (gap inclus), EV -2.5913 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.59 %) : P(cible) 10.0 % x 23.03 % + P(rien) 76.2 % x -1.54 % ne couvrent pas P(stop) 13.8 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 26.006 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 0.854, perte reelle 26.975 % (gap inclus), EV -2.0609 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 10.0 % x 23.03 % + P(rien) 81.5 % x -2.55 % ne couvrent pas P(stop) 8.5 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.77 ATR (stop 29.317 %) — p(stop avant cible) 0.0562 [0.04 ; 0.08], R/R 0.786, perte reelle 29.317 % (gap inclus), EV -2.058 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 10.0 % x 23.03 % + P(rien) 84.4 % x -3.22 % ne couvrent pas P(stop) 5.6 % x 29.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 31.785 %) — p(stop avant cible) 0.0327 [0.02 ; 0.06], R/R 0.725, perte reelle 31.785 % (gap inclus), EV -1.9638 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.96 %) : P(cible) 10.0 % x 23.03 % + P(rien) 86.7 % x -3.73 % ne couvrent pas P(stop) 3.3 % x 31.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 34.675 %) — p(stop avant cible) 0.0204 [0.01 ; 0.04], R/R 0.664, perte reelle 34.675 % (gap inclus), EV -1.908 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 10.0 % x 23.03 % + P(rien) 87.9 % x -3.99 % ne couvrent pas P(stop) 2.0 % x 34.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 37.564 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 0.613, perte reelle 37.564 % (gap inclus), EV -1.8089 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.81 %) : P(cible) 10.0 % x 23.03 % + P(rien) 89.3 % x -4.32 % ne couvrent pas P(stop) 0.7 % x 37.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 40.454 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.569, perte reelle 40.454 % (gap inclus), EV -1.7607 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 10.0 % x 23.03 % + P(rien) 89.9 % x -4.48 % ne couvrent pas P(stop) 0.1 % x 40.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 43.343 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.531, perte reelle 43.343 % (gap inclus), EV -1.7539 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 10.0 % x 23.03 % + P(rien) 89.9 % x -4.49 % ne couvrent pas P(stop) 0.1 % x 43.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 46.233 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.498, perte reelle 46.233 % (gap inclus), EV -1.7473 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 10.0 % x 23.03 % + P(rien) 90.0 % x -4.50 % ne couvrent pas P(stop) 0.0 % x 46.23 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 123.19, ATR14 7.1193 (5.779 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.397 ATR = 2.294 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.289 % | 122.834 | 94.36 % | 96.67 % | 97.07 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.578 % | 122.4781 | 88.32 % | 92.14 % | 93.54 % | 94.84 % | 96.75 % | 97.33 % |
| 0.15 ATR | 0.867 % | 122.1221 | 81.47 % | 87.2 % | 89.71 % | 91.81 % | 94.21 % | 95.59 % |
| 0.2 ATR | 1.156 % | 121.7661 | 73.82 % | 81.96 % | 84.96 % | 88.17 % | 91.57 % | 93.84 % |
| 0.25 ATR | 1.445 % | 121.4102 | 67.98 % | 78.12 % | 82.24 % | 86.25 % | 89.33 % | 92.3 % |
| 0.35 ATR | 2.023 % | 120.6983 | 55.29 % | 68.95 % | 75.48 % | 80.99 % | 85.87 % | 89.63 % |
| 0.5 ATR | 2.89 % | 119.6304 | 38.27 % | 55.54 % | 63.67 % | 71.39 % | 78.66 % | 84.91 % |
| 0.75 ATR | 4.334 % | 117.8505 | 19.23 % | 37.8 % | 47.33 % | 58.34 % | 68.6 % | 77.62 % |
| 1.0 ATR | 5.779 % | 116.0707 | 9.37 % | 25.3 % | 35.12 % | 46.81 % | 59.45 % | 70.53 % |
| 1.25 ATR | 7.224 % | 114.2909 | 4.13 % | 14.62 % | 25.33 % | 36.5 % | 50.41 % | 63.35 % |
| 1.5 ATR | 8.669 % | 112.5111 | 2.11 % | 8.77 % | 17.46 % | 29.32 % | 43.5 % | 57.49 % |
| 2.0 ATR | 11.558 % | 108.9514 | 0.2 % | 3.12 % | 7.47 % | 16.38 % | 31.71 % | 47.64 % |
| 2.5 ATR | 14.448 % | 105.3918 | 0.1 % | 0.91 % | 2.42 % | 8.8 % | 21.75 % | 37.89 % |
| 3.0 ATR | 17.337 % | 101.8321 | 0.1 % | 0.5 % | 1.01 % | 4.65 % | 14.74 % | 28.23 % |
| 4.0 ATR | 23.116 % | 94.7129 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.3 % | 18.17 % |
| 6.0 ATR | 34.675 % | 80.4743 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.85 ATR | 1.01 ATR | 1.12 ATR | 1.45 ATR | 1.83 ATR |
| **3 s.** | 0.36 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.42 ATR | 1.87 ATR | 2.25 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.37 ATR | 1.67 ATR | 1.86 ATR | 2.42 ATR | 2.96 ATR |
| **10 s.** | 0.59 ATR | 1.26 ATR | 1.45 ATR | 1.95 ATR | 2.34 ATR | 2.62 ATR | 3.56 ATR | 4.46 ATR |
| **20 s.** | 0.84 ATR | 1.88 ATR | 2.13 ATR | 2.75 ATR | 3.32 ATR | 3.82 ATR | 5.19 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.441–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.89 %, prix 119.6298), p(touche) 38.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.649–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.334 %, prix 117.8509), p(touche) 37.8 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.798–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.779 %, prix 116.0709), p(touche) 35.12 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.044–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.224 %, prix 114.2908), p(touche) 36.5 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.446–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.669 %, prix 112.5107), p(touche) 43.5 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.135–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.448 %, prix 105.3915), p(touche) 37.89 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.062 | EV/share : $-0.444 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 21 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 63.5 | bear 18.4 | side 18.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 370.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.177% → cible +2.448% / stop −4.0%, p_fill 71%, n_eff≈30.8) : P(cible|rempli) **45%** · **EV/risk +0.063** (×p_fill ; si rempli +0.35% du capital)
  - **swing** (entrée dip −2.581% → cible +5.473% / stop −5.932%, p_fill 63%, n_eff≈25.8) : P(cible|rempli) **42%** · **EV/risk +0.014** (×p_fill ; si rempli +0.13% du capital)
  - **deep** (entrée dip −3.991% → cible +7.74% / stop −9.029%, p_fill 62%, n_eff≈26.9) : P(cible|rempli) **63%** · **EV/risk +0.160** (×p_fill ; si rempli +2.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→72% · +2.0%→56% · +3.0%→40% · +5.0%→15% · +8.0%→8%
- Range intraday médian 5.44% (p90 9.85%) · excursion haute méd. +2.41% / basse méd. −2.6%
- Profil de vol intra : ouverture 3.394% vs midi 1.211% vs clôture 1.366% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.265% ; recovery-V 22%
- **σ réalisé intraday** 3.736% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 79% / bas 60% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 120.1996 (VA 118.8924–120.4901 ; dernier close 119.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 77% · **stop −4.58%** sous le fill (sous le bruit) · cible +1.75% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. -0.02% · baisse 52% (gap-down >1% 39% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.12%) · haut méd +0.71% · range méd 1.77%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.9%) · haut méd +1.18% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.44%) · haut méd +1.37% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.58% (p90 −3.66%) · haut méd +1.72% · range méd 3.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 119.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (123/159) · gap 43% · délai 0.0min · rebond 50% (61/123) (MFE +1.0%)
   - −1.0% : fill 30min 58% · séance 69% (118/159) · gap 39% · délai 0.0min · rebond 55% (67/118) (MFE +1.05%)
   - −1.5% : fill 30min 52% · séance 66% (110/159) · gap 31% · délai 0.0min · rebond 60% (66/110) (MFE +1.5%)
   - −2.0% : fill 30min 46% · séance 57% (99/159) · gap 24% · délai 0.0min · rebond 59% (61/99) (MFE +1.44%)
   - −3.0% : fill 30min 31% · séance 47% (78/159) · gap 13% · délai 3.6min · rebond 58% (47/78) (MFE +1.63%)
   - −4.0% : fill 30min 21% · séance 38% (64/159) · gap 5% · délai 18.2min · rebond 65% (42/64) (MFE +1.63%)
   - −5.0% : fill 30min 14% · séance 27% (47/159) · gap 3% · délai 31.7min · rebond 77% (34/47) (MFE +1.75%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.46%) → stop au-delà de −1.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.68%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.95% (p90 −2.54%) → stop au-delà de −1.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=972 jambes) : jambe baissière méd −1.13% (p90 −2.69%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 100% (76/76) · rebond 49% (37/76)
      · −2.0% : fill 92% (70/76) · rebond 58% (40/70)
      · −3.0% : fill 81% (62/76) · rebond 60% (37/62)
      · −4.0% : fill 67% (52/76) · rebond 65% (34/52)
      · −5.0% : fill 50% (40/76) · rebond 80% (30/40)
   - **flat** (20 séances) :
      · −1.0% : fill 71% (16/20) · rebond 78% (12/16)
      · −2.0% : fill 46% (11/20) · rebond 61% (8/11)
      · −3.0% : fill 28% (6/20) · rebond 37% (3/6)
      · −4.0% : fill 12% (4/20) · rebond 54% (3/4)
      · −5.0% : fill 9% (3/20) · rebond 9% (1/3)
   - **gap-up** (63 séances) :
      · −1.0% : fill 31% (26/63) · rebond 58% (18/26)
      · −2.0% : fill 19% (18/63) · rebond 67% (13/18)
      · −3.0% : fill 12% (10/63) · rebond 57% (7/10)
      · −4.0% : fill 11% (8/63) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/63) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 53% si les 15 1res min sont vertes (82 cas) · 36% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 71% si début vert vs 21% si rouge (base 45% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **71%** · continue >prix actuel 47% ; creux résiduel méd -1.78% (q20 -3.88%) → **SL/trailing à −3.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +3.57% → **scale +1.69% / runner +3.57%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **21%** (continue à baisser 53%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.71%** (au-delà de la MAE q10 -4.71%), cible rebond +2.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.36% .. +3.61%] · haut q95 +3.97% · bas q05 -3.82%
   - 60min (n=160) : retour [-4.73% .. +3.98%] · haut q95 +5.43% · bas q05 -5.04%
   - 2h (n=160) : retour [-4.37% .. +5.62%] · haut q95 +6.54% · bas q05 -5.18%
   - 4h (n=160) : retour [-5.7% .. +7.99%] · haut q95 +9.02% · bas q05 -6.89%
   - 6h (n=160) : retour [-5.9% .. +6.91%] · haut q95 +9.84% · bas q05 -7.3%
   - session (n=160) : retour [-5.09% .. +6.26%] · haut q95 +9.84% · bas q05 -7.78%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 4.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 12% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.22% (p75 2.61% / p90 4.03%) · ~3.12 replis/séance, durée méd 49.07 min. P(nouveau plus-haut après repli) :
   - −0.5% → **75%** (reprise méd 15.0 min, n=30)
   - −1.0% → **57%** (reprise méd 38.91 min, n=17)
   - −1.5% → **43%** (reprise méd 74.97 min, n=13)
   - −2.0% → **28%** (reprise méd 89.44 min, n=8)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−4.03%** (p90, défaut prudent ; serré/agressif −2.61%) ; extension open→close méd +8.28% (q75 +9.94% / q95 +16.06%), MFE méd +11.04% / q90 +15.91%
   - Échelle scale-out : +11.04% (33%) / +12.88% (33%) / +15.91% (34%)
- **DÉSARMER** : repli > **−4.03%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.91% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 98% du temps (retour médian dernière heure +0.79%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 71.1  _(surachat)_
- **ADX** : 22.7  _(pas de tendance nette)_
- **MACD** : hist 3.72  _(pas de croisement recent)_
- **BB** : %B 0.95 · largeur 43.9%
- **ATR** : 7.12 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.17  _(accumulation)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 37.6  _(marche directionnel)_
- **MA** : MA20 102.79 · MA50 99.73 · MA200 142.12  _(prix > MA20)_
- **Dist MA** : MA20 +19.8% · MA50 +23.5% · MA200 -13.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (820139 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
