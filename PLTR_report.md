# PLTR

**Generated** : 2026-09-16T00:36:09.444449+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $172.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $172.56 (+1.7% vs entrée) · entrée $169.73 · stop $166.47 · T1 $176.26 · R/R 2.0  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk -0.081 _(réel 5 s)_ (GBM 0.009) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.92% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $169.12–$170.34 (mid $169.73)
- Spot actuel : $172.56 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $166.47 (stop swing_plan-based (-7.98%))
- Targets : T1 $176.26 · R/R 2.0 | T2 $177.56 · R/R 2.4 | T3 $178.85 · R/R 2.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $166.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.98 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1253).
   - exécution **3.738 pt plus bas** dans le cas TYPIQUE (médiane), 7.67 au p90, **9.952 au pire**
   - perte réelle **11.982 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 7.98 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0256 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4362** [0.3639 ; 0.5106] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4098** [0.3589 ; 0.4622] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3476** [0.2988 ; 0.3989] _(largeur 10.0 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (40.9 pt), swing (45.3 pt), deep (38.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.09 %** | CVaR **-7.27 %** | vol 3.84 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.59 % contre 4.42 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7057** (β de hausse 1.4186, asymétrie 1.2024) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 153.6904 sur atr_grid (2.5 ATR, 10.935 %) — p(stop avant cible) 0.2558 [0.21 ; 0.30], R/R 0.631, perte reelle 13.763 % (gap inclus), CVaR 10.946 %, EV -0.3367 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.561 %) — p(stop avant cible) 0.4332 [0.38 ; 0.49], R/R 0.816, perte reelle 10.642 % (gap inclus), EV -1.0865 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 38.0 % x 8.69 % + P(rien) 18.6 % x 1.18 % ne couvrent pas P(stop) 43.3 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.26 ATR (stop 8.032 %) — p(stop avant cible) 0.3545 [0.31 ; 0.41], R/R 0.725, perte reelle 11.982 % (gap inclus), EV -0.7302 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 39.6 % x 8.69 % + P(rien) 24.9 % x 0.31 % ne couvrent pas P(stop) 35.4 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.6 ATR (stop 9.511 %) — p(stop avant cible) 0.3045 [0.26 ; 0.35], R/R 0.662, perte reelle 13.126 % (gap inclus), EV -0.617 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 39.9 % x 8.69 % + P(rien) 29.6 % x -0.29 % ne couvrent pas P(stop) 30.4 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.31 ATR (stop 17.003 %) — p(stop avant cible) 0.1035 [0.07 ; 0.14], R/R 0.484, perte reelle 17.932 % (gap inclus), EV 0.3981 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.00 % > budget 12.00 %
   - 🟢 support a 7.24 ATR (stop 34.197 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.254, perte reelle 34.197 % (gap inclus), EV 0.9443 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.20 % > budget 12.00 %
   - 🟢 support a 8.77 ATR (stop 40.873 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.212, perte reelle 40.873 % (gap inclus), EV 0.9468 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.87 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.094 %) — p(stop avant cible) 0.8821 [0.84 ; 0.91], R/R 3.414, perte reelle 2.544 % (gap inclus), EV -1.2383 % — **REFUSE**
      - refuse : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.882, borne haute 0.913 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 11.5 % x 8.69 % + P(rien) 0.3 % x 3.44 % ne couvrent pas P(stop) 88.2 % x 2.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.187 %) — p(stop avant cible) 0.7629 [0.72 ; 0.81], R/R 2.208, perte reelle 3.934 % (gap inclus), EV -1.0368 % — **REFUSE**
      - refuse : p_stop_first 0.763, borne haute 0.805 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 21.8 % x 8.69 % + P(rien) 1.9 % x 3.62 % ne couvrent pas P(stop) 76.3 % x 3.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.281 %) — p(stop avant cible) 0.6826 [0.63 ; 0.73], R/R 1.549, perte reelle 5.607 % (gap inclus), EV -1.3117 % — **REFUSE**
      - refuse : p_stop_first 0.683, borne haute 0.730 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 27.1 % x 8.69 % + P(rien) 4.7 % x 3.53 % ne couvrent pas P(stop) 68.3 % x 5.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.374 %) — p(stop avant cible) 0.6167 [0.56 ; 0.67], R/R 1.172, perte reelle 7.412 % (gap inclus), EV -1.7634 % — **REFUSE**
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 30.4 % x 8.69 % + P(rien) 7.9 % x 2.07 % ne couvrent pas P(stop) 61.7 % x 7.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.748 %) — p(stop avant cible) 0.3216 [0.27 ; 0.37], R/R 0.693, perte reelle 12.528 % (gap inclus), EV -0.5935 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 39.8 % x 8.69 % + P(rien) 28.1 % x -0.06 % ne couvrent pas P(stop) 32.2 % x 12.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.935 %) — p(stop avant cible) 0.2558 [0.21 ; 0.30], R/R 0.631, perte reelle 13.763 % (gap inclus), EV -0.3367 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 40.7 % x 8.69 % + P(rien) 33.7 % x -1.05 % ne couvrent pas P(stop) 25.6 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 12.029 %) — p(stop avant cible) 0.2122 [0.17 ; 0.26], R/R 0.604, perte reelle 14.376 % (gap inclus), EV 0.0107 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.04 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 13.122 %) — p(stop avant cible) 0.176 [0.14 ; 0.22], R/R 0.533, perte reelle 16.302 % (gap inclus), EV -0.0734 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 41.7 % x 8.69 % + P(rien) 40.7 % x -2.03 % ne couvrent pas P(stop) 17.6 % x 16.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.31 ATR (stop 15.8 %) — p(stop avant cible) 0.1198 [0.09 ; 0.16], R/R 0.484, perte reelle 17.932 % (gap inclus), EV 0.2369 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.80 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 19.683 %) — p(stop avant cible) 0.0531 [0.03 ; 0.08], R/R 0.441, perte reelle 19.683 % (gap inclus), EV 0.6871 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.68 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.87 %) — p(stop avant cible) 0.0323 [0.02 ; 0.06], R/R 0.397, perte reelle 21.87 % (gap inclus), EV 0.7867 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 24.057 %) — p(stop avant cible) 0.0087 [0.00 ; 0.02], R/R 0.361, perte reelle 24.057 % (gap inclus), EV 0.9023 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.06 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 26.244 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.331, perte reelle 26.244 % (gap inclus), EV 0.9231 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 28.431 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.305, perte reelle 28.431 % (gap inclus), EV 0.9386 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.43 % > budget 12.00 %
   - 🟢 grid_snapped a 7.24 ATR (stop 32.994 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.263, perte reelle 32.994 % (gap inclus), EV 0.94 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.99 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 34.992 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.248, perte reelle 34.992 % (gap inclus), EV 0.9432 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.99 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 172.56, ATR14 7.5479 (4.374 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.36 ATR = 1.575 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.219 % | 172.1826 | 92.55 % | 95.06 % | 95.86 % | 96.66 % | 97.97 % | 98.67 % |
| 0.1 ATR | 0.437 % | 171.8052 | 84.49 % | 89.11 % | 91.02 % | 93.23 % | 94.92 % | 96.41 % |
| 0.15 ATR | 0.656 % | 171.4278 | 77.04 % | 83.47 % | 85.77 % | 89.59 % | 92.28 % | 94.25 % |
| 0.2 ATR | 0.875 % | 171.0504 | 69.28 % | 78.23 % | 81.63 % | 86.25 % | 90.14 % | 92.51 % |
| 0.25 ATR | 1.094 % | 170.673 | 62.24 % | 73.69 % | 77.6 % | 82.91 % | 87.8 % | 90.97 % |
| 0.35 ATR | 1.531 % | 169.9182 | 50.96 % | 65.62 % | 71.14 % | 78.26 % | 83.84 % | 87.89 % |
| 0.5 ATR | 2.187 % | 168.7861 | 36.05 % | 53.02 % | 59.94 % | 69.36 % | 78.15 % | 83.37 % |
| 0.75 ATR | 3.281 % | 166.8991 | 19.44 % | 35.38 % | 45.01 % | 55.81 % | 67.17 % | 76.18 % |
| 1.0 ATR | 4.374 % | 165.0121 | 8.96 % | 22.88 % | 32.8 % | 44.39 % | 56.61 % | 67.66 % |
| 1.25 ATR | 5.468 % | 163.1252 | 4.43 % | 15.42 % | 23.41 % | 34.58 % | 46.75 % | 58.83 % |
| 1.5 ATR | 6.561 % | 161.2382 | 2.11 % | 10.48 % | 17.36 % | 26.9 % | 40.04 % | 54.11 % |
| 2.0 ATR | 8.748 % | 157.4643 | 0.6 % | 3.73 % | 9.38 % | 15.77 % | 29.17 % | 40.66 % |
| 2.5 ATR | 10.935 % | 153.6904 | 0.1 % | 1.51 % | 3.33 % | 9.3 % | 19.31 % | 30.18 % |
| 3.0 ATR | 13.122 % | 149.9164 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 17.496 % | 142.3686 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 26.244 % | 127.2728 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.21 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.41 ATR | 0.88 ATR | 0.99 ATR | 1.30 ATR | 1.58 ATR | 1.81 ATR | 2.45 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.31 ATR | 1.82 ATR | 2.21 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.65 ATR | 1.84 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.187 %, prix 168.7861), p(touche) 36.05 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.281 %, prix 166.8983), p(touche) 35.38 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.75–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.281 %, prix 166.8983), p(touche) 45.01 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.987–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.374 %, prix 165.0122), p(touche) 44.39 % (en stress 100.0 %)  ✅ optimum identifie (81.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.315–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.561 %, prix 161.2383), p(touche) 40.04 % (en stress 100.0 %)  ✅ optimum identifie (88.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.839–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.122 %, prix 149.9167), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : $0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 15 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 35.6 | side 59.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 345.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.639% → cible +3.845% / stop −1.922%, p_fill 50%, n_eff≈20.5) : P(cible|rempli) **12%** · **EV/risk -0.081** (×p_fill ; si rempli -0.31% du capital)
  - **swing** (entrée dip −3.606% → cible +4.007% / stop −4.538%, p_fill 25%, n_eff≈15.2) : P(cible|rempli) **62%** · **EV/risk +0.088** (×p_fill ; si rempli +1.58% du capital)
  - **deep** (entrée dip −5.579% → cible +5.666% / stop −6.948%, p_fill 24%, n_eff≈17.2) : P(cible|rempli) **76%** · **EV/risk +0.104** (×p_fill ; si rempli +2.96% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.9  _(neutre)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist -2.392  _(pas de croisement recent)_
- **BB** : %B 0.38 · largeur 14.2%
- **ATR** : 7.55 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.011  _(neutre)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 56.5  _(transition)_
- **MA** : MA20 175.52 · MA50 155.61 · MA200 151.62  _(prix < MA20)_
- **Dist MA** : MA20 -1.7% · MA50 +10.9% · MA200 +13.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (758974 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
