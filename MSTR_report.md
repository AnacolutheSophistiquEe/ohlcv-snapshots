# MSTR

**Generated** : 2026-08-31T00:23:40.964920+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $127.31  

> 🟡 **WAIT-FOR-DIP** — spot +4.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $127.31 (+4.5% vs entrée) · entrée $121.86 · stop $113.71 · T1 $129.55 · R/R 0.94  
> ↳ P(T1 av. stop) 56 % _(réel 5 s)_ · EV/risk 0.083 _(réel 5 s)_ (GBM -0.059) · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $120.32–$123.40 (mid $121.86)
- Spot actuel : $127.31 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : $113.71 (stop swing_plan-based (-10.68%))
- Targets : T1 $129.55 · R/R 0.94 | T2 $137.23 · R/R 1.89 | T3 $144.92 · R/R 2.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $113.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.68 %)** : le gap seul le franchit 0.478 % des séances (6 fois sur 1254).
   - exécution **2.633 pt plus bas** dans le cas TYPIQUE (médiane), 16.295 au p90, **16.692 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 10.68 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0313 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.428 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.22** [0.1632 ; 0.286] _(largeur 12.3 pt, n_eff 173.1)_
   - swing : **0.4212** [0.37 ; 0.4737] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4121** [0.3611 ; 0.4645] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.6 pt), swing (44.4 pt), deep (41.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.77 %** | CVaR **-10.4 %** | vol 5.47 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.44 % contre 4.82 % aujourd'hui, rapport 1.75)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.76 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3313** (β de hausse 1.8577, asymétrie 1.255) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 113.9559 sur grid_snapped (1.34 ATR, 10.489 %) — p(stop avant cible) 0.4443 [0.39 ; 0.50], R/R 1.093, perte reelle 17.215 % (gap inclus), CVaR 10.521 %, EV -3.7547 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.599 %) — p(stop avant cible) 0.4911 [0.44 ; 0.54], R/R 1.093, perte reelle 17.215 % (gap inclus), EV -4.457 % — **REFUSE**
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.46 %) : P(cible) 16.6 % x 18.81 % + P(rien) 34.3 % x 2.55 % ne couvrent pas P(stop) 49.1 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.34 ATR (stop 11.987 %) — p(stop avant cible) 0.3869 [0.34 ; 0.44], R/R 0.82, perte reelle 22.94 % (gap inclus), EV -5.1351 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.14 %) : P(cible) 17.0 % x 18.81 % + P(rien) 44.3 % x 1.24 % ne couvrent pas P(stop) 38.7 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.84 ATR (stop 21.593 %) — p(stop avant cible) 0.1504 [0.12 ; 0.19], R/R 0.697, perte reelle 26.975 % (gap inclus), EV -2.5448 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.54 %) : P(cible) 17.4 % x 18.81 % + P(rien) 67.5 % x -2.62 % ne couvrent pas P(stop) 15.0 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.68 ATR (stop 33.344 %) — p(stop avant cible) 0.0293 [0.02 ; 0.05], R/R 0.564, perte reelle 33.344 % (gap inclus), EV -1.7563 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 17.4 % x 18.81 % + P(rien) 79.6 % x -5.10 % ne couvrent pas P(stop) 2.9 % x 33.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.6 %) — p(stop avant cible) 0.9443 [0.92 ; 0.96], R/R 5.342, perte reelle 3.521 % (gap inclus), EV -2.6373 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.944, borne haute 0.965 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.64 %) : P(cible) 2.7 % x 18.81 % + P(rien) 2.9 % x 6.22 % ne couvrent pas P(stop) 94.4 % x 3.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.2 %) — p(stop avant cible) 0.8453 [0.80 ; 0.88], R/R 3.331, perte reelle 5.647 % (gap inclus), EV -2.8279 % — **REFUSE**
      - refuse : cible atteinte seulement 8.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.845, borne haute 0.880 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.83 %) : P(cible) 8.4 % x 18.81 % + P(rien) 7.1 % x 5.25 % ne couvrent pas P(stop) 84.5 % x 5.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.8 %) — p(stop avant cible) 0.7368 [0.69 ; 0.78], R/R 2.459, perte reelle 7.649 % (gap inclus), EV -2.552 % — **REFUSE**
      - refuse : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.737, borne haute 0.781 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.55 %) : P(cible) 12.7 % x 18.81 % + P(rien) 13.6 % x 5.09 % ne couvrent pas P(stop) 73.7 % x 7.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.399 %) — p(stop avant cible) 0.643 [0.59 ; 0.69], R/R 2.009, perte reelle 9.362 % (gap inclus), EV -2.4453 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.643, borne haute 0.692 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 14.8 % x 18.81 % + P(rien) 20.9 % x 3.75 % ne couvrent pas P(stop) 64.3 % x 9.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.34 ATR (stop 10.489 %) — p(stop avant cible) 0.4443 [0.39 ; 0.50], R/R 1.093, perte reelle 17.215 % (gap inclus), EV -3.7547 % — **REFUSE**
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.75 %) : P(cible) 16.8 % x 18.81 % + P(rien) 38.8 % x 1.88 % ne couvrent pas P(stop) 44.4 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.799 %) — p(stop avant cible) 0.3626 [0.31 ; 0.41], R/R 0.82, perte reelle 22.94 % (gap inclus), EV -4.7951 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.80 %) : P(cible) 17.0 % x 18.81 % + P(rien) 46.7 % x 0.69 % ne couvrent pas P(stop) 36.3 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 14.399 %) — p(stop avant cible) 0.3143 [0.27 ; 0.36], R/R 0.82, perte reelle 22.94 % (gap inclus), EV -3.9186 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.92 %) : P(cible) 17.2 % x 18.81 % + P(rien) 51.3 % x 0.10 % ne couvrent pas P(stop) 31.4 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 15.999 %) — p(stop avant cible) 0.2575 [0.21 ; 0.31], R/R 0.697, perte reelle 26.975 % (gap inclus), EV -4.2632 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.26 %) : P(cible) 17.3 % x 18.81 % + P(rien) 56.9 % x -1.01 % ne couvrent pas P(stop) 25.8 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.84 ATR (stop 20.096 %) — p(stop avant cible) 0.1784 [0.14 ; 0.22], R/R 0.697, perte reelle 26.975 % (gap inclus), EV -2.9878 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.99 %) : P(cible) 17.4 % x 18.81 % + P(rien) 64.8 % x -2.24 % ne couvrent pas P(stop) 17.8 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 22.398 %) — p(stop avant cible) 0.1442 [0.11 ; 0.18], R/R 0.697, perte reelle 26.975 % (gap inclus), EV -2.4677 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 17.4 % x 18.81 % + P(rien) 68.2 % x -2.72 % ne couvrent pas P(stop) 14.4 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 25.598 %) — p(stop avant cible) 0.0941 [0.07 ; 0.13], R/R 0.697, perte reelle 26.975 % (gap inclus), EV -1.9415 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 17.4 % x 18.81 % + P(rien) 73.2 % x -3.67 % ne couvrent pas P(stop) 9.4 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.68 ATR (stop 31.847 %) — p(stop avant cible) 0.0323 [0.02 ; 0.06], R/R 0.591, perte reelle 31.847 % (gap inclus), EV -1.7458 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 17.4 % x 18.81 % + P(rien) 79.3 % x -5.04 % ne couvrent pas P(stop) 3.2 % x 31.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 35.197 %) — p(stop avant cible) 0.0176 [0.01 ; 0.04], R/R 0.534, perte reelle 35.197 % (gap inclus), EV -1.6457 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 17.4 % x 18.81 % + P(rien) 80.8 % x -5.33 % ne couvrent pas P(stop) 1.8 % x 35.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 38.397 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 0.49, perte reelle 38.397 % (gap inclus), EV -1.5911 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 17.4 % x 18.81 % + P(rien) 81.9 % x -5.65 % ne couvrent pas P(stop) 0.6 % x 38.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 41.596 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.452, perte reelle 41.596 % (gap inclus), EV -1.5405 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 17.4 % x 18.81 % + P(rien) 82.5 % x -5.81 % ne couvrent pas P(stop) 0.1 % x 41.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 44.796 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.42, perte reelle 44.796 % (gap inclus), EV -1.5299 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.53 %) : P(cible) 17.4 % x 18.81 % + P(rien) 82.5 % x -5.82 % ne couvrent pas P(stop) 0.0 % x 44.80 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 47.996 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.392, perte reelle 47.996 % (gap inclus), EV -1.5311 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.53 %) : P(cible) 17.4 % x 18.81 % + P(rien) 82.5 % x -5.82 % ne couvrent pas P(stop) 0.0 % x 48.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 51.196 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.367, perte reelle 51.196 % (gap inclus), EV -1.5327 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.53 %) : P(cible) 17.4 % x 18.81 % + P(rien) 82.5 % x -5.82 % ne couvrent pas P(stop) 0.0 % x 51.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 127.31, ATR14 8.1471 (6.399 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.396 ATR = 2.534 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.32 % | 126.9026 | 94.37 % | 96.68 % | 97.08 % | 97.68 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.64 % | 126.4953 | 88.33 % | 92.04 % | 93.45 % | 94.85 % | 96.75 % | 97.33 % |
| 0.15 ATR | 0.96 % | 126.0879 | 81.49 % | 87.11 % | 89.62 % | 91.82 % | 94.21 % | 95.59 % |
| 0.2 ATR | 1.28 % | 125.6806 | 73.84 % | 81.87 % | 84.88 % | 88.18 % | 91.57 % | 93.85 % |
| 0.25 ATR | 1.6 % | 125.2732 | 68.11 % | 78.15 % | 82.16 % | 86.26 % | 89.34 % | 92.31 % |
| 0.35 ATR | 2.24 % | 124.4585 | 55.23 % | 68.88 % | 75.4 % | 81.01 % | 85.89 % | 89.64 % |
| 0.5 ATR | 3.2 % | 123.2364 | 38.23 % | 55.49 % | 63.61 % | 71.41 % | 78.68 % | 84.92 % |
| 0.75 ATR | 4.8 % | 121.1996 | 19.22 % | 37.76 % | 47.18 % | 58.28 % | 68.43 % | 77.64 % |
| 1.0 ATR | 6.399 % | 119.1629 | 9.36 % | 25.28 % | 34.98 % | 46.67 % | 59.29 % | 70.46 % |
| 1.25 ATR | 7.999 % | 117.1261 | 4.12 % | 14.6 % | 25.3 % | 36.36 % | 50.25 % | 63.18 % |
| 1.5 ATR | 9.599 % | 115.0893 | 2.11 % | 8.76 % | 17.44 % | 29.19 % | 43.35 % | 57.33 % |
| 2.0 ATR | 12.799 % | 111.0157 | 0.2 % | 3.12 % | 7.46 % | 16.36 % | 31.57 % | 47.49 % |
| 2.5 ATR | 15.999 % | 106.9421 | 0.1 % | 0.91 % | 2.42 % | 8.79 % | 21.62 % | 37.74 % |
| 3.0 ATR | 19.198 % | 102.8686 | 0.1 % | 0.5 % | 1.01 % | 4.65 % | 14.62 % | 28.1 % |
| 4.0 ATR | 25.598 % | 94.7214 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.29 % | 18.15 % |
| 6.0 ATR | 38.397 % | 78.4271 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.84 ATR | 1.01 ATR | 1.12 ATR | 1.45 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.42 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.37 ATR | 1.66 ATR | 1.86 ATR | 2.42 ATR | 2.96 ATR |
| **10 s.** | 0.59 ATR | 1.26 ATR | 1.44 ATR | 1.94 ATR | 2.33 ATR | 2.62 ATR | 3.56 ATR | 4.45 ATR |
| **20 s.** | 0.84 ATR | 1.87 ATR | 2.13 ATR | 2.75 ATR | 3.31 ATR | 3.81 ATR | 5.19 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.2 %, prix 123.2361), p(touche) 38.23 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.648–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.8 %, prix 121.1991), p(touche) 37.76 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.399 %, prix 119.1634), p(touche) 34.98 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.04–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.999 %, prix 117.1265), p(touche) 36.36 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.44–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.599 %, prix 115.0895), p(touche) 43.35 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.128–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.999 %, prix 106.9417), p(touche) 37.74 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.059 | EV/share : $-0.480 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 18 % | T3 9 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 53.7 | bear 24.3 | side 22.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 509.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.948% → cible +2.821% / stop −4.0%, p_fill 59%, n_eff≈23.6) : P(cible|rempli) **30%** · **EV/risk +0.021** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −4.281% → cible +6.308% / stop −6.686%, p_fill 32%, n_eff≈16.7) : P(cible|rempli) **56%** · **EV/risk +0.083** (×p_fill ; si rempli +1.76% du capital)
  - **deep** (entrée dip −6.621% → cible +8.922% / stop −10.279%, p_fill 30%, n_eff≈19.2) : P(cible|rempli) **57%** · **EV/risk +0.065** (×p_fill ; si rempli +2.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→75% · +2.0%→57% · +3.0%→42% · +5.0%→16% · +8.0%→10%
- Range intraday médian 5.59% (p90 10.3%) · excursion haute méd. +2.46% / basse méd. −2.51%
- Profil de vol intra : ouverture 3.466% vs midi 1.231% vs clôture 1.352% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.004)_ ; drift intra méd. 0.628% ; recovery-V 28%
- **σ réalisé intraday** 3.752% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 79% / bas 56% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 127.1821 (VA 126.4689–131.6994 ; dernier close 127.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 72% · **stop −4.48%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 52% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.89% (p90 −2.06%) · haut méd +0.78% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.83%) · haut méd +1.22% · range méd 2.49%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.27%) · haut méd +1.44% · range méd 3.15%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −3.62%) · haut méd +1.84% · range méd 3.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 127.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 73% (122/159) · gap 45% · délai 0.0min · rebond 49% (60/122) (MFE +0.94%)
   - −1.0% : fill 30min 58% · séance 69% (117/159) · gap 41% · délai 0.0min · rebond 53% (65/117) (MFE +1.02%)
   - −1.5% : fill 30min 53% · séance 65% (110/159) · gap 34% · délai 0.0min · rebond 58% (65/110) (MFE +1.49%)
   - −2.0% : fill 30min 47% · séance 57% (100/159) · gap 28% · délai 0.0min · rebond 60% (61/100) (MFE +1.31%)
   - −3.0% : fill 30min 31% · séance 48% (79/159) · gap 12% · délai 1.9min · rebond 58% (47/79) (MFE +1.67%)
   - −4.0% : fill 30min 19% · séance 38% (65/159) · gap 4% · délai 29.0min · rebond 68% (43/65) (MFE +1.75%)
   - −5.0% : fill 30min 13% · séance 26% (47/159) · gap 3% · délai 39.2min · rebond 72% (33/47) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.28%) → stop au-delà de −1.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −2.49%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −2.48%) → stop au-delà de −1.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=970 jambes) : jambe baissière méd −1.13% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (78/78) · rebond 47% (37/78)
      · −2.0% : fill 93% (72/78) · rebond 59% (41/72)
      · −3.0% : fill 83% (64/78) · rebond 61% (38/64)
      · −4.0% : fill 67% (54/78) · rebond 69% (36/54)
      · −5.0% : fill 48% (41/78) · rebond 73% (30/41)
   - **flat** (19 séances) :
      · −1.0% : fill 71% (15/19) · rebond 79% (12/15)
      · −2.0% : fill 46% (10/19) · rebond 60% (7/10)
      · −3.0% : fill 28% (5/19) · rebond 35% (2/5)
      · −4.0% : fill 11% (3/19) · rebond 51% (2/3)
      · −5.0% : fill 9% (2/19) · rebond 0% (0/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 28% (24/62) · rebond 57% (16/24)
      · −2.0% : fill 17% (18/62) · rebond 67% (13/18)
      · −3.0% : fill 12% (10/62) · rebond 57% (7/10)
      · −4.0% : fill 10% (8/62) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/62) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 54% si les 15 1res min sont vertes (82 cas) · 37% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 79% si début vert vs 13% si rouge (base 46% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **79%** · continue >prix actuel 43% ; creux résiduel méd -1.49% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.55% → **scale +1.59% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **13%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.84%** (au-delà de la MAE q10 -4.84%), cible rebond +1.62% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.31% .. +3.73%] · haut q95 +3.94% · bas q05 -3.66%
   - 60min (n=160) : retour [-4.53% .. +5.45%] · haut q95 +5.68% · bas q05 -4.99%
   - 2h (n=160) : retour [-4.33% .. +6.69%] · haut q95 +8.34% · bas q05 -5.05%
   - 4h (n=160) : retour [-5.63% .. +8.54%] · haut q95 +10.12% · bas q05 -6.79%
   - 6h (n=160) : retour [-5.9% .. +7.69%] · haut q95 +10.19% · bas q05 -7.21%
   - session (n=160) : retour [-5.09% .. +6.89%] · haut q95 +10.19% · bas q05 -7.41%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 15% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 2.61% / p90 3.53%) · ~3.99 replis/séance, durée méd 49.8 min. P(nouveau plus-haut après repli) :
   - −0.5% → **75%** (reprise méd 15.0 min, n=31)
   - −1.0% → **54%** (reprise méd 21.99 min, n=18)
   - −1.5% → **46%** (reprise méd 37.49 min, n=15)
   - −2.0% → **20%** (reprise méd 89.44 min, n=9)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.53%** (p90, défaut prudent ; serré/agressif −2.61%) ; extension open→close méd +8.34% (q75 +9.19% / q95 +15.39%), MFE méd +10.26% / q90 +14.97%
   - Échelle scale-out : +10.26% (33%) / +12.41% (33%) / +14.97% (34%)
- **DÉSARMER** : repli > **−3.53%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 221.98 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.97% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.51%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_up
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

- **RSI** : 68.5  _(momentum haussier)_
- **ADX** : 28.3  _(tendance etablie)_
- **MACD** : hist 3.819  _(pas de croisement recent)_
- **BB** : %B 0.87 · largeur 53.3%
- **ATR** : 8.15 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.133  _(accumulation)_
- **Vol ratio** : 1.23  _(volume normal)_
- **Choppiness** : 32.7  _(marche directionnel)_
- **MA** : MA20 106.48 · MA50 100.23 · MA200 141.04  _(prix > MA20)_
- **Dist MA** : MA20 +19.6% · MA50 +27.0% · MA200 -9.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (908812 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
