# AL2SI

**Generated** : 2026-09-03T21:47:15.956676+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.52  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €27.52 (+2.0% vs entrée) · entrée €26.97 · stop €26.36 · T1 €28.18 · R/R 1.98  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk -0.238 _(réel 5 s)_ (GBM 0.138) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.24% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €26.87–€27.07 (mid €26.97)
- Spot actuel : €27.52 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €26.36 (stop swing_plan-based (-9.7%))
- Targets : T1 €28.18 · R/R 1.98 | T2 €28.31 · R/R 2.2 | T3 €28.45 · R/R 2.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.36


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.7 %)** : le gap seul le franchit 0.547 % des séances (7 fois sur 1280).
   - exécution **8.26 pt plus bas** dans le cas TYPIQUE (médiane), 21.846 au p90, **28.417 au pire**
   - perte réelle **20.706 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 9.7 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0602 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5629** [0.4885 ; 0.6352] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4093** [0.3584 ; 0.4617] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3611** [0.3118 ; 0.4127] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.1 pt), swing (37.8 pt), deep (36.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.28 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.13 % contre 7.26 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2094** (β de hausse 0.9487, asymétrie 1.2747) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.933× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 24.235 sur atr_grid (2.25 ATR, 11.937 %) — p(stop avant cible) 0.28 [0.23 ; 0.33], R/R 0.369, perte reelle 24.668 % (gap inclus), CVaR 11.987 %, EV -2.1065 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.4 % de la queue et il ne reste que -955.87 EUR a partager. Prix du risque -0.692 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.958 %) — p(stop avant cible) 0.4683 [0.42 ; 0.52], R/R 0.554, perte reelle 16.422 % (gap inclus), EV -3.4184 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.42 %) : P(cible) 46.4 % x 9.09 % + P(rien) 6.8 % x 0.82 % ne couvrent pas P(stop) 46.8 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.51 ATR (stop 10.594 %) — p(stop avant cible) 0.3266 [0.28 ; 0.38], R/R 0.404, perte reelle 22.515 % (gap inclus), EV -2.577 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.58 %) : P(cible) 54.5 % x 9.09 % + P(rien) 12.8 % x -1.41 % ne couvrent pas P(stop) 32.7 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.37 ATR (stop 20.477 %) — p(stop avant cible) 0.148 [0.11 ; 0.19], R/R 0.303, perte reelle 30.031 % (gap inclus), EV -0.475 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 57.7 % x 9.09 % + P(rien) 27.5 % x -4.64 % ne couvrent pas P(stop) 14.8 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.08 ATR (stop 29.562 %) — p(stop avant cible) 0.0867 [0.06 ; 0.12], R/R 0.239, perte reelle 38.117 % (gap inclus), EV -0.2876 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 57.7 % x 9.09 % + P(rien) 33.6 % x -6.63 % ne couvrent pas P(stop) 8.7 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.326 %) — p(stop avant cible) 0.8311 [0.79 ; 0.87], R/R 2.571, perte reelle 3.536 % (gap inclus), EV -1.4092 % — **REFUSE**
      - refuse : p_stop_first 0.831, borne haute 0.868 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.41 %) : P(cible) 16.8 % x 9.09 % + P(rien) 0.1 % x 1.54 % ne couvrent pas P(stop) 83.1 % x 3.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.653 %) — p(stop avant cible) 0.7239 [0.68 ; 0.77], R/R 1.356, perte reelle 6.707 % (gap inclus), EV -2.393 % — **REFUSE**
      - refuse : p_stop_first 0.724, borne haute 0.769 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.39 %) : P(cible) 26.9 % x 9.09 % + P(rien) 0.7 % x 2.60 % ne couvrent pas P(stop) 72.4 % x 6.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.979 %) — p(stop avant cible) 0.6579 [0.61 ; 0.71], R/R 0.998, perte reelle 9.107 % (gap inclus), EV -2.958 % — **REFUSE**
      - refuse : p_stop_first 0.658, borne haute 0.706 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.96 %) : P(cible) 33.0 % x 9.09 % + P(rien) 1.2 % x 2.94 % ne couvrent pas P(stop) 65.8 % x 9.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.305 %) — p(stop avant cible) 0.5895 [0.54 ; 0.64], R/R 0.725, perte reelle 12.539 % (gap inclus), EV -3.8211 % — **REFUSE**
      - refuse : p_stop_first 0.590, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.82 %) : P(cible) 38.3 % x 9.09 % + P(rien) 2.8 % x 3.28 % ne couvrent pas P(stop) 59.0 % x 12.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 6.632 %) — p(stop avant cible) 0.5179 [0.47 ; 0.57], R/R 0.629, perte reelle 14.446 % (gap inclus), EV -3.4508 % — **REFUSE**
      - refuse : p_stop_first 0.518, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.45 %) : P(cible) 43.4 % x 9.09 % + P(rien) 4.8 % x 1.70 % ne couvrent pas P(stop) 51.8 % x 14.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.51 ATR (stop 9.586 %) — p(stop avant cible) 0.3723 [0.32 ; 0.42], R/R 0.439, perte reelle 20.706 % (gap inclus), EV -3.0837 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.08 %) : P(cible) 51.9 % x 9.09 % + P(rien) 10.9 % x -0.83 % ne couvrent pas P(stop) 37.2 % x 20.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.937 %) — p(stop avant cible) 0.28 [0.23 ; 0.33], R/R 0.369, perte reelle 24.668 % (gap inclus), EV -2.1065 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.11 %) : P(cible) 56.1 % x 9.09 % + P(rien) 15.9 % x -1.92 % ne couvrent pas P(stop) 28.0 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 13.263 %) — p(stop avant cible) 0.2538 [0.21 ; 0.30], R/R 0.369, perte reelle 24.668 % (gap inclus), EV -1.4394 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.44 %) : P(cible) 56.9 % x 9.09 % + P(rien) 17.7 % x -2.01 % ne couvrent pas P(stop) 25.4 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 14.589 %) — p(stop avant cible) 0.242 [0.20 ; 0.29], R/R 0.369, perte reelle 24.668 % (gap inclus), EV -1.2052 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 57.1 % x 9.09 % + P(rien) 18.7 % x -2.29 % ne couvrent pas P(stop) 24.2 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 15.916 %) — p(stop avant cible) 0.2208 [0.18 ; 0.27], R/R 0.337, perte reelle 27.014 % (gap inclus), EV -1.3107 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 57.2 % x 9.09 % + P(rien) 20.7 % x -2.66 % ne couvrent pas P(stop) 22.1 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.37 ATR (stop 19.469 %) — p(stop avant cible) 0.173 [0.14 ; 0.22], R/R 0.303, perte reelle 30.031 % (gap inclus), EV -0.9106 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 57.7 % x 9.09 % + P(rien) 25.0 % x -3.84 % ne couvrent pas P(stop) 17.3 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 21.221 %) — p(stop avant cible) 0.1442 [0.11 ; 0.18], R/R 0.303, perte reelle 30.031 % (gap inclus), EV -0.4118 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 57.7 % x 9.09 % + P(rien) 27.9 % x -4.76 % ne couvrent pas P(stop) 14.4 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 23.874 %) — p(stop avant cible) 0.1133 [0.08 ; 0.15], R/R 0.303, perte reelle 30.031 % (gap inclus), EV 0.1167 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.89 % > budget 12.00 %
   - 🟢 grid_snapped a 5.08 ATR (stop 28.554 %) — p(stop avant cible) 0.0872 [0.06 ; 0.12], R/R 0.239, perte reelle 38.117 % (gap inclus), EV -0.297 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 57.7 % x 9.09 % + P(rien) 33.6 % x -6.61 % ne couvrent pas P(stop) 8.7 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 31.831 %) — p(stop avant cible) 0.0807 [0.06 ; 0.11], R/R 0.239, perte reelle 38.117 % (gap inclus), EV -0.174 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 57.7 % x 9.09 % + P(rien) 34.2 % x -6.85 % ne couvrent pas P(stop) 8.1 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 34.484 %) — p(stop avant cible) 0.0598 [0.04 ; 0.09], R/R 0.239, perte reelle 38.117 % (gap inclus), EV 0.2736 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 37.137 %) — p(stop avant cible) 0.0537 [0.03 ; 0.08], R/R 0.239, perte reelle 38.117 % (gap inclus), EV 0.4159 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 39.789 %) — p(stop avant cible) 0.0394 [0.02 ; 0.06], R/R 0.229, perte reelle 39.789 % (gap inclus), EV 0.6548 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.79 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 42.442 %) — p(stop avant cible) 0.0394 [0.02 ; 0.06], R/R 0.214, perte reelle 42.442 % (gap inclus), EV 0.5502 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.44 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.52, ATR14 1.46 (5.305 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.399 ATR = 2.117 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.265 % | 27.447 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.531 % | 27.374 | 82.45 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 95.9 % |
| 0.15 ATR | 0.796 % | 27.301 | 78.43 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.71 % |
| 0.2 ATR | 1.061 % | 27.228 | 72.55 % | 79.2 % | 83.2 % | 85.73 % | 89.42 % | 92.51 % |
| 0.25 ATR | 1.326 % | 27.155 | 66.47 % | 74.58 % | 79.08 % | 82.38 % | 87.14 % | 90.91 % |
| 0.35 ATR | 1.857 % | 27.009 | 54.41 % | 65.75 % | 70.92 % | 75.69 % | 82.29 % | 87.61 % |
| 0.5 ATR | 2.653 % | 26.79 | 40.78 % | 54.17 % | 61.89 % | 68.8 % | 77.74 % | 85.11 % |
| 0.75 ATR | 3.979 % | 26.425 | 22.75 % | 37.88 % | 47.84 % | 55.81 % | 66.96 % | 76.42 % |
| 1.0 ATR | 5.305 % | 26.06 | 13.04 % | 25.42 % | 34.48 % | 44.88 % | 57.37 % | 68.23 % |
| 1.25 ATR | 6.632 % | 25.695 | 7.75 % | 17.86 % | 25.15 % | 36.52 % | 50.45 % | 62.14 % |
| 1.5 ATR | 7.958 % | 25.33 | 3.82 % | 11.48 % | 17.78 % | 28.84 % | 43.42 % | 56.04 % |
| 2.0 ATR | 10.61 % | 24.6 | 0.88 % | 5.3 % | 9.82 % | 17.13 % | 31.95 % | 44.46 % |
| 2.5 ATR | 13.263 % | 23.87 | 0.1 % | 2.36 % | 4.91 % | 10.43 % | 22.06 % | 34.67 % |
| 3.0 ATR | 15.916 % | 23.14 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.02 % | 27.37 % |
| 4.0 ATR | 21.221 % | 21.68 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 18.68 % |
| 6.0 ATR | 31.831 % | 18.76 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 8.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.01 ATR | 1.18 ATR | 1.62 ATR | 2.05 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.25 ATR | 1.43 ATR | 1.99 ATR | 2.49 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 1.00 ATR | 1.36 ATR | 1.66 ATR | 1.88 ATR | 2.56 ATR | 3.52 ATR |
| **10 s.** | 0.56 ATR | 1.27 ATR | 1.44 ATR | 1.95 ATR | 2.35 ATR | 2.67 ATR | 3.92 ATR | 5.28 ATR |
| **20 s.** | 0.79 ATR | 1.76 ATR | 1.98 ATR | 2.61 ATR | 3.27 ATR | 3.85 ATR | 5.79 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.454–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.653 %, prix 26.7899), p(touche) 40.78 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (93.8 % des re-echantillons)
- **2 seance(s)** : plage utile 0.641–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.979 %, prix 26.425), p(touche) 37.88 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.305 %, prix 26.0601), p(touche) 34.48 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.997–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.305 %, prix 26.0601), p(touche) 44.88 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.444–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.958 %, prix 25.33), p(touche) 43.42 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.977–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.61 %, prix 24.6001), p(touche) 44.46 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.138 | EV/share : €0.084 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.072 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 6.3 | side 8.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 385.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.002% → cible +4.486% / stop −2.243%, p_fill 59%, n_eff≈27.0) : P(cible|rempli) **10%** · **EV/risk -0.238** (×p_fill ; si rempli -0.90% du capital)
  - **swing** (entrée dip −4.395% → cible +4.083% / stop −5.549%, p_fill 41%, n_eff≈23.9) : P(cible|rempli) **58%** · **EV/risk +0.013** (×p_fill ; si rempli +0.18% du capital)
  - **deep** (entrée dip −6.792% → cible +5.774% / stop −8.538%, p_fill 56%, n_eff≈25.1) : P(cible|rempli) **64%** · **EV/risk +0.035** (×p_fill ; si rempli +0.54% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→75% · +2.0%→66% · +3.0%→52% · +5.0%→42% · +8.0%→20%
- Range intraday médian 7.5% (p90 22.19%) · excursion haute méd. +3.87% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.305% vs midi 1.705% vs clôture 1.811% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.096)_ ; drift intra méd. -0.368% ; recovery-V 21%
- **σ réalisé intraday** 5.086% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 72% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 25.5693 (VA 25.5693–25.7103 ; dernier close 25.66)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 89% · **stop −5.18%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 41% (gap-down >1% 13% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −4.35%) · haut méd +0.77% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −5.24%) · haut méd +1.24% · range méd 3.08%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −5.56%) · haut méd +1.94% · range méd 3.94%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −6.11%) · haut méd +2.06% · range méd 4.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 25.72 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 79% (122/159) · gap 22% · délai 0.3min · rebond 63% (84/122) (MFE +2.11%)
   - −1.0% : fill 30min 50% · séance 75% (116/159) · gap 13% · délai 1.2min · rebond 62% (78/116) (MFE +1.88%)
   - −1.5% : fill 30min 42% · séance 68% (103/159) · gap 9% · délai 6.7min · rebond 60% (64/103) (MFE +1.45%)
   - −2.0% : fill 30min 36% · séance 62% (95/159) · gap 5% · délai 13.6min · rebond 62% (60/95) (MFE +1.56%)
   - −3.0% : fill 30min 23% · séance 52% (81/159) · gap 4% · délai 41.0min · rebond 61% (58/81) (MFE +1.55%)
   - −4.0% : fill 30min 19% · séance 42% (69/159) · gap 3% · délai 86.3min · rebond 76% (56/69) (MFE +1.91%)
   - −5.0% : fill 30min 13% · séance 31% (57/159) · gap 2% · délai 85.2min · rebond 89% (52/57) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −4.28%) → stop au-delà de −1.87% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.07% (p90 −4.55%) → stop au-delà de −2.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −5.09%) → stop au-delà de −3.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1522 jambes) : jambe baissière méd −1.25% (p90 −3.19%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 95% (46/49) · rebond 53% (27/46)
      · −2.0% : fill 85% (42/49) · rebond 54% (24/42)
      · −3.0% : fill 79% (40/49) · rebond 65% (30/40)
      · −4.0% : fill 68% (36/49) · rebond 67% (28/36)
      · −5.0% : fill 51% (31/49) · rebond 79% (27/31)
   - **flat** (30 séances) :
      · −1.0% : fill 72% (23/30) · rebond 65% (16/23)
      · −2.0% : fill 49% (18/30) · rebond 57% (12/18)
      · −3.0% : fill 41% (13/30) · rebond 53% (8/13)
      · −4.0% : fill 36% (12/30) · rebond 85% (10/12)
      · −5.0% : fill 22% (9/30) · rebond 100% (9/9)
   - **gap-up** (80 séances) :
      · −1.0% : fill 64% (47/80) · rebond 67% (35/47)
      · −2.0% : fill 54% (35/80) · rebond 73% (24/35)
      · −3.0% : fill 41% (28/80) · rebond 60% (20/28)
      · −4.0% : fill 29% (21/80) · rebond 84% (18/21)
      · −5.0% : fill 23% (17/80) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 55% si les 15 1res min sont vertes (73 cas) · 31% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:02** → P(séance verte=clôture>ouverture) 73% si début vert vs 12% si rouge (base 43% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 43% ; creux résiduel méd -2.73% (q20 -4.95%) → **SL/trailing à −4.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.37% → **scale +1.72% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **12%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.51%** (au-delà de la MAE q10 -6.51%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.01% .. +6.19%] · haut q95 +7.8% · bas q05 -7.17%
   - 60min (n=160) : retour [-5.76% .. +6.19%] · haut q95 +8.32% · bas q05 -7.63%
   - 2h (n=160) : retour [-5.84% .. +8.72%] · haut q95 +9.95% · bas q05 -7.84%
   - 4h (n=160) : retour [-6.32% .. +8.85%] · haut q95 +11.46% · bas q05 -9.54%
   - 6h (n=160) : retour [-6.7% .. +9.28%] · haut q95 +12.72% · bas q05 -10.21%
   - session (n=160) : retour [-7.57% .. +11.44%] · haut q95 +13.24% · bas q05 -11.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.5  _(neutre)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 0.253  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 12.9%
- **ATR** : 1.46 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.173  _(distribution)_
- **Vol ratio** : 1.85  _(volume au-dessus de la moyenne)_
- **Choppiness** : 60.9  _(transition)_
- **MA** : MA20 27.1 · MA50 28.36 · MA200 26.42  _(prix > MA20)_
- **Dist MA** : MA20 +1.6% · MA50 -3.0% · MA200 +4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (767631 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
