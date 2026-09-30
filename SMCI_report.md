# SMCI

**Generated** : 2026-09-30T00:26:51.130103+00:00  
**Santé technique** : 9/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $41.03  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $41.03 (+2.1% vs entrée) · entrée $40.17 · stop $37.79 · T1 $41.92 · R/R 0.74  
> ↳ ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -4.3 % ≠ (strike 40.0 − spot 41.03)/spot = -2.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $39.82–$40.52 (mid $40.17)
- Spot actuel : $41.03 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : $37.79 (plancher anti-bruit (R/R<2) ; -5.92 % depuis l'entree)
- Targets : T1 $41.92 · R/R 0.74 | T2 $44.23 · R/R 1.71 | T3 $46.55 · R/R 2.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $37.79


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.89 %)** : le gap seul le franchit 1.596 % des séances (20 fois sur 1253).
   - exécution **4.066 pt plus bas** dans le cas TYPIQUE (médiane), 16.987 au p90, **21.161 au pire**
   - perte réelle **14.137 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 7.89 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0997 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4732** [0.3998 ; 0.5475] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3912** [0.3408 ; 0.4434] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.4235** [0.3722 ; 0.476] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.86 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.62 % contre 6.51 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.529** (β de hausse 1.218, asymétrie 1.2553) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.825× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 38.7562 sur grid_snapped (0.66 ATR, 5.542 %) — p(stop avant cible) 0.6489 [0.60 ; 0.70], R/R 2.113, perte reelle 6.363 % (gap inclus), CVaR 15.939 %, EV -0.279 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8925 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 15.94 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 17 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 41.9 % de la queue et il ne reste que 294.13 EUR a partager. Prix du risque 0.099 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.66 ATR (stop 6.441 %) — p(stop avant cible) 0.5889 [0.54 ; 0.64], R/R 1.811, perte reelle 7.427 % (gap inclus), EV -0.1412 % — **REFUSE**
      - refuse : p_stop_first 0.589, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.57 % > budget 12.00 %
      - ⚠ support DETECTE a 0.66 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 29.2 % x 13.45 % + P(rien) 11.9 % x 2.55 % ne couvrent pas P(stop) 58.9 % x 7.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 8.698 %) — p(stop avant cible) 0.4439 [0.39 ; 0.50], R/R 1.309, perte reelle 10.273 % (gap inclus), EV 0.3071 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.39 % > budget 12.00 %
   - 🟢 support a 7.42 ATR (stop 45.656 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.294, perte reelle 45.803 % (gap inclus), EV 1.4063 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.38 % > budget 12.00 %
   - 🟢 support a 9.06 ATR (stop 55.161 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.241, perte reelle 55.756 % (gap inclus), EV 1.3935 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.63 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.45 %) — p(stop avant cible) 0.8937 [0.86 ; 0.92], R/R 8.093, perte reelle 1.662 % (gap inclus), EV -0.0788 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 8.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.894, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 10.3 % x 13.45 % + P(rien) 0.3 % x 5.93 % ne couvrent pas P(stop) 89.4 % x 1.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.66 ATR (stop 5.542 %) — p(stop avant cible) 0.6489 [0.60 ; 0.70], R/R 2.113, perte reelle 6.363 % (gap inclus), EV -0.279 % — **REFUSE**
      - refuse : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 27.0 % x 13.45 % + P(rien) 8.1 % x 2.73 % ne couvrent pas P(stop) 64.9 % x 6.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.249 %) — p(stop avant cible) 0.5354 [0.48 ; 0.59], R/R 1.576, perte reelle 8.535 % (gap inclus), EV -0.0028 % — **REFUSE**
      - refuse : p_stop_first 0.535, borne haute 0.588 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 31.1 % x 13.45 % + P(rien) 15.4 % x 2.51 % ne couvrent pas P(stop) 53.5 % x 8.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 10.148 %) — p(stop avant cible) 0.3991 [0.35 ; 0.45], R/R 1.142, perte reelle 11.779 % (gap inclus), EV 0.3382 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 11.598 %) — p(stop avant cible) 0.3267 [0.28 ; 0.38], R/R 1.001, perte reelle 13.437 % (gap inclus), EV 0.7278 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.32 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 13.048 %) — p(stop avant cible) 0.2645 [0.22 ; 0.31], R/R 0.892, perte reelle 15.072 % (gap inclus), EV 1.1032 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.53 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 14.497 %) — p(stop avant cible) 0.2221 [0.18 ; 0.27], R/R 0.806, perte reelle 16.675 % (gap inclus), EV 1.1535 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.02 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.947 %) — p(stop avant cible) 0.1978 [0.16 ; 0.24], R/R 0.733, perte reelle 18.334 % (gap inclus), EV 1.1867 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.88 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.397 %) — p(stop avant cible) 0.1639 [0.13 ; 0.21], R/R 0.674, perte reelle 19.952 % (gap inclus), EV 1.65 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.23 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.296 %) — p(stop avant cible) 0.129 [0.10 ; 0.17], R/R 0.601, perte reelle 22.356 % (gap inclus), EV 1.7367 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.55 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.196 %) — p(stop avant cible) 0.1094 [0.08 ; 0.15], R/R 0.538, perte reelle 24.979 % (gap inclus), EV 1.6353 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.10 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.095 %) — p(stop avant cible) 0.0839 [0.06 ; 0.12], R/R 0.496, perte reelle 27.132 % (gap inclus), EV 1.6338 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.83 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.994 %) — p(stop avant cible) 0.0772 [0.05 ; 0.11], R/R 0.46, perte reelle 29.237 % (gap inclus), EV 1.4988 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.37 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.894 %) — p(stop avant cible) 0.0696 [0.05 ; 0.10], R/R 0.42, perte reelle 32.034 % (gap inclus), EV 1.3327 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.09 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.793 %) — p(stop avant cible) 0.0604 [0.04 ; 0.09], R/R 0.385, perte reelle 34.917 % (gap inclus), EV 1.2148 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.94 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.693 %) — p(stop avant cible) 0.041 [0.02 ; 0.07], R/R 0.357, perte reelle 37.716 % (gap inclus), EV 1.2371 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.97 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.592 %) — p(stop avant cible) 0.0122 [0.00 ; 0.03], R/R 0.331, perte reelle 40.598 % (gap inclus), EV 1.399 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.50 % > budget 12.00 %
   - 🟢 grid_snapped a 7.42 ATR (stop 44.757 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.299, perte reelle 44.93 % (gap inclus), EV 1.4085 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.34 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.391 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.285, perte reelle 47.185 % (gap inclus), EV 1.4005 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.44 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 41.03, ATR14 2.3793 (5.799 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.343 ATR = 1.989 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.29 % | 40.911 | 90.43 % | 93.25 % | 94.65 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.58 % | 40.7921 | 82.07 % | 87.2 % | 89.2 % | 91.1 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.87 % | 40.6731 | 74.92 % | 82.06 % | 84.96 % | 88.17 % | 90.65 % | 93.53 % |
| 0.2 ATR | 1.16 % | 40.5541 | 67.98 % | 77.32 % | 80.52 % | 85.64 % | 89.13 % | 92.2 % |
| 0.25 ATR | 1.45 % | 40.4352 | 61.83 % | 72.68 % | 76.29 % | 82.31 % | 87.09 % | 90.45 % |
| 0.35 ATR | 2.03 % | 40.1972 | 49.14 % | 63.31 % | 69.53 % | 77.05 % | 82.83 % | 87.78 % |
| 0.5 ATR | 2.899 % | 39.8404 | 34.94 % | 49.8 % | 58.43 % | 68.66 % | 77.03 % | 83.37 % |
| 0.75 ATR | 4.349 % | 39.2455 | 17.42 % | 33.17 % | 42.89 % | 54.9 % | 66.36 % | 75.15 % |
| 1.0 ATR | 5.799 % | 38.6507 | 7.96 % | 21.47 % | 30.37 % | 43.38 % | 57.01 % | 68.38 % |
| 1.25 ATR | 7.249 % | 38.0559 | 3.73 % | 14.82 % | 22.1 % | 32.86 % | 47.66 % | 60.78 % |
| 1.5 ATR | 8.698 % | 37.4611 | 1.51 % | 9.48 % | 16.15 % | 25.78 % | 41.46 % | 54.52 % |
| 2.0 ATR | 11.598 % | 36.2714 | 0.3 % | 3.53 % | 8.17 % | 15.87 % | 29.57 % | 43.33 % |
| 2.5 ATR | 14.497 % | 35.0818 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 17.397 % | 33.8921 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 23.196 % | 31.5129 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 34.793 % | 26.7543 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.57 ATR | 0.75 ATR | 0.93 ATR | 1.05 ATR | 1.48 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.16 ATR | 1.34 ATR | 1.89 ATR | 2.40 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.96 ATR | 1.25 ATR | 1.54 ATR | 1.79 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.55 ATR | 1.19 ATR | 1.36 ATR | 1.86 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.70 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.572–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.349 %, prix 39.2456), p(touche) 33.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.716–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.349 %, prix 39.2456), p(touche) 42.89 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.965–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.249 %, prix 38.0557), p(touche) 32.86 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.357–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.698 %, prix 37.4612), p(touche) 41.46 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.925–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (17.397 %, prix 33.892), p(touche) 23.72 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : $0.078 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 32 % | T3 19 %
- Kelly (position) : f* 0.033 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 84.2 | bear 5.3 | side 10.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 615.0 (= 17 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.95% → cible +1.23% / stop −1.756%, p_fill 80%, n_eff≈84.8) : P(cible|rempli) **61%** · **EV/risk +0.026** (×p_fill ; si rempli +0.06% du capital)
  - **swing** (entrée dip −2.091% → cible +4.351% / stop −5.923%, p_fill 73%, n_eff≈83.7) : P(cible|rempli) **56%** · **EV/risk -0.044** (×p_fill ; si rempli -0.36% du capital)
  - **deep** (entrée dip −3.236% → cible +19.333% / stop −9.667%, p_fill 70%, n_eff≈77.0) : P(cible|rempli) **32%** · **EV/risk +0.140** (×p_fill ; si rempli +1.95% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→77% · +2.0%→61% · +3.0%→42% · +5.0%→25% · +8.0%→10%
- Range intraday médian 5.91% (p90 10.0%) · excursion haute méd. +2.54% / basse méd. −2.47%
- Profil de vol intra : ouverture 3.805% vs midi 1.225% vs clôture 1.455% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 72% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.019)_ ; drift intra méd. 0.304% ; recovery-V 36%
- **σ réalisé intraday** 3.832% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 40.5704 (VA 39.4716–40.8634 ; dernier close 39.59)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 79% · **stop −4.23%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. 0.28% · baisse 44% (gap-down >1% 35% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −2.79%) · haut méd +0.97% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.31% (p90 −3.26%) · haut méd +1.36% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.61% (p90 −3.96%) · haut méd +1.48% · range méd 3.64%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −4.97%) · haut méd +1.7% · range méd 4.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (119/159) · gap 42% · délai 0.0min · rebond 58% (71/119) (MFE +1.41%)
   - −1.0% : fill 30min 55% · séance 68% (111/159) · gap 35% · délai 0.0min · rebond 60% (64/111) (MFE +1.59%)
   - −1.5% : fill 30min 49% · séance 63% (100/159) · gap 22% · délai 0.1min · rebond 69% (62/100) (MFE +1.59%)
   - −2.0% : fill 30min 42% · séance 55% (88/159) · gap 16% · délai 0.7min · rebond 73% (57/88) (MFE +1.78%)
   - −3.0% : fill 30min 30% · séance 48% (75/159) · gap 9% · délai 8.4min · rebond 61% (45/75) (MFE +1.8%)
   - −4.0% : fill 30min 16% · séance 36% (55/159) · gap 4% · délai 39.6min · rebond 76% (36/55) (MFE +1.75%)
   - −5.0% : fill 30min 12% · séance 26% (44/159) · gap 2% · délai 48.0min · rebond 79% (32/44) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.81%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.98%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.78% (p90 −2.8%) → stop au-delà de −2.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=901 jambes) : jambe baissière méd −1.2% (p90 −2.87%) · ~11.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 97% (67/69) · rebond 48% (33/67)
      · −2.0% : fill 92% (63/69) · rebond 68% (37/63)
      · −3.0% : fill 85% (57/69) · rebond 58% (32/57)
      · −4.0% : fill 64% (43/69) · rebond 76% (28/43)
      · −5.0% : fill 47% (35/69) · rebond 78% (25/35)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 88% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 39% (31/77) · rebond 76% (20/31)
      · −2.0% : fill 25% (19/77) · rebond 84% (16/19)
      · −3.0% : fill 17% (15/77) · rebond 70% (10/15)
      · −4.0% : fill 12% (10/77) · rebond 71% (6/10)
      · −5.0% : fill 11% (9/77) · rebond 84% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 64% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:47** → P(séance verte=clôture>ouverture) 80% si début vert vs 9% si rouge (base 46% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=87) : tient le vert **80%** · continue >prix actuel 47% ; creux résiduel méd -1.36% (q20 -3.09%) → **SL/trailing à −3.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.76% / q75 +2.98% → **scale +1.76% / runner +2.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **9%** (continue à baisser 48%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.6%** (au-delà de la MAE q10 -4.6%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.2% .. +4.47%] · haut q95 +5.91% · bas q05 -4.5%
   - 60min (n=160) : retour [-4.44% .. +5.29%] · haut q95 +6.52% · bas q05 -5.33%
   - 2h (n=160) : retour [-4.69% .. +6.64%] · haut q95 +7.45% · bas q05 -5.85%
   - 4h (n=160) : retour [-5.2% .. +6.73%] · haut q95 +8.53% · bas q05 -6.7%
   - 6h (n=160) : retour [-5.63% .. +6.83%] · haut q95 +9.25% · bas q05 -6.91%
   - session (n=160) : retour [-6.78% .. +7.51%] · haut q95 +9.37% · bas q05 -7.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.61%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.9  _(neutre)_
- **ADX** : 27.0  _(tendance etablie)_
- **MACD** : hist 0.087  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 22.0%
- **ATR** : 2.38 (64.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.066  _(accumulation)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 52.2  _(transition)_
- **MA** : MA20 39.41 · MA50 35.73 · MA200 31.86  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +14.8% · MA200 +28.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (852063 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
