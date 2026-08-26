# SMR

**Generated** : 2026-08-26T00:31:19.733015+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.81  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $9.81 (+2.2% vs entrée) · entrée $9.60 · stop $9.40 · T1 $9.90 · R/R 1.5  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.11 _(réel 5 s)_ (GBM 0.071) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.11% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 328 % hors [0,100] (R² max 0.71). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.54–$9.66 (mid $9.60)
- Spot actuel : $9.81 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : $9.40 (stop swing_plan-based (-12.97%))
- Targets : T1 $9.90 · R/R 1.5 | T2 $10.21 · R/R 3.05 | T3 $10.51 · R/R 4.55
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.40


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.31 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.97 %)** : le gap seul le franchit 0.356 % des séances (4 fois sur 1125).
   - exécution **3.039 pt plus bas** dans le cas TYPIQUE (médiane), 13.426 au p90, **17.353 au pire**
   - perte réelle **18.976 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 12.97 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0214 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.432 % | p01 -6.963 % | pire -30.323 % _(sur 1125 séances)_
- **P(stop avant cible)** _(source : daily, 1126 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5748** [0.5004 ; 0.6467] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4987** [0.4462 ; 0.5513] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.4789** [0.4266 ; 0.5316] _(largeur 10.5 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.4 pt), swing (36.4 pt), deep (41.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.93 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.01 % contre 5.90 % aujourd'hui, rapport 1.87)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.97 % vs -18.7 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6124** (β de hausse 1.3683, asymétrie 1.1784) vs IWM — 533 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.038× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.6478 sur grid_snapped (1.42 ATR, 11.847 %) — p(stop avant cible) 0.5144 [0.46 ; 0.57], R/R 0.878, perte reelle 17.667 % (gap inclus), CVaR 11.873 %, EV -4.0434 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0305 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.514, borne haute 0.567 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.305 %) — p(stop avant cible) 0.5622 [0.51 ; 0.61], R/R 0.942, perte reelle 16.461 % (gap inclus), EV -4.3955 % — **REFUSE**
      - refuse : p_stop_first 0.562, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.94 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.40 %) : P(cible) 31.9 % x 15.50 % + P(rien) 11.9 % x -0.73 % ne couvrent pas P(stop) 56.2 % x 16.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.42 ATR (stop 12.905 %) — p(stop avant cible) 0.4715 [0.42 ; 0.52], R/R 0.817, perte reelle 18.976 % (gap inclus), EV -3.8141 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.81 %) : P(cible) 34.8 % x 15.50 % + P(rien) 18.0 % x -1.50 % ne couvrent pas P(stop) 47.1 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.1 ATR (stop 17.541 %) — p(stop avant cible) 0.3196 [0.27 ; 0.37], R/R 0.511, perte reelle 30.323 % (gap inclus), EV -4.991 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.99 %) : P(cible) 36.7 % x 15.50 % + P(rien) 31.4 % x -3.14 % ne couvrent pas P(stop) 32.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.86 ATR (stop 29.623 %) — p(stop avant cible) 0.061 [0.04 ; 0.09], R/R 0.511, perte reelle 30.323 % (gap inclus), EV -0.4957 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 37.2 % x 15.50 % + P(rien) 56.7 % x -7.78 % ne couvrent pas P(stop) 6.1 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.717 %) — p(stop avant cible) 0.9102 [0.88 ; 0.94], R/R 4.24, perte reelle 3.657 % (gap inclus), EV -2.0339 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.910, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.03 %) : P(cible) 8.3 % x 15.50 % + P(rien) 0.6 % x 0.50 % ne couvrent pas P(stop) 91.0 % x 3.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.435 %) — p(stop avant cible) 0.8388 [0.80 ; 0.87], R/R 2.543, perte reelle 6.097 % (gap inclus), EV -2.7732 % — **REFUSE**
      - refuse : p_stop_first 0.839, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.77 %) : P(cible) 15.1 % x 15.50 % + P(rien) 1.1 % x 0.57 % ne couvrent pas P(stop) 83.9 % x 6.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.152 %) — p(stop avant cible) 0.778 [0.73 ; 0.82], R/R 1.616, perte reelle 9.596 % (gap inclus), EV -4.2159 % — **REFUSE**
      - refuse : p_stop_first 0.778, borne haute 0.819 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.22 %) : P(cible) 20.9 % x 15.50 % + P(rien) 1.3 % x 0.84 % ne couvrent pas P(stop) 77.8 % x 9.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.87 %) — p(stop avant cible) 0.7146 [0.67 ; 0.76], R/R 1.291, perte reelle 12.006 % (gap inclus), EV -4.5913 % — **REFUSE**
      - refuse : p_stop_first 0.715, borne haute 0.760 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.59 %) : P(cible) 25.3 % x 15.50 % + P(rien) 3.2 % x 1.91 % ne couvrent pas P(stop) 71.5 % x 12.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.42 ATR (stop 11.847 %) — p(stop avant cible) 0.5144 [0.46 ; 0.57], R/R 0.878, perte reelle 17.667 % (gap inclus), EV -4.0434 % — **REFUSE**
      - refuse : p_stop_first 0.514, borne haute 0.567 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.04 %) : P(cible) 33.5 % x 15.50 % + P(rien) 15.0 % x -1.00 % ne couvrent pas P(stop) 51.4 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.1 ATR (stop 16.483 %) — p(stop avant cible) 0.3451 [0.30 ; 0.40], R/R 0.652, perte reelle 23.778 % (gap inclus), EV -3.3498 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.35 %) : P(cible) 36.5 % x 15.50 % + P(rien) 28.9 % x -2.80 % ne couvrent pas P(stop) 34.5 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 18.892 %) — p(stop avant cible) 0.2584 [0.21 ; 0.31], R/R 0.511, perte reelle 30.323 % (gap inclus), EV -3.618 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.62 %) : P(cible) 36.9 % x 15.50 % + P(rien) 37.3 % x -4.01 % ne couvrent pas P(stop) 25.8 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 20.609 %) — p(stop avant cible) 0.2234 [0.18 ; 0.27], R/R 0.511, perte reelle 30.323 % (gap inclus), EV -2.9614 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.96 %) : P(cible) 37.0 % x 15.50 % + P(rien) 40.6 % x -4.74 % ne couvrent pas P(stop) 22.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.044 %) — p(stop avant cible) 0.147 [0.11 ; 0.19], R/R 0.511, perte reelle 30.323 % (gap inclus), EV -1.5739 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 37.2 % x 15.50 % + P(rien) 48.1 % x -5.99 % ne couvrent pas P(stop) 14.7 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.86 ATR (stop 28.565 %) — p(stop avant cible) 0.0745 [0.05 ; 0.11], R/R 0.511, perte reelle 30.323 % (gap inclus), EV -0.5833 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 37.2 % x 15.50 % + P(rien) 55.4 % x -7.39 % ne couvrent pas P(stop) 7.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 30.914 %) — p(stop avant cible) 0.0536 [0.03 ; 0.08], R/R 0.502, perte reelle 30.914 % (gap inclus), EV -0.4859 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 37.2 % x 15.50 % + P(rien) 57.4 % x -8.00 % ne couvrent pas P(stop) 5.4 % x 30.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 34.349 %) — p(stop avant cible) 0.0328 [0.02 ; 0.06], R/R 0.451, perte reelle 34.349 % (gap inclus), EV -0.4362 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 37.2 % x 15.50 % + P(rien) 59.5 % x -8.54 % ne couvrent pas P(stop) 3.3 % x 34.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 37.784 %) — p(stop avant cible) 0.0239 [0.01 ; 0.04], R/R 0.41, perte reelle 37.784 % (gap inclus), EV -0.5065 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 37.2 % x 15.50 % + P(rien) 60.4 % x -8.90 % ne couvrent pas P(stop) 2.4 % x 37.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 41.219 %) — p(stop avant cible) 0.0164 [0.01 ; 0.03], R/R 0.376, perte reelle 41.219 % (gap inclus), EV -0.5185 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 37.2 % x 15.50 % + P(rien) 61.1 % x -9.18 % ne couvrent pas P(stop) 1.6 % x 41.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 44.654 %) — p(stop avant cible) 0.0127 [0.00 ; 0.03], R/R 0.347, perte reelle 44.654 % (gap inclus), EV -0.5079 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 37.2 % x 15.50 % + P(rien) 61.5 % x -9.29 % ne couvrent pas P(stop) 1.3 % x 44.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 48.089 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.322, perte reelle 48.089 % (gap inclus), EV -0.512 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 37.2 % x 15.50 % + P(rien) 62.5 % x -9.86 % ne couvrent pas P(stop) 0.2 % x 48.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 51.524 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.301, perte reelle 51.524 % (gap inclus), EV -0.5104 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 37.2 % x 15.50 % + P(rien) 62.8 % x -9.99 % ne couvrent pas P(stop) 0.0 % x 51.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 54.958 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.282, perte reelle 54.958 % (gap inclus), EV -0.5111 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 37.2 % x 15.50 % + P(rien) 62.8 % x -9.99 % ne couvrent pas P(stop) 0.0 % x 54.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.81, ATR14 0.6739 (6.87 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.429 ATR = 2.947 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.343 % | 9.7763 | 92.6 % | 95.14 % | 96.41 % | 97.1 % | 97.9 % | 98.35 % |
| 0.1 ATR | 0.687 % | 9.7426 | 86.94 % | 91.32 % | 93.28 % | 94.66 % | 96.14 % | 97.4 % |
| 0.15 ATR | 1.03 % | 9.7089 | 80.92 % | 87.04 % | 89.69 % | 91.64 % | 93.81 % | 96.1 % |
| 0.2 ATR | 1.374 % | 9.6752 | 75.38 % | 82.75 % | 86.44 % | 89.2 % | 92.17 % | 95.04 % |
| 0.25 ATR | 1.717 % | 9.6415 | 70.06 % | 79.63 % | 83.78 % | 87.11 % | 90.54 % | 93.85 % |
| 0.35 ATR | 2.404 % | 9.5741 | 58.38 % | 72.11 % | 77.4 % | 82.93 % | 87.5 % | 91.49 % |
| 0.5 ATR | 3.435 % | 9.473 | 42.43 % | 59.14 % | 67.21 % | 74.33 % | 82.94 % | 88.42 % |
| 0.75 ATR | 5.152 % | 9.3046 | 20.69 % | 37.5 % | 47.97 % | 59.93 % | 72.31 % | 80.85 % |
| 1.0 ATR | 6.87 % | 9.1361 | 11.33 % | 25.93 % | 36.04 % | 49.48 % | 64.37 % | 75.3 % |
| 1.25 ATR | 8.587 % | 8.9676 | 4.74 % | 16.09 % | 25.38 % | 38.79 % | 54.79 % | 68.91 % |
| 1.5 ATR | 10.305 % | 8.7991 | 2.31 % | 9.84 % | 16.34 % | 28.46 % | 45.44 % | 62.17 % |
| 2.0 ATR | 13.74 % | 8.4621 | 0.35 % | 3.24 % | 6.49 % | 14.63 % | 31.54 % | 49.88 % |
| 2.5 ATR | 17.175 % | 8.1252 | 0.12 % | 1.27 % | 2.78 % | 6.85 % | 20.68 % | 39.01 % |
| 3.0 ATR | 20.609 % | 7.7882 | 0.12 % | 0.58 % | 1.74 % | 3.72 % | 11.92 % | 28.96 % |
| 4.0 ATR | 27.479 % | 7.1143 | 0.0 % | 0.23 % | 0.35 % | 1.05 % | 4.56 % | 13.95 % |
| 6.0 ATR | 41.219 % | 5.7664 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.65 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.48 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.61 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.99 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.81 ATR | 2.30 ATR | 2.80 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.52 ATR | 1.95 ATR | 2.30 ATR | 2.54 ATR | 3.26 ATR | 3.94 ATR |
| **20 s.** | 1.01 ATR | 2.00 ATR | 2.22 ATR | 2.80 ATR | 3.26 ATR | 3.60 ATR | 4.64 ATR | 5.46 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.476–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.435 %, prix 9.473), p(touche) 42.43 % (en stress 81.61 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.152 %, prix 9.3046), p(touche) 37.5 % (en stress 88.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.812–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.87 %, prix 9.1361), p(touche) 36.04 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.105–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.587 %, prix 8.9676), p(touche) 38.79 % (en stress 95.4 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.516–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.74 %, prix 8.4621), p(touche) 31.54 % (en stress 96.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.224–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.175 %, prix 8.1251), p(touche) 39.01 % (en stress 98.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.071 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.5 | bear 7.0 | side 9.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 157.0 (= 16 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.129% → cible +3.116% / stop −2.106%, p_fill 61%, n_eff≈26.0) : P(cible|rempli) **27%** · **EV/risk -0.110** (×p_fill ; si rempli -0.38% du capital)
  - **swing** (entrée dip −4.696% → cible +17.364% / stop −8.681%, p_fill 59%, n_eff≈24.1) : P(cible|rempli) **8%** · **EV/risk +0.010** (×p_fill ; si rempli +0.15% du capital)
  - **deep** (entrée dip −7.245% → cible +9.988% / stop −11.11%, p_fill 36%, n_eff≈19.0) : P(cible|rempli) **60%** · **EV/risk +0.026** (×p_fill ; si rempli +0.81% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→81% · +2.0%→66% · +3.0%→61% · +5.0%→39% · +8.0%→11%
- Range intraday médian 7.39% (p90 12.48%) · excursion haute méd. +3.55% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.824% vs midi 1.503% vs clôture 1.831% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. 0.265% ; recovery-V 38%
- **σ réalisé intraday** 4.596% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 66% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 9.4947 (VA 9.3901–9.5761 ; dernier close 9.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 48% · rebond 76% · **stop −5.09%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 58% (gap-down >1% 36% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −2.96%) · haut méd +1.2% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.8%) · haut méd +1.86% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.73% (p90 −4.61%) · haut méd +2.25% · range méd 4.41%
- Excursion ouverture 60min (n=160) : bas méd −2.09% (p90 −5.56%) · haut méd +2.62% · range méd 5.22%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 81% (131/159) · gap 50% · délai 0.0min · rebond 67% (83/131) (MFE +1.9%)
   - −1.0% : fill 30min 66% · séance 78% (125/159) · gap 36% · délai 0.0min · rebond 67% (81/125) (MFE +2.13%)
   - −1.5% : fill 30min 63% · séance 73% (118/159) · gap 31% · délai 0.0min · rebond 74% (87/118) (MFE +2.12%)
   - −2.0% : fill 30min 56% · séance 65% (110/159) · gap 26% · délai 0.6min · rebond 70% (78/110) (MFE +2.23%)
   - −3.0% : fill 30min 43% · séance 54% (96/159) · gap 10% · délai 4.4min · rebond 76% (78/96) (MFE +2.23%)
   - −4.0% : fill 30min 34% · séance 48% (84/159) · gap 5% · délai 8.8min · rebond 76% (64/84) (MFE +2.53%)
   - −5.0% : fill 30min 24% · séance 40% (66/159) · gap 2% · délai 22.4min · rebond 76% (50/66) (MFE +2.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.66%) → stop au-delà de −1.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.68%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −3.23%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1164 jambes) : jambe baissière méd −1.33% (p90 −3.11%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (87 séances) :
      · −1.0% : fill 98% (86/87) · rebond 64% (55/86)
      · −2.0% : fill 91% (81/87) · rebond 74% (61/81)
      · −3.0% : fill 81% (75/87) · rebond 79% (63/75)
      · −4.0% : fill 74% (67/87) · rebond 79% (54/67)
      · −5.0% : fill 61% (51/87) · rebond 80% (41/51)
   - **flat** (11 séances) :
      · −1.0% : fill 92% (9/11) · rebond 49% (5/9)
      · −2.0% : fill 80% (7/11) · rebond 41% (3/7)
      · −3.0% : fill 80% (7/11) · rebond 51% (4/7)
      · −4.0% : fill 80% (7/11) · rebond 61% (4/7)
      · −5.0% : fill 61% (5/11) · rebond 79% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 48% (30/61) · rebond 82% (21/30)
      · −2.0% : fill 28% (22/61) · rebond 61% (14/22)
      · −3.0% : fill 12% (14/61) · rebond 73% (11/14)
      · −4.0% : fill 9% (10/61) · rebond 54% (6/10)
      · −5.0% : fill 9% (10/61) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 66% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 88% si début vert vs 10% si rouge (base 47% · écart 79 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **88%** · continue >prix actuel 55% ; creux résiduel méd -1.59% (q20 -3.4%) → **SL/trailing à −3.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.43% / q75 +3.62% → **scale +2.43% / runner +3.62%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **10%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +1.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.33% .. +4.9%] · haut q95 +6.22% · bas q05 -5.82%
   - 60min (n=160) : retour [-5.34% .. +5.47%] · haut q95 +6.78% · bas q05 -6.38%
   - 2h (n=160) : retour [-6.34% .. +5.53%] · haut q95 +8.67% · bas q05 -8.0%
   - 4h (n=160) : retour [-7.02% .. +7.27%] · haut q95 +9.67% · bas q05 -8.84%
   - 6h (n=160) : retour [-7.2% .. +8.26%] · haut q95 +10.85% · bas q05 -9.15%
   - session (n=160) : retour [-7.12% .. +9.14%] · haut q95 +10.99% · bas q05 -9.57%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 53.7  _(neutre)_
- **ADX** : 12.7  _(pas de tendance nette)_
- **MACD** : hist 0.043  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 24.5%
- **ATR** : 0.67 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.05  _(neutre)_
- **Vol ratio** : 1.67  _(volume au-dessus de la moyenne)_
- **Choppiness** : 67.1  _(marche en range (choppy))_
- **MA** : MA20 9.21 · MA50 9.29 · MA200 13.69  _(prix > MA20)_
- **Dist MA** : MA20 +6.6% · MA50 +5.6% · MA200 -28.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (819221 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
