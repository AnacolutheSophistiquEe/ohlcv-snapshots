# SMR

**Generated** : 2026-09-04T00:34:16.391816+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.76  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $9.76 (+2.3% vs entrée) · entrée $9.54 · stop $9.29 · T1 $10.02 · R/R 1.92  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.043 _(réel 5 s)_ (GBM 0.131) · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.53% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -0.6 % ≠ (strike 9.5 − spot 9.76)/spot = -2.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.48–$9.59 (mid $9.54)
- Spot actuel : $9.76 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : $9.29 (stop swing_plan-based (-11.54%))
- Targets : T1 $10.02 · R/R 1.92 | T2 $10.16 · R/R 2.48 | T3 $10.29 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.29


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.54 %)** : le gap seul le franchit 0.442 % des séances (5 fois sur 1132).
   - exécution **3.245 pt plus bas** dans le cas TYPIQUE (médiane), 13.547 au p90, **18.783 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 11.54 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0271 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.452 % | p01 -6.962 % | pire -30.323 % _(sur 1132 séances)_
- **P(stop avant cible)** _(source : daily, 1133 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5752** [0.5008 ; 0.6471] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4875** [0.4351 ; 0.5401] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.471** [0.4188 ; 0.5237] _(largeur 10.5 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.4 pt), swing (40.4 pt), deep (41.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.93 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.91 % contre 5.91 % aujourd'hui, rapport 1.85)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.95 % vs -18.65 % si l'on extrapolait par √5 _(rapport 1.016 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6027** (β de hausse 1.3614, asymétrie 1.1773) vs IWM — 537 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.877× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.6093 sur grid_snapped (1.52 ATR, 11.79 %) — p(stop avant cible) 0.4689 [0.42 ; 0.52], R/R 0.669, perte reelle 17.667 % (gap inclus), CVaR 11.816 %, EV -3.4633 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.726 %) — p(stop avant cible) 0.5386 [0.49 ; 0.59], R/R 0.761, perte reelle 15.541 % (gap inclus), EV -3.8402 % — **REFUSE**
      - refuse : p_stop_first 0.539, borne haute 0.591 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.84 %) : P(cible) 39.4 % x 11.82 % + P(rien) 6.7 % x -1.99 % ne couvrent pas P(stop) 53.9 % x 15.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.52 ATR (stop 13.022 %) — p(stop avant cible) 0.4274 [0.38 ; 0.48], R/R 0.623, perte reelle 18.976 % (gap inclus), EV -3.2322 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.23 %) : P(cible) 44.5 % x 11.82 % + P(rien) 12.8 % x -3.02 % ne couvrent pas P(stop) 42.7 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.94 ATR (stop 15.78 %) — p(stop avant cible) 0.3335 [0.29 ; 0.38], R/R 0.497, perte reelle 23.778 % (gap inclus), EV -3.1525 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.15 %) : P(cible) 47.3 % x 11.82 % + P(rien) 19.3 % x -4.24 % ne couvrent pas P(stop) 33.4 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.03 ATR (stop 29.304 %) — p(stop avant cible) 0.064 [0.04 ; 0.09], R/R 0.39, perte reelle 30.323 % (gap inclus), EV -0.1446 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 48.7 % x 11.82 % + P(rien) 44.9 % x -8.82 % ne couvrent pas P(stop) 6.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.621 %) — p(stop avant cible) 0.8934 [0.86 ; 0.92], R/R 3.393, perte reelle 3.485 % (gap inclus), EV -1.921 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.893, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 10.1 % x 11.82 % + P(rien) 0.6 % x 0.31 % ne couvrent pas P(stop) 89.3 % x 3.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.242 %) — p(stop avant cible) 0.8148 [0.77 ; 0.85], R/R 2.024, perte reelle 5.842 % (gap inclus), EV -2.681 % — **REFUSE**
      - refuse : p_stop_first 0.815, borne haute 0.853 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 17.5 % x 11.82 % + P(rien) 1.0 % x 0.41 % ne couvrent pas P(stop) 81.5 % x 5.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.863 %) — p(stop avant cible) 0.739 [0.69 ; 0.78], R/R 1.286, perte reelle 9.197 % (gap inclus), EV -3.8366 % — **REFUSE**
      - refuse : p_stop_first 0.739, borne haute 0.783 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.84 %) : P(cible) 25.0 % x 11.82 % + P(rien) 1.1 % x 0.37 % ne couvrent pas P(stop) 73.9 % x 9.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.484 %) — p(stop avant cible) 0.6765 [0.63 ; 0.72], R/R 1.016, perte reelle 11.636 % (gap inclus), EV -4.2236 % — **REFUSE**
      - refuse : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.22 %) : P(cible) 30.8 % x 11.82 % + P(rien) 1.6 % x 0.48 % ne couvrent pas P(stop) 67.7 % x 11.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.105 %) — p(stop avant cible) 0.6057 [0.55 ; 0.66], R/R 0.876, perte reelle 13.499 % (gap inclus), EV -3.8764 % — **REFUSE**
      - refuse : p_stop_first 0.606, borne haute 0.656 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.88 %) : P(cible) 36.4 % x 11.82 % + P(rien) 3.1 % x 0.06 % ne couvrent pas P(stop) 60.6 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.52 ATR (stop 11.79 %) — p(stop avant cible) 0.4689 [0.42 ; 0.52], R/R 0.669, perte reelle 17.667 % (gap inclus), EV -3.4633 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.46 %) : P(cible) 43.2 % x 11.82 % + P(rien) 9.9 % x -2.91 % ne couvrent pas P(stop) 46.9 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.94 ATR (stop 14.548 %) — p(stop avant cible) 0.3851 [0.33 ; 0.44], R/R 0.569, perte reelle 20.78 % (gap inclus), EV -2.9417 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.94 %) : P(cible) 46.6 % x 11.82 % + P(rien) 14.9 % x -2.99 % ne couvrent pas P(stop) 38.5 % x 20.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 17.832 %) — p(stop avant cible) 0.2754 [0.23 ; 0.32], R/R 0.39, perte reelle 30.323 % (gap inclus), EV -3.8507 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.85 %) : P(cible) 48.0 % x 11.82 % + P(rien) 24.5 % x -4.79 % ne couvrent pas P(stop) 27.5 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 19.453 %) — p(stop avant cible) 0.2237 [0.18 ; 0.27], R/R 0.39, perte reelle 30.323 % (gap inclus), EV -2.709 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.71 %) : P(cible) 48.2 % x 11.82 % + P(rien) 29.4 % x -5.53 % ne couvrent pas P(stop) 22.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 22.695 %) — p(stop avant cible) 0.1541 [0.12 ; 0.20], R/R 0.39, perte reelle 30.323 % (gap inclus), EV -1.4183 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 48.4 % x 11.82 % + P(rien) 36.1 % x -6.84 % ne couvrent pas P(stop) 15.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.03 ATR (stop 28.072 %) — p(stop avant cible) 0.0719 [0.05 ; 0.10], R/R 0.39, perte reelle 30.323 % (gap inclus), EV -0.1815 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 48.7 % x 11.82 % + P(rien) 44.1 % x -8.52 % ne couvrent pas P(stop) 7.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 32.421 %) — p(stop avant cible) 0.0383 [0.02 ; 0.06], R/R 0.365, perte reelle 32.421 % (gap inclus), EV -0.0295 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 48.7 % x 11.82 % + P(rien) 47.5 % x -9.58 % ne couvrent pas P(stop) 3.8 % x 32.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 35.663 %) — p(stop avant cible) 0.0291 [0.02 ; 0.05], R/R 0.332, perte reelle 35.663 % (gap inclus), EV -0.0479 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 48.7 % x 11.82 % + P(rien) 48.4 % x -9.86 % ne couvrent pas P(stop) 2.9 % x 35.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 38.905 %) — p(stop avant cible) 0.0221 [0.01 ; 0.04], R/R 0.304, perte reelle 38.905 % (gap inclus), EV -0.1133 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 48.7 % x 11.82 % + P(rien) 49.1 % x -10.21 % ne couvrent pas P(stop) 2.2 % x 38.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 42.147 %) — p(stop avant cible) 0.0128 [0.00 ; 0.03], R/R 0.281, perte reelle 42.147 % (gap inclus), EV -0.07 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 48.7 % x 11.82 % + P(rien) 50.0 % x -10.58 % ne couvrent pas P(stop) 1.3 % x 42.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 45.389 %) — p(stop avant cible) 0.0102 [0.00 ; 0.03], R/R 0.261, perte reelle 45.389 % (gap inclus), EV -0.1006 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 48.7 % x 11.82 % + P(rien) 50.3 % x -10.73 % ne couvrent pas P(stop) 1.0 % x 45.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 48.631 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.243, perte reelle 48.631 % (gap inclus), EV -0.0982 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 48.7 % x 11.82 % + P(rien) 51.1 % x -11.25 % ne couvrent pas P(stop) 0.2 % x 48.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 51.874 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.228, perte reelle 51.874 % (gap inclus), EV -0.0972 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 48.7 % x 11.82 % + P(rien) 51.3 % x -11.40 % ne couvrent pas P(stop) 0.0 % x 51.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.76, ATR14 0.6329 (6.484 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.428 ATR = 2.775 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.324 % | 9.7284 | 92.55 % | 95.18 % | 96.44 % | 97.12 % | 97.91 % | 98.36 % |
| 0.1 ATR | 0.648 % | 9.6967 | 86.81 % | 91.39 % | 93.33 % | 94.7 % | 96.18 % | 97.42 % |
| 0.15 ATR | 0.973 % | 9.6651 | 80.85 % | 87.14 % | 89.77 % | 91.71 % | 93.86 % | 96.01 % |
| 0.2 ATR | 1.297 % | 9.6334 | 75.23 % | 82.78 % | 86.55 % | 89.29 % | 92.24 % | 94.96 % |
| 0.25 ATR | 1.621 % | 9.6018 | 69.95 % | 79.68 % | 83.91 % | 87.1 % | 90.5 % | 93.79 % |
| 0.35 ATR | 2.269 % | 9.5385 | 58.26 % | 72.1 % | 77.47 % | 82.83 % | 87.49 % | 91.32 % |
| 0.5 ATR | 3.242 % | 9.4436 | 42.32 % | 59.13 % | 67.36 % | 74.31 % | 82.97 % | 88.28 % |
| 0.75 ATR | 4.863 % | 9.2854 | 20.64 % | 37.31 % | 47.82 % | 59.68 % | 72.19 % | 80.66 % |
| 1.0 ATR | 6.484 % | 9.1271 | 11.35 % | 25.83 % | 35.98 % | 49.31 % | 64.31 % | 74.91 % |
| 1.25 ATR | 8.105 % | 8.9689 | 4.7 % | 15.96 % | 25.17 % | 38.59 % | 54.81 % | 68.46 % |
| 1.5 ATR | 9.726 % | 8.8107 | 2.29 % | 9.76 % | 16.21 % | 28.34 % | 45.31 % | 61.66 % |
| 2.0 ATR | 12.968 % | 8.4943 | 0.34 % | 3.21 % | 6.44 % | 14.52 % | 31.29 % | 49.47 % |
| 2.5 ATR | 16.21 % | 8.1779 | 0.11 % | 1.26 % | 2.76 % | 6.8 % | 20.51 % | 38.69 % |
| 3.0 ATR | 19.453 % | 7.8614 | 0.11 % | 0.57 % | 1.72 % | 3.69 % | 11.82 % | 28.72 % |
| 4.0 ATR | 25.937 % | 7.2286 | 0.0 % | 0.23 % | 0.34 % | 1.04 % | 4.52 % | 13.83 % |
| 6.0 ATR | 38.905 % | 5.9629 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.64 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.86 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.29 ATR | 2.79 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.29 ATR | 2.53 ATR | 3.25 ATR | 3.93 ATR |
| **20 s.** | 1.00 ATR | 1.98 ATR | 2.21 ATR | 2.79 ATR | 3.25 ATR | 3.59 ATR | 4.63 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.475–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.242 %, prix 9.4436), p(touche) 42.32 % (en stress 81.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.662–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.863 %, prix 9.2854), p(touche) 37.31 % (en stress 88.64 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.81–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.484 %, prix 9.1272), p(touche) 35.98 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.101–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.105 %, prix 8.969), p(touche) 38.59 % (en stress 95.4 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.511–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.968 %, prix 8.4943), p(touche) 31.29 % (en stress 96.55 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.207–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.21 %, prix 8.1779), p(touche) 38.69 % (en stress 98.84 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.131 | EV/share : $0.032 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.104 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.9 | bear 6.9 | side 9.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 156.0 (= 16 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.298% → cible +5.062% / stop −2.531%, p_fill 58%, n_eff≈25.0) : P(cible|rempli) **20%** · **EV/risk -0.043** (×p_fill ; si rempli -0.19% du capital)
  - **swing** (entrée dip −5.055% → cible +5.927% / stop −6.83%, p_fill 46%, n_eff≈20.3) : P(cible|rempli) **60%** · **EV/risk +0.086** (×p_fill ; si rempli +1.29% du capital)
  - **deep** (entrée dip −7.813% → cible +8.383% / stop −10.551%, p_fill 35%, n_eff≈15.7) : P(cible|rempli) **73%** · **EV/risk +0.101** (×p_fill ; si rempli +3.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→81% · +2.0%→70% · +3.0%→64% · +5.0%→38% · +8.0%→10%
- Range intraday médian 7.05% (p90 12.01%) · excursion haute méd. +3.65% / basse méd. −2.91%
- Profil de vol intra : ouverture 4.639% vs midi 1.458% vs clôture 1.741% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.064)_ ; drift intra méd. 0.255% ; recovery-V 42%
- **σ réalisé intraday** 4.463% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 59% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 9.1709 (VA 9.1311–9.2239 ; dernier close 9.225)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 42% · rebond 76% · **stop −4.13%** sous le fill (sous le bruit) · cible +2.49% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.55% · baisse 58% (gap-down >1% 38% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −1.05% (p90 −3.02%) · haut méd +1.13% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.82%) · haut méd +1.75% · range méd 3.59%
- Excursion ouverture 30min (n=160) : bas méd −1.67% (p90 −4.64%) · haut méd +2.22% · range méd 4.27%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.48%) · haut méd +2.56% · range méd 5.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.21 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (130/159) · gap 51% · délai 0.0min · rebond 65% (82/130) (MFE +1.62%)
   - −1.0% : fill 30min 65% · séance 77% (124/159) · gap 39% · délai 0.0min · rebond 66% (79/124) (MFE +2.08%)
   - −1.5% : fill 30min 60% · séance 72% (117/159) · gap 29% · délai 0.0min · rebond 70% (84/117) (MFE +2.04%)
   - −2.0% : fill 30min 52% · séance 64% (108/159) · gap 24% · délai 0.5min · rebond 67% (74/108) (MFE +2.07%)
   - −3.0% : fill 30min 41% · séance 54% (94/159) · gap 11% · délai 4.4min · rebond 76% (75/94) (MFE +2.2%)
   - −4.0% : fill 30min 33% · séance 49% (85/159) · gap 4% · délai 8.8min · rebond 76% (65/85) (MFE +2.53%)
   - −5.0% : fill 30min 24% · séance 42% (67/159) · gap 2% · délai 22.6min · rebond 76% (50/67) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.67%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.81% (p90 −2.7%) → stop au-delà de −2.1% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −2.8%) → stop au-delà de −2.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1149 jambes) : jambe baissière méd −1.33% (p90 −3.12%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (88 séances) :
      · −1.0% : fill 99% (87/88) · rebond 65% (56/87)
      · −2.0% : fill 89% (81/88) · rebond 73% (60/81)
      · −3.0% : fill 80% (75/88) · rebond 81% (63/75)
      · −4.0% : fill 74% (68/88) · rebond 82% (55/68)
      · −5.0% : fill 62% (52/88) · rebond 82% (42/52)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 48% (4/8)
      · −2.0% : fill 80% (6/10) · rebond 40% (2/6)
      · −3.0% : fill 80% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 80% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 60% (4/10) · rebond 79% (3/4)
   - **gap-up** (61 séances) :
      · −1.0% : fill 46% (29/61) · rebond 74% (19/29)
      · −2.0% : fill 28% (21/61) · rebond 51% (12/21)
      · −3.0% : fill 14% (13/61) · rebond 50% (9/13)
      · −4.0% : fill 12% (11/61) · rebond 35% (6/11)
      · −5.0% : fill 12% (11/61) · rebond 27% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 63% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 17% si rouge (base 49% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **83%** · continue >prix actuel 58% ; creux résiduel méd -1.67% (q20 -3.52%) → **SL/trailing à −3.52%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.07% / q75 +4.1% → **scale +3.07% / runner +4.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.42%** (au-delà de la MAE q10 -5.42%), cible rebond +1.61% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.1% .. +4.62%] · haut q95 +6.16% · bas q05 -5.74%
   - 60min (n=160) : retour [-5.15% .. +4.8%] · haut q95 +6.73% · bas q05 -6.3%
   - 2h (n=160) : retour [-6.23% .. +5.45%] · haut q95 +7.93% · bas q05 -7.94%
   - 4h (n=160) : retour [-7.17% .. +7.04%] · haut q95 +8.74% · bas q05 -8.19%
   - 6h (n=160) : retour [-6.99% .. +8.15%] · haut q95 +10.34% · bas q05 -8.89%
   - session (n=160) : retour [-7.0% .. +8.86%] · haut q95 +10.69% · bas q05 -8.84%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.85%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.6  _(neutre)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist 0.031  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 14.1%
- **ATR** : 0.63 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.037  _(neutre)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 62.0  _(marche en range (choppy))_
- **MA** : MA20 9.41 · MA50 9.11 · MA200 13.07  _(prix > MA20)_
- **Dist MA** : MA20 +3.7% · MA50 +7.1% · MA200 -25.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760806 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
