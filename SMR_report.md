# SMR

**Generated** : 2026-08-28T00:32:50.583568+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.74  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $9.74 (+2.3% vs entrée) · entrée $9.52 · stop $9.31 · T1 $9.90 · R/R 1.81  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk -0.196 _(réel 5 s)_ (GBM 0.059) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.21% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.47–$9.57 (mid $9.52)
- Spot actuel : $9.74 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : $9.31 (stop swing_plan-based (-12.15%))
- Targets : T1 $9.90 · R/R 1.81 | T2 $10.10 · R/R 2.76 | T3 $10.30 · R/R 3.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.31


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.15 %)** : le gap seul le franchit 0.444 % des séances (5 fois sur 1127).
   - exécution **2.635 pt plus bas** dans le cas TYPIQUE (médiane), 12.937 au p90, **18.173 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 12.15 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0245 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.43 % | p01 -6.963 % | pire -30.323 % _(sur 1127 séances)_
- **P(stop avant cible)** _(source : daily, 1128 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.6061** [0.532 ; 0.6766] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4659** [0.4137 ; 0.5186] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.4406** [0.3889 ; 0.4933] _(largeur 10.4 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.6 pt), swing (38.6 pt), deep (41.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.94 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.01 % contre 5.92 % aujourd'hui, rapport 1.86)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.97 % vs -18.68 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6004** (β de hausse 1.3622, asymétrie 1.1748) vs IWM — 534 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.008× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.5491 sur sr_based (1.35 ATR, 12.227 %) — p(stop avant cible) 0.4725 [0.42 ; 0.53], R/R 0.709, perte reelle 17.667 % (gap inclus), CVaR 12.251 %, EV -3.5197 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0209 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.25 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.35 ATR (stop 12.227 %) — p(stop avant cible) 0.4725 [0.42 ; 0.53], R/R 0.709, perte reelle 17.667 % (gap inclus), EV -3.5197 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 41.4 % x 12.53 % + P(rien) 11.3 % x -3.22 % ne couvrent pas P(stop) 47.2 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.73 ATR (stop 14.921 %) — p(stop avant cible) 0.3874 [0.34 ; 0.44], R/R 0.527, perte reelle 23.778 % (gap inclus), EV -4.2565 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.26 %) : P(cible) 44.1 % x 12.53 % + P(rien) 17.2 % x -3.29 % ne couvrent pas P(stop) 38.7 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.61 ATR (stop 28.473 %) — p(stop avant cible) 0.0712 [0.05 ; 0.10], R/R 0.413, perte reelle 30.323 % (gap inclus), EV -0.3791 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 45.9 % x 12.53 % + P(rien) 47.0 % x -8.45 % ne couvrent pas P(stop) 7.1 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.799 %) — p(stop avant cible) 0.8916 [0.86 ; 0.92], R/R 3.349, perte reelle 3.741 % (gap inclus), EV -2.0519 % — **REFUSE**
      - refuse : cible atteinte seulement 10.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.892, borne haute 0.921 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 10.2 % x 12.53 % + P(rien) 0.6 % x 0.31 % ne couvrent pas P(stop) 89.2 % x 3.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.599 %) — p(stop avant cible) 0.812 [0.77 ; 0.85], R/R 1.975, perte reelle 6.345 % (gap inclus), EV -2.9213 % — **REFUSE**
      - refuse : p_stop_first 0.812, borne haute 0.851 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.92 %) : P(cible) 17.8 % x 12.53 % + P(rien) 1.0 % x 0.44 % ne couvrent pas P(stop) 81.2 % x 6.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.398 %) — p(stop avant cible) 0.7322 [0.68 ; 0.78], R/R 1.215, perte reelle 10.315 % (gap inclus), EV -4.3826 % — **REFUSE**
      - refuse : p_stop_first 0.732, borne haute 0.777 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.38 %) : P(cible) 25.2 % x 12.53 % + P(rien) 1.6 % x 0.81 % ne couvrent pas P(stop) 73.2 % x 10.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 7.198 %) — p(stop avant cible) 0.6644 [0.61 ; 0.71], R/R 0.928, perte reelle 13.499 % (gap inclus), EV -5.0369 % — **REFUSE**
      - refuse : p_stop_first 0.664, borne haute 0.713 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.04 %) : P(cible) 31.2 % x 12.53 % + P(rien) 2.4 % x 1.07 % ne couvrent pas P(stop) 66.4 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.195 %) — p(stop avant cible) 0.3357 [0.29 ; 0.39], R/R 0.527, perte reelle 23.778 % (gap inclus), EV -3.2633 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.26 %) : P(cible) 44.6 % x 12.53 % + P(rien) 21.8 % x -4.01 % ne couvrent pas P(stop) 33.6 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 17.995 %) — p(stop avant cible) 0.2797 [0.23 ; 0.33], R/R 0.413, perte reelle 30.323 % (gap inclus), EV -4.0616 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.06 %) : P(cible) 45.4 % x 12.53 % + P(rien) 26.7 % x -4.74 % ne couvrent pas P(stop) 28.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 19.794 %) — p(stop avant cible) 0.2123 [0.17 ; 0.26], R/R 0.413, perte reelle 30.323 % (gap inclus), EV -2.6702 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.67 %) : P(cible) 45.6 % x 12.53 % + P(rien) 33.1 % x -5.88 % ne couvrent pas P(stop) 21.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 21.594 %) — p(stop avant cible) 0.178 [0.14 ; 0.22], R/R 0.413, perte reelle 30.323 % (gap inclus), EV -2.0072 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.01 %) : P(cible) 45.7 % x 12.53 % + P(rien) 36.5 % x -6.39 % ne couvrent pas P(stop) 17.8 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 32.39 %) — p(stop avant cible) 0.0395 [0.02 ; 0.06], R/R 0.387, perte reelle 32.39 % (gap inclus), EV -0.2487 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 45.9 % x 12.53 % + P(rien) 50.1 % x -9.42 % ne couvrent pas P(stop) 4.0 % x 32.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 35.989 %) — p(stop avant cible) 0.03 [0.02 ; 0.05], R/R 0.348, perte reelle 35.989 % (gap inclus), EV -0.2772 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 45.9 % x 12.53 % + P(rien) 51.1 % x -9.69 % ne couvrent pas P(stop) 3.0 % x 35.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 39.588 %) — p(stop avant cible) 0.0189 [0.01 ; 0.04], R/R 0.316, perte reelle 39.588 % (gap inclus), EV -0.3241 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 45.9 % x 12.53 % + P(rien) 52.2 % x -10.21 % ne couvrent pas P(stop) 1.9 % x 39.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 43.187 %) — p(stop avant cible) 0.0129 [0.00 ; 0.03], R/R 0.29, perte reelle 43.187 % (gap inclus), EV -0.3006 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 45.9 % x 12.53 % + P(rien) 52.8 % x -10.41 % ne couvrent pas P(stop) 1.3 % x 43.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 46.786 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 0.268, perte reelle 46.786 % (gap inclus), EV -0.3239 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 45.9 % x 12.53 % + P(rien) 53.3 % x -10.69 % ne couvrent pas P(stop) 0.8 % x 46.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 50.385 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.249, perte reelle 50.385 % (gap inclus), EV -0.3203 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 45.9 % x 12.53 % + P(rien) 53.9 % x -11.08 % ne couvrent pas P(stop) 0.2 % x 50.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 53.984 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.232, perte reelle 53.984 % (gap inclus), EV -0.316 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 45.9 % x 12.53 % + P(rien) 54.1 % x -11.21 % ne couvrent pas P(stop) 0.0 % x 53.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 57.583 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.218, perte reelle 57.583 % (gap inclus), EV -0.3115 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 45.9 % x 12.53 % + P(rien) 54.1 % x -11.21 % ne couvrent pas P(stop) 0.0 % x 57.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.74, ATR14 0.7011 (7.198 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.429 ATR = 3.088 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.36 % | 9.7049 | 92.62 % | 95.15 % | 96.42 % | 97.1 % | 97.9 % | 98.35 % |
| 0.1 ATR | 0.72 % | 9.6699 | 86.97 % | 91.34 % | 93.29 % | 94.67 % | 96.15 % | 97.41 % |
| 0.15 ATR | 1.08 % | 9.6348 | 80.97 % | 87.07 % | 89.71 % | 91.66 % | 93.82 % | 95.99 % |
| 0.2 ATR | 1.44 % | 9.5998 | 75.43 % | 82.79 % | 86.47 % | 89.22 % | 92.19 % | 94.93 % |
| 0.25 ATR | 1.799 % | 9.5647 | 70.13 % | 79.68 % | 83.82 % | 87.02 % | 90.56 % | 93.75 % |
| 0.35 ATR | 2.519 % | 9.4946 | 58.36 % | 72.06 % | 77.46 % | 82.85 % | 87.53 % | 91.39 % |
| 0.5 ATR | 3.599 % | 9.3895 | 42.45 % | 59.12 % | 67.28 % | 74.28 % | 82.98 % | 88.33 % |
| 0.75 ATR | 5.398 % | 9.2142 | 20.76 % | 37.41 % | 47.86 % | 59.79 % | 72.38 % | 80.66 % |
| 1.0 ATR | 7.198 % | 9.0389 | 11.42 % | 25.87 % | 35.95 % | 49.36 % | 64.45 % | 75.12 % |
| 1.25 ATR | 8.997 % | 8.8637 | 4.73 % | 16.05 % | 25.32 % | 38.7 % | 54.9 % | 68.75 % |
| 1.5 ATR | 10.797 % | 8.6884 | 2.31 % | 9.82 % | 16.3 % | 28.39 % | 45.45 % | 62.03 % |
| 2.0 ATR | 14.396 % | 8.3379 | 0.35 % | 3.23 % | 6.47 % | 14.6 % | 31.47 % | 49.76 % |
| 2.5 ATR | 17.995 % | 7.9873 | 0.12 % | 1.27 % | 2.77 % | 6.84 % | 20.63 % | 38.92 % |
| 3.0 ATR | 21.594 % | 7.6368 | 0.12 % | 0.58 % | 1.73 % | 3.71 % | 11.89 % | 28.89 % |
| 4.0 ATR | 28.791 % | 6.9357 | 0.0 % | 0.23 % | 0.35 % | 1.04 % | 4.55 % | 13.92 % |
| 6.0 ATR | 43.187 % | 5.5336 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.65 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.48 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.30 ATR | 2.79 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.52 ATR | 1.95 ATR | 2.30 ATR | 2.54 ATR | 3.26 ATR | 3.94 ATR |
| **20 s.** | 1.00 ATR | 1.99 ATR | 2.22 ATR | 2.79 ATR | 3.26 ATR | 3.59 ATR | 4.64 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.476–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.599 %, prix 9.3895), p(touche) 42.45 % (en stress 81.61 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.398 %, prix 9.2142), p(touche) 37.41 % (en stress 88.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.81–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.198 %, prix 9.0389), p(touche) 35.95 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.102–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.997 %, prix 8.8637), p(touche) 38.7 % (en stress 95.4 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.516–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.396 %, prix 8.3378), p(touche) 31.47 % (en stress 96.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.22–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.995 %, prix 7.9873), p(touche) 38.92 % (en stress 98.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.059 | EV/share : $0.013 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.075 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.5 | bear 7.1 | side 9.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 156.0 (= 16 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.251% → cible +3.985% / stop −2.209%, p_fill 60%, n_eff≈25.1) : P(cible|rempli) **15%** · **EV/risk -0.196** (×p_fill ; si rempli -0.73% du capital)
  - **swing** (entrée dip −4.952% → cible +6.131% / stop −7.573%, p_fill 52%, n_eff≈22.4) : P(cible|rempli) **59%** · **EV/risk +0.053** (×p_fill ; si rempli +0.76% du capital)
  - **deep** (entrée dip −7.653% → cible +8.672% / stop −11.692%, p_fill 36%, n_eff≈19.0) : P(cible|rempli) **63%** · **EV/risk +0.015** (×p_fill ; si rempli +0.51% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 49.4  _(neutre)_
- **ADX** : 13.9  _(pas de tendance nette)_
- **MACD** : hist 0.048  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 16.8%
- **ATR** : 0.7 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.041  _(neutre)_
- **Vol ratio** : 1.1  _(volume normal)_
- **Choppiness** : 65.9  _(marche en range (choppy))_
- **MA** : MA20 9.35 · MA50 9.26 · MA200 13.47  _(prix > MA20)_
- **Dist MA** : MA20 +4.2% · MA50 +5.2% · MA200 -27.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841894 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
