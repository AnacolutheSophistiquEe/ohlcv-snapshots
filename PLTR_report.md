# PLTR

**Generated** : 2026-09-23T00:36:00.735091+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $184.98  

> 🟡 **WAIT-FOR-DIP** — spot +5.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $184.98 (+5.3% vs entrée) · entrée $175.59 · stop $172.95 · T1 $178.65 · R/R 1.16  
> ↳ P(T1 av. stop) 47 % · EV/risk 0.281 · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -4.4 % ≠ (strike 175.0 − spot 184.98)/spot = -5.4 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $174.97–$176.20 (mid $175.59)
- Spot actuel : $184.98 (+5.3% au-dessus de la zone — repli à attendre)
- Stop : $172.95 (stop swing_plan-based (-14.99%))
- Targets : T1 $178.65 · R/R 1.16 | T2 $181.72 · R/R 2.32 | T3 $184.79 · R/R 3.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $172.95


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.99 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **2.942 pt plus bas** dans le cas TYPIQUE (médiane), 2.942 au p90, **2.942 au pire**
   - perte réelle **17.932 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 14.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0023 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4723** [0.3989 ; 0.5466] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4301** [0.3787 ; 0.4827] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3555** [0.3064 ; 0.407] _(largeur 10.1 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.41 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.77 % si l'on extrapolait par √5 _(rapport 0.976 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6986** (β de hausse 1.4127, asymétrie 1.2024) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 177.9273 sur atr_grid (1.0 ATR, 3.813 %) — p(stop avant cible) 0.4621 [0.41 ; 0.51], R/R 0.511, perte reelle 6.717 % (gap inclus), CVaR 3.892 %, EV -1.2603 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **4.05 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.313 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 45.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.719 %) — p(stop avant cible) 0.3345 [0.29 ; 0.39], R/R 0.353, perte reelle 9.704 % (gap inclus), EV -1.0056 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 5.76 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 65.1 % x 3.43 % + P(rien) 1.5 % x 0.53 % ne couvrent pas P(stop) 33.5 % x 9.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.1 ATR (stop 14.274 %) — p(stop avant cible) 0.098 [0.07 ; 0.13], R/R 0.21, perte reelle 16.302 % (gap inclus), EV 0.1337 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.28 % > budget 4.05 %
   - ⚪ sr_based a 5.43 ATR (stop 23.162 %) — p(stop avant cible) 0.0168 [0.01 ; 0.03], R/R 0.148, perte reelle 23.162 % (gap inclus), EV 0.5239 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.16 % > budget 4.05 %
   - 🟢 support a 9.51 ATR (stop 38.736 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.089, perte reelle 38.736 % (gap inclus), EV 0.627 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.74 % > budget 4.05 %
   - 🟢 support a 11.15 ATR (stop 44.963 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.076, perte reelle 44.963 % (gap inclus), EV 0.6255 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.96 % > budget 4.05 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.953 %) — p(stop avant cible) 0.7541 [0.71 ; 0.80], R/R 1.441, perte reelle 2.381 % (gap inclus), EV -0.9521 % — **REFUSE**
      - refuse : p_stop_first 0.754, borne haute 0.797 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 5.15 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 24.6 % x 3.43 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 75.4 % x 2.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.906 %) — p(stop avant cible) 0.6409 [0.59 ; 0.69], R/R 1.011, perte reelle 3.392 % (gap inclus), EV -0.9422 % — **REFUSE**
      - refuse : p_stop_first 0.641, borne haute 0.690 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 5.15 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 35.9 % x 3.43 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 64.1 % x 3.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.86 %) — p(stop avant cible) 0.5309 [0.48 ; 0.58], R/R 0.666, perte reelle 5.152 % (gap inclus), EV -1.1262 % — **REFUSE**
      - refuse : p_stop_first 0.531, borne haute 0.583 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 5.15 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 46.9 % x 3.43 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 53.1 % x 5.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.813 %) — p(stop avant cible) 0.4621 [0.41 ; 0.51], R/R 0.511, perte reelle 6.717 % (gap inclus), EV -1.2603 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 53.7 % x 3.43 % + P(rien) 0.1 % x 0.93 % ne couvrent pas P(stop) 46.2 % x 6.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.766 %) — p(stop avant cible) 0.3839 [0.33 ; 0.44], R/R 0.417, perte reelle 8.218 % (gap inclus), EV -1.0707 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 4.82 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 60.6 % x 3.43 % + P(rien) 1.0 % x 0.53 % ne couvrent pas P(stop) 38.4 % x 8.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.672 %) — p(stop avant cible) 0.2789 [0.23 ; 0.33], R/R 0.322, perte reelle 10.642 % (gap inclus), EV -0.5651 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.71 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 69.9 % x 3.43 % + P(rien) 2.2 % x 0.19 % ne couvrent pas P(stop) 27.9 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.625 %) — p(stop avant cible) 0.2509 [0.21 ; 0.30], R/R 0.286, perte reelle 11.982 % (gap inclus), EV -0.5251 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.65 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 72.3 % x 3.43 % + P(rien) 2.6 % x -0.00 % ne couvrent pas P(stop) 25.1 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.579 %) — p(stop avant cible) 0.2293 [0.19 ; 0.28], R/R 0.274, perte reelle 12.528 % (gap inclus), EV -0.4193 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.60 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 73.0 % x 3.43 % + P(rien) 4.1 % x -1.18 % ne couvrent pas P(stop) 22.9 % x 12.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.532 %) — p(stop avant cible) 0.2084 [0.17 ; 0.25], R/R 0.261, perte reelle 13.126 % (gap inclus), EV -0.3372 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.55 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 73.4 % x 3.43 % + P(rien) 5.8 % x -2.05 % ne couvrent pas P(stop) 20.8 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.485 %) — p(stop avant cible) 0.1929 [0.15 ; 0.24], R/R 0.249, perte reelle 13.763 % (gap inclus), EV -0.3053 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.50 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 73.8 % x 3.43 % + P(rien) 6.9 % x -2.61 % ne couvrent pas P(stop) 19.3 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.1 ATR (stop 12.951 %) — p(stop avant cible) 0.1225 [0.09 ; 0.16], R/R 0.21, perte reelle 16.302 % (gap inclus), EV -0.0636 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.96 % > budget 4.05 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 75.1 % x 3.43 % + P(rien) 12.6 % x -5.11 % ne couvrent pas P(stop) 12.2 % x 16.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 15.251 %) — p(stop avant cible) 0.0868 [0.06 ; 0.12], R/R 0.191, perte reelle 17.932 % (gap inclus), EV 0.0967 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.25 % > budget 4.05 %
   - ⚪ atr_grid a 4.5 ATR (stop 17.157 %) — p(stop avant cible) 0.0722 [0.05 ; 0.10], R/R 0.191, perte reelle 17.932 % (gap inclus), EV 0.2664 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.16 % > budget 4.05 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.063 %) — p(stop avant cible) 0.0565 [0.04 ; 0.08], R/R 0.18, perte reelle 19.063 % (gap inclus), EV 0.35 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.06 % > budget 4.05 %
   - ⚪ grid_snapped a 5.43 ATR (stop 21.839 %) — p(stop avant cible) 0.0275 [0.01 ; 0.05], R/R 0.157, perte reelle 21.839 % (gap inclus), EV 0.4642 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.84 % > budget 4.05 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.782 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.138, perte reelle 24.782 % (gap inclus), EV 0.5774 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.78 % > budget 4.05 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.689 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.129, perte reelle 26.689 % (gap inclus), EV 0.5997 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.69 % > budget 4.05 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.595 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.12, perte reelle 28.595 % (gap inclus), EV 0.615 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.60 % > budget 4.05 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.502 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.112, perte reelle 30.502 % (gap inclus), EV 0.6108 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.50 % > budget 4.05 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 184.98, ATR14 7.0527 (3.813 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.36 ATR = 1.373 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.191 % | 184.6274 | 92.65 % | 95.16 % | 95.96 % | 96.76 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.381 % | 184.2747 | 84.69 % | 89.31 % | 91.22 % | 93.43 % | 95.02 % | 96.41 % |
| 0.15 ATR | 0.572 % | 183.9221 | 77.14 % | 83.67 % | 85.97 % | 89.79 % | 92.38 % | 94.25 % |
| 0.2 ATR | 0.763 % | 183.5695 | 69.28 % | 78.33 % | 81.74 % | 86.45 % | 90.24 % | 92.51 % |
| 0.25 ATR | 0.953 % | 183.2168 | 62.24 % | 73.69 % | 77.6 % | 83.01 % | 87.91 % | 90.97 % |
| 0.35 ATR | 1.334 % | 182.5115 | 50.96 % | 65.62 % | 71.14 % | 78.26 % | 83.94 % | 87.99 % |
| 0.5 ATR | 1.906 % | 181.4536 | 36.05 % | 53.02 % | 59.84 % | 69.26 % | 78.25 % | 83.47 % |
| 0.75 ATR | 2.86 % | 179.6905 | 19.44 % | 35.28 % | 44.9 % | 55.81 % | 67.28 % | 76.28 % |
| 1.0 ATR | 3.813 % | 177.9273 | 8.96 % | 22.88 % | 32.8 % | 44.29 % | 56.81 % | 67.45 % |
| 1.25 ATR | 4.766 % | 176.1641 | 4.43 % | 15.42 % | 23.41 % | 34.48 % | 46.85 % | 58.62 % |
| 1.5 ATR | 5.719 % | 174.4009 | 2.11 % | 10.48 % | 17.36 % | 26.9 % | 40.24 % | 54.11 % |
| 2.0 ATR | 7.625 % | 170.8746 | 0.6 % | 3.73 % | 9.38 % | 15.77 % | 29.17 % | 40.55 % |
| 2.5 ATR | 9.532 % | 167.3482 | 0.1 % | 1.51 % | 3.33 % | 9.3 % | 19.41 % | 30.18 % |
| 3.0 ATR | 11.438 % | 163.8219 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 15.251 % | 156.7691 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 22.876 % | 142.6637 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.21 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.98 ATR | 1.30 ATR | 1.58 ATR | 1.81 ATR | 2.45 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.32 ATR | 1.83 ATR | 2.21 ATR | 2.47 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.65 ATR | 1.84 ATR | 2.36 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.906 %, prix 181.4543), p(touche) 36.05 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.86 %, prix 179.6896), p(touche) 35.28 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.86 %, prix 179.6896), p(touche) 44.9 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.985–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.813 %, prix 177.9267), p(touche) 44.29 % (en stress 100.0 %)  ✅ optimum identifie (79.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.32–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.719 %, prix 174.401), p(touche) 40.24 % (en stress 100.0 %)  ✅ optimum identifie (87.8 % des re-echantillons)
- **20 seance(s)** : plage utile 1.836–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (11.438 %, prix 163.822), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.074 | EV/share : $0.196 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 21 % | T3 11 %
- Kelly (position) : f* 0.063 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 18.5 | side 76.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 555.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→49% · +3.0%→30% · +5.0%→11% · +8.0%→4%
- Range intraday médian 4.13% (p90 7.39%) · excursion haute méd. +1.92% / basse méd. −1.67%
- Profil de vol intra : ouverture 3.101% vs midi 0.751% vs clôture 0.844% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 24% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.151 ; neutre — autocorr 0.004)_ ; drift intra méd. 0.512% ; recovery-V 20%
- **σ réalisé intraday** 2.612% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 50% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 174.1906 (VA 173.9824–176.0649 ; dernier close 174.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 52% · **stop −3.93%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.27 (high win-rate)
- Gaps overnight (n=159) : méd. -0.28% · baisse 56% (gap-down >1% 30% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.97% · range méd 1.91%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.79%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −3.47%) · haut méd +1.3% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.16% (p90 −3.55%) · haut méd +1.39% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 174.33 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (119/159) · gap 42% · délai 0.0min · rebond 55% (64/119) (MFE +1.16%)
   - −1.0% : fill 30min 56% · séance 66% (109/159) · gap 30% · délai 0.0min · rebond 62% (65/109) (MFE +1.34%)
   - −1.5% : fill 30min 44% · séance 54% (91/159) · gap 20% · délai 0.1min · rebond 62% (56/91) (MFE +1.27%)
   - −2.0% : fill 30min 38% · séance 49% (80/159) · gap 10% · délai 1.4min · rebond 63% (50/80) (MFE +1.35%)
   - −3.0% : fill 30min 23% · séance 32% (58/159) · gap 6% · délai 4.6min · rebond 54% (28/58) (MFE +1.36%)
   - −4.0% : fill 30min 15% · séance 21% (39/159) · gap 3% · délai 8.2min · rebond 52% (18/39) (MFE +1.06%)
   - −5.0% : fill 30min 7% · séance 14% (28/159) · gap 1% · délai 28.8min · rebond 45% (13/28) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.72%) → stop au-delà de −1.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −1.71%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.28%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=552 jambes) : jambe baissière méd −1.07% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 89% (72/77) · rebond 61% (43/72)
      · −2.0% : fill 72% (59/77) · rebond 64% (36/59)
      · −3.0% : fill 54% (45/77) · rebond 52% (22/45)
      · −4.0% : fill 37% (32/77) · rebond 54% (15/32)
      · −5.0% : fill 26% (24/77) · rebond 50% (12/24)
   - **flat** (24 séances) :
      · −1.0% : fill 72% (20/24) · rebond 41% (9/20)
      · −2.0% : fill 57% (14/24) · rebond 62% (9/14)
      · −3.0% : fill 31% (10/24) · rebond 58% (5/10)
      · −4.0% : fill 18% (6/24) · rebond 41% (3/6)
      · −5.0% : fill 10% (3/24) · rebond 9% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 33% (17/58) · rebond 83% (13/17)
      · −2.0% : fill 15% (7/58) · rebond 57% (5/7)
      · −3.0% : fill 4% (3/58) · rebond 71% (1/3)
      · −4.0% : fill 1% (1/58) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 70% si les 15 1res min sont vertes (83 cas) · 30% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 85% si début vert vs 17% si rouge (base 52% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **85%** · continue >prix actuel 55% ; creux résiduel méd -0.84% (q20 -1.49%) → **SL/trailing à −1.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +2.18% → **scale +1.06% / runner +2.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **17%** (continue à baisser 51%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.77%** (au-delà de la MAE q10 -2.77%), cible rebond +1.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.41% .. +4.57%] · haut q95 +4.99% · bas q05 -3.97%
   - 60min (n=160) : retour [-3.45% .. +5.92%] · haut q95 +6.29% · bas q05 -4.19%
   - 2h (n=160) : retour [-4.1% .. +6.18%] · haut q95 +6.97% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.41% .. +5.88%] · haut q95 +6.96% · bas q05 -5.82%
   - 6h (n=160) : retour [-4.59% .. +6.51%] · haut q95 +7.39% · bas q05 -6.3%
   - session (n=160) : retour [-4.24% .. +5.84%] · haut q95 +7.69% · bas q05 -6.3%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 3.1% / strong 4.4%) · base = 12 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **40%**. Lecture précoce 30 min : signature présente → 19% vs absente 4% (base 8%)
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

- **RSI** : 54.2  _(neutre)_
- **ADX** : 21.8  _(pas de tendance nette)_
- **MACD** : hist -0.087  _(pas de croisement recent)_
- **BB** : %B 0.82 · largeur 15.0%
- **ATR** : 7.05 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.135  _(accumulation)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 58.2  _(transition)_
- **MA** : MA20 176.51 · MA50 160.48 · MA200 151.86  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 +15.3% · MA200 +21.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (846901 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
