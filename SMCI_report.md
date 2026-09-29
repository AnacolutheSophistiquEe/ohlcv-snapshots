# SMCI

**Generated** : 2026-09-29T00:34:05.466801+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $41.78  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $41.78 (+1.0% vs entrée) · entrée $41.38 · stop $39.03 · T1 $43.55 · R/R 0.92  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk -0.114 _(réel 5 s)_ (GBM 0.059) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -7.5 % ≠ (strike 40.0 − spot 41.78)/spot = -4.3 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $40.97–$41.78 (mid $41.38)
- Spot actuel : $41.78 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $39.03 (plancher anti-bruit (R/R<2) ; -5.68 % depuis l'entree)
- Targets : T1 $43.55 · R/R 0.92 | T2 $45.72 · R/R 1.85 | T3 $47.89 · R/R 2.77
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.03


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.59 %)** : le gap seul le franchit 1.915 % des séances (24 fois sur 1253).
   - exécution **4.643 pt plus bas** dans le cas TYPIQUE (médiane), 16.403 au p90, **22.461 au pire**
   - perte réelle **12.976 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 6.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.1223 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5457** [0.4713 ; 0.6186] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4419** [0.3902 ; 0.4946] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.388** [0.3377 ; 0.4401] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.0 pt), swing (32.3 pt), deep (31.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.86 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.62 % contre 6.51 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5316** (β de hausse 1.218, asymétrie 1.2575) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.829× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 40.1633 sur grid_snapped (0.39 ATR, 3.881 %) — p(stop avant cible) 0.7451 [0.70 ; 0.79], R/R 1.816, perte reelle 8.051 % (gap inclus), CVaR 4.084 %, EV -3.024 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5035 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.745, borne haute 0.789 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 4.08 % > budget 3.82 %
- Budget de queue : **3.82 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.18 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 47.6 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.39 ATR (stop 4.781 %) — p(stop avant cible) 0.6974 [0.65 ; 0.74], R/R 1.497, perte reelle 9.766 % (gap inclus), EV -3.351 % — **REFUSE**
      - refuse : p_stop_first 0.697, borne haute 0.744 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 4.95 % > budget 3.82 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.35 %) : P(cible) 21.6 % x 14.62 % + P(rien) 8.6 % x 3.46 % ne couvrent pas P(stop) 69.7 % x 9.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 0.99 ATR (stop 8.127 %) — p(stop avant cible) 0.4806 [0.43 ; 0.53], R/R 1.034, perte reelle 14.137 % (gap inclus), EV -2.0246 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.22 % > budget 3.82 %
      - ⚠ support DETECTE a 0.29 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.441 ; 0.507] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 29.4 % x 14.62 % + P(rien) 22.5 % x 2.07 % ne couvrent pas P(stop) 48.1 % x 14.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 2.93 ATR (stop 19.088 %) — p(stop avant cible) 0.1373 [0.10 ; 0.18], R/R 0.587, perte reelle 24.92 % (gap inclus), EV 1.2472 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.11 % > budget 3.82 %
   - 🟢 support a 7.83 ATR (stop 46.634 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.314, perte reelle 46.634 % (gap inclus), EV 1.3402 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.63 % > budget 3.82 %
   - 🟢 support a 9.49 ATR (stop 55.967 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.261, perte reelle 55.967 % (gap inclus), EV 1.3296 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.97 % > budget 3.82 %
   - ⚪ grid_snapped a 0.39 ATR (stop 3.881 %) — p(stop avant cible) 0.7451 [0.70 ; 0.79], R/R 1.816, perte reelle 8.051 % (gap inclus), EV -3.024 % — **REFUSE**
      - refuse : p_stop_first 0.745, borne haute 0.789 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 4.08 % > budget 3.82 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.02 %) : P(cible) 18.7 % x 14.62 % + P(rien) 6.8 % x 3.61 % ne couvrent pas P(stop) 74.5 % x 8.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.99 ATR (stop 7.227 %) — p(stop avant cible) 0.5447 [0.49 ; 0.60], R/R 1.079, perte reelle 13.549 % (gap inclus), EV -2.8517 % — **REFUSE**
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.34 % > budget 3.82 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.85 %) : P(cible) 27.7 % x 14.62 % + P(rien) 17.8 % x 2.69 % ne couvrent pas P(stop) 54.5 % x 13.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 9.842 %) — p(stop avant cible) 0.4151 [0.36 ; 0.47], R/R 0.866, perte reelle 16.875 % (gap inclus), EV -2.068 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.91 % > budget 3.82 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 30.8 % x 14.62 % + P(rien) 27.7 % x 1.56 % ne couvrent pas P(stop) 41.5 % x 16.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 11.248 %) — p(stop avant cible) 0.3414 [0.29 ; 0.39], R/R 0.843, perte reelle 17.348 % (gap inclus), EV -0.7846 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.31 % > budget 3.82 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 32.8 % x 14.62 % + P(rien) 33.1 % x 1.05 % ne couvrent pas P(stop) 34.1 % x 17.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 12.654 %) — p(stop avant cible) 0.2872 [0.24 ; 0.34], R/R 0.761, perte reelle 19.221 % (gap inclus), EV -0.4479 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.70 % > budget 3.82 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 33.7 % x 14.62 % + P(rien) 37.6 % x 0.39 % ne couvrent pas P(stop) 28.7 % x 19.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 14.06 %) — p(stop avant cible) 0.2338 [0.19 ; 0.28], R/R 0.702, perte reelle 20.821 % (gap inclus), EV 0.063 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.10 % > budget 3.82 %
   - ⚪ grid_snapped a 2.93 ATR (stop 18.188 %) — p(stop avant cible) 0.1468 [0.11 ; 0.19], R/R 0.587, perte reelle 24.92 % (gap inclus), EV 1.0489 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.21 % > budget 3.82 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.496 %) — p(stop avant cible) 0.1123 [0.08 ; 0.15], R/R 0.544, perte reelle 26.856 % (gap inclus), EV 1.328 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.51 % > budget 3.82 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.308 %) — p(stop avant cible) 0.0885 [0.06 ; 0.12], R/R 0.523, perte reelle 27.955 % (gap inclus), EV 1.4765 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.31 % > budget 3.82 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.12 %) — p(stop avant cible) 0.0788 [0.05 ; 0.11], R/R 0.503, perte reelle 29.051 % (gap inclus), EV 1.4472 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.12 % > budget 3.82 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.932 %) — p(stop avant cible) 0.0713 [0.05 ; 0.10], R/R 0.473, perte reelle 30.932 % (gap inclus), EV 1.339 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.93 % > budget 3.82 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.744 %) — p(stop avant cible) 0.0609 [0.04 ; 0.09], R/R 0.433, perte reelle 33.744 % (gap inclus), EV 1.2197 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.74 % > budget 3.82 %
   - ⚪ atr_grid a 6.5 ATR (stop 36.556 %) — p(stop avant cible) 0.054 [0.03 ; 0.08], R/R 0.4, perte reelle 36.556 % (gap inclus), EV 1.1046 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.56 % > budget 3.82 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.368 %) — p(stop avant cible) 0.0156 [0.01 ; 0.03], R/R 0.371, perte reelle 39.368 % (gap inclus), EV 1.3275 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.37 % > budget 3.82 %
   - ⚪ atr_grid a 7.5 ATR (stop 42.18 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.347, perte reelle 42.18 % (gap inclus), EV 1.3504 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.18 % > budget 3.82 %
   - 🟢 grid_snapped a 7.83 ATR (stop 45.734 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.32, perte reelle 45.734 % (gap inclus), EV 1.3409 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.73 % > budget 3.82 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 41.785, ATR14 2.35 (5.624 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.342 ATR = 1.923 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.281 % | 41.6675 | 90.43 % | 93.25 % | 94.65 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.562 % | 41.55 | 82.07 % | 87.2 % | 89.2 % | 91.1 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.844 % | 41.4325 | 74.92 % | 82.06 % | 84.96 % | 88.17 % | 90.65 % | 93.53 % |
| 0.2 ATR | 1.125 % | 41.315 | 67.98 % | 77.32 % | 80.52 % | 85.64 % | 89.13 % | 92.2 % |
| 0.25 ATR | 1.406 % | 41.1975 | 61.83 % | 72.68 % | 76.39 % | 82.31 % | 87.09 % | 90.45 % |
| 0.35 ATR | 1.968 % | 40.9625 | 49.04 % | 63.31 % | 69.63 % | 77.05 % | 82.83 % | 87.78 % |
| 0.5 ATR | 2.812 % | 40.61 | 34.84 % | 49.9 % | 58.53 % | 68.66 % | 77.03 % | 83.47 % |
| 0.75 ATR | 4.218 % | 40.0225 | 17.32 % | 33.27 % | 42.99 % | 55.01 % | 66.46 % | 75.26 % |
| 1.0 ATR | 5.624 % | 39.435 | 7.96 % | 21.57 % | 30.47 % | 43.48 % | 57.11 % | 68.48 % |
| 1.25 ATR | 7.03 % | 38.8475 | 3.73 % | 14.82 % | 22.2 % | 32.96 % | 47.76 % | 60.88 % |
| 1.5 ATR | 8.436 % | 38.26 | 1.51 % | 9.48 % | 16.25 % | 25.88 % | 41.57 % | 54.62 % |
| 2.0 ATR | 11.248 % | 37.085 | 0.3 % | 3.53 % | 8.17 % | 15.87 % | 29.57 % | 43.33 % |
| 2.5 ATR | 14.06 % | 35.91 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 16.872 % | 34.735 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 22.496 % | 32.385 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 33.744 % | 27.685 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.57 ATR | 0.76 ATR | 0.93 ATR | 1.06 ATR | 1.48 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.17 ATR | 1.34 ATR | 1.89 ATR | 2.40 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.25 ATR | 1.54 ATR | 1.79 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.55 ATR | 1.19 ATR | 1.36 ATR | 1.86 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.71 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.393–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.574–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.218 %, prix 40.0225), p(touche) 33.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.718–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.218 %, prix 40.0225), p(touche) 42.99 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.967–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.03 %, prix 38.8475), p(touche) 32.96 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.361–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.436 %, prix 38.26), p(touche) 41.57 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.926–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (16.872 %, prix 34.735), p(touche) 23.72 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.059 | EV/share : $0.137 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 31 % | T3 20 %
- Kelly (position) : f* 0.014 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 78.8 | bear 5.7 | side 15.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 627.0 (= 15 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.443% → cible +2.347% / stop −1.695%, p_fill 92%, n_eff≈37.3) : P(cible|rempli) **46%** · **EV/risk +0.106** (×p_fill ; si rempli +0.20% du capital)
  - **swing** (entrée dip −0.966% → cible +5.248% / stop −5.679%, p_fill 85%, n_eff≈34.2) : P(cible|rempli) **42%** · **EV/risk -0.114** (×p_fill ; si rempli -0.76% du capital)
  - **deep** (entrée dip −1.424% → cible +7.422% / stop −8.558%, p_fill 89%, n_eff≈34.2) : P(cible|rempli) **59%** · **EV/risk +0.083** (×p_fill ; si rempli +0.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→92% · +1.0%→76% · +2.0%→61% · +3.0%→46% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.2% (p90 10.79%) · excursion haute méd. +2.57% / basse méd. −2.36%
- Profil de vol intra : ouverture 4.155% vs midi 1.244% vs clôture 1.619% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.019)_ ; drift intra méd. 0.322% ; recovery-V 35%
- **σ réalisé intraday** 3.833% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 40.5704 (VA 39.4716–40.8634 ; dernier close 39.59)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 81% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.59% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 45% (gap-down >1% 36% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.79%) · haut méd +0.96% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.21%) · haut méd +1.42% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −3.93%) · haut méd +1.5% · range méd 3.68%
- Excursion ouverture 60min (n=160) : bas méd −1.72% (p90 −4.91%) · haut méd +1.81% · range méd 4.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (120/159) · gap 42% · délai 0.0min · rebond 58% (73/120) (MFE +1.37%)
   - −1.0% : fill 30min 55% · séance 69% (111/159) · gap 36% · délai 0.0min · rebond 62% (67/111) (MFE +1.61%)
   - −1.5% : fill 30min 49% · séance 63% (101/159) · gap 22% · délai 0.0min · rebond 71% (66/101) (MFE +1.61%)
   - −2.0% : fill 30min 43% · séance 55% (88/159) · gap 17% · délai 0.5min · rebond 74% (58/88) (MFE +1.91%)
   - −3.0% : fill 30min 31% · séance 48% (75/159) · gap 10% · délai 7.1min · rebond 63% (47/75) (MFE +1.9%)
   - −4.0% : fill 30min 17% · séance 36% (57/159) · gap 5% · délai 36.7min · rebond 78% (38/57) (MFE +1.88%)
   - −5.0% : fill 30min 13% · séance 27% (46/159) · gap 3% · délai 42.5min · rebond 81% (34/46) (MFE +2.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.79%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.95%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.74% (p90 −2.73%) → stop au-delà de −2.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=897 jambes) : jambe baissière méd −1.19% (p90 −2.87%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 97% (68/70) · rebond 50% (36/68)
      · −2.0% : fill 92% (64/70) · rebond 70% (39/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (35/58)
      · −4.0% : fill 65% (45/70) · rebond 78% (30/45)
      · −5.0% : fill 49% (37/70) · rebond 80% (27/37)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 40% (30/76) · rebond 77% (20/30)
      · −2.0% : fill 24% (18/76) · rebond 84% (15/18)
      · −3.0% : fill 16% (14/76) · rebond 70% (9/14)
      · −4.0% : fill 12% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 11% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 64% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:47** → P(séance verte=clôture>ouverture) 80% si début vert vs 9% si rouge (base 47% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=87) : tient le vert **80%** · continue >prix actuel 48% ; creux résiduel méd -1.35% (q20 -3.0%) → **SL/trailing à −3.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.95% → **scale +1.8% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **9%** (continue à baisser 48%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.18% .. +4.68%] · haut q95 +5.63% · bas q05 -4.48%
   - 60min (n=160) : retour [-4.4% .. +5.2%] · haut q95 +6.46% · bas q05 -5.33%
   - 2h (n=160) : retour [-4.66% .. +6.65%] · haut q95 +7.25% · bas q05 -5.84%
   - 4h (n=160) : retour [-5.17% .. +7.01%] · haut q95 +8.34% · bas q05 -6.68%
   - 6h (n=160) : retour [-5.44% .. +6.82%] · haut q95 +9.16% · bas q05 -6.9%
   - session (n=160) : retour [-6.74% .. +7.68%] · haut q95 +9.32% · bas q05 -7.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.61%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.5  _(neutre)_
- **ADX** : 27.0  _(tendance etablie)_
- **MACD** : hist 0.196  _(pas de croisement recent)_
- **BB** : %B 0.79 · largeur 22.3%
- **ATR** : 2.35 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.109  _(accumulation)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 39.23 · MA50 35.38 · MA200 31.83  _(prix > MA20)_
- **Dist MA** : MA20 +6.5% · MA50 +18.1% · MA200 +31.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (855712 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
