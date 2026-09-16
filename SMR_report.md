# SMR

**Generated** : 2026-09-16T00:44:08.403439+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.44  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $8.44 (+3.3% vs entrée) · entrée $8.17 · stop $7.83 · T1 $8.85 · R/R 2.0  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.023 _(réel 5 s)_ (GBM 0.124) · ¼-Kelly 0.056 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.12% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +11.6 % ≠ (strike 9.5 − spot 8.44)/spot = +12.6 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.11–$8.23 (mid $8.17)
- Spot actuel : $8.44 (+3.3% au-dessus de la zone — repli à attendre)
- Stop : $7.83 (stop swing_plan-based (-17.66%))
- Targets : T1 $8.85 · R/R 2.0 | T2 $8.95 · R/R 2.29 | T3 $9.06 · R/R 2.62
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.50 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.66 %)** : le gap seul le franchit 0.088 % des séances (1 fois sur 1139).
   - exécution **12.663 pt plus bas** dans le cas TYPIQUE (médiane), 12.663 au p90, **12.663 au pire**
   - perte réelle **30.323 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 17.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0111 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.488 % | p01 -6.961 % | pire -30.323 % _(sur 1139 séances)_
- **P(stop avant cible)** _(source : daily, 1140 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3697** [0.3004 ; 0.4433] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.3449** [0.2962 ; 0.3962] _(largeur 10.0 pt, n_eff 345.3)_
   - deep : **0.4071** [0.3562 ; 0.4595] _(largeur 10.3 pt, n_eff 345.2)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 8.2 observations effectives », dont la borne haute a 95 % vaut environ 36.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.8 pt), swing (40.8 pt), deep (44.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.97 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.83 % contre 6.23 % aujourd'hui, rapport 1.74)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.05 % vs -18.73 % si l'on extrapolait par √5 _(rapport 1.017 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6263** (β de hausse 1.3855, asymétrie 1.1739) vs IWM — 542 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.974× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 7.3448 sur atr_based (1.5 ATR, 12.953 %) — p(stop avant cible) 0.4548 [0.40 ; 0.51], R/R 0.961, perte reelle 18.976 % (gap inclus), CVaR 12.974 %, EV -3.2693 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0812 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.97 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 12.953 %) — p(stop avant cible) 0.4548 [0.40 ; 0.51], R/R 0.961, perte reelle 18.976 % (gap inclus), EV -3.2693 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.27 %) : P(cible) 29.5 % x 18.24 % + P(rien) 25.0 % x -0.08 % ne couvrent pas P(stop) 45.5 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.69 ATR (stop 17.046 %) — p(stop avant cible) 0.3174 [0.27 ; 0.37], R/R 0.767, perte reelle 23.778 % (gap inclus), EV -2.5384 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.54 %) : P(cible) 30.9 % x 18.24 % + P(rien) 37.4 % x -1.67 % ne couvrent pas P(stop) 31.7 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 2.159 %) — p(stop avant cible) 0.8947 [0.86 ; 0.92], R/R 4.359, perte reelle 4.184 % (gap inclus), EV -2.0589 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.895, borne haute 0.924 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 9.0 % x 18.24 % + P(rien) 1.5 % x 2.83 % ne couvrent pas P(stop) 89.5 % x 4.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 4.317 %) — p(stop avant cible) 0.8182 [0.78 ; 0.86], R/R 2.338, perte reelle 7.801 % (gap inclus), EV -3.5219 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.818, borne haute 0.856 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 14.9 % x 18.24 % + P(rien) 3.3 % x 4.30 % ne couvrent pas P(stop) 81.8 % x 7.80 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 6.476 %) — p(stop avant cible) 0.7386 [0.69 ; 0.78], R/R 1.567, perte reelle 11.636 % (gap inclus), EV -4.5926 % — **REFUSE**
      - refuse : p_stop_first 0.739, borne haute 0.783 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.59 %) : P(cible) 20.7 % x 18.24 % + P(rien) 5.5 % x 4.22 % ne couvrent pas P(stop) 73.9 % x 11.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 8.635 %) — p(stop avant cible) 0.6413 [0.59 ; 0.69], R/R 1.299, perte reelle 14.043 % (gap inclus), EV -4.2234 % — **REFUSE**
      - refuse : p_stop_first 0.641, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.22 %) : P(cible) 24.6 % x 18.24 % + P(rien) 11.3 % x 2.62 % ne couvrent pas P(stop) 64.1 % x 14.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 10.793 %) — p(stop avant cible) 0.5516 [0.50 ; 0.60], R/R 1.032, perte reelle 17.667 % (gap inclus), EV -4.5626 % — **REFUSE**
      - refuse : p_stop_first 0.552, borne haute 0.604 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.56 %) : P(cible) 27.5 % x 18.24 % + P(rien) 17.3 % x 0.94 % ne couvrent pas P(stop) 55.2 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 19.428 %) — p(stop avant cible) 0.2465 [0.20 ; 0.29], R/R 0.601, perte reelle 30.323 % (gap inclus), EV -3.0354 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.04 %) : P(cible) 31.0 % x 18.24 % + P(rien) 44.3 % x -2.76 % ne couvrent pas P(stop) 24.6 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 21.587 %) — p(stop avant cible) 0.1855 [0.15 ; 0.23], R/R 0.601, perte reelle 30.323 % (gap inclus), EV -1.8987 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 31.2 % x 18.24 % + P(rien) 50.3 % x -3.90 % ne couvrent pas P(stop) 18.6 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 23.745 %) — p(stop avant cible) 0.1434 [0.11 ; 0.18], R/R 0.601, perte reelle 30.323 % (gap inclus), EV -1.1851 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 31.2 % x 18.24 % + P(rien) 54.5 % x -4.64 % ne couvrent pas P(stop) 14.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 25.904 %) — p(stop avant cible) 0.0916 [0.06 ; 0.13], R/R 0.601, perte reelle 30.323 % (gap inclus), EV -0.4302 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 31.2 % x 18.24 % + P(rien) 59.6 % x -5.61 % ne couvrent pas P(stop) 9.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 30.222 %) — p(stop avant cible) 0.0531 [0.03 ; 0.08], R/R 0.601, perte reelle 30.323 % (gap inclus), EV -0.1051 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 31.2 % x 18.24 % + P(rien) 63.5 % x -6.60 % ne couvrent pas P(stop) 5.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 34.539 %) — p(stop avant cible) 0.0302 [0.02 ; 0.05], R/R 0.528, perte reelle 34.539 % (gap inclus), EV -0.064 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 31.2 % x 18.24 % + P(rien) 65.7 % x -7.18 % ne couvrent pas P(stop) 3.0 % x 34.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 38.856 %) — p(stop avant cible) 0.0213 [0.01 ; 0.04], R/R 0.469, perte reelle 38.856 % (gap inclus), EV -0.1453 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 31.2 % x 18.24 % + P(rien) 66.6 % x -7.53 % ne couvrent pas P(stop) 2.1 % x 38.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 43.174 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 0.422, perte reelle 43.174 % (gap inclus), EV -0.1155 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 31.2 % x 18.24 % + P(rien) 67.5 % x -7.83 % ne couvrent pas P(stop) 1.2 % x 43.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 47.491 %) — p(stop avant cible) 0.0057 [0.00 ; 0.02], R/R 0.384, perte reelle 47.491 % (gap inclus), EV -0.1293 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 31.2 % x 18.24 % + P(rien) 68.2 % x -8.15 % ne couvrent pas P(stop) 0.6 % x 47.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 51.808 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.352, perte reelle 51.808 % (gap inclus), EV -0.1295 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 31.2 % x 18.24 % + P(rien) 68.8 % x -8.46 % ne couvrent pas P(stop) 0.0 % x 51.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 56.126 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.325, perte reelle 56.126 % (gap inclus), EV -0.1304 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 31.2 % x 18.24 % + P(rien) 68.8 % x -8.46 % ne couvrent pas P(stop) 0.0 % x 56.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 60.443 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.302, perte reelle 60.443 % (gap inclus), EV -0.1244 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 31.2 % x 18.24 % + P(rien) 68.8 % x -8.47 % ne couvrent pas P(stop) 0.0 % x 60.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 64.76 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.282, perte reelle 64.76 % (gap inclus), EV -0.1244 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 64.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 31.2 % x 18.24 % + P(rien) 68.8 % x -8.47 % ne couvrent pas P(stop) 0.0 % x 64.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 69.078 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.264, perte reelle 69.078 % (gap inclus), EV -0.1244 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 69.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 31.2 % x 18.24 % + P(rien) 68.8 % x -8.47 % ne couvrent pas P(stop) 0.0 % x 69.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 8.4377, ATR14 0.7286 (8.635 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.427 ATR = 3.687 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.432 % | 8.4013 | 92.61 % | 95.1 % | 96.35 % | 97.03 % | 97.93 % | 98.37 % |
| 0.1 ATR | 0.863 % | 8.3648 | 86.8 % | 91.34 % | 93.27 % | 94.63 % | 96.21 % | 97.44 % |
| 0.15 ATR | 1.295 % | 8.3284 | 80.77 % | 87.02 % | 89.62 % | 91.66 % | 93.91 % | 96.05 % |
| 0.2 ATR | 1.727 % | 8.292 | 75.09 % | 82.69 % | 86.32 % | 89.14 % | 92.3 % | 95.0 % |
| 0.25 ATR | 2.159 % | 8.2556 | 69.85 % | 79.61 % | 83.69 % | 86.97 % | 90.57 % | 93.84 % |
| 0.35 ATR | 3.022 % | 8.1827 | 58.25 % | 72.1 % | 77.31 % | 82.74 % | 87.59 % | 91.4 % |
| 0.5 ATR | 4.317 % | 8.0734 | 42.21 % | 59.0 % | 67.05 % | 74.17 % | 83.1 % | 88.37 % |
| 0.75 ATR | 6.476 % | 7.8913 | 20.59 % | 37.36 % | 47.66 % | 59.54 % | 72.18 % | 80.81 % |
| 1.0 ATR | 8.635 % | 7.7091 | 11.38 % | 25.97 % | 35.92 % | 49.26 % | 64.25 % | 75.12 % |
| 1.25 ATR | 10.793 % | 7.527 | 4.78 % | 16.17 % | 25.2 % | 38.51 % | 54.71 % | 68.6 % |
| 1.5 ATR | 12.952 % | 7.3448 | 2.28 % | 9.91 % | 16.31 % | 28.34 % | 45.17 % | 61.74 % |
| 2.0 ATR | 17.269 % | 6.9806 | 0.34 % | 3.3 % | 6.61 % | 14.51 % | 31.03 % | 49.07 % |
| 2.5 ATR | 21.587 % | 6.6163 | 0.11 % | 1.37 % | 2.96 % | 6.74 % | 20.34 % | 38.37 % |
| 3.0 ATR | 25.904 % | 6.252 | 0.11 % | 0.57 % | 1.94 % | 3.66 % | 11.72 % | 28.49 % |
| 4.0 ATR | 34.539 % | 5.5234 | 0.0 % | 0.23 % | 0.34 % | 1.03 % | 4.48 % | 13.72 % |
| 6.0 ATR | 51.808 % | 4.0663 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.50 ATR | 1.87 ATR |
| **3 s.** | 0.38 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.22 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.29 ATR | 2.78 ATR |
| **10 s.** | 0.69 ATR | 1.37 ATR | 1.51 ATR | 1.93 ATR | 2.28 ATR | 2.52 ATR | 3.24 ATR | 3.93 ATR |
| **20 s.** | 1.00 ATR | 1.96 ATR | 2.19 ATR | 2.77 ATR | 3.24 ATR | 3.58 ATR | 4.62 ATR | 5.44 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.474–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.317 %, prix 8.0734), p(touche) 42.21 % (en stress 81.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.662–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.476 %, prix 7.8913), p(touche) 37.36 % (en stress 88.64 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.807–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.635 %, prix 7.7091), p(touche) 35.92 % (en stress 89.77 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.099–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.793 %, prix 7.527), p(touche) 38.51 % (en stress 94.32 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.506–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (17.269 %, prix 6.9806), p(touche) 31.03 % (en stress 96.55 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.19–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.124 | EV/share : $0.042 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.223 | ¼-Kelly 0.056 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 51.6 | bear 13.7 | side 34.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.146% → cible +8.248% / stop −4.124%, p_fill 43%, n_eff≈21.2) : P(cible|rempli) **1%** · **EV/risk -0.023** (×p_fill ; si rempli -0.22% du capital)
  - **swing** (entrée dip −6.923% → cible +23.071% / stop −11.535%, p_fill 17%, n_eff≈8.2) : P(cible|rempli) **0%** · **EV/risk +0.047** (×p_fill ; si rempli +3.22% du capital)
  - **deep** (entrée dip −10.709% → cible +30.04% / stop −15.019%, p_fill 17%, n_eff≈10.8) : P(cible|rempli) **1%** · **EV/risk +0.048** (×p_fill ; si rempli +4.21% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→92% · +1.0%→81% · +2.0%→70% · +3.0%→64% · +5.0%→39% · +8.0%→10%
- Range intraday médian 7.03% (p90 12.01%) · excursion haute méd. +3.75% / basse méd. −2.71%
- Profil de vol intra : ouverture 4.625% vs midi 1.437% vs clôture 1.737% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.074)_ ; drift intra méd. 0.451% ; recovery-V 48%
- **σ réalisé intraday** 4.311% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 60% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 9.4737 (VA 9.4479–9.5856 ; dernier close 9.695)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 76% · **stop −4.13%** sous le fill (sous le bruit) · cible +2.5% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. -0.56% · baisse 58% (gap-down >1% 36% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −2.93%) · haut méd +1.22% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.78%) · haut méd +1.87% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.55% (p90 −4.61%) · haut méd +2.23% · range méd 4.13%
- Excursion ouverture 60min (n=160) : bas méd −2.06% (p90 −5.35%) · haut méd +2.64% · range méd 5.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (130/159) · gap 52% · délai 0.0min · rebond 64% (82/130) (MFE +1.62%)
   - −1.0% : fill 30min 63% · séance 75% (123/159) · gap 37% · délai 0.0min · rebond 65% (77/123) (MFE +2.03%)
   - −1.5% : fill 30min 59% · séance 70% (116/159) · gap 27% · délai 0.0min · rebond 71% (83/116) (MFE +1.99%)
   - −2.0% : fill 30min 51% · séance 62% (107/159) · gap 23% · délai 0.7min · rebond 68% (73/107) (MFE +1.98%)
   - −3.0% : fill 30min 39% · séance 53% (93/159) · gap 10% · délai 4.6min · rebond 76% (74/93) (MFE +2.31%)
   - −4.0% : fill 30min 32% · séance 46% (83/159) · gap 4% · délai 8.7min · rebond 76% (63/83) (MFE +2.53%)
   - −5.0% : fill 30min 23% · séance 40% (65/159) · gap 2% · délai 22.3min · rebond 76% (49/65) (MFE +2.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.66%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.68%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.05% (p90 −2.75%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1137 jambes) : jambe baissière méd −1.34% (p90 −3.08%) · ~13.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (89 séances) :
      · −1.0% : fill 96% (87/89) · rebond 63% (55/87)
      · −2.0% : fill 86% (81/89) · rebond 74% (60/81)
      · −3.0% : fill 78% (75/89) · rebond 82% (63/75)
      · −4.0% : fill 69% (67/89) · rebond 82% (54/67)
      · −5.0% : fill 58% (51/89) · rebond 83% (42/51)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 48% (4/8)
      · −2.0% : fill 80% (6/10) · rebond 40% (2/6)
      · −3.0% : fill 80% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 80% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 60% (4/10) · rebond 79% (3/4)
   - **gap-up** (60 séances) :
      · −1.0% : fill 44% (28/60) · rebond 74% (18/28)
      · −2.0% : fill 27% (20/60) · rebond 51% (11/20)
      · −3.0% : fill 14% (12/60) · rebond 49% (8/12)
      · −4.0% : fill 11% (10/60) · rebond 33% (5/10)
      · −5.0% : fill 11% (10/60) · rebond 26% (4/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 65% si les 15 1res min sont vertes (74 cas) · 38% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 85% si début vert vs 20% si rouge (base 52% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **85%** · continue >prix actuel 58% ; creux résiduel méd -1.67% (q20 -3.41%) → **SL/trailing à −3.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.07% / q75 +4.06% → **scale +3.07% / runner +4.06%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **20%** (continue à baisser 55%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.4%** (au-delà de la MAE q10 -5.4%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.92% .. +4.46%] · haut q95 +6.13% · bas q05 -5.65%
   - 60min (n=160) : retour [-4.99% .. +4.69%] · haut q95 +6.67% · bas q05 -6.2%
   - 2h (n=160) : retour [-6.22% .. +5.43%] · haut q95 +7.83% · bas q05 -7.86%
   - 4h (n=160) : retour [-7.13% .. +7.01%] · haut q95 +8.38% · bas q05 -7.96%
   - 6h (n=160) : retour [-6.87% .. +8.08%] · haut q95 +9.95% · bas q05 -8.33%
   - session (n=160) : retour [-6.95% .. +8.67%] · haut q95 +10.49% · bas q05 -8.41%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.83%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.2  _(momentum baissier)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -0.144  _(bearish_recent)_
- **BB** : %B 0.15 · largeur 30.0%
- **ATR** : 0.73 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.037  _(neutre)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 44.7  _(transition)_
- **MA** : MA20 9.44 · MA50 9.06 · MA200 12.71  _(prix < MA20)_
- **Dist MA** : MA20 -10.6% · MA50 -6.9% · MA200 -33.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (757585 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
