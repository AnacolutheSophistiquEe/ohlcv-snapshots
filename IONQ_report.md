# IONQ

**Generated** : 2026-09-02T00:27:32.775065+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $37.78  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $37.78 (+2.4% vs entrée) · entrée $36.88 · stop $35.88 · T1 $38.88 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.054 _(réel 5 s)_ (GBM -0.018) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.72% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -40 % hors [0,100] (R² max 0.10). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $36.67–$37.09 (mid $36.88)
- Spot actuel : $37.78 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : $35.88 (stop swing_plan-based (-13.31%))
- Targets : T1 $38.88 · R/R 2.0 | T2 $39.48 · R/R 2.6 | T3 $40.08 · R/R 3.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $35.88


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.86 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.31 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **8.549 pt plus bas** dans le cas TYPIQUE (médiane), 8.549 au p90, **8.549 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 13.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0068 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.035 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4858** [0.4121 ; 0.56] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4566** [0.4046 ; 0.5093] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4166** [0.3655 ; 0.4691] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.0 pt), swing (44.4 pt), deep (44.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.37 %** | CVaR **-10.04 %** | vol 6.11 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.65 % contre 6.02 % aujourd'hui, rapport 1.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2204** (β de hausse 1.9897, asymétrie 1.116) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 33.1304 sur support (1.29 ATR, 12.307 %) — p(stop avant cible) 0.4487 [0.40 ; 0.50], R/R 0.752, perte reelle 21.859 % (gap inclus), CVaR 12.315 %, EV -4.4562 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0262 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.31 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.29 ATR (stop 12.307 %) — p(stop avant cible) 0.4487 [0.40 ; 0.50], R/R 0.752, perte reelle 21.859 % (gap inclus), EV -4.4562 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.46 %) : P(cible) 34.0 % x 16.44 % + P(rien) 21.2 % x -1.08 % ne couvrent pas P(stop) 44.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.78 ATR (stop 23.398 %) — p(stop avant cible) 0.1359 [0.10 ; 0.17], R/R 0.703, perte reelle 23.398 % (gap inclus), EV 0.0804 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.40 % > budget 12.00 %
   - 🟢 support a 4.25 ATR (stop 34.25 %) — p(stop avant cible) 0.0239 [0.01 ; 0.04], R/R 0.48, perte reelle 34.25 % (gap inclus), EV -0.0456 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 37.0 % x 16.44 % + P(rien) 60.7 % x -8.74 % ne couvrent pas P(stop) 2.4 % x 34.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.852 %) — p(stop avant cible) 0.8952 [0.86 ; 0.92], R/R 4.425, perte reelle 3.715 % (gap inclus), EV -1.6362 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.895, borne haute 0.924 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.64 %) : P(cible) 10.0 % x 16.44 % + P(rien) 0.4 % x 8.69 % ne couvrent pas P(stop) 89.5 % x 3.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.704 %) — p(stop avant cible) 0.8084 [0.76 ; 0.85], R/R 2.932, perte reelle 5.606 % (gap inclus), EV -1.609 % — **REFUSE**
      - refuse : p_stop_first 0.808, borne haute 0.847 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.61 %) : P(cible) 17.0 % x 16.44 % + P(rien) 2.2 % x 6.14 % ne couvrent pas P(stop) 80.8 % x 5.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.556 %) — p(stop avant cible) 0.7397 [0.69 ; 0.78], R/R 2.004, perte reelle 8.204 % (gap inclus), EV -2.2511 % — **REFUSE**
      - refuse : p_stop_first 0.740, borne haute 0.784 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 22.0 % x 16.44 % + P(rien) 4.1 % x 5.07 % ne couvrent pas P(stop) 74.0 % x 8.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 7.408 %) — p(stop avant cible) 0.6493 [0.60 ; 0.70], R/R 1.545, perte reelle 10.638 % (gap inclus), EV -2.0604 % — **REFUSE**
      - refuse : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 28.0 % x 16.44 % + P(rien) 7.1 % x 3.44 % ne couvrent pas P(stop) 64.9 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.817 %) — p(stop avant cible) 0.3576 [0.31 ; 0.41], R/R 0.752, perte reelle 21.859 % (gap inclus), EV -2.9421 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.94 %) : P(cible) 34.5 % x 16.44 % + P(rien) 29.7 % x -2.71 % ne couvrent pas P(stop) 35.8 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.669 %) — p(stop avant cible) 0.2877 [0.24 ; 0.34], R/R 0.752, perte reelle 21.859 % (gap inclus), EV -1.7313 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 35.8 % x 16.44 % + P(rien) 35.4 % x -3.76 % ne couvrent pas P(stop) 28.8 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 18.521 %) — p(stop avant cible) 0.2501 [0.21 ; 0.30], R/R 0.752, perte reelle 21.859 % (gap inclus), EV -1.2123 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 36.1 % x 16.44 % + P(rien) 38.9 % x -4.34 % ne couvrent pas P(stop) 25.0 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 25.93 %) — p(stop avant cible) 0.0943 [0.07 ; 0.13], R/R 0.634, perte reelle 25.93 % (gap inclus), EV 0.0026 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.93 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 37.042 %) — p(stop avant cible) 0.011 [0.00 ; 0.03], R/R 0.444, perte reelle 37.042 % (gap inclus), EV 0.0211 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.04 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 40.747 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 0.403, perte reelle 40.747 % (gap inclus), EV 0.0324 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.75 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 44.451 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.37, perte reelle 44.451 % (gap inclus), EV 0.0311 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.45 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 48.155 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.341, perte reelle 48.155 % (gap inclus), EV 0.0508 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.15 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 51.859 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.317, perte reelle 51.859 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.86 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 55.564 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.296, perte reelle 55.564 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.56 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 59.268 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.277, perte reelle 59.268 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 59.27 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 37.78, ATR14 2.7989 (7.408 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 2.83 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.37 % | 37.6401 | 93.66 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.741 % | 37.5001 | 86.0 % | 91.13 % | 92.13 % | 94.64 % | 96.04 % | 96.92 % |
| 0.15 ATR | 1.111 % | 37.3602 | 79.15 % | 86.29 % | 88.4 % | 91.71 % | 93.8 % | 95.69 % |
| 0.2 ATR | 1.482 % | 37.2202 | 71.7 % | 80.54 % | 84.36 % | 88.57 % | 91.06 % | 93.63 % |
| 0.25 ATR | 1.852 % | 37.0803 | 65.76 % | 76.71 % | 80.83 % | 85.95 % | 88.82 % | 92.09 % |
| 0.35 ATR | 2.593 % | 36.8004 | 53.27 % | 67.74 % | 74.27 % | 79.37 % | 84.15 % | 88.5 % |
| 0.5 ATR | 3.704 % | 36.3805 | 38.17 % | 54.94 % | 62.46 % | 71.08 % | 78.56 % | 84.5 % |
| 0.75 ATR | 5.556 % | 35.6808 | 22.36 % | 39.11 % | 48.44 % | 58.85 % | 68.9 % | 76.59 % |
| 1.0 ATR | 7.408 % | 34.9811 | 9.97 % | 24.6 % | 34.81 % | 45.9 % | 57.83 % | 67.86 % |
| 1.25 ATR | 9.261 % | 34.2813 | 3.63 % | 14.31 % | 24.12 % | 34.88 % | 50.0 % | 61.7 % |
| 1.5 ATR | 11.113 % | 33.5816 | 1.01 % | 7.06 % | 15.84 % | 25.68 % | 41.16 % | 55.85 % |
| 2.0 ATR | 14.817 % | 32.1821 | 0.1 % | 1.92 % | 4.94 % | 14.56 % | 28.46 % | 44.66 % |
| 2.5 ATR | 18.521 % | 30.7827 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.29 % | 33.68 % |
| 3.0 ATR | 22.225 % | 29.3832 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.38 % | 25.87 % |
| 4.0 ATR | 29.634 % | 26.5843 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 44.451 % | 20.9864 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.58 ATR | 0.66 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.17 ATR | 2.42 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.76 ATR | 1.99 ATR | 2.54 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.657–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.556 %, prix 35.6809), p(touche) 39.11 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.813–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.408 %, prix 34.9813), p(touche) 34.81 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.02–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.261 %, prix 34.2812), p(touche) 34.88 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.391–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.113 %, prix 33.5815), p(touche) 41.16 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.985–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.817 %, prix 32.1821), p(touche) 44.66 % (en stress 98.98 %)  ✅ optimum identifie (68.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.018 | EV/share : $-0.018 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.054 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 56.9 | bear 33.2 | side 9.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.38% → cible +5.43% / stop −2.715%, p_fill 57%, n_eff≈23.9) : P(cible|rempli) **4%** · **EV/risk -0.054** (×p_fill ; si rempli -0.26% du capital)
  - **swing** (entrée dip −5.237% → cible +17.039% / stop −8.52%, p_fill 38%, n_eff≈16.8) : P(cible|rempli) **11%** · **EV/risk -0.072** (×p_fill ; si rempli -1.59% du capital)
  - **deep** (entrée dip −8.097% → cible +9.147% / stop −12.092%, p_fill 34%, n_eff≈16.6) : P(cible|rempli) **40%** · **EV/risk -0.072** (×p_fill ; si rempli -2.58% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→65% · +3.0%→55% · +5.0%→29% · +8.0%→12%
- Range intraday médian 7.42% (p90 12.17%) · excursion haute méd. +3.54% / basse méd. −2.69%
- Profil de vol intra : ouverture 5.116% vs midi 1.461% vs clôture 1.639% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr -0.004)_ ; drift intra méd. -0.156% ; recovery-V 22%
- **σ réalisé intraday** 4.195% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 54% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 39.6838 (VA 39.5787–40.1562 ; dernier close 39.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 77% · **stop −4.73%** sous le fill (sous le bruit) · cible +2.51% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. -0.43% · baisse 54% (gap-down >1% 40% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.78%) · haut méd +1.33% · range méd 2.71%
- Excursion ouverture 15min (n=160) : bas méd −1.59% (p90 −3.94%) · haut méd +1.55% · range méd 3.54%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.11%) · haut méd +2.05% · range méd 4.41%
- Excursion ouverture 60min (n=160) : bas méd −2.23% (p90 −5.38%) · haut méd +2.22% · range méd 5.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (132/159) · gap 48% · délai 0.0min · rebond 59% (84/132) (MFE +1.83%)
   - −1.0% : fill 30min 68% · séance 74% (124/159) · gap 40% · délai 0.0min · rebond 68% (89/124) (MFE +2.28%)
   - −1.5% : fill 30min 62% · séance 68% (116/159) · gap 33% · délai 0.0min · rebond 67% (79/116) (MFE +1.95%)
   - −2.0% : fill 30min 55% · séance 61% (106/159) · gap 19% · délai 0.0min · rebond 69% (73/106) (MFE +2.19%)
   - −3.0% : fill 30min 45% · séance 54% (91/159) · gap 9% · délai 5.7min · rebond 67% (64/91) (MFE +2.18%)
   - −4.0% : fill 30min 26% · séance 44% (75/159) · gap 5% · délai 20.6min · rebond 64% (55/75) (MFE +2.01%)
   - −5.0% : fill 30min 18% · séance 35% (63/159) · gap 3% · délai 24.8min · rebond 77% (53/63) (MFE +2.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.89%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.89%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.86% (p90 −2.67%) → stop au-delà de −1.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1115 jambes) : jambe baissière méd −1.3% (p90 −3.01%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 67% (56/79)
      · −2.0% : fill 88% (72/79) · rebond 72% (53/72)
      · −3.0% : fill 77% (62/79) · rebond 66% (44/62)
      · −4.0% : fill 62% (49/79) · rebond 62% (36/49)
      · −5.0% : fill 49% (41/79) · rebond 69% (32/41)
   - **flat** (15 séances) :
      · −1.0% : fill 78% (12/15) · rebond 65% (7/12)
      · −2.0% : fill 69% (11/15) · rebond 79% (6/11)
      · −3.0% : fill 62% (9/15) · rebond 62% (6/9)
      · −4.0% : fill 54% (8/15) · rebond 53% (4/8)
      · −5.0% : fill 39% (7/15) · rebond 95% (6/7)
   - **gap-up** (65 séances) :
      · −1.0% : fill 38% (33/65) · rebond 74% (26/33)
      · −2.0% : fill 24% (23/65) · rebond 49% (14/23)
      · −3.0% : fill 20% (20/65) · rebond 76% (14/20)
      · −4.0% : fill 18% (18/65) · rebond 79% (15/18)
      · −5.0% : fill 15% (15/65) · rebond 100% (15/15)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 58% si les 15 1res min sont vertes (82 cas) · 28% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:05** → P(séance verte=clôture>ouverture) 72% si début vert vs 17% si rouge (base 45% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **72%** · continue >prix actuel 43% ; creux résiduel méd -2.03% (q20 -4.02%) → **SL/trailing à −4.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.85% / q75 +3.58% → **scale +1.85% / runner +3.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **17%** (continue à baisser 54%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.75% .. +6.47%] · haut q95 +7.73% · bas q05 -5.5%
   - 60min (n=160) : retour [-4.93% .. +6.02%] · haut q95 +8.12% · bas q05 -6.07%
   - 2h (n=160) : retour [-6.34% .. +7.66%] · haut q95 +8.62% · bas q05 -6.98%
   - 4h (n=160) : retour [-6.91% .. +6.91%] · haut q95 +9.76% · bas q05 -8.08%
   - 6h (n=160) : retour [-7.16% .. +7.87%] · haut q95 +10.26% · bas q05 -8.11%
   - session (n=160) : retour [-6.47% .. +8.39%] · haut q95 +10.46% · bas q05 -8.26%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 13% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 35.1  _(momentum baissier)_
- **ADX** : 15.8  _(pas de tendance nette)_
- **MACD** : hist -0.49  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 24.4%
- **ATR** : 2.8 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.13  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 50.4  _(transition)_
- **MA** : MA20 42.45 · MA50 42.13 · MA200 44.34  _(prix < MA20)_
- **Dist MA** : MA20 -11.0% · MA50 -10.3% · MA200 -14.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (775032 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
