# MSTR

**Generated** : 2026-09-01T22:00:21.134745+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $124.88  

> 🟡 **WAIT-FOR-DIP** — spot +3.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $124.88 (+3.4% vs entrée) · entrée $120.77 · stop $111.93 · T1 $128.86 · R/R 0.92  
> ↳ P(T1 av. stop) 61 % _(réel 5 s)_ · EV/risk 0.121 _(réel 5 s)_ (GBM -0.056) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $119.15–$122.38 (mid $120.77)
- Spot actuel : $124.88 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : $111.93 (stop swing_plan-based (-10.37%))
- Targets : T1 $128.86 · R/R 0.92 | T2 $136.95 · R/R 1.83 | T3 $145.05 · R/R 2.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $111.93


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.29 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.37 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **2.943 pt plus bas** dans le cas TYPIQUE (médiane), 16.605 au p90, **17.002 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 10.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0328 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2878** [0.2243 ; 0.3583] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.3964** [0.3459 ; 0.4487] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3802** [0.3302 ; 0.4322] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.9 pt), swing (40.3 pt), deep (36.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.77 %** | CVaR **-10.4 %** | vol 5.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.34 % contre 4.87 % aujourd'hui, rapport 1.71)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.77 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3373** (β de hausse 1.8522, asymétrie 1.2619) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 111.633 sur atr_grid (1.5 ATR, 10.608 %) — p(stop avant cible) 0.4375 [0.39 ; 0.49], R/R 1.217, perte reelle 17.215 % (gap inclus), CVaR 10.64 %, EV -3.278 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 18 des 18 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 60.2 % de la queue et il ne reste que -755.68 EUR a partager. Prix du risque -0.422 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.96 ATR (stop 9.442 %) — p(stop avant cible) 0.4932 [0.44 ; 0.55], R/R 1.217, perte reelle 17.215 % (gap inclus), EV -4.1748 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.85 ATR du spot — compartiment <1, mesure a 46.1 % de casse (IC clusterise [0.427 ; 0.494] sur 1133 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.17 %) : P(cible) 15.5 % x 20.96 % + P(rien) 35.2 % x 3.04 % ne couvrent pas P(stop) 49.3 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.35 ATR (stop 19.236 %) — p(stop avant cible) 0.184 [0.15 ; 0.23], R/R 0.777, perte reelle 26.975 % (gap inclus), EV -2.7103 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.71 %) : P(cible) 16.0 % x 20.96 % + P(rien) 65.6 % x -1.67 % ne couvrent pas P(stop) 18.4 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.04 ATR (stop 31.215 %) — p(stop avant cible) 0.0377 [0.02 ; 0.06], R/R 0.671, perte reelle 31.215 % (gap inclus), EV -1.3302 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.33 %) : P(cible) 16.0 % x 20.96 % + P(rien) 80.2 % x -4.37 % ne couvrent pas P(stop) 3.8 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.768 %) — p(stop avant cible) 0.9155 [0.88 ; 0.94], R/R 5.693, perte reelle 3.681 % (gap inclus), EV -2.1995 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.915, borne haute 0.941 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 4.0 % x 20.96 % + P(rien) 4.5 % x 7.47 % ne couvrent pas P(stop) 91.5 % x 3.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.536 %) — p(stop avant cible) 0.8065 [0.76 ; 0.85], R/R 3.351, perte reelle 6.254 % (gap inclus), EV -2.3882 % — **REFUSE**
      - refuse : cible atteinte seulement 10.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.806, borne haute 0.846 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.39 %) : P(cible) 10.2 % x 20.96 % + P(rien) 9.1 % x 5.65 % ne couvrent pas P(stop) 80.7 % x 6.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 10.608 %) — p(stop avant cible) 0.4375 [0.39 ; 0.49], R/R 1.217, perte reelle 17.215 % (gap inclus), EV -3.278 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 15.6 % x 20.96 % + P(rien) 40.6 % x 2.40 % ne couvrent pas P(stop) 43.8 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 12.376 %) — p(stop avant cible) 0.3718 [0.32 ; 0.42], R/R 0.914, perte reelle 22.94 % (gap inclus), EV -4.499 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.50 %) : P(cible) 15.7 % x 20.96 % + P(rien) 47.1 % x 1.56 % ne couvrent pas P(stop) 37.2 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.144 %) — p(stop avant cible) 0.3122 [0.27 ; 0.36], R/R 0.914, perte reelle 22.94 % (gap inclus), EV -3.5098 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.51 %) : P(cible) 15.8 % x 20.96 % + P(rien) 53.0 % x 0.64 % ne couvrent pas P(stop) 31.2 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 21.216 %) — p(stop avant cible) 0.1516 [0.12 ; 0.19], R/R 0.777, perte reelle 26.975 % (gap inclus), EV -2.1591 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.16 %) : P(cible) 16.0 % x 20.96 % + P(rien) 68.9 % x -2.06 % ne couvrent pas P(stop) 15.2 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.751 %) — p(stop avant cible) 0.1001 [0.07 ; 0.14], R/R 0.777, perte reelle 26.975 % (gap inclus), EV -1.6431 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.64 %) : P(cible) 16.0 % x 20.96 % + P(rien) 74.0 % x -3.10 % ne couvrent pas P(stop) 10.0 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 35.359 %) — p(stop avant cible) 0.0148 [0.01 ; 0.03], R/R 0.593, perte reelle 35.359 % (gap inclus), EV -1.2344 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 16.0 % x 20.96 % + P(rien) 82.5 % x -4.93 % ne couvrent pas P(stop) 1.5 % x 35.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 38.895 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.539, perte reelle 38.895 % (gap inclus), EV -1.1493 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 16.0 % x 20.96 % + P(rien) 83.8 % x -5.29 % ne couvrent pas P(stop) 0.2 % x 38.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 42.431 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.494, perte reelle 42.431 % (gap inclus), EV -1.1303 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 16.0 % x 20.96 % + P(rien) 83.9 % x -5.32 % ne couvrent pas P(stop) 0.1 % x 42.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 45.967 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.456, perte reelle 45.967 % (gap inclus), EV -1.1248 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 16.0 % x 20.96 % + P(rien) 84.0 % x -5.33 % ne couvrent pas P(stop) 0.0 % x 45.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 49.503 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.423, perte reelle 49.503 % (gap inclus), EV -1.1255 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 16.0 % x 20.96 % + P(rien) 84.0 % x -5.33 % ne couvrent pas P(stop) 0.0 % x 49.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 53.039 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.395, perte reelle 53.039 % (gap inclus), EV -1.1272 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 16.0 % x 20.96 % + P(rien) 84.0 % x -5.33 % ne couvrent pas P(stop) 0.0 % x 53.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 56.575 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.37, perte reelle 56.575 % (gap inclus), EV -1.1275 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 16.0 % x 20.96 % + P(rien) 84.0 % x -5.33 % ne couvrent pas P(stop) 0.0 % x 56.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 124.88, ATR14 8.8313 (7.072 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.395 ATR = 2.793 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.354 % | 124.4384 | 94.36 % | 96.67 % | 97.07 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.707 % | 123.9969 | 88.32 % | 92.04 % | 93.44 % | 94.74 % | 96.75 % | 97.33 % |
| 0.15 ATR | 1.061 % | 123.5553 | 81.47 % | 87.1 % | 89.61 % | 91.71 % | 94.21 % | 95.59 % |
| 0.2 ATR | 1.414 % | 123.1137 | 73.82 % | 81.85 % | 84.86 % | 88.07 % | 91.46 % | 93.74 % |
| 0.25 ATR | 1.768 % | 122.6722 | 68.08 % | 78.12 % | 82.14 % | 86.15 % | 89.23 % | 92.2 % |
| 0.35 ATR | 2.475 % | 121.789 | 55.09 % | 68.75 % | 75.18 % | 80.89 % | 85.77 % | 89.53 % |
| 0.5 ATR | 3.536 % | 120.4643 | 38.17 % | 55.34 % | 63.37 % | 71.28 % | 78.56 % | 84.7 % |
| 0.75 ATR | 5.304 % | 118.2565 | 19.34 % | 37.7 % | 46.92 % | 58.04 % | 68.19 % | 77.41 % |
| 1.0 ATR | 7.072 % | 116.0487 | 9.37 % | 25.2 % | 34.71 % | 46.41 % | 59.04 % | 70.23 % |
| 1.25 ATR | 8.84 % | 113.8408 | 4.13 % | 14.52 % | 25.03 % | 36.1 % | 50.0 % | 62.94 % |
| 1.5 ATR | 10.608 % | 111.633 | 2.11 % | 8.67 % | 17.36 % | 28.92 % | 43.09 % | 57.08 % |
| 2.0 ATR | 14.144 % | 107.2174 | 0.2 % | 3.12 % | 7.37 % | 16.18 % | 31.3 % | 47.23 % |
| 2.5 ATR | 17.68 % | 102.8017 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.44 % | 37.58 % |
| 3.0 ATR | 21.216 % | 98.386 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 28.287 % | 89.5547 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 42.431 % | 71.8921 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.03 ATR | 1.36 ATR | 1.65 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.12 ATR | 2.74 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.536 %, prix 120.4642), p(touche) 38.17 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.647–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.304 %, prix 118.2564), p(touche) 37.7 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.789–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.072 %, prix 116.0485), p(touche) 34.71 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.034–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.84 %, prix 113.8406), p(touche) 36.1 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.431–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.608 %, prix 111.6327), p(touche) 43.09 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.116–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.68 %, prix 102.8012), p(touche) 37.58 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.056 | EV/share : $-0.492 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 15 % | T3 9 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 47.8 | bear 25.6 | side 26.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 500.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.503% → cible +2.997% / stop −3.5%, p_fill 71%, n_eff≈28.3) : P(cible|rempli) **42%** · **EV/risk +0.140** (×p_fill ; si rempli +0.69% du capital)
  - **swing** (entrée dip −3.298% → cible +6.702% / stop −7.313%, p_fill 43%, n_eff≈20.1) : P(cible|rempli) **61%** · **EV/risk +0.121** (×p_fill ; si rempli +2.04% du capital)
  - **deep** (entrée dip −5.092% → cible +9.478% / stop −11.177%, p_fill 50%, n_eff≈23.3) : P(cible|rempli) **68%** · **EV/risk +0.169** (×p_fill ; si rempli +3.79% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→75% · +2.0%→57% · +3.0%→42% · +5.0%→16% · +8.0%→10%
- Range intraday médian 5.59% (p90 10.3%) · excursion haute méd. +2.46% / basse méd. −2.4%
- Profil de vol intra : ouverture 3.444% vs midi 1.223% vs clôture 1.353% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.007)_ ; drift intra méd. 0.754% ; recovery-V 33%
- **σ réalisé intraday** 3.719% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 80% / bas 59% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 129.855 (VA 128.335–132.515 ; dernier close 132.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 72% · **stop −4.48%** sous le fill (sous le bruit) · cible +1.53% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.02% · baisse 51% (gap-down >1% 40% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.06%) · haut méd +0.76% · range méd 1.83%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.83%) · haut méd +1.2% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.26%) · haut méd +1.42% · range méd 3.12%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −3.61%) · haut méd +1.81% · range méd 3.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 132.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (122/159) · gap 44% · délai 0.0min · rebond 50% (61/122) (MFE +1.01%)
   - −1.0% : fill 30min 59% · séance 69% (117/159) · gap 40% · délai 0.0min · rebond 54% (66/117) (MFE +1.05%)
   - −1.5% : fill 30min 52% · séance 64% (109/159) · gap 33% · délai 0.0min · rebond 58% (65/109) (MFE +1.49%)
   - −2.0% : fill 30min 46% · séance 56% (99/159) · gap 27% · délai 0.0min · rebond 60% (61/99) (MFE +1.32%)
   - −3.0% : fill 30min 31% · séance 47% (78/159) · gap 12% · délai 1.9min · rebond 59% (47/78) (MFE +1.67%)
   - −4.0% : fill 30min 19% · séance 37% (64/159) · gap 4% · délai 29.0min · rebond 68% (43/64) (MFE +1.77%)
   - −5.0% : fill 30min 12% · séance 26% (46/159) · gap 3% · délai 39.2min · rebond 72% (33/46) (MFE +1.53%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.81% (p90 −2.28%) → stop au-delà de −1.85% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.01% (p90 −2.48%) → stop au-delà de −2.1% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −2.46%) → stop au-delà de −2.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=967 jambes) : jambe baissière méd −1.12% (p90 −2.7%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 100% (77/77) · rebond 47% (37/77)
      · −2.0% : fill 93% (71/77) · rebond 59% (41/71)
      · −3.0% : fill 83% (63/77) · rebond 61% (38/63)
      · −4.0% : fill 67% (53/77) · rebond 69% (36/53)
      · −5.0% : fill 48% (40/77) · rebond 74% (30/40)
   - **flat** (19 séances) :
      · −1.0% : fill 71% (15/19) · rebond 79% (12/15)
      · −2.0% : fill 46% (10/19) · rebond 60% (7/10)
      · −3.0% : fill 28% (5/19) · rebond 35% (2/5)
      · −4.0% : fill 11% (3/19) · rebond 51% (2/3)
      · −5.0% : fill 9% (2/19) · rebond 0% (0/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 31% (25/63) · rebond 64% (17/25)
      · −2.0% : fill 16% (18/63) · rebond 67% (13/18)
      · −3.0% : fill 11% (10/63) · rebond 57% (7/10)
      · −4.0% : fill 10% (8/63) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/63) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 54% si les 15 1res min sont vertes (82 cas) · 39% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 75% si début vert vs 12% si rouge (base 47% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=87) : tient le vert **75%** · continue >prix actuel 54% ; creux résiduel méd -1.46% (q20 -3.42%) → **SL/trailing à −3.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +3.01% → **scale +1.91% / runner +3.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **12%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +1.59% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.31% .. +3.72%] · haut q95 +3.94% · bas q05 -3.65%
   - 60min (n=160) : retour [-4.48% .. +5.43%] · haut q95 +5.67% · bas q05 -4.98%
   - 2h (n=160) : retour [-4.32% .. +6.61%] · haut q95 +8.16% · bas q05 -5.05%
   - 4h (n=160) : retour [-5.6% .. +8.5%] · haut q95 +10.11% · bas q05 -6.79%
   - 6h (n=160) : retour [-5.85% .. +7.57%] · haut q95 +10.18% · bas q05 -7.18%
   - session (n=160) : retour [-5.07% .. +6.73%] · haut q95 +10.18% · bas q05 -7.33%


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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 66.3  _(momentum haussier)_
- **ADX** : 32.3  _(tendance etablie)_
- **MACD** : hist 2.751  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 55.7%
- **ATR** : 8.83 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.105  _(accumulation)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 35.8  _(marche directionnel)_
- **MA** : MA20 109.74 · MA50 100.95 · MA200 140.05  _(prix > MA20)_
- **Dist MA** : MA20 +13.8% · MA50 +23.7% · MA200 -10.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (779965 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
