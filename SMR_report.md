# SMR

**Generated** : 2026-09-24T00:44:24.101456+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $8.67  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $8.67 (+1.9% vs entrée) · entrée $8.51 · stop $8.29 · T1 $8.85 · R/R 1.55  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.003 _(réel 5 s)_ (GBM 0.166) · ¼-Kelly 0.038 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.61% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.2 % ≠ (strike 9.0 − spot 8.67)/spot = +3.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.45–$8.58 (mid $8.51)
- Spot actuel : $8.67 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : $8.29 (stop swing_plan-based (-12.51%))
- Targets : T1 $8.85 · R/R 1.55 | T2 $9.14 · R/R 2.86 | T3 $9.44 · R/R 4.23
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.29


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.51 %)** : le gap seul le franchit 0.349 % des séances (4 fois sur 1145).
   - exécution **3.499 pt plus bas** dans le cas TYPIQUE (médiane), 13.886 au p90, **17.813 au pire**
   - perte réelle **18.976 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 12.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0226 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.482 % | p01 -6.96 % | pire -30.323 % _(sur 1145 séances)_
- **P(stop avant cible)** _(source : daily, 1146 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5256** [0.4513 ; 0.599] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4643** [0.4122 ; 0.517] _(largeur 10.5 pt, n_eff 345.3)_
   - deep : **0.4372** [0.3856 ; 0.4899] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.9 pt), swing (36.7 pt), deep (38.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.99 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.78 % contre 6.27 % aujourd'hui, rapport 1.72)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.22 % vs -18.74 % si l'on extrapolait par √5 _(rapport 1.026 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6132** (β de hausse 1.3726, asymétrie 1.1753) vs IWM — 545 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.909× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 7.5589 sur atr_based (1.5 ATR, 12.815 %) — p(stop avant cible) 0.4651 [0.41 ; 0.52], R/R 0.927, perte reelle 18.976 % (gap inclus), CVaR 12.837 %, EV -3.2825 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0697 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.84 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.84 ATR (stop 10.097 %) — p(stop avant cible) 0.5702 [0.52 ; 0.62], R/R 1.069, perte reelle 16.461 % (gap inclus), EV -4.1941 % — **REFUSE**
      - refuse : p_stop_first 0.570, borne haute 0.622 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.84 ATR du spot — compartiment <1, mesure a 46.2 % de casse (IC clusterise [0.431 ; 0.493] sur 1171 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.19 %) : P(cible) 28.9 % x 17.59 % + P(rien) 14.1 % x 0.82 % ne couvrent pas P(stop) 57.0 % x 16.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 12.815 %) — p(stop avant cible) 0.4651 [0.41 ; 0.52], R/R 0.927, perte reelle 18.976 % (gap inclus), EV -3.2825 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 31.6 % x 17.59 % + P(rien) 21.9 % x -0.03 % ne couvrent pas P(stop) 46.5 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.97 ATR (stop 19.728 %) — p(stop avant cible) 0.231 [0.19 ; 0.28], R/R 0.58, perte reelle 30.323 % (gap inclus), EV -2.5996 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.60 %) : P(cible) 33.3 % x 17.59 % + P(rien) 43.6 % x -3.32 % ne couvrent pas P(stop) 23.1 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 2.136 %) — p(stop avant cible) 0.8876 [0.85 ; 0.92], R/R 4.235, perte reelle 4.153 % (gap inclus), EV -1.8675 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.87 %) : P(cible) 10.3 % x 17.59 % + P(rien) 0.9 % x 0.93 % ne couvrent pas P(stop) 88.8 % x 4.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 4.272 %) — p(stop avant cible) 0.8124 [0.77 ; 0.85], R/R 2.285, perte reelle 7.699 % (gap inclus), EV -3.2839 % — **REFUSE**
      - refuse : p_stop_first 0.812, borne haute 0.851 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 16.4 % x 17.59 % + P(rien) 2.4 % x 3.88 % ne couvrent pas P(stop) 81.2 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 21.359 %) — p(stop avant cible) 0.1913 [0.15 ; 0.24], R/R 0.58, perte reelle 30.323 % (gap inclus), EV -1.9087 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 33.4 % x 17.59 % + P(rien) 47.5 % x -4.16 % ne couvrent pas P(stop) 19.1 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 23.494 %) — p(stop avant cible) 0.1466 [0.11 ; 0.19], R/R 0.58, perte reelle 30.323 % (gap inclus), EV -1.0823 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 33.4 % x 17.59 % + P(rien) 51.9 % x -4.84 % ne couvrent pas P(stop) 14.7 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 25.63 %) — p(stop avant cible) 0.1045 [0.08 ; 0.14], R/R 0.58, perte reelle 30.323 % (gap inclus), EV -0.4236 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 33.5 % x 17.59 % + P(rien) 56.1 % x -5.59 % ne couvrent pas P(stop) 10.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 29.902 %) — p(stop avant cible) 0.0559 [0.04 ; 0.08], R/R 0.58, perte reelle 30.323 % (gap inclus), EV 0.0283 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.90 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 34.174 %) — p(stop avant cible) 0.0304 [0.02 ; 0.05], R/R 0.515, perte reelle 34.174 % (gap inclus), EV 0.0887 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.17 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 38.445 %) — p(stop avant cible) 0.0206 [0.01 ; 0.04], R/R 0.458, perte reelle 38.445 % (gap inclus), EV 0.0192 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.45 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 42.717 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 0.412, perte reelle 42.717 % (gap inclus), EV 0.0452 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.72 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 46.989 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 0.374, perte reelle 46.989 % (gap inclus), EV 0.0187 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 51.261 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.343, perte reelle 51.261 % (gap inclus), EV 0.0273 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.26 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 55.532 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.317, perte reelle 55.532 % (gap inclus), EV 0.0265 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 59.804 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.294, perte reelle 59.804 % (gap inclus), EV 0.0317 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 59.80 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 64.076 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.275, perte reelle 64.076 % (gap inclus), EV 0.0317 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 64.08 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 68.347 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.257, perte reelle 68.347 % (gap inclus), EV 0.0317 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 68.35 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 8.67, ATR14 0.7407 (8.543 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.426 ATR = 3.639 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.427 % | 8.633 | 92.43 % | 95.02 % | 96.38 % | 97.05 % | 97.95 % | 98.38 % |
| 0.1 ATR | 0.854 % | 8.5959 | 86.67 % | 91.18 % | 93.32 % | 94.67 % | 96.23 % | 97.46 % |
| 0.15 ATR | 1.282 % | 8.5589 | 80.68 % | 86.88 % | 89.69 % | 91.71 % | 93.95 % | 96.07 % |
| 0.2 ATR | 1.709 % | 8.5219 | 74.92 % | 82.58 % | 86.41 % | 89.22 % | 92.35 % | 95.03 % |
| 0.25 ATR | 2.136 % | 8.4848 | 69.72 % | 79.52 % | 83.81 % | 87.06 % | 90.64 % | 93.88 % |
| 0.35 ATR | 2.99 % | 8.4108 | 58.08 % | 72.06 % | 77.35 % | 82.75 % | 87.67 % | 91.45 % |
| 0.5 ATR | 4.272 % | 8.2996 | 42.15 % | 58.82 % | 66.93 % | 74.12 % | 83.22 % | 88.45 % |
| 0.75 ATR | 6.408 % | 8.1145 | 20.68 % | 37.33 % | 47.68 % | 59.59 % | 72.37 % | 80.95 % |
| 1.0 ATR | 8.543 % | 7.9293 | 11.41 % | 25.9 % | 35.9 % | 49.26 % | 64.5 % | 75.06 % |
| 1.25 ATR | 10.679 % | 7.7441 | 4.75 % | 16.06 % | 25.14 % | 38.59 % | 54.91 % | 68.59 % |
| 1.5 ATR | 12.815 % | 7.5589 | 2.26 % | 9.84 % | 16.31 % | 28.49 % | 45.43 % | 61.78 % |
| 2.0 ATR | 17.087 % | 7.1886 | 0.34 % | 3.28 % | 6.57 % | 14.76 % | 31.28 % | 48.73 % |
| 2.5 ATR | 21.359 % | 6.8182 | 0.11 % | 1.36 % | 2.94 % | 6.92 % | 20.66 % | 38.11 % |
| 3.0 ATR | 25.63 % | 6.4479 | 0.11 % | 0.57 % | 1.93 % | 3.86 % | 11.76 % | 28.29 % |
| 4.0 ATR | 34.174 % | 5.7071 | 0.0 % | 0.23 % | 0.34 % | 1.14 % | 4.57 % | 13.63 % |
| 6.0 ATR | 51.261 % | 4.2257 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.38 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.25 ATR | 1.40 ATR | 1.82 ATR | 2.22 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.63 ATR | 1.81 ATR | 2.30 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.30 ATR | 2.54 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 1.00 ATR | 1.95 ATR | 2.18 ATR | 2.76 ATR | 3.22 ATR | 3.56 ATR | 4.60 ATR | 5.44 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.473–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.272 %, prix 8.2996), p(touche) 42.15 % (en stress 82.02 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.661–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.408 %, prix 8.1144), p(touche) 37.33 % (en stress 88.76 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.4 % des re-echantillons)
- **3 seance(s)** : plage utile 0.807–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.543 %, prix 7.9293), p(touche) 35.9 % (en stress 89.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.1–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.679 %, prix 7.7441), p(touche) 38.59 % (en stress 95.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.515–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (17.087 %, prix 7.1886), p(touche) 31.28 % (en stress 96.59 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.176–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.166 | EV/share : $0.037 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.152 | ¼-Kelly 0.038 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 42.9 | bear 13.7 | side 43.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.806% → cible +3.902% / stop −2.611%, p_fill 68%, n_eff≈29.0) : P(cible|rempli) **30%** · **EV/risk -0.003** (×p_fill ; si rempli -0.01% du capital)
  - **swing** (entrée dip −3.966% → cible +15.918% / stop −8.897%, p_fill 64%, n_eff≈25.3) : P(cible|rempli) **19%** · **EV/risk +0.198** (×p_fill ; si rempli +2.75% du capital)
  - **deep** (entrée dip −6.124% → cible +18.752% / stop −13.652%, p_fill 46%, n_eff≈22.6) : P(cible|rempli) **27%** · **EV/risk +0.133** (×p_fill ; si rempli +3.93% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 43.6  _(momentum baissier)_
- **ADX** : 13.9  _(pas de tendance nette)_
- **MACD** : hist -0.098  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 34.4%
- **ATR** : 0.74 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.14  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 43.1  _(transition)_
- **MA** : MA20 9.28 · MA50 9.05 · MA200 12.37  _(prix < MA20)_
- **Dist MA** : MA20 -6.5% · MA50 -4.2% · MA200 -29.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (832702 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
