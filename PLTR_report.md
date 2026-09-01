# PLTR

**Generated** : 2026-09-01T00:26:24.454028+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $186.38  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $186.38 (+9.8% vs entrée) · entrée $169.74 · stop $162.95 · T1 $183.13 · R/R 1.97  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.082 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 156 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $167.06–$172.42 (mid $169.74)
- Spot actuel : $186.38 (+9.8% au-dessus de la zone — repli à attendre)
- Stop : $162.95 (stop swing_plan-based (-12.57%))
- Targets : T1 $183.13 · R/R 1.97 | T2 $196.52 · R/R 3.94 | T3 $209.92 · R/R 5.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $162.95


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.57 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **2.102 pt plus bas** dans le cas TYPIQUE (médiane), 4.71 au p90, **5.362 au pire**
   - perte réelle **15.126 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 12.57 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0061 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.453** [0.3801 ; 0.5274] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.5297** [0.477 ; 0.5819] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4792** [0.4269 ; 0.5319] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.708** (β de hausse 1.4134, asymétrie 1.2084) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 165.5035 sur grid_snapped (2.77 ATR, 11.201 %) — p(stop avant cible) 0.2763 [0.23 ; 0.33], R/R 0.918, perte reelle 13.763 % (gap inclus), CVaR 11.211 %, EV 0.0508 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.467 %) — p(stop avant cible) 0.5438 [0.49 ; 0.60], R/R 1.375, perte reelle 9.186 % (gap inclus), EV -1.3353 % — **REFUSE**
      - refuse : p_stop_first 0.544, borne haute 0.596 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 23.1 % x 12.63 % + P(rien) 22.5 % x 3.29 % ne couvrent pas P(stop) 54.4 % x 9.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.77 ATR (stop 12.324 %) — p(stop avant cible) 0.2277 [0.19 ; 0.27], R/R 0.835, perte reelle 15.126 % (gap inclus), EV 0.2859 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.33 % > budget 12.00 %
   - ⚪ sr_based a 4.55 ATR (stop 18.815 %) — p(stop avant cible) 0.0722 [0.05 ; 0.10], R/R 0.671, perte reelle 18.815 % (gap inclus), EV 1.1076 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.82 % > budget 12.00 %
   - 🟢 support a 10.08 ATR (stop 38.964 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.324, perte reelle 38.964 % (gap inclus), EV 1.4489 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.96 % > budget 12.00 %
   - 🟢 support a 11.78 ATR (stop 45.144 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.28, perte reelle 45.144 % (gap inclus), EV 1.4481 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.14 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.911 %) — p(stop avant cible) 0.9108 [0.88 ; 0.94], R/R 5.355, perte reelle 2.358 % (gap inclus), EV -1.1376 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.911, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 6.4 % x 12.63 % + P(rien) 2.5 % x 7.97 % ne couvrent pas P(stop) 91.1 % x 2.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.822 %) — p(stop avant cible) 0.8363 [0.79 ; 0.87], R/R 3.808, perte reelle 3.316 % (gap inclus), EV -1.0424 % — **REFUSE**
      - refuse : cible atteinte seulement 11.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.836, borne haute 0.872 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 11.2 % x 12.63 % + P(rien) 5.2 % x 6.17 % ne couvrent pas P(stop) 83.6 % x 3.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.734 %) — p(stop avant cible) 0.7566 [0.71 ; 0.80], R/R 2.664, perte reelle 4.74 % (gap inclus), EV -1.064 % — **REFUSE**
      - refuse : p_stop_first 0.757, borne haute 0.800 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 16.4 % x 12.63 % + P(rien) 7.9 % x 5.66 % ne couvrent pas P(stop) 75.7 % x 4.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.645 %) — p(stop avant cible) 0.6826 [0.63 ; 0.73], R/R 1.971, perte reelle 6.407 % (gap inclus), EV -1.3662 % — **REFUSE**
      - refuse : p_stop_first 0.683, borne haute 0.730 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 19.2 % x 12.63 % + P(rien) 12.6 % x 4.67 % ne couvrent pas P(stop) 68.3 % x 6.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.556 %) — p(stop avant cible) 0.6222 [0.57 ; 0.67], R/R 1.623, perte reelle 7.779 % (gap inclus), EV -1.3939 % — **REFUSE**
      - refuse : p_stop_first 0.622, borne haute 0.672 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 22.3 % x 12.63 % + P(rien) 15.5 % x 4.08 % ne couvrent pas P(stop) 62.2 % x 7.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.378 %) — p(stop avant cible) 0.4865 [0.43 ; 0.54], R/R 1.226, perte reelle 10.298 % (gap inclus), EV -1.0173 % — **REFUSE**
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 25.1 % x 12.63 % + P(rien) 26.2 % x 3.12 % ne couvrent pas P(stop) 48.6 % x 10.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.289 %) — p(stop avant cible) 0.4194 [0.37 ; 0.47], R/R 1.102, perte reelle 11.461 % (gap inclus), EV -0.5242 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 27.5 % x 12.63 % + P(rien) 30.5 % x 2.64 % ne couvrent pas P(stop) 41.9 % x 11.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.201 %) — p(stop avant cible) 0.3919 [0.34 ; 0.44], R/R 1.008, perte reelle 12.528 % (gap inclus), EV -0.6672 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 27.6 % x 12.63 % + P(rien) 33.2 % x 2.27 % ne couvrent pas P(stop) 39.2 % x 12.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.112 %) — p(stop avant cible) 0.3502 [0.30 ; 0.40], R/R 0.962, perte reelle 13.126 % (gap inclus), EV -0.4595 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 27.8 % x 12.63 % + P(rien) 37.2 % x 1.70 % ne couvrent pas P(stop) 35.0 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.77 ATR (stop 11.201 %) — p(stop avant cible) 0.2763 [0.23 ; 0.33], R/R 0.918, perte reelle 13.763 % (gap inclus), EV 0.0508 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 14.579 %) — p(stop avant cible) 0.1586 [0.12 ; 0.20], R/R 0.775, perte reelle 16.302 % (gap inclus), EV 0.5746 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.58 % > budget 12.00 %
   - ⚪ grid_snapped a 4.55 ATR (stop 17.692 %) — p(stop avant cible) 0.0991 [0.07 ; 0.13], R/R 0.704, perte reelle 17.932 % (gap inclus), EV 0.9474 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.69 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.224 %) — p(stop avant cible) 0.0918 [0.06 ; 0.13], R/R 0.693, perte reelle 18.224 % (gap inclus), EV 0.9625 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.22 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.046 %) — p(stop avant cible) 0.0523 [0.03 ; 0.08], R/R 0.63, perte reelle 20.046 % (gap inclus), EV 1.1839 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.05 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.868 %) — p(stop avant cible) 0.0342 [0.02 ; 0.06], R/R 0.577, perte reelle 21.868 % (gap inclus), EV 1.2776 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.87 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.691 %) — p(stop avant cible) 0.0119 [0.00 ; 0.03], R/R 0.533, perte reelle 23.691 % (gap inclus), EV 1.3902 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.69 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.513 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 0.495, perte reelle 25.513 % (gap inclus), EV 1.409 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.51 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.336 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.462, perte reelle 27.336 % (gap inclus), EV 1.4202 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.34 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.158 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.433, perte reelle 29.158 % (gap inclus), EV 1.4367 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.16 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 186.38, ATR14 6.7931 (3.645 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 1.301 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.182 % | 186.0404 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.67 % |
| 0.1 ATR | 0.364 % | 185.7007 | 84.39 % | 89.01 % | 90.82 % | 93.02 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.547 % | 185.361 | 77.04 % | 83.37 % | 85.67 % | 89.38 % | 92.17 % | 94.25 % |
| 0.2 ATR | 0.729 % | 185.0214 | 68.98 % | 78.02 % | 81.33 % | 85.95 % | 89.94 % | 92.4 % |
| 0.25 ATR | 0.911 % | 184.6817 | 61.93 % | 73.49 % | 77.3 % | 82.71 % | 87.6 % | 90.97 % |
| 0.35 ATR | 1.276 % | 184.0024 | 50.65 % | 65.52 % | 71.04 % | 78.06 % | 83.74 % | 87.89 % |
| 0.5 ATR | 1.822 % | 182.9835 | 36.15 % | 52.82 % | 59.64 % | 69.06 % | 78.15 % | 83.47 % |
| 0.75 ATR | 2.734 % | 181.2852 | 19.34 % | 35.18 % | 44.6 % | 55.41 % | 67.17 % | 76.28 % |
| 1.0 ATR | 3.645 % | 179.5869 | 8.96 % | 22.78 % | 32.59 % | 43.98 % | 56.5 % | 67.86 % |
| 1.25 ATR | 4.556 % | 177.8887 | 4.43 % | 15.42 % | 23.31 % | 34.48 % | 46.75 % | 59.24 % |
| 1.5 ATR | 5.467 % | 176.1904 | 2.01 % | 10.38 % | 17.36 % | 26.59 % | 40.04 % | 54.41 % |
| 2.0 ATR | 7.289 % | 172.7939 | 0.6 % | 3.63 % | 9.18 % | 15.47 % | 28.96 % | 40.66 % |
| 2.5 ATR | 9.112 % | 169.3973 | 0.1 % | 1.41 % | 3.13 % | 9.0 % | 19.11 % | 30.18 % |
| 3.0 ATR | 10.934 % | 166.0008 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 14.579 % | 159.2077 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 21.868 % | 145.6216 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.53 ATR | 1.90 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.95 ATR | 2.35 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.57 ATR | 1.80 ATR | 2.42 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.31 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.66 ATR | 1.84 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.822 %, prix 182.9842), p(touche) 36.15 % (en stress 82.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.734 %, prix 181.2844), p(touche) 35.18 % (en stress 95.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.743–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.734 %, prix 181.2844), p(touche) 44.6 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.978–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.645 %, prix 179.5865), p(touche) 43.98 % (en stress 100.0 %)  ✅ optimum identifie (81.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.315–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.467 %, prix 176.1906), p(touche) 40.04 % (en stress 100.0 %)  ✅ optimum identifie (89.6 % des re-echantillons)
- **20 seance(s)** : plage utile 1.842–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (10.934 %, prix 166.0012), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (95.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 8 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 30.7 | side 64.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 559.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→51% · +3.0%→30% · +5.0%→10% · +8.0%→4%
- Range intraday médian 4.01% (p90 7.17%) · excursion haute méd. +2.11% / basse méd. −1.57%
- Profil de vol intra : ouverture 3.052% vs midi 0.747% vs clôture 0.839% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.007)_ ; drift intra méd. 0.783% ; recovery-V 26%
- **σ réalisé intraday** 2.61% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 42% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 185.9429 (VA 185.6481–186.6306 ; dernier close 186.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 67% · **stop −3.79%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 54% (gap-down >1% 27% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.09%) · haut méd +0.97% · range méd 1.92%
- Excursion ouverture 15min (n=160) : bas méd −0.83% (p90 −2.84%) · haut méd +1.2% · range méd 2.36%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −3.5%) · haut méd +1.31% · range méd 2.68%
- Excursion ouverture 60min (n=160) : bas méd −1.22% (p90 −3.59%) · haut méd +1.43% · range méd 3.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 186.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (118/159) · gap 38% · délai 0.0min · rebond 58% (66/118) (MFE +1.23%)
   - −1.0% : fill 30min 53% · séance 65% (108/159) · gap 27% · délai 0.0min · rebond 64% (65/108) (MFE +1.46%)
   - −1.5% : fill 30min 42% · séance 54% (90/159) · gap 19% · délai 0.3min · rebond 65% (57/90) (MFE +1.38%)
   - −2.0% : fill 30min 36% · séance 48% (79/159) · gap 11% · délai 1.4min · rebond 67% (51/79) (MFE +1.37%)
   - −3.0% : fill 30min 21% · séance 30% (56/159) · gap 6% · délai 3.6min · rebond 58% (28/56) (MFE +1.8%)
   - −4.0% : fill 30min 14% · séance 19% (38/159) · gap 3% · délai 8.2min · rebond 53% (18/38) (MFE +1.09%)
   - −5.0% : fill 30min 8% · séance 14% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.89%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.71%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.35%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.04% (p90 −2.46%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 88% (70/75) · rebond 64% (42/70)
      · −2.0% : fill 72% (57/75) · rebond 69% (36/57)
      · −3.0% : fill 50% (42/75) · rebond 57% (21/42)
      · −4.0% : fill 34% (30/75) · rebond 56% (14/30)
      · −5.0% : fill 26% (23/75) · rebond 58% (12/23)
   - **flat** (25 séances) :
      · −1.0% : fill 72% (21/25) · rebond 42% (10/21)
      · −2.0% : fill 57% (15/25) · rebond 63% (10/15)
      · −3.0% : fill 32% (11/25) · rebond 59% (6/11)
      · −4.0% : fill 19% (7/25) · rebond 44% (4/7)
      · −5.0% : fill 10% (3/25) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 34% (17/59) · rebond 83% (13/17)
      · −2.0% : fill 16% (7/59) · rebond 57% (5/7)
      · −3.0% : fill 4% (3/59) · rebond 71% (1/3)
      · −4.0% : fill 1% (1/59) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/59) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 71% si les 15 1res min sont vertes (82 cas) · 32% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 22% si rouge (base 53% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **86%** · continue >prix actuel 56% ; creux résiduel méd -0.89% (q20 -1.63%) → **SL/trailing à −1.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.36% / q75 +2.36% → **scale +1.36% / runner +2.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **22%** (continue à baisser 44%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.47%** (au-delà de la MAE q10 -2.47%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.49% .. +3.82%] · haut q95 +4.06% · bas q05 -4.02%
   - 60min (n=160) : retour [-3.61% .. +3.93%] · haut q95 +4.79% · bas q05 -4.27%
   - 2h (n=160) : retour [-3.82% .. +5.43%] · haut q95 +6.13% · bas q05 -4.53%
   - 4h (n=160) : retour [-4.11% .. +5.64%] · haut q95 +6.52% · bas q05 -5.27%
   - 6h (n=160) : retour [-4.2% .. +5.89%] · haut q95 +6.85% · bas q05 -5.58%
   - session (n=160) : retour [-4.04% .. +5.14%] · haut q95 +6.85% · bas q05 -5.58%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 3.1% / strong 4.4%) · base = 12 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 20% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.13% / p90 1.49%) · ~2.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 43.27 min, n=37)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.49%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +4.31% (q75 +7.51% / q95 +12.13%), MFE méd +5.25% / q90 +12.03%
   - Échelle scale-out : +5.25% (33%) / +7.95% (33%) / +12.03% (34%)
- **DÉSARMER** : repli > **−1.49%** depuis le plus-haut = décay → P(retournement) **82%** (préavis méd 214.54 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.03% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 58% du temps (retour médian dernière heure +0.19%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 61.2  _(momentum haussier)_
- **ADX** : 36.4  _(tendance etablie)_
- **MACD** : hist 0.149  _(bullish_recent)_
- **BB** : %B 0.88 · largeur 18.6%
- **ATR** : 6.79 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.228  _(accumulation)_
- **Vol ratio** : 0.58  _(volume atone)_
- **Choppiness** : 59.0  _(transition)_
- **MA** : MA20 174.06 · MA50 144.9 · MA200 151.35  _(prix > MA20)_
- **Dist MA** : MA20 +7.1% · MA50 +28.6% · MA200 +23.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (783596 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
