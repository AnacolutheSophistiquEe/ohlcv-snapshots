# SMCI

**Generated** : 2026-09-09T00:37:20.660631+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $40.26  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $40.26 (+1.2% vs entrée) · entrée $39.79 · stop $37.57 · T1 $42.28 · R/R 1.12  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.198 _(réel 5 s)_ (GBM 0.04) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -6.5 % ≠ (strike 37.0 − spot 40.26)/spot = -8.1 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 3554 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $39.32–$40.26 (mid $39.79)
- Spot actuel : $40.26 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $37.57 (stop swing_plan-based (-6.68%))
- Targets : T1 $42.28 · R/R 1.12 | T2 $44.77 · R/R 2.24 | T3 $47.26 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $37.57


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.68 %)** : le gap seul le franchit 1.756 % des séances (22 fois sur 1253).
   - exécution **4.708 pt plus bas** dans le cas TYPIQUE (médiane), 17.422 au p90, **22.371 au pire**
   - perte réelle **13.549 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 6.68 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.1206 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.765 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2639** [0.2025 ; 0.3331] _(largeur 13.1 pt, n_eff 173.1)_
   - swing : **0.4955** [0.443 ; 0.5481] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4314** [0.3799 ; 0.484] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.2 pt), swing (32.3 pt), deep (32.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.75 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.19 % contre 7.20 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.05 % si l'on extrapolait par √5 _(rapport 1.04 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5419** (β de hausse 1.2371, asymétrie 1.2464) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.942× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 35.8121 sur atr_grid (2.0 ATR, 11.037 %) — p(stop avant cible) 0.3814 [0.33 ; 0.43], R/R 1.032, perte reelle 16.875 % (gap inclus), CVaR 11.098 %, EV -0.8503 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.35 ATR (stop 4.406 %) — p(stop avant cible) 0.7231 [0.67 ; 0.77], R/R 1.921, perte reelle 9.064 % (gap inclus), EV -2.8023 % — **REFUSE**
      - refuse : p_stop_first 0.723, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.35 ATR du spot — compartiment <1, mesure a 49.4 % de casse (IC clusterise [0.461 ; 0.528] sur 1205 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.80 %) : P(cible) 18.9 % x 17.41 % + P(rien) 8.7 % x 5.17 % ne couvrent pas P(stop) 72.3 % x 9.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.277 %) — p(stop avant cible) 0.5001 [0.45 ; 0.55], R/R 1.232, perte reelle 14.137 % (gap inclus), EV -1.848 % — **REFUSE**
      - refuse : p_stop_first 0.500, borne haute 0.553 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.85 %) : P(cible) 26.2 % x 17.41 % + P(rien) 23.8 % x 2.80 % ne couvrent pas P(stop) 50.0 % x 14.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.28 ATR (stop 15.049 %) — p(stop avant cible) 0.2393 [0.20 ; 0.29], R/R 0.744, perte reelle 23.404 % (gap inclus), EV -0.5045 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 29.7 % x 17.41 % + P(rien) 46.4 % x -0.17 % ne couvrent pas P(stop) 23.9 % x 23.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.65 ATR (stop 33.619 %) — p(stop avant cible) 0.0738 [0.05 ; 0.10], R/R 0.518, perte reelle 33.619 % (gap inclus), EV 1.0123 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.62 % > budget 12.00 %
   - 🔴 support a 6.68 ATR (stop 39.333 %) — p(stop avant cible) 0.017 [0.01 ; 0.03], R/R 0.443, perte reelle 39.333 % (gap inclus), EV 1.1505 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.33 % > budget 12.00 %
      - ⚠ support DETECTE a 6.63 ATR du spot — compartiment >=6, mesure a 46.2 % de casse (IC clusterise [0.333 ; 0.612] sur 52 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🔴 grid_snapped a 0.35 ATR (stop 3.606 %) — p(stop avant cible) 0.764 [0.72 ; 0.81], R/R 2.32, perte reelle 7.507 % (gap inclus), EV -2.4483 % — **REFUSE**
      - refuse : p_stop_first 0.764, borne haute 0.806 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 16.9 % x 17.41 % + P(rien) 6.7 % x 5.21 % ne couvrent pas P(stop) 76.4 % x 7.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.518 %) — p(stop avant cible) 0.6729 [0.62 ; 0.72], R/R 1.527, perte reelle 11.406 % (gap inclus), EV -3.5019 % — **REFUSE**
      - refuse : p_stop_first 0.673, borne haute 0.721 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.50 %) : P(cible) 21.2 % x 17.41 % + P(rien) 11.5 % x 4.23 % ne couvrent pas P(stop) 67.3 % x 11.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 6.898 %) — p(stop avant cible) 0.5883 [0.54 ; 0.64], R/R 1.285, perte reelle 13.549 % (gap inclus), EV -3.1469 % — **REFUSE**
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.15 %) : P(cible) 23.9 % x 17.41 % + P(rien) 17.2 % x 3.81 % ne couvrent pas P(stop) 58.8 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.657 %) — p(stop avant cible) 0.4485 [0.40 ; 0.50], R/R 1.032, perte reelle 16.875 % (gap inclus), EV -2.2175 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 27.0 % x 17.41 % + P(rien) 28.2 % x 2.33 % ne couvrent pas P(stop) 44.9 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.037 %) — p(stop avant cible) 0.3814 [0.33 ; 0.43], R/R 1.032, perte reelle 16.875 % (gap inclus), EV -0.8503 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 28.6 % x 17.41 % + P(rien) 33.3 % x 1.84 % ne couvrent pas P(stop) 38.1 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.28 ATR (stop 14.248 %) — p(stop avant cible) 0.2546 [0.21 ; 0.30], R/R 0.836, perte reelle 20.821 % (gap inclus), EV -0.0575 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 29.7 % x 17.41 % + P(rien) 44.8 % x 0.15 % ne couvrent pas P(stop) 25.5 % x 20.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 16.555 %) — p(stop avant cible) 0.2059 [0.17 ; 0.25], R/R 0.744, perte reelle 23.404 % (gap inclus), EV 0.3869 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.58 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.314 %) — p(stop avant cible) 0.1523 [0.12 ; 0.19], R/R 0.648, perte reelle 26.856 % (gap inclus), EV 0.7781 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.33 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.074 %) — p(stop avant cible) 0.1335 [0.10 ; 0.17], R/R 0.648, perte reelle 26.856 % (gap inclus), EV 1.0243 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.09 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.833 %) — p(stop avant cible) 0.1045 [0.08 ; 0.14], R/R 0.623, perte reelle 27.955 % (gap inclus), EV 1.2904 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.84 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.592 %) — p(stop avant cible) 0.0916 [0.06 ; 0.13], R/R 0.599, perte reelle 29.051 % (gap inclus), EV 1.2734 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.59 % > budget 12.00 %
   - 🟢 grid_snapped a 5.65 ATR (stop 32.819 %) — p(stop avant cible) 0.0751 [0.05 ; 0.11], R/R 0.531, perte reelle 32.819 % (gap inclus), EV 1.0398 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.82 % > budget 12.00 %
   - 🔴 grid_snapped a 6.68 ATR (stop 38.533 %) — p(stop avant cible) 0.0272 [0.01 ; 0.05], R/R 0.452, perte reelle 38.533 % (gap inclus), EV 1.1327 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.388 %) — p(stop avant cible) 0.0092 [0.00 ; 0.02], R/R 0.421, perte reelle 41.388 % (gap inclus), EV 1.1709 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.39 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.147 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.394, perte reelle 44.147 % (gap inclus), EV 1.1736 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.15 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 40.255, ATR14 2.2214 (5.518 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 1.898 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.276 % | 40.1439 | 90.43 % | 93.15 % | 94.55 % | 95.05 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.552 % | 40.0329 | 82.18 % | 87.1 % | 89.1 % | 91.1 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.828 % | 39.9218 | 74.92 % | 81.96 % | 84.86 % | 88.07 % | 90.55 % | 93.53 % |
| 0.2 ATR | 1.104 % | 39.8107 | 67.98 % | 77.22 % | 80.42 % | 85.54 % | 89.13 % | 92.2 % |
| 0.25 ATR | 1.38 % | 39.6996 | 61.93 % | 72.68 % | 76.29 % | 82.2 % | 87.09 % | 90.45 % |
| 0.35 ATR | 1.931 % | 39.4775 | 49.24 % | 63.41 % | 69.63 % | 77.15 % | 82.72 % | 87.89 % |
| 0.5 ATR | 2.759 % | 39.1443 | 34.84 % | 49.9 % | 58.22 % | 68.66 % | 76.93 % | 83.68 % |
| 0.75 ATR | 4.139 % | 38.5889 | 17.32 % | 33.27 % | 42.89 % | 55.01 % | 66.46 % | 75.56 % |
| 1.0 ATR | 5.518 % | 38.0336 | 8.06 % | 21.77 % | 30.68 % | 43.68 % | 57.32 % | 68.58 % |
| 1.25 ATR | 6.898 % | 37.4782 | 3.83 % | 15.02 % | 22.6 % | 33.27 % | 48.27 % | 61.6 % |
| 1.5 ATR | 8.278 % | 36.9229 | 1.51 % | 9.68 % | 16.45 % | 26.19 % | 41.97 % | 55.13 % |
| 2.0 ATR | 11.037 % | 35.8121 | 0.3 % | 3.53 % | 8.38 % | 16.08 % | 30.08 % | 43.84 % |
| 2.5 ATR | 13.796 % | 34.7014 | 0.2 % | 1.51 % | 4.34 % | 9.81 % | 19.82 % | 32.03 % |
| 3.0 ATR | 16.555 % | 33.5907 | 0.2 % | 1.21 % | 2.62 % | 5.66 % | 14.23 % | 24.13 % |
| 4.0 ATR | 22.074 % | 31.3693 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 33.11 % | 26.9264 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.57 ATR | 0.76 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.63 ATR | 0.72 ATR | 0.95 ATR | 1.18 ATR | 1.36 ATR | 1.90 ATR | 2.42 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.56 ATR | 1.81 ATR | 2.48 ATR | 3.22 ATR |
| **10 s.** | 0.55 ATR | 1.20 ATR | 1.38 ATR | 1.88 ATR | 2.25 ATR | 2.49 ATR | 3.62 ATR | 4.90 ATR |
| **20 s.** | 0.77 ATR | 1.73 ATR | 1.95 ATR | 2.46 ATR | 2.94 ATR | 3.42 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.574–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.139 %, prix 38.5888), p(touche) 33.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.716–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.139 %, prix 38.5888), p(touche) 42.89 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.971–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.898 %, prix 37.4782), p(touche) 33.27 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.38–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.278 %, prix 36.9227), p(touche) 41.97 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.949–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (16.555 %, prix 33.5908), p(touche) 24.13 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.04 | EV/share : $0.089 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 23 % | T3 17 %
- Kelly (position) : f* 0.001 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 84.1 | bear 6.5 | side 9.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 604.0 (= 15 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.522% → cible +8.018% / stop −4.009%, p_fill 92%, n_eff≈37.1) : P(cible|rempli) **5%** · **EV/risk +0.045** (×p_fill ; si rempli +0.20% du capital)
  - **swing** (entrée dip −1.162% → cible +6.263% / stop −5.583%, p_fill 85%, n_eff≈34.0) : P(cible|rempli) **34%** · **EV/risk -0.198** (×p_fill ; si rempli -1.30% du capital)
  - **deep** (entrée dip −1.702% → cible +8.857% / stop −8.421%, p_fill 88%, n_eff≈33.8) : P(cible|rempli) **40%** · **EV/risk +0.024** (×p_fill ; si rempli +0.23% du capital)
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.6  _(momentum haussier)_
- **ADX** : 26.0  _(tendance etablie)_
- **MACD** : hist 0.019  _(bullish_recent)_
- **BB** : %B 0.87 · largeur 19.9%
- **ATR** : 2.22 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.072  _(accumulation)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 54.2  _(transition)_
- **MA** : MA20 37.47 · MA50 31.9 · MA200 31.4  _(prix > MA20)_
- **Dist MA** : MA20 +7.4% · MA50 +26.2% · MA200 +28.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759658 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
