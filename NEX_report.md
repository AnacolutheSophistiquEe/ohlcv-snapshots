# NEX

**Generated** : 2026-10-07T00:11:00.026947+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €133.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €133.00 (+0.9% vs entrée) · entrée €131.79 · stop €129.81 · T1 €133.67 · R/R 0.95  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -160 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €131.41–€132.16 (mid €131.79)
- Spot actuel : €133.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : €129.81 (plancher anti-bruit 5 s — stop EV-optimal −1.5% (first-passage 5 s réel) ; -1.50 % depuis l'entree)
- Targets : T1 €133.67 · R/R 0.95 | T2 €135.55 · R/R 1.9 | T3 €137.43 · R/R 2.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.81


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.44 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **2.728 pt plus bas** dans le cas TYPIQUE (médiane), 3.534 au p90, **4.156 au pire**
   - perte réelle **8.124 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 5.44 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0126 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3715** [0.3021 ; 0.4451] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4492** [0.3974 ; 0.5019] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.5106** [0.458 ; 0.563] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.1 pt), deep (26.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.52 %** | CVaR **-5.28 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 0.9999** (β de hausse 1.0901, asymétrie 0.9172) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 123.5893 sur atr_grid (2.5 ATR, 7.076 %) — p(stop avant cible) 0.2594 [0.22 ; 0.31], R/R 3.177, perte reelle 7.271 % (gap inclus), CVaR 8.085 %, EV 0.1751 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.958 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.76 ATR (stop 4.044 %) — p(stop avant cible) 0.5554 [0.50 ; 0.61], R/R 5.483, perte reelle 4.213 % (gap inclus), EV -0.2106 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.555, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.6 % x 23.10 % + P(rien) 43.8 % x 4.53 % ne couvrent pas P(stop) 55.5 % x 4.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.39 ATR (stop 5.834 %) — p(stop avant cible) 0.3749 [0.33 ; 0.43], R/R 3.81, perte reelle 6.063 % (gap inclus), EV -0.0621 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.6 % x 23.10 % + P(rien) 61.9 % x 3.34 % ne couvrent pas P(stop) 37.5 % x 6.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 6.71 ATR (stop 20.9 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 1.018, perte reelle 22.69 % (gap inclus), EV 0.4994 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.46 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.708 %) — p(stop avant cible) 0.9222 [0.89 ; 0.95], R/R 31.229, perte reelle 0.74 % (gap inclus), EV -0.0484 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 31.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.922, borne haute 0.947 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 0.3 % x 23.10 % + P(rien) 7.5 % x 7.53 % ne couvrent pas P(stop) 92.2 % x 0.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.415 %) — p(stop avant cible) 0.8289 [0.79 ; 0.87], R/R 15.591, perte reelle 1.482 % (gap inclus), EV -0.1637 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 15.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.829, borne haute 0.866 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.6 % x 23.10 % + P(rien) 16.5 % x 5.58 % ne couvrent pas P(stop) 82.9 % x 1.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.76 ATR (stop 2.994 %) — p(stop avant cible) 0.6598 [0.61 ; 0.71], R/R 7.448, perte reelle 3.102 % (gap inclus), EV -0.1738 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 7.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.660, borne haute 0.708 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.6 % x 23.10 % + P(rien) 33.4 % x 5.17 % ne couvrent pas P(stop) 66.0 % x 3.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.39 ATR (stop 4.784 %) — p(stop avant cible) 0.4675 [0.42 ; 0.52], R/R 4.634, perte reelle 4.986 % (gap inclus), EV -0.1028 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.6 % x 23.10 % + P(rien) 52.6 % x 3.96 % ne couvrent pas P(stop) 46.8 % x 4.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 6.368 %) — p(stop avant cible) 0.3188 [0.27 ; 0.37], R/R 3.523, perte reelle 6.558 % (gap inclus), EV 0.0426 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.5 ATR (stop 7.076 %) — p(stop avant cible) 0.2594 [0.22 ; 0.31], R/R 3.177, perte reelle 7.271 % (gap inclus), EV 0.1751 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.75 ATR (stop 7.783 %) — p(stop avant cible) 0.1995 [0.16 ; 0.24], R/R 2.893, perte reelle 7.985 % (gap inclus), EV 0.3742 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 8.491 %) — p(stop avant cible) 0.1797 [0.14 ; 0.22], R/R 2.674, perte reelle 8.639 % (gap inclus), EV 0.3308 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.906 %) — p(stop avant cible) 0.115 [0.08 ; 0.15], R/R 2.295, perte reelle 10.064 % (gap inclus), EV 0.3958 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 11.321 %) — p(stop avant cible) 0.0769 [0.05 ; 0.11], R/R 2.002, perte reelle 11.537 % (gap inclus), EV 0.4142 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 12.736 %) — p(stop avant cible) 0.0549 [0.03 ; 0.08], R/R 1.732, perte reelle 13.342 % (gap inclus), EV 0.3736 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.40 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 14.151 %) — p(stop avant cible) 0.0275 [0.01 ; 0.05], R/R 1.585, perte reelle 14.576 % (gap inclus), EV 0.4284 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.23 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 15.567 %) — p(stop avant cible) 0.017 [0.01 ; 0.03], R/R 1.43, perte reelle 16.154 % (gap inclus), EV 0.448 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.00 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.982 %) — p(stop avant cible) 0.0091 [0.00 ; 0.02], R/R 1.316, perte reelle 17.558 % (gap inclus), EV 0.4579 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.90 % > budget 12.00 %
   - 🟢 grid_snapped a 6.71 ATR (stop 19.85 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.116, perte reelle 20.693 % (gap inclus), EV 0.4965 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.642 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.972, perte reelle 23.762 % (gap inclus), EV 0.5011 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.40 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 133.0, ATR14 3.7643 (2.83 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 0.985 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.142 % | 132.8118 | 87.84 % | 91.56 % | 93.32 % | 95.18 % | 97.03 % | 97.9 % |
| 0.1 ATR | 0.283 % | 132.6236 | 81.96 % | 87.83 % | 90.47 % | 93.21 % | 95.65 % | 97.0 % |
| 0.15 ATR | 0.425 % | 132.4354 | 75.39 % | 83.61 % | 87.03 % | 90.26 % | 94.16 % | 95.7 % |
| 0.2 ATR | 0.566 % | 132.2471 | 68.82 % | 78.41 % | 83.3 % | 88.29 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.708 % | 132.0589 | 62.16 % | 73.6 % | 79.17 % | 85.14 % | 90.7 % | 93.81 % |
| 0.35 ATR | 0.991 % | 131.6825 | 49.71 % | 64.18 % | 71.71 % | 78.84 % | 86.65 % | 91.61 % |
| 0.5 ATR | 1.415 % | 131.1179 | 34.61 % | 52.4 % | 61.3 % | 70.77 % | 80.22 % | 87.41 % |
| 0.75 ATR | 2.123 % | 130.1768 | 20.39 % | 36.21 % | 47.05 % | 58.66 % | 70.23 % | 80.92 % |
| 1.0 ATR | 2.83 % | 129.2357 | 10.69 % | 24.14 % | 34.48 % | 48.33 % | 61.62 % | 74.23 % |
| 1.25 ATR | 3.538 % | 128.2946 | 4.8 % | 16.0 % | 24.85 % | 39.47 % | 54.4 % | 67.83 % |
| 1.5 ATR | 4.245 % | 127.3536 | 2.45 % | 11.19 % | 18.66 % | 30.81 % | 46.88 % | 60.34 % |
| 2.0 ATR | 5.661 % | 125.4714 | 0.88 % | 5.3 % | 10.12 % | 19.59 % | 35.11 % | 50.55 % |
| 2.5 ATR | 7.076 % | 123.5893 | 0.49 % | 2.65 % | 5.6 % | 11.52 % | 24.33 % | 38.66 % |
| 3.0 ATR | 8.491 % | 121.7071 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.51 % | 30.27 % |
| 4.0 ATR | 11.321 % | 117.9429 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.88 % |
| 6.0 ATR | 16.982 % | 110.4143 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.60 ATR | 2.06 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.45 ATR | 2.01 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.09 ATR | 1.44 ATR | 1.76 ATR | 1.98 ATR | 2.67 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.10 ATR | 2.47 ATR | 2.82 ATR | 3.75 ATR | 4.82 ATR |
| **20 s.** | 0.97 ATR | 2.02 ATR | 2.23 ATR | 2.84 ATR | 3.42 ATR | 3.83 ATR | 5.17 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (74.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.123 %, prix 130.1764), p(touche) 36.21 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.791–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.83 %, prix 129.2361), p(touche) 34.48 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.094–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.538 %, prix 128.2945), p(touche) 39.47 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.58–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.661 %, prix 125.4709), p(touche) 35.11 % (en stress 99.02 %)  ✅ optimum identifie (69.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.233–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.076 %, prix 123.5889), p(touche) 38.66 % (en stress 98.02 %)  ✅ optimum identifie (70.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.122 | EV/share : €-0.240 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 14 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.4 | bear 48.1 | side 43.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 133.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.914% → cible +1.428% / stop −1.5%, p_fill 59%, n_eff≈63.8) : P(cible|rempli) **24%** · **EV/risk -0.205** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −2.005% → cible +7.011% / stop −3.505%, p_fill 50%, n_eff≈58.0) : P(cible|rempli) **10%** · **EV/risk -0.071** (×p_fill ; si rempli -0.50% du capital)
  - **deep** (entrée dip −3.105% → cible +8.221% / stop −4.381%, p_fill 47%, n_eff≈52.7) : P(cible|rempli) **20%** · **EV/risk -0.009** (×p_fill ; si rempli -0.08% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→57% · +2.0%→28% · +3.0%→12% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.73% (p90 4.75%) · excursion haute méd. +1.13% / basse méd. −1.13%
- Profil de vol intra : ouverture 1.673% vs midi 0.529% vs clôture 0.71% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -0.332% ; recovery-V 10%
- **σ réalisé intraday** 1.991% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 71% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 136.2225 (VA 135.7475–137.0775 ; dernier close 136.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 25% · rebond 31% · **stop −2.1%** sous le fill (sous le bruit) · cible +0.53% · R/R 0.25 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 25% (gap-down >1% 3% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.34% (p90 −1.71%) · haut méd +0.28% · range méd 0.92%
- Excursion ouverture 15min (n=160) : bas méd −0.45% (p90 −1.95%) · haut méd +0.44% · range méd 1.27%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.08%) · haut méd +0.6% · range méd 1.4%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.28%) · haut méd +0.64% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 38% · séance 57% (88/159) · gap 9% · délai 3.9min · rebond 41% (38/88) (MFE +0.64%)
   - −1.0% : fill 30min 20% · séance 46% (69/159) · gap 3% · délai 51.9min · rebond 35% (27/69) (MFE +0.58%)
   - −1.5% : fill 30min 12% · séance 36% (54/159) · gap 0% · délai 62.0min · rebond 31% (19/54) (MFE +0.58%)
   - −2.0% : fill 30min 7% · séance 25% (39/159) · gap 0% · délai 111.9min · rebond 31% (15/39) (MFE +0.53%)
   - −3.0% : fill 30min 4% · séance 14% (23/159) · gap 0% · délai 268.3min · rebond 37% (10/23) (MFE +0.59%)
   - −4.0% : fill 30min 2% · séance 5% (10/159) · gap 0% · délai 161.7min · rebond 8% (3/10) (MFE +0.38%)
   - −5.0% : fill 30min 0% · séance 3% (4/159) · gap 0% · délai 260.4min · rebond 24% (2/4) (MFE +0.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.99%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.81%) → stop au-delà de −0.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.78%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.01% (p90 −2.27%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 77% (17/22) · rebond 27% (6/17)
      · −2.0% : fill 61% (12/22) · rebond 12% (2/12)
      · −3.0% : fill 43% (9/22) · rebond 15% (3/9)
      · −4.0% : fill 26% (6/22) · rebond 4% (1/6)
      · −5.0% : fill 20% (3/22) · rebond 20% (1/3)
   - **flat** (36 séances) :
      · −1.0% : fill 54% (21/36) · rebond 27% (7/21)
      · −2.0% : fill 25% (12/36) · rebond 33% (5/12)
      · −3.0% : fill 16% (8/36) · rebond 32% (3/8)
      · −4.0% : fill 5% (3/36) · rebond 8% (1/3)
      · −5.0% : fill 0% (1/36) · rebond 100% (1/1)
   - **gap-up** (101 séances) :
      · −1.0% : fill 35% (31/101) · rebond 44% (14/31)
      · −2.0% : fill 18% (15/101) · rebond 45% (8/15)
      · −3.0% : fill 6% (6/101) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/101) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/101) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 65% si les 15 1res min sont vertes (85 cas) · 22% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **20min** → P(séance verte=clôture>ouverture) 69% si début vert vs 23% si rouge (base 46% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 242min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **69%** · continue >prix actuel 58% ; creux résiduel méd -0.98% (q20 -1.84%) → **SL/trailing à −1.84%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.1% / q75 +1.84% → **scale +1.1% / runner +1.84%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **23%** (continue à baisser 63%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.05%** (au-delà de la MAE q10 -3.05%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.96% .. +1.64%] · haut q95 +2.01% · bas q05 -2.58%
   - 60min (n=160) : retour [-2.59% .. +2.13%] · haut q95 +2.44% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.07% .. +2.15%] · haut q95 +2.67% · bas q05 -3.66%
   - 4h (n=160) : retour [-2.91% .. +2.47%] · haut q95 +3.05% · bas q05 -3.75%
   - 6h (n=160) : retour [-3.6% .. +3.4%] · haut q95 +3.53% · bas q05 -4.13%
   - session (n=160) : retour [-3.38% .. +2.74%] · haut q95 +3.86% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.48 · part idiosyncratique 0.52
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.9  _(momentum baissier)_
- **ADX** : 10.6  _(pas de tendance nette)_
- **MACD** : hist -0.407  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 10.6%
- **ATR** : 3.76 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.226  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 52.7  _(transition)_
- **MA** : MA20 136.37 · MA50 137.5 · MA200 135.61  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 -3.3% · MA200 -1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (523581 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
