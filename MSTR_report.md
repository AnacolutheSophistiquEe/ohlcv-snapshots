# MSTR

**Generated** : 2026-10-02T00:22:45.416240+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $160.49  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $160.49 (+1.3% vs entrée) · entrée $158.44 · stop $154.25 · T1 $166.84 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -0.4 % ≠ (strike 152.5 − spot 160.49)/spot = -5.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $157.38–$159.50 (mid $158.44)
- Spot actuel : $160.49 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $154.25 (R/R 2 (resserré, parité Claude) ; -2.64 % depuis l'entree)
- Targets : T1 $166.84 · R/R 2.0 | T2 $171.51 · R/R 3.12 | T3 $176.18 · R/R 4.23
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $154.25


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.62 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **2.779 pt plus bas** dans le cas TYPIQUE (médiane), 18.117 au p90, **18.752 au pire**
   - perte réelle **14.455 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 8.62 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0419 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.349 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4453** [0.3727 ; 0.5197] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4465** [0.3947 ; 0.4992] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4413** [0.3896 ; 0.494] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.01 %** | CVaR **-9.02 %** | vol 4.89 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.03 % contre 5.35 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3634** (β de hausse 1.8191, asymétrie 1.2992) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 148.5722 sur grid_snapped (0.98 ATR, 7.426 %) — p(stop avant cible) 0.5391 [0.49 ; 0.59], R/R 2.366, perte reelle 7.616 % (gap inclus), CVaR 9.365 %, EV 0.4565 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8705 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.539, borne haute 0.591 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 9.36 % > budget 5.91 %
- Budget de queue : **5.91 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.206 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 43.2 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.98 ATR (stop 8.415 %) — p(stop avant cible) 0.4893 [0.44 ; 0.54], R/R 2.1, perte reelle 8.581 % (gap inclus), EV 0.5516 % — **REFUSE**
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.01 % > budget 5.91 %
   - 🔴 support a 1.67 ATR (stop 12.436 %) — p(stop avant cible) 0.3329 [0.28 ; 0.38], R/R 1.434, perte reelle 12.563 % (gap inclus), EV 0.47 % — **REFUSE**
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.28 % > budget 5.91 %
      - ⚠ support DETECTE a 0.88 ATR du spot — compartiment <1, mesure a 46.7 % de casse (IC clusterise [0.436 ; 0.499] sur 1172 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.6 ATR (stop 17.838 %) — p(stop avant cible) 0.1868 [0.15 ; 0.23], R/R 0.994, perte reelle 18.126 % (gap inclus), EV 0.1594 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.91 % > budget 5.91 %
   - ⚪ swing_based a 4.18 ATR (stop 27.052 %) — p(stop avant cible) 0.0629 [0.04 ; 0.09], R/R 0.655, perte reelle 27.531 % (gap inclus), EV -0.0291 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.65 % > budget 5.91 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 23.9 % x 18.02 % + P(rien) 69.8 % x -3.74 % ne couvrent pas P(stop) 6.3 % x 27.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 4.72 ATR (stop 30.206 %) — p(stop avant cible) 0.0418 [0.02 ; 0.07], R/R 0.588, perte reelle 30.629 % (gap inclus), EV -0.015 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.01 % > budget 5.91 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 23.9 % x 18.02 % + P(rien) 71.9 % x -4.24 % ne couvrent pas P(stop) 4.2 % x 30.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.454 %) — p(stop avant cible) 0.937 [0.91 ; 0.96], R/R 12.149, perte reelle 1.483 % (gap inclus), EV -0.4956 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.937, borne haute 0.959 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 4.2 % x 18.02 % + P(rien) 2.1 % x 6.38 % ne couvrent pas P(stop) 93.7 % x 1.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.909 %) — p(stop avant cible) 0.8389 [0.80 ; 0.87], R/R 5.968, perte reelle 3.019 % (gap inclus), EV -0.4744 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.839, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 9.7 % x 18.02 % + P(rien) 6.5 % x 4.95 % ne couvrent pas P(stop) 83.9 % x 3.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.98 ATR (stop 7.426 %) — p(stop avant cible) 0.5391 [0.49 ; 0.59], R/R 2.366, perte reelle 7.616 % (gap inclus), EV 0.4565 % — **REFUSE**
      - refuse : p_stop_first 0.539, borne haute 0.591 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.36 % > budget 5.91 %
   - 🔴 grid_snapped a 1.67 ATR (stop 11.447 %) — p(stop avant cible) 0.3571 [0.31 ; 0.41], R/R 1.561, perte reelle 11.547 % (gap inclus), EV 0.6722 % — **REFUSE**
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.16 % > budget 5.91 %
   - 🟢 grid_snapped a 2.6 ATR (stop 16.849 %) — p(stop avant cible) 0.2035 [0.16 ; 0.25], R/R 1.054, perte reelle 17.09 % (gap inclus), EV 0.2185 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.83 % > budget 5.91 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.361 %) — p(stop avant cible) 0.1519 [0.12 ; 0.19], R/R 0.87, perte reelle 20.702 % (gap inclus), EV -0.008 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.40 % > budget 5.91 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 23.9 % x 18.02 % + P(rien) 60.9 % x -1.92 % ne couvrent pas P(stop) 15.2 % x 20.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 4.18 ATR (stop 26.063 %) — p(stop avant cible) 0.0736 [0.05 ; 0.10], R/R 0.682, perte reelle 26.434 % (gap inclus), EV 0.0002 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.61 % > budget 5.91 %
   - 🟢 grid_snapped a 4.72 ATR (stop 29.217 %) — p(stop avant cible) 0.0494 [0.03 ; 0.08], R/R 0.607, perte reelle 29.702 % (gap inclus), EV -0.0701 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.69 % > budget 5.91 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 23.9 % x 18.02 % + P(rien) 71.1 % x -4.10 % ne couvrent pas P(stop) 4.9 % x 29.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 31.996 %) — p(stop avant cible) 0.0283 [0.01 ; 0.05], R/R 0.554, perte reelle 32.511 % (gap inclus), EV 0.0247 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.26 % > budget 5.91 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.905 %) — p(stop avant cible) 0.0177 [0.01 ; 0.04], R/R 0.508, perte reelle 35.461 % (gap inclus), EV 0.0782 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.84 % > budget 5.91 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.813 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.471, perte reelle 38.261 % (gap inclus), EV 0.181 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.52 % > budget 5.91 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.722 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.437, perte reelle 41.232 % (gap inclus), EV 0.2178 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.78 % > budget 5.91 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.631 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.413, perte reelle 43.677 % (gap inclus), EV 0.2279 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.63 % > budget 5.91 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.54 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.387, perte reelle 46.54 % (gap inclus), EV 0.232 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.53 % > budget 5.91 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 160.49, ATR14 9.3364 (5.817 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.395 ATR = 2.298 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.291 % | 160.0232 | 93.96 % | 96.47 % | 96.97 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.582 % | 159.5564 | 88.12 % | 91.94 % | 93.44 % | 94.84 % | 96.65 % | 97.23 % |
| 0.15 ATR | 0.873 % | 159.0895 | 81.27 % | 87.1 % | 89.81 % | 91.91 % | 94.21 % | 95.48 % |
| 0.2 ATR | 1.163 % | 158.6227 | 73.72 % | 81.75 % | 85.07 % | 88.37 % | 91.57 % | 93.53 % |
| 0.25 ATR | 1.454 % | 158.1559 | 67.77 % | 77.92 % | 82.24 % | 86.25 % | 89.13 % | 91.89 % |
| 0.35 ATR | 2.036 % | 157.2223 | 54.98 % | 68.85 % | 75.38 % | 80.99 % | 85.67 % | 89.22 % |
| 0.5 ATR | 2.909 % | 155.8218 | 38.27 % | 55.34 % | 63.47 % | 71.39 % | 78.35 % | 84.39 % |
| 0.75 ATR | 4.363 % | 153.4877 | 19.44 % | 37.6 % | 46.92 % | 58.04 % | 67.78 % | 76.69 % |
| 1.0 ATR | 5.817 % | 151.1536 | 9.37 % | 25.1 % | 34.61 % | 46.11 % | 58.43 % | 69.61 % |
| 1.25 ATR | 7.272 % | 148.8195 | 4.13 % | 14.52 % | 24.72 % | 35.69 % | 49.59 % | 62.22 % |
| 1.5 ATR | 8.726 % | 146.4854 | 2.11 % | 8.67 % | 17.26 % | 28.82 % | 42.78 % | 56.67 % |
| 2.0 ATR | 11.635 % | 141.8171 | 0.2 % | 3.12 % | 7.37 % | 15.98 % | 30.89 % | 46.82 % |
| 2.5 ATR | 14.544 % | 137.1489 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.24 % | 37.37 % |
| 3.0 ATR | 17.452 % | 132.4807 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 23.27 % | 123.1443 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 34.905 % | 104.4714 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.24 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.03 ATR | 1.35 ATR | 1.65 ATR | 1.84 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.31 ATR | 2.59 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.81 ATR | 1.84 ATR | 2.10 ATR | 2.73 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.909 %, prix 155.8214), p(touche) 38.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.363 %, prix 153.4878), p(touche) 37.6 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.789–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.817 %, prix 151.1543), p(touche) 34.61 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.027–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.272 %, prix 148.8192), p(touche) 35.69 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.419–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.726 %, prix 146.4856), p(touche) 42.78 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.096–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.544 %, prix 137.1483), p(touche) 37.37 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 15.6 | bear 5.0 | side 79.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 571.0 (= 4 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.274% → cible +5.299% / stop −2.65%, p_fill 72%, n_eff≈78.9) : P(cible|rempli) **11%** · **EV/risk +0.006** (×p_fill ; si rempli +0.02% du capital)
  - **swing** (entrée dip −2.802% → cible +6.957% / stop −5.985%, p_fill 60%, n_eff≈71.3) : P(cible|rempli) **43%** · **EV/risk +0.027** (×p_fill ; si rempli +0.27% du capital)
  - **deep** (entrée dip −4.334% → cible +10.892% / stop −9.122%, p_fill 54%, n_eff≈61.0) : P(cible|rempli) **54%** · **EV/risk +0.135** (×p_fill ; si rempli +2.27% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→58% · +3.0%→41% · +5.0%→18% · +8.0%→9%
- Range intraday médian 5.35% (p90 9.67%) · excursion haute méd. +2.57% / basse méd. −2.28%
- Profil de vol intra : ouverture 3.339% vs midi 1.144% vs clôture 1.279% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑3%/↓0% ; spike-down 69% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. 0.349% ; recovery-V 28%
- **σ réalisé intraday** 3.51% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 56% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 154.2144 (VA 153.6559–154.7729 ; dernier close 153.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 79% · **stop −3.87%** sous le fill (sous le bruit) · cible +2.49% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. -0.03% · baisse 51% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.27%) · haut méd +0.84% · range méd 1.88%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −2.93%) · haut méd +1.23% · range méd 2.59%
- Excursion ouverture 30min (n=160) : bas méd −1.26% (p90 −3.24%) · haut méd +1.45% · range méd 3.04%
- Excursion ouverture 60min (n=160) : bas méd −1.53% (p90 −3.84%) · haut méd +1.83% · range méd 3.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 153.09 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (118/159) · gap 43% · délai 0.0min · rebond 44% (55/118) (MFE +0.56%)
   - −1.0% : fill 30min 55% · séance 68% (112/159) · gap 36% · délai 0.0min · rebond 46% (59/112) (MFE +0.85%)
   - −1.5% : fill 30min 46% · séance 64% (105/159) · gap 29% · délai 0.0min · rebond 52% (58/105) (MFE +1.13%)
   - −2.0% : fill 30min 39% · séance 57% (94/159) · gap 25% · délai 0.0min · rebond 60% (56/94) (MFE +1.28%)
   - −3.0% : fill 30min 27% · séance 44% (75/159) · gap 15% · délai 1.2min · rebond 59% (43/75) (MFE +1.57%)
   - −4.0% : fill 30min 20% · séance 33% (60/159) · gap 4% · délai 11.4min · rebond 76% (42/60) (MFE +1.92%)
   - −5.0% : fill 30min 14% · séance 23% (42/159) · gap 3% · délai 17.2min · rebond 79% (32/42) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.19%) → stop au-delà de −1.65% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.23%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.28%) → stop au-delà de −1.82% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=935 jambes) : jambe baissière méd −1.11% (p90 −2.66%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 96% (75/76) · rebond 41% (33/75)
      · −2.0% : fill 91% (69/76) · rebond 60% (40/69)
      · −3.0% : fill 74% (60/76) · rebond 56% (34/60)
      · −4.0% : fill 63% (51/76) · rebond 76% (36/51)
      · −5.0% : fill 46% (38/76) · rebond 81% (30/38)
   - **flat** (18 séances) :
      · −1.0% : fill 69% (13/18) · rebond 68% (10/13)
      · −2.0% : fill 52% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 43% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 20% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 6% (2/18) · rebond 0% (0/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 36% (24/65) · rebond 47% (16/24)
      · −2.0% : fill 21% (16/65) · rebond 63% (11/16)
      · −3.0% : fill 10% (8/65) · rebond 68% (5/8)
      · −4.0% : fill 5% (5/65) · rebond 61% (3/5)
      · −5.0% : fill 3% (2/65) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 57% si les 15 1res min sont vertes (84 cas) · 31% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 73% si début vert vs 9% si rouge (base 45% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=89) : tient le vert **73%** · continue >prix actuel 51% ; creux résiduel méd -1.31% (q20 -2.96%) → **SL/trailing à −2.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.01% / q75 +2.95% → **scale +2.01% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **9%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.69%** (au-delà de la MAE q10 -4.69%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.25% .. +4.02%] · haut q95 +4.48% · bas q05 -3.68%
   - 60min (n=160) : retour [-4.14% .. +5.6%] · haut q95 +5.94% · bas q05 -4.8%
   - 2h (n=160) : retour [-4.62% .. +8.55%] · haut q95 +8.82% · bas q05 -5.67%
   - 4h (n=160) : retour [-4.86% .. +9.48%] · haut q95 +10.36% · bas q05 -6.01%
   - 6h (n=160) : retour [-5.08% .. +8.59%] · haut q95 +11.49% · bas q05 -6.11%
   - session (n=160) : retour [-5.0% .. +8.31%] · haut q95 +11.49% · bas q05 -6.34%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0.6% / strong 5.6%) · base = 10 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **43%**. Lecture précoce 30 min : signature présente → 23% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.77% (p75 1.13% / p90 2.71%) · ~4.0 replis/séance, durée méd 34.08 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 20.0 min, n=37)
   - −1.0% → **60%** (reprise méd 31.69 min, n=14)
   - −1.5% → **43%** (reprise méd 42.45 min, n=10)
   - −2.0% → **19%** (reprise méd None min, n=7)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.71%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +9.11% (q75 +12.7% / q95 +13.17%), MFE méd +11.91% / q90 +13.21%
   - Échelle scale-out : +11.91% (33%) / +13.03% (33%) / +13.21% (34%)
- **DÉSARMER** : repli > **−2.71%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 182.05 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.21% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 84% du temps (retour médian dernière heure +0.85%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.78 · part idiosyncratique 0.22
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.0  _(momentum haussier)_
- **ADX** : 39.1  _(tendance etablie)_
- **MACD** : hist -0.27  _(bearish_recent)_
- **BB** : %B 0.74 · largeur 38.9%
- **ATR** : 9.34 (38.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.111  _(accumulation)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 38.1  _(marche directionnel)_
- **MA** : MA20 146.95 · MA50 122.28 · MA200 136.0  _(prix > MA20)_
- **Dist MA** : MA20 +9.2% · MA50 +31.2% · MA200 +18.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (844196 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
