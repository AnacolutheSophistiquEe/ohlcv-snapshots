# SMCI

**Generated** : 2026-09-14T00:34:41.508906+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $40.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $40.10 (+0.9% vs entrée) · entrée $39.74 · stop $37.52 · T1 $41.62 · R/R 0.85  
> ↳ P(T1 av. stop) 43 % _(réel 5 s)_ · EV/risk -0.146 _(réel 5 s)_ (GBM 0.033) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $39.38–$40.10 (mid $39.74)
- Spot actuel : $40.10 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $37.52 (stop swing_plan-based (-6.44%))
- Targets : T1 $41.62 · R/R 0.85 | T2 $43.50 · R/R 1.69 | T3 $45.38 · R/R 2.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $37.52


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.44 %)** : le gap seul le franchit 1.834 % des séances (23 fois sur 1254).
   - exécution **4.827 pt plus bas** dans le cas TYPIQUE (médiane), 17.108 au p90, **22.611 au pire**
   - perte réelle **13.25 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 6.44 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.1249 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.763 % | p01 -10.29 % | pire -29.051 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5421** [0.4677 ; 0.6151] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4437** [0.392 ; 0.4964] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3955** [0.345 ; 0.4477] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.7 pt), swing (32.4 pt), deep (31.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.78 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.74 % contre 6.53 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.68 % vs -16.02 % si l'on extrapolait par √5 _(rapport 1.042 ; < 1 = le √5 surestime)_
- **β de baisse : 1.542** (β de hausse 1.2299, asymétrie 1.2537) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.921× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 36.7679 sur atr_based (1.5 ATR, 8.309 %) — p(stop avant cible) 0.4915 [0.44 ; 0.54], R/R 1.268, perte reelle 14.137 % (gap inclus), CVaR 8.402 %, EV -1.6372 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.28 ATR (stop 4.657 %) — p(stop avant cible) 0.712 [0.66 ; 0.76], R/R 1.821, perte reelle 9.842 % (gap inclus), EV -3.123 % — **REFUSE**
      - refuse : p_stop_first 0.712, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.28 ATR du spot — compartiment <1, mesure a 46.4 % de casse (IC clusterise [0.434 ; 0.494] sur 1185 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.12 %) : P(cible) 18.6 % x 17.93 % + P(rien) 10.2 % x 5.44 % ne couvrent pas P(stop) 71.2 % x 9.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.309 %) — p(stop avant cible) 0.4915 [0.44 ; 0.54], R/R 1.268, perte reelle 14.137 % (gap inclus), EV -1.6372 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.64 %) : P(cible) 25.4 % x 17.93 % + P(rien) 25.4 % x 2.95 % ne couvrent pas P(stop) 49.1 % x 14.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.21 ATR (stop 15.341 %) — p(stop avant cible) 0.2284 [0.19 ; 0.27], R/R 0.766, perte reelle 23.404 % (gap inclus), EV -0.141 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 28.9 % x 17.93 % + P(rien) 48.2 % x 0.04 % ne couvrent pas P(stop) 22.8 % x 23.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.58 ATR (stop 33.983 %) — p(stop avant cible) 0.0688 [0.05 ; 0.10], R/R 0.528, perte reelle 33.983 % (gap inclus), EV 1.128 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.98 % > budget 12.00 %
   - 🟢 support a 6.61 ATR (stop 39.719 %) — p(stop avant cible) 0.016 [0.01 ; 0.03], R/R 0.451, perte reelle 39.719 % (gap inclus), EV 1.2776 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.72 % > budget 12.00 %
   - 🔴 grid_snapped a 0.28 ATR (stop 3.233 %) — p(stop avant cible) 0.7913 [0.75 ; 0.83], R/R 2.66, perte reelle 6.74 % (gap inclus), EV -2.2366 % — **REFUSE**
      - refuse : cible atteinte seulement 15.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.791, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.24 %) : P(cible) 15.0 % x 17.93 % + P(rien) 5.9 % x 7.00 % ne couvrent pas P(stop) 79.1 % x 6.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.54 %) — p(stop avant cible) 0.6701 [0.62 ; 0.72], R/R 1.572, perte reelle 11.406 % (gap inclus), EV -3.374 % — **REFUSE**
      - refuse : p_stop_first 0.670, borne haute 0.718 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.37 %) : P(cible) 20.6 % x 17.93 % + P(rien) 12.4 % x 4.69 % ne couvrent pas P(stop) 67.0 % x 11.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 6.925 %) — p(stop avant cible) 0.5796 [0.53 ; 0.63], R/R 1.323, perte reelle 13.549 % (gap inclus), EV -2.8459 % — **REFUSE**
      - refuse : p_stop_first 0.580, borne haute 0.631 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.85 %) : P(cible) 23.7 % x 17.93 % + P(rien) 18.3 % x 4.12 % ne couvrent pas P(stop) 58.0 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.695 %) — p(stop avant cible) 0.44 [0.39 ; 0.49], R/R 1.062, perte reelle 16.875 % (gap inclus), EV -1.9819 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.98 %) : P(cible) 26.2 % x 17.93 % + P(rien) 29.8 % x 2.49 % ne couvrent pas P(stop) 44.0 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.21 ATR (stop 13.917 %) — p(stop avant cible) 0.2598 [0.22 ; 0.31], R/R 0.861, perte reelle 20.821 % (gap inclus), EV 0.0191 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.96 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.619 %) — p(stop avant cible) 0.2018 [0.16 ; 0.25], R/R 0.766, perte reelle 23.404 % (gap inclus), EV 0.5321 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.65 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.389 %) — p(stop avant cible) 0.1497 [0.12 ; 0.19], R/R 0.668, perte reelle 26.856 % (gap inclus), EV 0.9062 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.41 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.159 %) — p(stop avant cible) 0.1312 [0.10 ; 0.17], R/R 0.668, perte reelle 26.856 % (gap inclus), EV 1.1516 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.17 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.929 %) — p(stop avant cible) 0.1015 [0.07 ; 0.14], R/R 0.641, perte reelle 27.955 % (gap inclus), EV 1.4183 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.93 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.699 %) — p(stop avant cible) 0.0883 [0.06 ; 0.12], R/R 0.617, perte reelle 29.051 % (gap inclus), EV 1.398 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.70 % > budget 12.00 %
   - 🟢 grid_snapped a 5.58 ATR (stop 32.56 %) — p(stop avant cible) 0.0748 [0.05 ; 0.11], R/R 0.551, perte reelle 32.56 % (gap inclus), EV 1.1793 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.56 % > budget 12.00 %
   - 🟢 grid_snapped a 6.61 ATR (stop 38.295 %) — p(stop avant cible) 0.0338 [0.02 ; 0.06], R/R 0.468, perte reelle 38.295 % (gap inclus), EV 1.1978 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.30 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.548 %) — p(stop avant cible) 0.009 [0.00 ; 0.02], R/R 0.431, perte reelle 41.548 % (gap inclus), EV 1.2968 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.55 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.318 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.405, perte reelle 44.318 % (gap inclus), EV 1.301 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.32 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 40.1, ATR14 2.2214 (5.54 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.343 ATR = 1.9 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.277 % | 39.9889 | 90.34 % | 93.15 % | 94.56 % | 95.05 % | 96.35 % | 97.54 % |
| 0.1 ATR | 0.554 % | 39.8779 | 82.09 % | 87.11 % | 89.11 % | 91.11 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.831 % | 39.7668 | 74.85 % | 81.87 % | 84.78 % | 88.08 % | 90.56 % | 93.54 % |
| 0.2 ATR | 1.108 % | 39.6557 | 67.91 % | 77.14 % | 80.34 % | 85.56 % | 89.04 % | 92.21 % |
| 0.25 ATR | 1.385 % | 39.5446 | 61.87 % | 72.61 % | 76.21 % | 82.22 % | 87.01 % | 90.46 % |
| 0.35 ATR | 1.939 % | 39.3225 | 49.09 % | 63.34 % | 69.46 % | 76.97 % | 82.64 % | 87.9 % |
| 0.5 ATR | 2.77 % | 38.9893 | 34.81 % | 49.75 % | 58.06 % | 68.48 % | 76.85 % | 83.59 % |
| 0.75 ATR | 4.155 % | 38.4339 | 17.3 % | 33.13 % | 42.74 % | 54.85 % | 66.4 % | 75.38 % |
| 1.0 ATR | 5.54 % | 37.8786 | 8.05 % | 21.65 % | 30.54 % | 43.43 % | 57.16 % | 68.41 % |
| 1.25 ATR | 6.925 % | 37.3232 | 3.82 % | 15.01 % | 22.48 % | 33.13 % | 48.12 % | 61.44 % |
| 1.5 ATR | 8.31 % | 36.7679 | 1.51 % | 9.67 % | 16.43 % | 26.16 % | 41.93 % | 55.08 % |
| 2.0 ATR | 11.079 % | 35.6571 | 0.3 % | 3.52 % | 8.37 % | 16.06 % | 30.05 % | 43.79 % |
| 2.5 ATR | 13.849 % | 34.5464 | 0.2 % | 1.51 % | 4.33 % | 9.8 % | 19.8 % | 32.0 % |
| 3.0 ATR | 16.619 % | 33.4357 | 0.2 % | 1.21 % | 2.62 % | 5.66 % | 14.21 % | 24.1 % |
| 4.0 ATR | 22.159 % | 31.2143 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.41 % | 14.15 % |
| 6.0 ATR | 33.238 % | 26.7714 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.57 ATR | 0.75 ATR | 0.93 ATR | 1.06 ATR | 1.49 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.63 ATR | 0.71 ATR | 0.95 ATR | 1.17 ATR | 1.35 ATR | 1.90 ATR | 2.42 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.25 ATR | 1.56 ATR | 1.80 ATR | 2.48 ATR | 3.22 ATR |
| **10 s.** | 0.54 ATR | 1.20 ATR | 1.38 ATR | 1.88 ATR | 2.25 ATR | 2.49 ATR | 3.62 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.73 ATR | 1.95 ATR | 2.46 ATR | 2.94 ATR | 3.41 ATR | 4.96 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.393–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.571–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.155 %, prix 38.4338), p(touche) 33.13 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.713–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.155 %, prix 38.4338), p(touche) 42.74 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 15.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.966–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.925 %, prix 37.3231), p(touche) 33.13 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.376–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.31 %, prix 36.7677), p(touche) 41.93 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.946–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (16.619 %, prix 33.4358), p(touche) 24.1 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : $0.073 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 34 % | T3 22 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 83.6 | bear 6.7 | side 9.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 602.0 (= 15 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.408% → cible +2.118% / stop −1.669%, p_fill 93%, n_eff≈37.9) : P(cible|rempli) **42%** · **EV/risk -0.052** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −0.9% → cible +4.735% / stop −5.59%, p_fill 85%, n_eff≈34.2) : P(cible|rempli) **43%** · **EV/risk -0.146** (×p_fill ; si rempli -0.96% du capital)
  - **deep** (entrée dip −1.33% → cible +6.696% / stop −8.422%, p_fill 90%, n_eff≈35.0) : P(cible|rempli) **59%** · **EV/risk +0.048** (×p_fill ; si rempli +0.45% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.6  _(momentum haussier)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist -0.08  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 14.2%
- **ATR** : 2.22 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.008  _(neutre)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 54.2  _(transition)_
- **MA** : MA20 37.88 · MA50 32.52 · MA200 31.49  _(prix > MA20)_
- **Dist MA** : MA20 +5.9% · MA50 +23.3% · MA200 +27.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (752499 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
