# RGTI

**Generated** : 2026-09-01T00:29:24.096028+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.66  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $15.66 (+0.4% vs entrée) · entrée $15.59 · stop $15.27 · T1 $16.04 · R/R 1.41  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.112 _(réel 5 s)_ (GBM 0.169) · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.05% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.52–$15.66 (mid $15.59)
- Spot actuel : $15.66 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $15.27 (stop swing_plan-based (-7.72%))
- Targets : T1 $16.04 · R/R 1.41 | T2 $16.50 · R/R 2.84 | T3 $16.95 · R/R 4.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.27


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.72 %)** : le gap seul le franchit 1.357 % des séances (17 fois sur 1253).
   - exécution **2.793 pt plus bas** dans le cas TYPIQUE (médiane), 8.24 au p90, **23.493 au pire**
   - perte réelle **12.435 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 7.72 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.064 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.085 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5385** [0.4641 ; 0.6116] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4676** [0.4155 ; 0.5203] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5282** [0.4755 ; 0.5804] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 36.9 observations effectives », dont la borne haute a 95 % vaut environ 8.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.8 pt), swing (32.1 pt), deep (31.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.85 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 14.86 % contre 6.50 % aujourd'hui, rapport 2.28)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8213** (β de hausse 1.9923, asymétrie 0.9142) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.639× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 13.7975 sur atr_grid (1.75 ATR, 11.893 %) — p(stop avant cible) 0.558 [0.51 ; 0.61], R/R 2.076, perte reelle 16.825 % (gap inclus), CVaR 11.921 %, EV -2.9894 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1085 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.558, borne haute 0.610 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 19 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 61.4 % de la queue et il ne reste que 29.65 EUR a partager. Prix du risque 0.019 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.2 ATR (stop 4.406 %) — p(stop avant cible) 0.8139 [0.77 ; 0.85], R/R 4.564, perte reelle 7.654 % (gap inclus), EV -2.2174 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.814, borne haute 0.852 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 7.8 % x 34.93 % + P(rien) 10.8 % x 11.91 % ne couvrent pas P(stop) 81.4 % x 7.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 0.82 ATR (stop 8.666 %) — p(stop avant cible) 0.6665 [0.62 ; 0.71], R/R 2.612, perte reelle 13.376 % (gap inclus), EV -2.9705 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.666, borne haute 0.715 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.15 ATR du spot — compartiment <1, mesure a 46.4 % de casse (IC clusterise [0.430 ; 0.496] sur 1146 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.97 %) : P(cible) 10.6 % x 34.93 % + P(rien) 22.7 % x 9.83 % ne couvrent pas P(stop) 66.6 % x 13.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.94 ATR (stop 23.066 %) — p(stop avant cible) 0.1482 [0.11 ; 0.19], R/R 1.119, perte reelle 31.213 % (gap inclus), EV -0.0398 % — **REFUSE**
      - refuse : cible atteinte seulement 14.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 14.4 % x 34.93 % + P(rien) 70.7 % x -0.65 % ne couvrent pas P(stop) 14.8 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.2 ATR (stop 3.366 %) — p(stop avant cible) 0.8471 [0.81 ; 0.88], R/R 5.589, perte reelle 6.25 % (gap inclus), EV -1.7609 % — **REFUSE**
      - refuse : cible atteinte seulement 7.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 7.3 % x 34.93 % + P(rien) 8.0 % x 12.39 % ne couvrent pas P(stop) 84.7 % x 6.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.82 ATR (stop 7.626 %) — p(stop avant cible) 0.703 [0.65 ; 0.75], R/R 2.871, perte reelle 12.17 % (gap inclus), EV -2.9606 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.703, borne haute 0.749 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.96 %) : P(cible) 10.4 % x 34.93 % + P(rien) 19.3 % x 10.18 % ne couvrent pas P(stop) 70.3 % x 12.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 10.194 %) — p(stop avant cible) 0.6423 [0.59 ; 0.69], R/R 2.329, perte reelle 15.002 % (gap inclus), EV -3.5764 % — **REFUSE**
      - refuse : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.642, borne haute 0.692 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.58 %) : P(cible) 10.8 % x 34.93 % + P(rien) 24.9 % x 9.15 % ne couvrent pas P(stop) 64.2 % x 15.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 11.893 %) — p(stop avant cible) 0.558 [0.51 ; 0.61], R/R 2.076, perte reelle 16.825 % (gap inclus), EV -2.9894 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.558, borne haute 0.610 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.99 %) : P(cible) 11.6 % x 34.93 % + P(rien) 32.6 % x 7.20 % ne couvrent pas P(stop) 55.8 % x 16.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 13.592 %) — p(stop avant cible) 0.4753 [0.42 ; 0.53], R/R 1.894, perte reelle 18.441 % (gap inclus), EV -2.2154 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 11.9 % x 34.93 % + P(rien) 40.6 % x 5.89 % ne couvrent pas P(stop) 47.5 % x 18.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 15.291 %) — p(stop avant cible) 0.4055 [0.35 ; 0.46], R/R 1.422, perte reelle 24.565 % (gap inclus), EV -3.3854 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.39 %) : P(cible) 12.9 % x 34.93 % + P(rien) 46.6 % x 4.47 % ne couvrent pas P(stop) 40.6 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 16.991 %) — p(stop avant cible) 0.3472 [0.30 ; 0.40], R/R 1.422, perte reelle 24.565 % (gap inclus), EV -2.1583 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.16 %) : P(cible) 13.3 % x 34.93 % + P(rien) 51.9 % x 3.29 % ne couvrent pas P(stop) 34.7 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.94 ATR (stop 22.026 %) — p(stop avant cible) 0.1791 [0.14 ; 0.22], R/R 1.119, perte reelle 31.213 % (gap inclus), EV -0.525 % — **REFUSE**
      - refuse : cible atteinte seulement 14.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 14.4 % x 34.93 % + P(rien) 67.7 % x 0.03 % ne couvrent pas P(stop) 17.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 27.185 %) — p(stop avant cible) 0.0858 [0.06 ; 0.12], R/R 1.119, perte reelle 31.213 % (gap inclus), EV 0.9946 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.19 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 30.583 %) — p(stop avant cible) 0.0559 [0.04 ; 0.08], R/R 1.119, perte reelle 31.213 % (gap inclus), EV 1.3798 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.58 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.981 %) — p(stop avant cible) 0.0308 [0.02 ; 0.05], R/R 1.028, perte reelle 33.981 % (gap inclus), EV 1.5124 % — **REFUSE**
      - refuse : cible atteinte seulement 15.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.98 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 37.379 %) — p(stop avant cible) 0.0209 [0.01 ; 0.04], R/R 0.935, perte reelle 37.379 % (gap inclus), EV 1.4877 % — **REFUSE**
      - refuse : cible atteinte seulement 15.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.38 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 40.777 %) — p(stop avant cible) 0.011 [0.00 ; 0.03], R/R 0.857, perte reelle 40.777 % (gap inclus), EV 1.5792 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.78 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 44.175 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 0.791, perte reelle 44.175 % (gap inclus), EV 1.5778 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.18 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 47.573 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 0.734, perte reelle 47.573 % (gap inclus), EV 1.5712 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 50.972 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.685, perte reelle 50.972 % (gap inclus), EV 1.5563 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.97 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 54.37 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.643, perte reelle 54.37 % (gap inclus), EV 1.5821 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.37 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.66, ATR14 1.0643 (6.796 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.411 ATR = 2.793 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.34 % | 15.6068 | 92.25 % | 94.56 % | 95.66 % | 97.07 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.68 % | 15.5536 | 86.51 % | 91.23 % | 92.43 % | 94.94 % | 95.83 % | 97.43 % |
| 0.15 ATR | 1.019 % | 15.5004 | 81.07 % | 87.5 % | 89.1 % | 92.01 % | 93.9 % | 96.1 % |
| 0.2 ATR | 1.359 % | 15.4471 | 74.72 % | 82.96 % | 85.67 % | 88.88 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.699 % | 15.3939 | 68.68 % | 78.73 % | 81.84 % | 85.84 % | 88.82 % | 92.51 % |
| 0.35 ATR | 2.379 % | 15.2875 | 56.09 % | 68.55 % | 74.07 % | 79.68 % | 84.45 % | 89.63 % |
| 0.5 ATR | 3.398 % | 15.1279 | 41.19 % | 56.96 % | 64.98 % | 71.89 % | 79.27 % | 85.52 % |
| 0.75 ATR | 5.097 % | 14.8618 | 21.75 % | 39.01 % | 49.55 % | 59.15 % | 70.93 % | 79.26 % |
| 1.0 ATR | 6.796 % | 14.5957 | 9.57 % | 23.79 % | 33.6 % | 46.41 % | 61.89 % | 73.1 % |
| 1.25 ATR | 8.495 % | 14.3296 | 4.03 % | 14.52 % | 23.51 % | 36.91 % | 52.85 % | 65.2 % |
| 1.5 ATR | 10.194 % | 14.0636 | 1.71 % | 7.16 % | 13.72 % | 25.48 % | 43.09 % | 56.98 % |
| 2.0 ATR | 13.592 % | 13.5314 | 0.4 % | 1.71 % | 3.94 % | 10.72 % | 25.51 % | 40.86 % |
| 2.5 ATR | 16.991 % | 12.9993 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.43 % | 28.44 % |
| 3.0 ATR | 20.389 % | 12.4671 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.15 % |
| 4.0 ATR | 27.185 % | 11.4029 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 40.777 % | 9.2743 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.21 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.32 ATR | 1.45 ATR | 1.79 ATR | 2.02 ATR | 2.25 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.72 ATR | 1.87 ATR | 2.32 ATR | 2.65 ATR | 2.87 ATR | 3.58 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.462–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.398 %, prix 15.1279), p(touche) 41.19 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.667–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.097 %, prix 14.8618), p(touche) 39.01 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.821–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.796 %, prix 14.5957), p(touche) 33.6 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.037–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.495 %, prix 14.3297), p(touche) 36.91 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.194 %, prix 14.0636), p(touche) 43.09 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.872–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.592 %, prix 13.5315), p(touche) 40.86 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.169 | EV/share : $0.054 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.103 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 19.9 | side 75.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.441% → cible +2.909% / stop −2.048%, p_fill 85%, n_eff≈35.2) : P(cible|rempli) **30%** · **EV/risk -0.112** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −0.924% → cible +6.504% / stop −6.86%, p_fill 82%, n_eff≈34.8) : P(cible|rempli) **47%** · **EV/risk -0.078** (×p_fill ; si rempli -0.65% du capital)
  - **deep** (entrée dip −1.346% → cible +9.198% / stop −10.333%, p_fill 92%, n_eff≈36.9) : P(cible|rempli) **49%** · **EV/risk -0.107** (×p_fill ; si rempli -1.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→71% · +3.0%→54% · +5.0%→40% · +8.0%→14%
- Range intraday médian 7.62% (p90 13.36%) · excursion haute méd. +3.52% / basse méd. −2.8%
- Profil de vol intra : ouverture 5.444% vs midi 1.581% vs clôture 1.79% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 26% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. -0.147% ; recovery-V 33%
- **σ réalisé intraday** 4.285% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 48% / whipsaw 4%
- POC intraday (dernière séance, temps-au-prix) : 15.5205 (VA 15.4515–15.8195 ; dernier close 15.605)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 45% · rebond 73% · **stop −6.0%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.49% · baisse 59% (gap-down >1% 42% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.21% (p90 −2.88%) · haut méd +1.16% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.47% (p90 −3.82%) · haut méd +1.7% · range méd 3.63%
- Excursion ouverture 30min (n=160) : bas méd −1.78% (p90 −4.54%) · haut méd +2.09% · range méd 4.51%
- Excursion ouverture 60min (n=160) : bas méd −2.35% (p90 −5.72%) · haut méd +2.24% · range méd 5.3%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (133/159) · gap 49% · délai 0.0min · rebond 62% (84/133) (MFE +2.11%)
   - −1.0% : fill 30min 67% · séance 74% (125/159) · gap 42% · délai 0.0min · rebond 64% (79/125) (MFE +1.68%)
   - −1.5% : fill 30min 61% · séance 69% (119/159) · gap 34% · délai 0.0min · rebond 65% (77/119) (MFE +2.08%)
   - −2.0% : fill 30min 54% · séance 62% (110/159) · gap 26% · délai 0.0min · rebond 65% (73/110) (MFE +1.85%)
   - −3.0% : fill 30min 46% · séance 57% (99/159) · gap 10% · délai 1.2min · rebond 67% (71/99) (MFE +2.09%)
   - −4.0% : fill 30min 35% · séance 45% (78/159) · gap 5% · délai 6.5min · rebond 73% (56/78) (MFE +2.19%)
   - −5.0% : fill 30min 18% · séance 38% (68/159) · gap 2% · délai 31.4min · rebond 55% (46/68) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −2.4%) → stop au-delà de −1.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.81%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −2.92%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1155 jambes) : jambe baissière méd −1.28% (p90 −3.1%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 96% (83/85) · rebond 58% (48/83)
      · −2.0% : fill 86% (78/85) · rebond 62% (50/78)
      · −3.0% : fill 83% (74/85) · rebond 60% (50/74)
      · −4.0% : fill 70% (60/85) · rebond 71% (42/60)
      · −5.0% : fill 60% (53/85) · rebond 51% (35/53)
   - **flat** (15 séances) :
      · −1.0% : fill 96% (14/15) · rebond 94% (12/14)
      · −2.0% : fill 74% (12/15) · rebond 85% (10/12)
      · −3.0% : fill 50% (7/15) · rebond 90% (5/7)
      · −4.0% : fill 34% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 21% (5/15) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 37% (28/59) · rebond 67% (19/28)
      · −2.0% : fill 25% (20/59) · rebond 64% (13/20)
      · −3.0% : fill 21% (18/59) · rebond 90% (16/18)
      · −4.0% : fill 13% (12/59) · rebond 84% (10/12)
      · −5.0% : fill 11% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 72% si les 15 1res min sont vertes (80 cas) · 28% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 94% si début vert vs 9% si rouge (base 51% · écart 85 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **94%** · continue >prix actuel 54% ; creux résiduel méd -1.86% (q20 -2.9%) → **SL/trailing à −2.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.26% / q75 +4.34% → **scale +2.26% / runner +4.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **9%** (continue à baisser 70%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.02% .. +4.88%] · haut q95 +6.44% · bas q05 -6.02%
   - 60min (n=160) : retour [-5.42% .. +6.2%] · haut q95 +6.62% · bas q05 -6.69%
   - 2h (n=160) : retour [-6.34% .. +6.73%] · haut q95 +9.07% · bas q05 -7.4%
   - 4h (n=160) : retour [-6.67% .. +7.89%] · haut q95 +9.19% · bas q05 -7.81%
   - 6h (n=160) : retour [-7.31% .. +8.64%] · haut q95 +10.13% · bas q05 -8.51%
   - session (n=160) : retour [-7.13% .. +9.11%] · haut q95 +10.34% · bas q05 -8.62%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 5% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 37.7  _(momentum baissier)_
- **ADX** : 13.5  _(pas de tendance nette)_
- **MACD** : hist -0.21  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 24.1%
- **ATR** : 1.06 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.041  _(neutre)_
- **Vol ratio** : 0.54  _(volume atone)_
- **Choppiness** : 50.5  _(transition)_
- **MA** : MA20 17.23 · MA50 16.84 · MA200 19.51  _(prix < MA20)_
- **Dist MA** : MA20 -9.1% · MA50 -7.0% · MA200 -19.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (791027 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
