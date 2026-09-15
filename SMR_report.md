# SMR

**Generated** : 2026-09-15T00:44:09.150692+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $8.51  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $8.51 (+8.0% vs entrée) · entrée $7.88 · stop $6.99 · T1 $9.66 · R/R 2.0  
> ↳ P(T1 av. stop) 12 % · EV/risk -0.077 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +16.1 % ≠ (strike 10.0 − spot 8.51)/spot = +17.6 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $7.76–$8.01 (mid $7.88)
- Spot actuel : $8.51 (+8.0% au-dessus de la zone — repli à attendre)
- Stop : $6.99 (stop swing_plan-based (-17.78%))
- Targets : T1 $9.66 · R/R 2.0 | T2 $9.73 · R/R 2.08 | T3 $9.79 · R/R 2.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $6.99


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.50 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.78 %)** : le gap seul le franchit 0.088 % des séances (1 fois sur 1138).
   - exécution **12.543 pt plus bas** dans le cas TYPIQUE (médiane), 12.543 au p90, **12.543 au pire**
   - perte réelle **30.323 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 17.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.011 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.49 % | p01 -6.961 % | pire -30.323 % _(sur 1138 séances)_
- **P(stop avant cible)** _(source : daily, 1139 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.419** [0.3473 ; 0.4933] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.3527** [0.3037 ; 0.4042] _(largeur 10.0 pt, n_eff 345.3)_
   - deep : **0.3423** [0.2937 ; 0.3935] _(largeur 10.0 pt, n_eff 345.2)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 8.2 observations effectives », dont la borne haute a 95 % vaut environ 36.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.0 pt), swing (40.8 pt), deep (54.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.99 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.81 % contre 6.23 % aujourd'hui, rapport 1.73)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.93 % vs -18.73 % si l'on extrapolait par √5 _(rapport 1.011 ; < 1 = le √5 surestime)_
- **β de baisse : 1.626** (β de hausse 1.3855, asymétrie 1.1736) vs IWM — 541 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.941× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 7.5492 sur atr_grid (1.25 ATR, 11.238 %) — p(stop avant cible) 0.5095 [0.46 ; 0.56], R/R 0.972, perte reelle 17.667 % (gap inclus), CVaR 11.266 %, EV -3.712 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0218 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.509, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 13.486 %) — p(stop avant cible) 0.4258 [0.37 ; 0.48], R/R 0.905, perte reelle 18.976 % (gap inclus), EV -2.5491 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.55 %) : P(cible) 31.9 % x 17.17 % + P(rien) 25.5 % x 0.20 % ne couvrent pas P(stop) 42.6 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.69 ATR (stop 17.869 %) — p(stop avant cible) 0.2896 [0.24 ; 0.34], R/R 0.566, perte reelle 30.323 % (gap inclus), EV -3.8506 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.85 %) : P(cible) 33.3 % x 17.17 % + P(rien) 37.8 % x -2.08 % ne couvrent pas P(stop) 29.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 2.248 %) — p(stop avant cible) 0.8922 [0.86 ; 0.92], R/R 3.982, perte reelle 4.313 % (gap inclus), EV -2.159 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.892, borne haute 0.922 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.16 %) : P(cible) 9.8 % x 17.17 % + P(rien) 1.0 % x 0.95 % ne couvrent pas P(stop) 89.2 % x 4.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 4.495 %) — p(stop avant cible) 0.7993 [0.75 ; 0.84], R/R 2.007, perte reelle 8.556 % (gap inclus), EV -3.8624 % — **REFUSE**
      - refuse : p_stop_first 0.799, borne haute 0.839 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.86 %) : P(cible) 16.4 % x 17.17 % + P(rien) 3.6 % x 4.25 % ne couvrent pas P(stop) 79.9 % x 8.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 6.743 %) — p(stop avant cible) 0.7223 [0.67 ; 0.77], R/R 1.476, perte reelle 11.636 % (gap inclus), EV -4.3709 % — **REFUSE**
      - refuse : p_stop_first 0.722, borne haute 0.767 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.37 %) : P(cible) 22.1 % x 17.17 % + P(rien) 5.7 % x 4.15 % ne couvrent pas P(stop) 72.2 % x 11.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 8.991 %) — p(stop avant cible) 0.6086 [0.56 ; 0.66], R/R 1.105, perte reelle 15.541 % (gap inclus), EV -4.7069 % — **REFUSE**
      - refuse : p_stop_first 0.609, borne haute 0.659 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.71 %) : P(cible) 26.8 % x 17.17 % + P(rien) 12.3 % x 1.19 % ne couvrent pas P(stop) 60.9 % x 15.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 11.238 %) — p(stop avant cible) 0.5095 [0.46 ; 0.56], R/R 0.972, perte reelle 17.667 % (gap inclus), EV -3.712 % — **REFUSE**
      - refuse : p_stop_first 0.509, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.71 %) : P(cible) 30.0 % x 17.17 % + P(rien) 19.1 % x 0.75 % ne couvrent pas P(stop) 50.9 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 20.229 %) — p(stop avant cible) 0.2143 [0.17 ; 0.26], R/R 0.566, perte reelle 30.323 % (gap inclus), EV -2.3015 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.30 %) : P(cible) 33.5 % x 17.17 % + P(rien) 45.1 % x -3.45 % ne couvrent pas P(stop) 21.4 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 22.476 %) — p(stop avant cible) 0.1658 [0.13 ; 0.21], R/R 0.566, perte reelle 30.323 % (gap inclus), EV -1.4099 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.41 %) : P(cible) 33.6 % x 17.17 % + P(rien) 49.9 % x -4.30 % ne couvrent pas P(stop) 16.6 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 24.724 %) — p(stop avant cible) 0.1278 [0.10 ; 0.17], R/R 0.566, perte reelle 30.323 % (gap inclus), EV -0.8045 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 33.6 % x 17.17 % + P(rien) 53.6 % x -5.03 % ne couvrent pas P(stop) 12.8 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 26.972 %) — p(stop avant cible) 0.0821 [0.06 ; 0.11], R/R 0.566, perte reelle 30.323 % (gap inclus), EV -0.1319 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 33.6 % x 17.17 % + P(rien) 58.2 % x -5.86 % ne couvrent pas P(stop) 8.2 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 31.467 %) — p(stop avant cible) 0.0465 [0.03 ; 0.07], R/R 0.546, perte reelle 31.467 % (gap inclus), EV 0.1037 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.47 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 35.962 %) — p(stop avant cible) 0.0282 [0.01 ; 0.05], R/R 0.478, perte reelle 35.962 % (gap inclus), EV 0.1124 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.96 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 40.457 %) — p(stop avant cible) 0.0157 [0.01 ; 0.03], R/R 0.425, perte reelle 40.457 % (gap inclus), EV 0.0751 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.46 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 44.953 %) — p(stop avant cible) 0.0118 [0.00 ; 0.03], R/R 0.382, perte reelle 44.953 % (gap inclus), EV 0.0736 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.95 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 49.448 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.347, perte reelle 49.448 % (gap inclus), EV 0.0761 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.45 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 53.943 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.318, perte reelle 53.943 % (gap inclus), EV 0.0744 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.94 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 58.438 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.294, perte reelle 58.438 % (gap inclus), EV 0.0791 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.44 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 62.934 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.273, perte reelle 62.934 % (gap inclus), EV 0.0791 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 62.93 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 67.429 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.255, perte reelle 67.429 % (gap inclus), EV 0.0791 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 67.43 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 71.924 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.239, perte reelle 71.924 % (gap inclus), EV 0.0791 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 71.92 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 8.505, ATR14 0.7646 (8.991 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.428 ATR = 3.848 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.45 % | 8.4668 | 92.6 % | 95.1 % | 96.35 % | 97.03 % | 97.93 % | 98.37 % |
| 0.1 ATR | 0.899 % | 8.4285 | 86.9 % | 91.33 % | 93.26 % | 94.62 % | 96.2 % | 97.44 % |
| 0.15 ATR | 1.349 % | 8.3903 | 80.87 % | 87.0 % | 89.61 % | 91.65 % | 93.9 % | 96.04 % |
| 0.2 ATR | 1.798 % | 8.3521 | 75.17 % | 82.67 % | 86.3 % | 89.13 % | 92.29 % | 94.99 % |
| 0.25 ATR | 2.248 % | 8.3138 | 69.93 % | 79.59 % | 83.68 % | 86.96 % | 90.56 % | 93.83 % |
| 0.35 ATR | 3.147 % | 8.2374 | 58.31 % | 72.06 % | 77.28 % | 82.72 % | 87.57 % | 91.39 % |
| 0.5 ATR | 4.495 % | 8.1227 | 42.26 % | 58.95 % | 67.01 % | 74.14 % | 83.08 % | 88.36 % |
| 0.75 ATR | 6.743 % | 7.9315 | 20.62 % | 37.29 % | 47.6 % | 59.5 % | 72.15 % | 80.79 % |
| 1.0 ATR | 8.991 % | 7.7404 | 11.39 % | 25.88 % | 35.84 % | 49.2 % | 64.21 % | 75.09 % |
| 1.25 ATR | 11.238 % | 7.5492 | 4.78 % | 16.08 % | 25.11 % | 38.44 % | 54.66 % | 68.57 % |
| 1.5 ATR | 13.486 % | 7.358 | 2.28 % | 9.81 % | 16.21 % | 28.26 % | 45.22 % | 61.7 % |
| 2.0 ATR | 17.981 % | 6.9757 | 0.34 % | 3.31 % | 6.51 % | 14.42 % | 31.07 % | 49.13 % |
| 2.5 ATR | 22.476 % | 6.5934 | 0.11 % | 1.37 % | 2.85 % | 6.75 % | 20.37 % | 38.42 % |
| 3.0 ATR | 26.972 % | 6.2111 | 0.11 % | 0.57 % | 1.83 % | 3.66 % | 11.74 % | 28.52 % |
| 4.0 ATR | 35.962 % | 5.4464 | 0.0 % | 0.23 % | 0.34 % | 1.03 % | 4.49 % | 13.74 % |
| 6.0 ATR | 53.943 % | 3.9171 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.38 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.21 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.38 ATR | 1.62 ATR | 1.80 ATR | 2.29 ATR | 2.78 ATR |
| **10 s.** | 0.69 ATR | 1.37 ATR | 1.51 ATR | 1.93 ATR | 2.28 ATR | 2.52 ATR | 3.24 ATR | 3.93 ATR |
| **20 s.** | 1.00 ATR | 1.97 ATR | 2.19 ATR | 2.77 ATR | 3.24 ATR | 3.58 ATR | 4.62 ATR | 5.44 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.474–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.495 %, prix 8.1227), p(touche) 42.26 % (en stress 81.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.661–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.743 %, prix 7.9315), p(touche) 37.29 % (en stress 88.64 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (68.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.991 %, prix 7.7403), p(touche) 35.84 % (en stress 89.77 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.098–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (11.238 %, prix 7.5492), p(touche) 38.44 % (en stress 94.32 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.508–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.193–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.083 | EV/share : $-0.074 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 8 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 62.5 | bear 17.0 | side 20.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.325% → cible +7.583% / stop −3.791%, p_fill 40%, n_eff≈19.4) : P(cible|rempli) **1%** · **EV/risk -0.043** (×p_fill ; si rempli -0.41% du capital)
  - **swing** (entrée dip −7.307% → cible +22.598% / stop −11.298%, p_fill 17%, n_eff≈8.2) : P(cible|rempli) **0%** · **EV/risk +0.054** (×p_fill ; si rempli +3.64% du capital)
  - **deep** (entrée dip −11.294% → cible +11.415% / stop −15.203%, p_fill 16%, n_eff≈9.8) : P(cible|rempli) **64%** · **EV/risk +0.035** (×p_fill ; si rempli +3.44% du capital)
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.1  _(neutre)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist -0.087  _(bearish_recent)_
- **BB** : %B 0.14 · largeur 28.4%
- **ATR** : 0.76 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.058  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 46.5  _(transition)_
- **MA** : MA20 9.48 · MA50 9.09 · MA200 12.76  _(prix < MA20)_
- **Dist MA** : MA20 -10.3% · MA50 -6.4% · MA200 -33.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (752451 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
