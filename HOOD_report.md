# HOOD

**Generated** : 2026-09-23T00:45:50.117227+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $124.20  

> 🟡 **WAIT-FOR-DIP** — spot +4.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $124.20 (+4.7% vs entrée) · entrée $118.59 · stop $107.55 · T1 $140.69 · R/R 2.0  
> ↳ P(T1 av. stop) 17 % _(réel 5 s)_ · EV/risk 0.105 _(réel 5 s)_ (GBM 0.045) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -8.3 % ≠ (strike 113.0 − spot 124.20)/spot = -9.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $117.08–$120.11 (mid $118.59)
- Spot actuel : $124.20 (+4.7% au-dessus de la zone — repli à attendre)
- Stop : $107.55 (stop swing_plan-based (-13.41%))
- Targets : T1 $140.69 · R/R 2.0 | T2 $140.99 · R/R 2.03 | T3 $141.29 · R/R 2.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $107.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.41 %)** : le gap seul le franchit 0.16 % des séances (2 fois sur 1253).
   - exécution **2.545 pt plus bas** dans le cas TYPIQUE (médiane), 4.009 au p90, **4.375 au pire**
   - perte réelle **15.955 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 13.41 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0041 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3092** [0.2439 ; 0.3808] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.2526** [0.209 ; 0.3003] _(largeur 9.1 pt, n_eff 345.7)_
   - deep : **0.3607** [0.3114 ; 0.4123] _(largeur 10.1 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.1 pt), swing (49.4 pt), deep (47.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.41 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 1.95 % contre 4.70 % aujourd'hui, rapport 0.41)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7649** (β de hausse 1.6002, asymétrie 1.1029) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.461× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 116.9164 sur atr_grid (1.0 ATR, 5.864 %) — p(stop avant cible) 0.5867 [0.53 ; 0.64], R/R 2.217, perte reelle 9.362 % (gap inclus), CVaR 5.914 %, EV -0.1749 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1595 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.587, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **6.78 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.313 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 45.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.797 %) — p(stop avant cible) 0.4166 [0.37 ; 0.47], R/R 1.79, perte reelle 11.595 % (gap inclus), EV 1.2777 % — **REFUSE**
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.82 % > budget 6.78 %
   - ⚪ sr_based a 1.5 ATR (stop 11.994 %) — p(stop avant cible) 0.2884 [0.24 ; 0.34], R/R 1.301, perte reelle 15.955 % (gap inclus), EV 1.7167 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.00 % > budget 6.78 %
   - 🟢 support a 3.23 ATR (stop 22.139 %) — p(stop avant cible) 0.059 [0.04 ; 0.09], R/R 0.938, perte reelle 22.139 % (gap inclus), EV 3.0621 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.14 % > budget 6.78 %
   - 🟢 support a 4.5 ATR (stop 29.579 %) — p(stop avant cible) 0.0232 [0.01 ; 0.04], R/R 0.702, perte reelle 29.579 % (gap inclus), EV 3.0605 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.58 % > budget 6.78 %
   - 🟢 support a 8.33 ATR (stop 52.063 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.399, perte reelle 52.063 % (gap inclus), EV 3.2109 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.06 % > budget 6.78 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.466 %) — p(stop avant cible) 0.9005 [0.87 ; 0.93], R/R 6.472, perte reelle 3.207 % (gap inclus), EV -1.3369 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.900, borne haute 0.929 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 5.0 % x 20.76 % + P(rien) 5.0 % x 10.37 % ne couvrent pas P(stop) 90.0 % x 3.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.932 %) — p(stop avant cible) 0.7652 [0.72 ; 0.81], R/R 4.172, perte reelle 4.975 % (gap inclus), EV -0.2826 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.765, borne haute 0.807 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 11.4 % x 20.76 % + P(rien) 12.1 % x 9.61 % ne couvrent pas P(stop) 76.5 % x 4.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.398 %) — p(stop avant cible) 0.6695 [0.62 ; 0.72], R/R 2.938, perte reelle 7.064 % (gap inclus), EV -0.1966 % — **REFUSE**
      - refuse : cible atteinte seulement 14.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.669, borne haute 0.718 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 14.3 % x 20.76 % + P(rien) 18.7 % x 8.34 % ne couvrent pas P(stop) 67.0 % x 7.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.864 %) — p(stop avant cible) 0.5867 [0.53 ; 0.64], R/R 2.217, perte reelle 9.362 % (gap inclus), EV -0.1749 % — **REFUSE**
      - refuse : p_stop_first 0.587, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 16.2 % x 20.76 % + P(rien) 25.1 % x 7.79 % ne couvrent pas P(stop) 58.7 % x 9.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.5 ATR (stop 10.552 %) — p(stop avant cible) 0.3568 [0.31 ; 0.41], R/R 1.573, perte reelle 13.192 % (gap inclus), EV 1.5642 % — **REFUSE**
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.56 % > budget 6.78 %
   - ⚪ atr_grid a 2.25 ATR (stop 13.195 %) — p(stop avant cible) 0.254 [0.21 ; 0.30], R/R 1.301, perte reelle 15.955 % (gap inclus), EV 2.1135 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.20 % > budget 6.78 %
   - ⚪ atr_grid a 2.5 ATR (stop 14.661 %) — p(stop avant cible) 0.2061 [0.17 ; 0.25], R/R 1.167, perte reelle 17.785 % (gap inclus), EV 2.2474 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.66 % > budget 6.78 %
   - ⚪ atr_grid a 2.75 ATR (stop 16.127 %) — p(stop avant cible) 0.1735 [0.14 ; 0.22], R/R 1.167, perte reelle 17.785 % (gap inclus), EV 2.5833 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.13 % > budget 6.78 %
   - 🟢 grid_snapped a 3.23 ATR (stop 20.697 %) — p(stop avant cible) 0.0757 [0.05 ; 0.11], R/R 1.003, perte reelle 20.697 % (gap inclus), EV 3.0338 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.70 % > budget 6.78 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.458 %) — p(stop avant cible) 0.0396 [0.02 ; 0.06], R/R 0.885, perte reelle 23.458 % (gap inclus), EV 3.0814 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.46 % > budget 6.78 %
   - 🟢 grid_snapped a 4.5 ATR (stop 28.136 %) — p(stop avant cible) 0.0252 [0.01 ; 0.05], R/R 0.738, perte reelle 28.136 % (gap inclus), EV 3.0599 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.14 % > budget 6.78 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.254 %) — p(stop avant cible) 0.0127 [0.00 ; 0.03], R/R 0.644, perte reelle 32.254 % (gap inclus), EV 3.092 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.25 % > budget 6.78 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.187 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.59, perte reelle 35.187 % (gap inclus), EV 3.1889 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.19 % > budget 6.78 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.119 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.545, perte reelle 38.119 % (gap inclus), EV 3.1921 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.12 % > budget 6.78 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.051 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.506, perte reelle 41.051 % (gap inclus), EV 3.2109 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.05 % > budget 6.78 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.983 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.472, perte reelle 43.983 % (gap inclus), EV 3.2109 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.98 % > budget 6.78 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.916 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.442, perte reelle 46.916 % (gap inclus), EV 3.2109 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.92 % > budget 6.78 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 124.2, ATR14 7.2836 (5.864 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 2.199 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.293 % | 123.8358 | 93.05 % | 95.16 % | 96.06 % | 96.56 % | 97.05 % | 98.05 % |
| 0.1 ATR | 0.586 % | 123.4716 | 85.7 % | 90.52 % | 92.23 % | 93.73 % | 94.72 % | 96.41 % |
| 0.15 ATR | 0.88 % | 123.1075 | 77.74 % | 85.28 % | 87.99 % | 90.29 % | 92.58 % | 95.07 % |
| 0.2 ATR | 1.173 % | 122.7433 | 71.7 % | 80.14 % | 83.75 % | 86.96 % | 90.35 % | 93.22 % |
| 0.25 ATR | 1.466 % | 122.3791 | 64.75 % | 74.4 % | 79.11 % | 83.42 % | 87.7 % | 90.86 % |
| 0.35 ATR | 2.053 % | 121.6507 | 52.57 % | 65.32 % | 71.95 % | 77.65 % | 83.43 % | 87.99 % |
| 0.5 ATR | 2.932 % | 120.5582 | 37.26 % | 53.53 % | 61.25 % | 68.35 % | 76.52 % | 82.44 % |
| 0.75 ATR | 4.398 % | 118.7373 | 19.64 % | 36.29 % | 46.01 % | 55.71 % | 65.65 % | 73.31 % |
| 1.0 ATR | 5.864 % | 116.9164 | 9.26 % | 23.08 % | 32.8 % | 43.88 % | 54.98 % | 65.71 % |
| 1.25 ATR | 7.331 % | 115.0954 | 4.83 % | 14.62 % | 22.5 % | 33.57 % | 46.85 % | 59.14 % |
| 1.5 ATR | 8.797 % | 113.2745 | 2.42 % | 9.88 % | 16.35 % | 27.1 % | 39.84 % | 53.49 % |
| 2.0 ATR | 11.729 % | 109.6327 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.57 % | 44.05 % |
| 2.5 ATR | 14.661 % | 105.9909 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.34 % | 34.6 % |
| 3.0 ATR | 17.593 % | 102.3491 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.59 % |
| 4.0 ATR | 23.458 % | 95.0654 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 35.187 % | 80.4981 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.77 ATR | 1.00 ATR | 1.19 ATR | 1.35 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.98 ATR | 1.27 ATR | 1.59 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.54 ATR | 1.15 ATR | 1.32 ATR | 1.83 ATR | 2.28 ATR | 2.61 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.69 ATR | 1.95 ATR | 2.60 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.424–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.398 %, prix 118.7377), p(touche) 36.29 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.769–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.864 %, prix 116.9169), p(touche) 32.8 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.8 % des re-echantillons)
- **5 seance(s)** : plage utile 0.976–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.864 %, prix 116.9169), p(touche) 43.88 % (en stress 98.99 %)  ✅ optimum identifie (61.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.316–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.797 %, prix 113.2741), p(touche) 39.84 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.95–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.729 %, prix 109.6326), p(touche) 44.05 % (en stress 97.96 %)  ✅ optimum identifie (63.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.045 | EV/share : $0.503 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 48.7 | bear 21.1 | side 30.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 621.0 (= 5 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.052% → cible +2.852% / stop −3.0%, p_fill 54%, n_eff≈23.9) : P(cible|rempli) **52%** · **EV/risk +0.181** (×p_fill ; si rempli +1.00% du capital)
  - **swing** (entrée dip −4.517% → cible +18.628% / stop −9.314%, p_fill 30%, n_eff≈13.0) : P(cible|rempli) **17%** · **EV/risk +0.105** (×p_fill ; si rempli +3.25% du capital)
  - **deep** (entrée dip −6.973% → cible +9.02% / stop −9.456%, p_fill 28%, n_eff≈14.6) : P(cible|rempli) **52%** · **EV/risk +0.012** (×p_fill ; si rempli +0.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→84% · +2.0%→57% · +3.0%→38% · +5.0%→22% · +8.0%→10%
- Range intraday médian 5.24% (p90 9.08%) · excursion haute méd. +2.18% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.95% vs midi 1.007% vs clôture 1.167% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr -0.028)_ ; drift intra méd. 0.571% ; recovery-V 34%
- **σ réalisé intraday** 3.51% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 42% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 123.065 (VA 122.039–123.635 ; dernier close 122.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 40% · rebond 80% · **stop −3.83%** sous le fill (sous le bruit) · cible +2.2% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 50% (gap-down >1% 32% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.68%) · haut méd +1.04% · range méd 2.28%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.52%) · haut méd +1.41% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −3.84%) · haut méd +1.64% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.84% (p90 −3.9%) · haut méd +1.69% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.11 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (124/159) · gap 42% · délai 0.0min · rebond 61% (68/124) (MFE +1.5%)
   - −1.0% : fill 30min 61% · séance 69% (110/159) · gap 32% · délai 0.0min · rebond 64% (65/110) (MFE +1.69%)
   - −1.5% : fill 30min 51% · séance 61% (101/159) · gap 24% · délai 0.6min · rebond 65% (59/101) (MFE +1.44%)
   - −2.0% : fill 30min 39% · séance 51% (89/159) · gap 15% · délai 1.5min · rebond 71% (56/89) (MFE +1.45%)
   - −3.0% : fill 30min 28% · séance 40% (69/159) · gap 7% · délai 10.8min · rebond 80% (49/69) (MFE +2.2%)
   - −4.0% : fill 30min 16% · séance 27% (51/159) · gap 3% · délai 11.9min · rebond 72% (34/51) (MFE +2.29%)
   - −5.0% : fill 30min 8% · séance 16% (33/159) · gap 2% · délai 28.3min · rebond 67% (24/33) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.64% (p90 −2.62%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.65% (p90 −2.3%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.37%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=786 jambes) : jambe baissière méd −1.12% (p90 −2.73%) · ~9.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 95% (73/76) · rebond 52% (38/73)
      · −2.0% : fill 82% (63/76) · rebond 66% (38/63)
      · −3.0% : fill 72% (54/76) · rebond 79% (38/54)
      · −4.0% : fill 49% (41/76) · rebond 71% (29/41)
      · −5.0% : fill 29% (28/76) · rebond 62% (19/28)
   - **flat** (17 séances) :
      · −1.0% : fill 69% (12/17) · rebond 85% (8/12)
      · −2.0% : fill 33% (9/17) · rebond 61% (6/9)
      · −3.0% : fill 10% (4/17) · rebond 18% (1/4)
      · −4.0% : fill 10% (4/17) · rebond 18% (1/4)
      · −5.0% : fill 4% (2/17) · rebond 100% (2/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (25/66) · rebond 84% (19/25)
      · −2.0% : fill 23% (17/66) · rebond 92% (12/17)
      · −3.0% : fill 13% (11/66) · rebond 97% (10/11)
      · −4.0% : fill 9% (6/66) · rebond 91% (4/6)
      · −5.0% : fill 4% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 67% si les 15 1res min sont vertes (75 cas) · 34% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **21min** → P(séance verte=clôture>ouverture) 70% si début vert vs 27% si rouge (base 49% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **70%** · continue >prix actuel 53% ; creux résiduel méd -1.6% (q20 -3.49%) → **SL/trailing à −3.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.54% → **scale +1.96% / runner +3.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **27%** (continue à baisser 58%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.71%** (au-delà de la MAE q10 -3.71%), cible rebond +1.67% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.1% .. +4.84%] · haut q95 +5.45% · bas q05 -4.99%
   - 60min (n=160) : retour [-3.67% .. +5.05%] · haut q95 +6.42% · bas q05 -5.48%
   - 2h (n=160) : retour [-4.69% .. +6.51%] · haut q95 +7.7% · bas q05 -5.97%
   - 4h (n=160) : retour [-4.7% .. +7.65%] · haut q95 +8.51% · bas q05 -6.61%
   - 6h (n=160) : retour [-5.74% .. +7.98%] · haut q95 +8.8% · bas q05 -7.09%
   - session (n=160) : retour [-5.29% .. +8.24%] · haut q95 +8.88% · bas q05 -7.11%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 8.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 22% vs absente 2% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.5% / p90 2.5%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 20.0 min, n=51)
   - −1.0% → **65%** (reprise méd 38.77 min, n=23)
   - −1.5% → **47%** (reprise méd 41.95 min, n=13)
   - −2.0% → **14%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.5%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +6.95% (q75 +9.04% / q95 +12.46%), MFE méd +8.52% / q90 +13.87%
   - Échelle scale-out : +8.52% (33%) / +9.47% (33%) / +13.87% (34%)
- **DÉSARMER** : repli > **−2.5%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 286.42 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.87% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 66.0  _(momentum haussier)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist 0.667  _(bullish_recent)_
- **BB** : %B 0.9 · largeur 24.6%
- **ATR** : 7.28 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.081  _(accumulation)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 53.7  _(transition)_
- **MA** : MA20 113.08 · MA50 103.69 · MA200 94.84  _(prix > MA20)_
- **Dist MA** : MA20 +9.8% · MA50 +19.8% · MA200 +31.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (845556 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
