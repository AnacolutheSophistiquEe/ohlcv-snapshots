# RGTI

**Generated** : 2026-08-27T00:31:15.476548+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.94  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $15.94 (+1.5% vs entrée) · entrée $15.71 · stop $15.37 · T1 $16.30 · R/R 1.74  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk -0.039 _(réel 5 s)_ (GBM 0.288) · ¼-Kelly 0.043 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.16% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.60–$15.81 (mid $15.71)
- Spot actuel : $15.94 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $15.37 (stop swing_plan-based (-10.31%))
- Targets : T1 $16.30 · R/R 1.74 | T2 $16.77 · R/R 3.12 | T3 $17.23 · R/R 4.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.37


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.31 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **3.325 pt plus bas** dans le cas TYPIQUE (médiane), 8.937 au p90, **20.903 au pire**
   - perte réelle **15.002 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 10.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0374 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.085 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5409** [0.4665 ; 0.6139] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4694** [0.4172 ; 0.5221] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5167** [0.4641 ; 0.5691] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.8 pt), swing (37.1 pt), deep (34.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.86 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 15.31 % contre 6.49 % aujourd'hui, rapport 2.36)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8198** (β de hausse 1.9982, asymétrie 0.9107) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.618× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 14.0816 sur support (1.3 ATR, 11.659 %) — p(stop avant cible) 0.5398 [0.49 ; 0.59], R/R 1.059, perte reelle 16.825 % (gap inclus), CVaR 11.688 %, EV -3.3028 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.076 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.540, borne haute 0.592 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 24 des 24 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 55.6 % de la queue et il ne reste que -172.39 EUR a partager. Prix du risque -0.087 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.44 ATR (stop 5.578 %) — p(stop avant cible) 0.7479 [0.70 ; 0.79], R/R 1.882, perte reelle 9.47 % (gap inclus), EV -2.9481 % — **REFUSE**
      - refuse : p_stop_first 0.748, borne haute 0.791 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.95 %) : P(cible) 22.6 % x 17.82 % + P(rien) 2.7 % x 4.37 % ne couvrent pas P(stop) 74.8 % x 9.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 0.93 ATR (stop 9.018 %) — p(stop avant cible) 0.6353 [0.58 ; 0.68], R/R 1.298, perte reelle 13.724 % (gap inclus), EV -3.3251 % — **REFUSE**
      - refuse : p_stop_first 0.635, borne haute 0.685 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.33 %) : P(cible) 29.4 % x 17.82 % + P(rien) 7.1 % x 2.21 % ne couvrent pas P(stop) 63.5 % x 13.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.3 ATR (stop 11.659 %) — p(stop avant cible) 0.5398 [0.49 ; 0.59], R/R 1.059, perte reelle 16.825 % (gap inclus), EV -3.3028 % — **REFUSE**
      - refuse : p_stop_first 0.540, borne haute 0.592 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.83 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.451 ; 0.510] sur 1199 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.30 %) : P(cible) 32.5 % x 17.82 % + P(rien) 13.6 % x -0.03 % ne couvrent pas P(stop) 54.0 % x 16.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.02 ATR (stop 23.829 %) — p(stop avant cible) 0.1312 [0.10 ; 0.17], R/R 0.571, perte reelle 31.213 % (gap inclus), EV -0.3598 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 38.4 % x 17.82 % + P(rien) 48.4 % x -6.43 % ne couvrent pas P(stop) 13.1 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.165 %) — p(stop avant cible) 0.4355 [0.38 ; 0.49], R/R 0.909, perte reelle 19.597 % (gap inclus), EV -2.4841 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.48 %) : P(cible) 35.9 % x 17.82 % + P(rien) 20.6 % x -1.65 % ne couvrent pas P(stop) 43.5 % x 19.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 15.936 %) — p(stop avant cible) 0.356 [0.31 ; 0.41], R/R 0.725, perte reelle 24.565 % (gap inclus), EV -3.0089 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.01 %) : P(cible) 36.6 % x 17.82 % + P(rien) 27.8 % x -2.80 % ne couvrent pas P(stop) 35.6 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 17.706 %) — p(stop avant cible) 0.2941 [0.25 ; 0.34], R/R 0.725, perte reelle 24.565 % (gap inclus), EV -1.7929 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.79 %) : P(cible) 37.6 % x 17.82 % + P(rien) 33.0 % x -3.83 % ne couvrent pas P(stop) 29.4 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 19.477 %) — p(stop avant cible) 0.2535 [0.21 ; 0.30], R/R 0.571, perte reelle 31.213 % (gap inclus), EV -2.6361 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.64 %) : P(cible) 38.2 % x 17.82 % + P(rien) 36.5 % x -4.19 % ne couvrent pas P(stop) 25.4 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.789 %) — p(stop avant cible) 0.1208 [0.09 ; 0.16], R/R 0.571, perte reelle 31.213 % (gap inclus), EV -0.0798 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 38.8 % x 17.82 % + P(rien) 49.1 % x -6.58 % ne couvrent pas P(stop) 12.1 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 28.33 %) — p(stop avant cible) 0.0745 [0.05 ; 0.11], R/R 0.571, perte reelle 31.213 % (gap inclus), EV 0.5376 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.33 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 31.872 %) — p(stop avant cible) 0.0481 [0.03 ; 0.07], R/R 0.559, perte reelle 31.872 % (gap inclus), EV 0.6988 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 35.413 %) — p(stop avant cible) 0.0286 [0.01 ; 0.05], R/R 0.503, perte reelle 35.413 % (gap inclus), EV 0.7891 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.41 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 38.954 %) — p(stop avant cible) 0.0139 [0.01 ; 0.03], R/R 0.457, perte reelle 38.954 % (gap inclus), EV 0.8368 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.95 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.496 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.419, perte reelle 42.496 % (gap inclus), EV 0.8958 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.50 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.037 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.387, perte reelle 46.037 % (gap inclus), EV 0.8803 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.04 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 49.578 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.359, perte reelle 49.578 % (gap inclus), EV 0.8816 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.58 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.119 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.335, perte reelle 53.119 % (gap inclus), EV 0.9075 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.12 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 56.661 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.314, perte reelle 56.661 % (gap inclus), EV 0.9051 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.66 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.94, ATR14 1.129 (7.083 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.41 ATR = 2.904 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.354 % | 15.8836 | 92.25 % | 94.56 % | 95.66 % | 97.07 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.708 % | 15.8271 | 86.51 % | 91.23 % | 92.43 % | 94.94 % | 95.83 % | 97.54 % |
| 0.15 ATR | 1.062 % | 15.7707 | 81.07 % | 87.5 % | 89.1 % | 92.01 % | 93.9 % | 96.2 % |
| 0.2 ATR | 1.417 % | 15.7142 | 74.62 % | 82.96 % | 85.67 % | 88.88 % | 91.46 % | 94.66 % |
| 0.25 ATR | 1.771 % | 15.6578 | 68.58 % | 78.73 % | 81.84 % | 85.84 % | 88.82 % | 92.71 % |
| 0.35 ATR | 2.479 % | 15.5449 | 55.99 % | 68.45 % | 74.07 % | 79.78 % | 84.45 % | 89.84 % |
| 0.5 ATR | 3.541 % | 15.3755 | 40.99 % | 56.65 % | 64.68 % | 71.89 % | 79.27 % | 85.83 % |
| 0.75 ATR | 5.312 % | 15.0933 | 21.75 % | 38.81 % | 49.24 % | 59.15 % | 70.93 % | 79.57 % |
| 1.0 ATR | 7.083 % | 14.811 | 9.57 % | 23.79 % | 33.4 % | 46.21 % | 61.89 % | 73.41 % |
| 1.25 ATR | 8.853 % | 14.5288 | 4.03 % | 14.52 % | 23.41 % | 36.8 % | 52.85 % | 65.5 % |
| 1.5 ATR | 10.624 % | 14.2466 | 1.71 % | 7.16 % | 13.72 % | 25.38 % | 42.99 % | 57.29 % |
| 2.0 ATR | 14.165 % | 13.6821 | 0.4 % | 1.71 % | 3.94 % | 10.72 % | 25.2 % | 40.86 % |
| 2.5 ATR | 17.706 % | 13.1176 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.33 % | 28.44 % |
| 3.0 ATR | 21.248 % | 12.5531 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.15 % |
| 4.0 ATR | 28.33 % | 11.4241 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 42.496 % | 9.1662 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.59 ATR | 0.66 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.21 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.03 ATR | 1.33 ATR | 1.51 ATR | 1.68 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.94 ATR | 1.72 ATR | 1.87 ATR | 2.32 ATR | 2.65 ATR | 2.87 ATR | 3.58 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.46–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.541 %, prix 15.3756), p(touche) 40.99 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (68.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.312 %, prix 15.0933), p(touche) 38.81 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.817–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.083 %, prix 14.811), p(touche) 33.4 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.032–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.853 %, prix 14.5288), p(touche) 36.8 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.449–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.624 %, prix 14.2465), p(touche) 42.99 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.874–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.165 %, prix 13.6821), p(touche) 40.86 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.288 | EV/share : $0.097 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.173 | ¼-Kelly 0.043 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 19.3 | side 75.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.466% → cible +3.783% / stop −2.156%, p_fill 66%, n_eff≈29.2) : P(cible|rempli) **24%** · **EV/risk -0.039** (×p_fill ; si rempli -0.13% du capital)
  - **swing** (entrée dip −3.227% → cible +7.251% / stop −7.319%, p_fill 53%, n_eff≈25.4) : P(cible|rempli) **48%** · **EV/risk -0.038** (×p_fill ; si rempli -0.52% du capital)
  - **deep** (entrée dip −4.997% → cible +10.254% / stop −11.182%, p_fill 59%, n_eff≈30.2) : P(cible|rempli) **56%** · **EV/risk +0.031** (×p_fill ; si rempli +0.59% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→72% · +3.0%→57% · +5.0%→42% · +8.0%→14%
- Range intraday médian 7.89% (p90 13.36%) · excursion haute méd. +4.06% / basse méd. −2.61%
- Profil de vol intra : ouverture 5.522% vs midi 1.598% vs clôture 1.838% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.515% ; recovery-V 31%
- **σ réalisé intraday** 4.56% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 45% / whipsaw 5%
- POC intraday (dernière séance, temps-au-prix) : 17.6928 (VA 17.3518–17.9911 ; dernier close 17.895)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 44% · rebond 74% · **stop −6.31%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. -0.46% · baisse 59% (gap-down >1% 40% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −1.19% (p90 −2.84%) · haut méd +1.28% · range méd 2.63%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −3.96%) · haut méd +1.88% · range méd 3.78%
- Excursion ouverture 30min (n=160) : bas méd −1.83% (p90 −4.65%) · haut méd +2.1% · range méd 4.66%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.98%) · haut méd +2.53% · range méd 5.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.91 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 84% (135/159) · gap 48% · délai 0.0min · rebond 67% (88/135) (MFE +2.43%)
   - −1.0% : fill 30min 67% · séance 75% (126/159) · gap 40% · délai 0.0min · rebond 67% (82/126) (MFE +1.87%)
   - −1.5% : fill 30min 61% · séance 70% (120/159) · gap 35% · délai 0.0min · rebond 65% (78/120) (MFE +2.22%)
   - −2.0% : fill 30min 56% · séance 62% (111/159) · gap 27% · délai 0.0min · rebond 71% (76/111) (MFE +2.39%)
   - −3.0% : fill 30min 48% · séance 56% (99/159) · gap 11% · délai 1.2min · rebond 74% (73/99) (MFE +2.53%)
   - −4.0% : fill 30min 36% · séance 44% (78/159) · gap 5% · délai 6.3min · rebond 74% (57/78) (MFE +2.37%)
   - −5.0% : fill 30min 18% · séance 35% (65/159) · gap 3% · délai 27.2min · rebond 64% (46/65) (MFE +1.85%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.2%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.65%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.91%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1171 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 96% (82/84) · rebond 61% (49/82)
      · −2.0% : fill 85% (77/84) · rebond 70% (52/77)
      · −3.0% : fill 81% (72/84) · rebond 68% (51/72)
      · −4.0% : fill 67% (58/84) · rebond 71% (41/58)
      · −5.0% : fill 55% (50/84) · rebond 62% (35/50)
   - **flat** (15 séances) :
      · −1.0% : fill 96% (14/15) · rebond 94% (12/14)
      · −2.0% : fill 74% (12/15) · rebond 85% (10/12)
      · −3.0% : fill 50% (7/15) · rebond 90% (5/7)
      · −4.0% : fill 34% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 21% (5/15) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (30/60) · rebond 68% (21/30)
      · −2.0% : fill 28% (22/60) · rebond 63% (14/22)
      · −3.0% : fill 23% (20/60) · rebond 89% (17/20)
      · −4.0% : fill 15% (14/60) · rebond 84% (12/14)
      · −5.0% : fill 12% (10/60) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 71% si les 15 1res min sont vertes (80 cas) · 29% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 89% si début vert vs 15% si rouge (base 52% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **89%** · continue >prix actuel 52% ; creux résiduel méd -2.13% (q20 -3.51%) → **SL/trailing à −3.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.53% / q75 +5.77% → **scale +2.53% / runner +5.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **15%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.35%** (au-delà de la MAE q10 -5.35%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.17% .. +4.96%] · haut q95 +6.49% · bas q05 -6.26%
   - 60min (n=160) : retour [-5.56% .. +6.35%] · haut q95 +6.68% · bas q05 -6.83%
   - 2h (n=160) : retour [-6.39% .. +6.97%] · haut q95 +9.12% · bas q05 -7.59%
   - 4h (n=160) : retour [-7.13% .. +8.07%] · haut q95 +9.21% · bas q05 -7.87%
   - 6h (n=160) : retour [-7.45% .. +8.87%] · haut q95 +10.37% · bas q05 -8.62%
   - session (n=160) : retour [-7.26% .. +9.29%] · haut q95 +10.63% · bas q05 -8.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 6% (base 7%)
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
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 47.2  _(neutre)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist -0.122  _(bearish_recent)_
- **BB** : %B 0.25 · largeur 27.7%
- **ATR** : 1.13 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.044  _(neutre)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 55.0  _(transition)_
- **MA** : MA20 17.14 · MA50 17.13 · MA200 19.76  _(prix < MA20)_
- **Dist MA** : MA20 -7.0% · MA50 -6.9% · MA200 -19.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (807451 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
