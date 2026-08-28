# SOI

**Generated** : 2026-08-28T00:10:54.634514+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €110.85  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €110.85 (+0.8% vs entrée) · entrée €109.95 · stop €106.06 · T1 €117.75 · R/R 2.01  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.179 _(réel 5 s)_ (GBM 0.043) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.54% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 135 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €109.34–€110.57 (mid €109.95)
- Spot actuel : €110.85 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €106.06 (stop swing_plan-based (-10.4%))
- Targets : T1 €117.75 · R/R 2.01 | T2 €118.43 · R/R 2.18 | T3 €119.10 · R/R 2.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €106.06


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.4 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **8.319 pt plus bas** dans le cas TYPIQUE (médiane), 16.779 au p90, **18.894 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.4 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0259 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3719** [0.3025 ; 0.4455] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.3551** [0.306 ; 0.4066] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.4145** [0.3635 ; 0.467] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.2 pt), swing (33.6 pt), deep (32.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.47 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.41 % contre 7.71 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.22 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1322** (β de hausse 1.6203, asymétrie 0.6988) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.047× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 98.8937 sur atr_grid (1.75 ATR, 10.786 %) — p(stop avant cible) 0.4253 [0.37 ; 0.48], R/R 0.961, perte reelle 21.456 % (gap inclus), CVaR 10.811 %, EV -3.4475 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.78 ATR (stop 8.136 %) — p(stop avant cible) 0.5439 [0.49 ; 0.60], R/R 1.346, perte reelle 15.318 % (gap inclus), EV -3.0058 % — **REFUSE**
      - refuse : p_stop_first 0.544, borne haute 0.596 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 46.7 % de casse (IC clusterise [0.437 ; 0.496] sur 1206 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.01 %) : P(cible) 20.9 % x 20.61 % + P(rien) 24.8 % x 4.14 % ne couvrent pas P(stop) 54.4 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.27 ATR (stop 29.643 %) — p(stop avant cible) 0.0333 [0.02 ; 0.06], R/R 0.695, perte reelle 29.643 % (gap inclus), EV 2.0092 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.64 % > budget 12.00 %
   - 🟢 support a 6.69 ATR (stop 44.528 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.463, perte reelle 44.528 % (gap inclus), EV 1.9936 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.53 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.541 %) — p(stop avant cible) 0.8724 [0.83 ; 0.90], R/R 6.247, perte reelle 3.3 % (gap inclus), EV -0.7553 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 6.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.872, borne haute 0.904 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 8.3 % x 20.61 % + P(rien) 4.5 % x 9.33 % ne couvrent pas P(stop) 87.2 % x 3.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.082 %) — p(stop avant cible) 0.7732 [0.73 ; 0.81], R/R 3.591, perte reelle 5.74 % (gap inclus), EV -0.9028 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.773, borne haute 0.815 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 13.5 % x 20.61 % + P(rien) 9.2 % x 8.16 % ne couvrent pas P(stop) 77.3 % x 5.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.78 ATR (stop 6.675 %) — p(stop avant cible) 0.6002 [0.55 ; 0.65], R/R 1.456, perte reelle 14.154 % (gap inclus), EV -3.2801 % — **REFUSE**
      - refuse : p_stop_first 0.600, borne haute 0.651 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 19.8 % x 20.61 % + P(rien) 20.2 % x 5.63 % ne couvrent pas P(stop) 60.0 % x 14.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 9.245 %) — p(stop avant cible) 0.4942 [0.44 ; 0.55], R/R 1.118, perte reelle 18.446 % (gap inclus), EV -3.4569 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.46 %) : P(cible) 23.0 % x 20.61 % + P(rien) 27.6 % x 3.31 % ne couvrent pas P(stop) 49.4 % x 18.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.786 %) — p(stop avant cible) 0.4253 [0.37 ; 0.48], R/R 0.961, perte reelle 21.456 % (gap inclus), EV -3.4475 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.45 %) : P(cible) 24.5 % x 20.61 % + P(rien) 33.0 % x 1.90 % ne couvrent pas P(stop) 42.5 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.327 %) — p(stop avant cible) 0.3748 [0.33 ; 0.43], R/R 0.961, perte reelle 21.456 % (gap inclus), EV -2.4533 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 25.5 % x 20.61 % + P(rien) 37.1 % x 0.92 % ne couvrent pas P(stop) 37.5 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 13.868 %) — p(stop avant cible) 0.3236 [0.28 ; 0.37], R/R 0.961, perte reelle 21.456 % (gap inclus), EV -1.495 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 26.0 % x 20.61 % + P(rien) 41.7 % x 0.23 % ne couvrent pas P(stop) 32.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 15.409 %) — p(stop avant cible) 0.2664 [0.22 ; 0.31], R/R 0.961, perte reelle 21.456 % (gap inclus), EV -0.5226 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 26.3 % x 20.61 % + P(rien) 47.0 % x -0.50 % ne couvrent pas P(stop) 26.6 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 16.949 %) — p(stop avant cible) 0.2209 [0.18 ; 0.27], R/R 0.859, perte reelle 24.006 % (gap inclus), EV -0.1069 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 27.6 % x 20.61 % + P(rien) 50.3 % x -0.99 % ne couvrent pas P(stop) 22.1 % x 24.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 18.49 %) — p(stop avant cible) 0.1896 [0.15 ; 0.23], R/R 0.859, perte reelle 24.006 % (gap inclus), EV 0.6365 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.572 %) — p(stop avant cible) 0.1119 [0.08 ; 0.15], R/R 0.704, perte reelle 29.294 % (gap inclus), EV 1.0849 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.58 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 24.654 %) — p(stop avant cible) 0.0623 [0.04 ; 0.09], R/R 0.704, perte reelle 29.294 % (gap inclus), EV 1.8139 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.66 % > budget 12.00 %
   - 🟢 grid_snapped a 4.27 ATR (stop 28.182 %) — p(stop avant cible) 0.0384 [0.02 ; 0.06], R/R 0.704, perte reelle 29.294 % (gap inclus), EV 1.9721 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.18 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.817 %) — p(stop avant cible) 0.0333 [0.02 ; 0.06], R/R 0.669, perte reelle 30.817 % (gap inclus), EV 1.9701 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.82 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.899 %) — p(stop avant cible) 0.0285 [0.01 ; 0.05], R/R 0.608, perte reelle 33.899 % (gap inclus), EV 1.9131 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.90 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.98 %) — p(stop avant cible) 0.0178 [0.01 ; 0.04], R/R 0.557, perte reelle 36.98 % (gap inclus), EV 1.9116 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.98 % > budget 12.00 %
   - 🟢 grid_snapped a 6.69 ATR (stop 43.067 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.479, perte reelle 43.067 % (gap inclus), EV 1.9936 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.07 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.226 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.446, perte reelle 46.226 % (gap inclus), EV 1.9936 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.23 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 49.307 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.418, perte reelle 49.307 % (gap inclus), EV 1.9936 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.31 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 110.85, ATR14 6.8321 (6.163 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.361 ATR = 2.225 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.308 % | 110.5084 | 91.08 % | 94.11 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.616 % | 110.1668 | 84.9 % | 89.99 % | 92.04 % | 94.59 % | 96.24 % | 97.4 % |
| 0.15 ATR | 0.925 % | 109.8252 | 77.94 % | 85.08 % | 87.92 % | 91.14 % | 93.77 % | 95.3 % |
| 0.2 ATR | 1.233 % | 109.4836 | 69.51 % | 80.08 % | 83.99 % | 88.39 % | 91.59 % | 93.41 % |
| 0.25 ATR | 1.541 % | 109.142 | 63.14 % | 76.35 % | 80.75 % | 86.71 % | 90.31 % | 92.81 % |
| 0.35 ATR | 2.157 % | 108.4587 | 51.08 % | 67.81 % | 73.77 % | 81.59 % | 86.05 % | 90.21 % |
| 0.5 ATR | 3.082 % | 107.4339 | 36.08 % | 55.64 % | 63.06 % | 73.72 % | 81.4 % | 87.51 % |
| 0.75 ATR | 4.623 % | 105.7259 | 17.06 % | 35.72 % | 47.45 % | 59.35 % | 73.79 % | 81.42 % |
| 1.0 ATR | 6.163 % | 104.0179 | 8.33 % | 24.24 % | 34.48 % | 48.33 % | 65.58 % | 76.22 % |
| 1.25 ATR | 7.704 % | 102.3098 | 4.12 % | 15.8 % | 25.64 % | 38.09 % | 57.27 % | 70.53 % |
| 1.5 ATR | 9.245 % | 100.6018 | 2.35 % | 10.79 % | 18.86 % | 30.41 % | 49.36 % | 64.44 % |
| 2.0 ATR | 12.327 % | 97.1857 | 0.59 % | 4.71 % | 9.14 % | 18.5 % | 35.51 % | 54.15 % |
| 2.5 ATR | 15.409 % | 93.7696 | 0.29 % | 2.45 % | 4.81 % | 11.81 % | 24.63 % | 46.05 % |
| 3.0 ATR | 18.49 % | 90.3536 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 17.01 % | 38.06 % |
| 4.0 ATR | 24.654 % | 83.5214 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.79 % | 24.88 % |
| 6.0 ATR | 36.98 % | 69.8571 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.19 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.63 ATR | 0.81 ATR | 0.98 ATR | 1.13 ATR | 1.56 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.27 ATR | 1.46 ATR | 1.96 ATR | 2.48 ATR |
| **5 s.** | 0.48 ATR | 0.96 ATR | 1.08 ATR | 1.42 ATR | 1.73 ATR | 1.94 ATR | 2.69 ATR | 3.59 ATR |
| **10 s.** | 0.71 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.48 ATR | 2.80 ATR | 3.97 ATR | 5.79 ATR |
| **20 s.** | 1.05 ATR | 2.26 ATR | 2.57 ATR | 3.38 ATR | 3.99 ATR | 4.77 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.634–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.163 %, prix 104.0183), p(touche) 34.48 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.081–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.704 %, prix 102.3101), p(touche) 38.09 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.657–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.566–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.043 | EV/share : €0.168 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.121 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.8 | bear 16.9 | side 6.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 111.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.804% → cible +7.089% / stop −3.545%, p_fill 84%, n_eff≈34.5) : P(cible|rempli) **7%** · **EV/risk -0.179** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −1.776% → cible +17.56% / stop −8.78%, p_fill 77%, n_eff≈31.5) : P(cible|rempli) **16%** · **EV/risk +0.003** (×p_fill ; si rempli +0.04% du capital)
  - **deep** (entrée dip −2.746% → cible +23.144% / stop −11.572%, p_fill 73%, n_eff≈33.8) : P(cible|rempli) **26%** · **EV/risk -0.155** (×p_fill ; si rempli -2.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→65% · +3.0%→51% · +5.0%→34% · +8.0%→11%
- Range intraday médian 8.23% (p90 14.47%) · excursion haute méd. +3.37% / basse méd. −3.46%
- Profil de vol intra : ouverture 5.163% vs midi 1.446% vs clôture 2.296% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑0%/↓3% ; spike-down 76% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.078)_ ; drift intra méd. -0.684% ; recovery-V 32%
- **σ réalisé intraday** 4.759% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 53% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 111.478 (VA 110.49–111.934 ; dernier close 109.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 50% · rebond 84% · **stop −8.21%** sous le fill (sous le bruit) · cible +3.13% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. 0.5% · baisse 41% (gap-down >1% 27% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.1% (p90 −3.73%) · haut méd +0.89% · range méd 2.73%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −5.04%) · haut méd +1.24% · range méd 3.47%
- Excursion ouverture 30min (n=160) : bas méd −1.49% (p90 −5.35%) · haut méd +1.5% · range méd 3.83%
- Excursion ouverture 60min (n=160) : bas méd −1.7% (p90 −5.86%) · haut méd +1.58% · range méd 4.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 109.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 79% (127/159) · gap 36% · délai 0.1min · rebond 69% (88/127) (MFE +1.87%)
   - −1.0% : fill 30min 59% · séance 73% (115/159) · gap 27% · délai 0.2min · rebond 72% (84/115) (MFE +2.02%)
   - −1.5% : fill 30min 52% · séance 65% (106/159) · gap 23% · délai 0.2min · rebond 73% (78/106) (MFE +2.34%)
   - −2.0% : fill 30min 45% · séance 60% (95/159) · gap 19% · délai 0.4min · rebond 70% (73/95) (MFE +2.4%)
   - −3.0% : fill 30min 36% · séance 50% (80/159) · gap 11% · délai 1.5min · rebond 84% (69/80) (MFE +3.13%)
   - −4.0% : fill 30min 26% · séance 41% (65/159) · gap 6% · délai 11.4min · rebond 79% (55/65) (MFE +3.3%)
   - −5.0% : fill 30min 18% · séance 34% (48/159) · gap 2% · délai 26.8min · rebond 70% (38/48) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −3.58%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.9%) → stop au-delà de −2.14% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.37%) → stop au-delà de −1.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1359 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 97% (55/57) · rebond 64% (36/55)
      · −2.0% : fill 93% (52/57) · rebond 70% (40/52)
      · −3.0% : fill 84% (47/57) · rebond 80% (40/47)
      · −4.0% : fill 68% (38/57) · rebond 88% (35/38)
      · −5.0% : fill 58% (31/57) · rebond 77% (26/31)
   - **flat** (14 séances) :
      · −1.0% : fill 93% (11/14) · rebond 78% (9/11)
      · −2.0% : fill 73% (10/14) · rebond 79% (9/10)
      · −3.0% : fill 71% (9/14) · rebond 78% (8/9)
      · −4.0% : fill 57% (8/14) · rebond 56% (5/8)
      · −5.0% : fill 56% (7/14) · rebond 72% (6/7)
   - **gap-up** (88 séances) :
      · −1.0% : fill 55% (49/88) · rebond 80% (39/49)
      · −2.0% : fill 36% (33/88) · rebond 68% (24/33)
      · −3.0% : fill 23% (24/88) · rebond 96% (21/24)
      · −4.0% : fill 20% (19/88) · rebond 68% (15/19)
      · −5.0% : fill 14% (10/88) · rebond 48% (6/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 66% si les 15 1res min sont vertes (75 cas) · 30% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:08** → P(séance verte=clôture>ouverture) 76% si début vert vs 25% si rouge (base 48% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **76%** · continue >prix actuel 58% ; creux résiduel méd -2.31% (q20 -5.6%) → **SL/trailing à −5.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.43% / q75 +4.57% → **scale +2.43% / runner +4.57%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **25%** (continue à baisser 54%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.33%** (au-delà de la MAE q10 -7.33%), cible rebond +2.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.04% .. +6.39%] · haut q95 +7.84% · bas q05 -6.21%
   - 60min (n=160) : retour [-5.66% .. +6.76%] · haut q95 +8.11% · bas q05 -6.7%
   - 2h (n=160) : retour [-6.77% .. +6.49%] · haut q95 +11.63% · bas q05 -7.74%
   - 4h (n=160) : retour [-7.21% .. +9.21%] · haut q95 +12.35% · bas q05 -8.5%
   - 6h (n=160) : retour [-8.67% .. +10.05%] · haut q95 +12.88% · bas q05 -9.45%
   - session (n=160) : retour [-12.01% .. +12.42%] · haut q95 +14.53% · bas q05 -12.9%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.5  _(momentum baissier)_
- **ADX** : 14.5  _(pas de tendance nette)_
- **MACD** : hist -1.623  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 32.0%
- **ATR** : 6.83 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.235  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 44.2  _(transition)_
- **MA** : MA20 117.2 · MA50 110.67 · MA200 78.4  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 +0.2% · MA200 +41.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (854898 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
