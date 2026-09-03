# SMR

**Generated** : 2026-09-03T00:32:08.146022+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.56  

> 🟡 **WAIT-FOR-DIP** — spot +1.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $9.56 (+1.8% vs entrée) · entrée $9.39 · stop $9.07 · T1 $10.02 · R/R 1.97  
> ↳ P(T1 av. stop) 13 % _(réel 5 s)_ · EV/risk 0.124 _(réel 5 s)_ (GBM 0.101) · ¼-Kelly 0.036 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.37% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +3.1 % ≠ (strike 9.5 − spot 9.56)/spot = -0.6 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.34–$9.44 (mid $9.39)
- Spot actuel : $9.56 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $9.07 (stop swing_plan-based (-10.81%))
- Targets : T1 $10.02 · R/R 1.97 | T2 $10.07 · R/R 2.12 | T3 $10.13 · R/R 2.31
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.07


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.37 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.81 %)** : le gap seul le franchit 0.442 % des séances (5 fois sur 1131).
   - exécution **3.975 pt plus bas** dans le cas TYPIQUE (médiane), 14.277 au p90, **19.513 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 10.81 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0303 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.453 % | p01 -6.962 % | pire -30.323 % _(sur 1131 séances)_
- **P(stop avant cible)** _(source : daily, 1132 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4857** [0.412 ; 0.5599] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5425** [0.4898 ; 0.5945] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.5626** [0.5099 ; 0.6142] _(largeur 10.4 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.2 pt), swing (36.9 pt), deep (37.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.93 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.96 % contre 5.91 % aujourd'hui, rapport 1.85)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.96 % vs -18.65 % si l'on extrapolait par √5 _(rapport 1.016 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6027** (β de hausse 1.3626, asymétrie 1.1763) vs IWM — 537 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.877× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.4777 sur sr_based (1.17 ATR, 11.321 %) — p(stop avant cible) 0.4876 [0.44 ; 0.54], R/R 0.721, perte reelle 17.667 % (gap inclus), CVaR 11.349 %, EV -3.689 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.17 ATR (stop 11.321 %) — p(stop avant cible) 0.4876 [0.44 ; 0.54], R/R 0.721, perte reelle 17.667 % (gap inclus), EV -3.689 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.69 %) : P(cible) 40.4 % x 12.74 % + P(rien) 10.9 % x -2.00 % ne couvrent pas P(stop) 48.8 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.58 ATR (stop 14.119 %) — p(stop avant cible) 0.4019 [0.35 ; 0.45], R/R 0.613, perte reelle 20.78 % (gap inclus), EV -3.1448 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.14 %) : P(cible) 43.5 % x 12.74 % + P(rien) 16.3 % x -2.05 % ne couvrent pas P(stop) 40.2 % x 20.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.62 ATR (stop 27.927 %) — p(stop avant cible) 0.0723 [0.05 ; 0.10], R/R 0.42, perte reelle 30.323 % (gap inclus), EV -0.1899 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 45.1 % x 12.74 % + P(rien) 47.7 % x -7.85 % ne couvrent pas P(stop) 7.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.7 %) — p(stop avant cible) 0.8913 [0.86 ; 0.92], R/R 3.494, perte reelle 3.647 % (gap inclus), EV -1.9396 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.921 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 10.3 % x 12.74 % + P(rien) 0.6 % x 0.36 % ne couvrent pas P(stop) 89.1 % x 3.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.4 %) — p(stop avant cible) 0.8179 [0.77 ; 0.86], R/R 2.118, perte reelle 6.016 % (gap inclus), EV -2.7225 % — **REFUSE**
      - refuse : p_stop_first 0.818, borne haute 0.856 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.72 %) : P(cible) 17.2 % x 12.74 % + P(rien) 1.0 % x 0.47 % ne couvrent pas P(stop) 81.8 % x 6.02 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.099 %) — p(stop avant cible) 0.7405 [0.69 ; 0.78], R/R 1.328, perte reelle 9.596 % (gap inclus), EV -3.9453 % — **REFUSE**
      - refuse : p_stop_first 0.741, borne haute 0.785 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.95 %) : P(cible) 24.7 % x 12.74 % + P(rien) 1.2 % x 0.73 % ne couvrent pas P(stop) 74.1 % x 9.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.17 ATR (stop 10.016 %) — p(stop avant cible) 0.5426 [0.49 ; 0.59], R/R 0.82, perte reelle 15.541 % (gap inclus), EV -3.7109 % — **REFUSE**
      - refuse : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.71 %) : P(cible) 37.9 % x 12.74 % + P(rien) 7.8 % x -1.36 % ne couvrent pas P(stop) 54.3 % x 15.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.58 ATR (stop 12.814 %) — p(stop avant cible) 0.445 [0.39 ; 0.50], R/R 0.672, perte reelle 18.976 % (gap inclus), EV -3.4258 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.43 %) : P(cible) 42.0 % x 12.74 % + P(rien) 13.5 % x -2.45 % ne couvrent pas P(stop) 44.5 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 15.298 %) — p(stop avant cible) 0.3598 [0.31 ; 0.41], R/R 0.536, perte reelle 23.778 % (gap inclus), EV -3.6253 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.63 %) : P(cible) 43.7 % x 12.74 % + P(rien) 20.3 % x -3.16 % ne couvrent pas P(stop) 36.0 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 16.998 %) — p(stop avant cible) 0.298 [0.25 ; 0.35], R/R 0.536, perte reelle 23.778 % (gap inclus), EV -2.4235 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 44.3 % x 12.74 % + P(rien) 25.9 % x -3.78 % ne couvrent pas P(stop) 29.8 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 18.698 %) — p(stop avant cible) 0.2527 [0.21 ; 0.30], R/R 0.42, perte reelle 30.323 % (gap inclus), EV -3.3543 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.35 %) : P(cible) 44.6 % x 12.74 % + P(rien) 30.1 % x -4.57 % ne couvrent pas P(stop) 25.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 20.397 %) — p(stop avant cible) 0.204 [0.16 ; 0.25], R/R 0.42, perte reelle 30.323 % (gap inclus), EV -2.3413 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 44.8 % x 12.74 % + P(rien) 34.8 % x -5.37 % ne couvrent pas P(stop) 20.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.62 ATR (stop 26.621 %) — p(stop avant cible) 0.0773 [0.05 ; 0.11], R/R 0.42, perte reelle 30.323 % (gap inclus), EV -0.2409 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 45.1 % x 12.74 % + P(rien) 47.2 % x -7.72 % ne couvrent pas P(stop) 7.7 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 30.596 %) — p(stop avant cible) 0.0515 [0.03 ; 0.08], R/R 0.417, perte reelle 30.596 % (gap inclus), EV -0.0711 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 45.1 % x 12.74 % + P(rien) 49.8 % x -8.52 % ne couvrent pas P(stop) 5.1 % x 30.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 33.996 %) — p(stop avant cible) 0.0343 [0.02 ; 0.06], R/R 0.375, perte reelle 33.996 % (gap inclus), EV -0.0403 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 45.1 % x 12.74 % + P(rien) 51.5 % x -8.98 % ne couvrent pas P(stop) 3.4 % x 34.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 37.395 %) — p(stop avant cible) 0.023 [0.01 ; 0.04], R/R 0.341, perte reelle 37.395 % (gap inclus), EV -0.0903 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 45.1 % x 12.74 % + P(rien) 52.6 % x -9.46 % ne couvrent pas P(stop) 2.3 % x 37.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 40.795 %) — p(stop avant cible) 0.0159 [0.01 ; 0.03], R/R 0.312, perte reelle 40.795 % (gap inclus), EV -0.1051 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 45.1 % x 12.74 % + P(rien) 53.3 % x -9.76 % ne couvrent pas P(stop) 1.6 % x 40.80 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 44.195 %) — p(stop avant cible) 0.0126 [0.00 ; 0.03], R/R 0.288, perte reelle 44.195 % (gap inclus), EV -0.102 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 45.1 % x 12.74 % + P(rien) 53.6 % x -9.87 % ne couvrent pas P(stop) 1.3 % x 44.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 47.594 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.268, perte reelle 47.594 % (gap inclus), EV -0.107 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 45.1 % x 12.74 % + P(rien) 54.3 % x -10.26 % ne couvrent pas P(stop) 0.6 % x 47.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 50.994 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.25, perte reelle 50.994 % (gap inclus), EV -0.104 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 45.1 % x 12.74 % + P(rien) 54.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 50.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 54.393 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.234, perte reelle 54.393 % (gap inclus), EV -0.1047 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 45.1 % x 12.74 % + P(rien) 54.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 54.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.56, ATR14 0.65 (6.799 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.428 ATR = 2.91 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.34 % | 9.5275 | 92.65 % | 95.17 % | 96.43 % | 97.12 % | 97.91 % | 98.36 % |
| 0.1 ATR | 0.68 % | 9.495 | 86.91 % | 91.38 % | 93.33 % | 94.69 % | 96.17 % | 97.42 % |
| 0.15 ATR | 1.02 % | 9.4625 | 80.94 % | 87.13 % | 89.76 % | 91.7 % | 93.85 % | 96.01 % |
| 0.2 ATR | 1.36 % | 9.43 | 75.32 % | 82.87 % | 86.54 % | 89.27 % | 92.23 % | 94.95 % |
| 0.25 ATR | 1.7 % | 9.3975 | 70.03 % | 79.77 % | 83.89 % | 87.08 % | 90.49 % | 93.78 % |
| 0.35 ATR | 2.38 % | 9.3325 | 58.32 % | 72.18 % | 77.45 % | 82.81 % | 87.47 % | 91.31 % |
| 0.5 ATR | 3.4 % | 9.235 | 42.37 % | 59.2 % | 67.32 % | 74.28 % | 82.95 % | 88.26 % |
| 0.75 ATR | 5.099 % | 9.0725 | 20.67 % | 37.36 % | 47.87 % | 59.63 % | 72.27 % | 80.63 % |
| 1.0 ATR | 6.799 % | 8.91 | 11.37 % | 25.86 % | 36.02 % | 49.25 % | 64.39 % | 74.88 % |
| 1.25 ATR | 8.499 % | 8.7475 | 4.71 % | 15.98 % | 25.2 % | 38.64 % | 54.87 % | 68.54 % |
| 1.5 ATR | 10.199 % | 8.585 | 2.3 % | 9.77 % | 16.23 % | 28.37 % | 45.36 % | 61.74 % |
| 2.0 ATR | 13.598 % | 8.26 | 0.34 % | 3.22 % | 6.44 % | 14.53 % | 31.32 % | 49.53 % |
| 2.5 ATR | 16.998 % | 7.935 | 0.11 % | 1.26 % | 2.76 % | 6.81 % | 20.53 % | 38.73 % |
| 3.0 ATR | 20.397 % | 7.61 | 0.11 % | 0.57 % | 1.73 % | 3.69 % | 11.83 % | 28.76 % |
| 4.0 ATR | 27.197 % | 6.96 | 0.0 % | 0.23 % | 0.35 % | 1.04 % | 4.52 % | 13.85 % |
| 6.0 ATR | 40.795 % | 5.66 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.64 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.86 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.29 ATR | 2.79 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.29 ATR | 2.53 ATR | 3.25 ATR | 3.93 ATR |
| **20 s.** | 0.99 ATR | 1.98 ATR | 2.21 ATR | 2.79 ATR | 3.25 ATR | 3.59 ATR | 4.63 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.475–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.4 %, prix 9.235), p(touche) 42.37 % (en stress 81.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.099 %, prix 9.0725), p(touche) 37.36 % (en stress 88.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.5 % des re-echantillons)
- **3 seance(s)** : plage utile 0.811–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.799 %, prix 8.91), p(touche) 36.02 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.1–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.499 %, prix 8.7475), p(touche) 38.64 % (en stress 95.4 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.513–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.598 %, prix 8.26), p(touche) 31.32 % (en stress 96.55 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.21–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.998 %, prix 7.935), p(touche) 38.73 % (en stress 98.84 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.101 | EV/share : $0.032 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.143 | ¼-Kelly 0.036 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.9 | bear 6.9 | side 9.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 153.0 (= 16 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.821% → cible +6.741% / stop −3.37%, p_fill 73%, n_eff≈29.4) : P(cible|rempli) **13%** · **EV/risk +0.124** (×p_fill ; si rempli +0.57% du capital)
  - **swing** (entrée dip −4.011% → cible +10.828% / stop −7.083%, p_fill 63%, n_eff≈25.1) : P(cible|rempli) **43%** · **EV/risk +0.173** (×p_fill ; si rempli +1.94% du capital)
  - **deep** (entrée dip −6.197% → cible +22.373% / stop −11.186%, p_fill 54%, n_eff≈23.0) : P(cible|rempli) **9%** · **EV/risk +0.162** (×p_fill ; si rempli +3.38% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.3  _(neutre)_
- **ADX** : 13.9  _(pas de tendance nette)_
- **MACD** : hist 0.012  _(pas de croisement recent)_
- **BB** : %B 0.63 · largeur 13.7%
- **ATR** : 0.65 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.042  _(neutre)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 63.0  _(marche en range (choppy))_
- **MA** : MA20 9.4 · MA50 9.12 · MA200 13.13  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 +4.8% · MA200 -27.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (494216 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
