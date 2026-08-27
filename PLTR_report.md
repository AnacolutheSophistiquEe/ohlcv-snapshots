# PLTR

**Generated** : 2026-08-27T00:28:09.867733+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $177.50  

> 🟡 **WAIT-FOR-DIP** — spot +4.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $177.50 (+4.4% vs entrée) · entrée $169.95 · stop $165.70 · T1 $177.69 · R/R 1.82  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.106 · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $168.75–$171.15 (mid $169.95)
- Spot actuel : $177.50 (+4.4% au-dessus de la zone — repli à attendre)
- Stop : $165.70 (stop swing_plan-based (-18.05%))
- Targets : T1 $177.69 · R/R 1.82 | T2 $182.78 · R/R 3.02 | T3 $187.87 · R/R 4.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $165.70


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (18.05 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1253).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.05 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3197** [0.2537 ; 0.3917] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.192** [0.1531 ; 0.236] _(largeur 8.3 pt, n_eff 345.7)_
   - deep : **0.4052** [0.3544 ; 0.4576] _(largeur 10.3 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7091** (β de hausse 1.4177, asymétrie 1.2056) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 156.2773 sur atr_grid (2.75 ATR, 11.956 %) — p(stop avant cible) 0.2538 [0.21 ; 0.30], R/R 0.836, perte reelle 14.376 % (gap inclus), CVaR 11.964 %, EV 0.0921 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.2 ATR (stop 7.128 %) — p(stop avant cible) 0.4339 [0.38 ; 0.49], R/R 1.049, perte reelle 11.461 % (gap inclus), EV -0.7526 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 29.9 % x 12.02 % + P(rien) 26.7 % x 2.36 % ne couvrent pas P(stop) 43.4 % x 11.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 4.01 ATR (stop 19.352 %) — p(stop avant cible) 0.0612 [0.04 ; 0.09], R/R 0.621, perte reelle 19.352 % (gap inclus), EV 1.06 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.35 % > budget 12.00 %
   - 🟢 support a 7.72 ATR (stop 35.487 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.339, perte reelle 35.487 % (gap inclus), EV 1.3387 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.49 % > budget 12.00 %
   - 🔴 support a 9.22 ATR (stop 41.978 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.286, perte reelle 41.978 % (gap inclus), EV 1.3426 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.98 % > budget 12.00 %
      - ⚠ support DETECTE a 9.22 ATR du spot — compartiment >=6, mesure a 46.3 % de casse (IC clusterise [0.346 ; 0.571] sur 54 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 1.087 %) — p(stop avant cible) 0.8988 [0.86 ; 0.93], R/R 4.701, perte reelle 2.556 % (gap inclus), EV -1.1784 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.899, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 8.2 % x 12.02 % + P(rien) 1.9 % x 6.98 % ne couvrent pas P(stop) 89.9 % x 2.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.174 %) — p(stop avant cible) 0.8 [0.76 ; 0.84], R/R 3.066, perte reelle 3.919 % (gap inclus), EV -1.0434 % — **REFUSE**
      - refuse : p_stop_first 0.800, borne haute 0.840 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 15.3 % x 12.02 % + P(rien) 4.7 % x 5.37 % ne couvrent pas P(stop) 80.0 % x 3.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.261 %) — p(stop avant cible) 0.7188 [0.67 ; 0.76], R/R 2.16, perte reelle 5.563 % (gap inclus), EV -1.2244 % — **REFUSE**
      - refuse : p_stop_first 0.719, borne haute 0.764 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 19.9 % x 12.02 % + P(rien) 8.2 % x 4.63 % ne couvrent pas P(stop) 71.9 % x 5.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.2 ATR (stop 6.528 %) — p(stop avant cible) 0.4838 [0.43 ; 0.54], R/R 1.129, perte reelle 10.642 % (gap inclus), EV -1.1543 % — **REFUSE**
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 28.1 % x 12.02 % + P(rien) 23.5 % x 2.63 % ne couvrent pas P(stop) 48.4 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.696 %) — p(stop avant cible) 0.3599 [0.31 ; 0.41], R/R 0.959, perte reelle 12.528 % (gap inclus), EV -0.4587 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 30.2 % x 12.02 % + P(rien) 33.8 % x 1.23 % ne couvrent pas P(stop) 36.0 % x 12.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.783 %) — p(stop avant cible) 0.337 [0.29 ; 0.39], R/R 0.916, perte reelle 13.126 % (gap inclus), EV -0.4202 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 30.4 % x 12.02 % + P(rien) 35.9 % x 0.96 % ne couvrent pas P(stop) 33.7 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.87 %) — p(stop avant cible) 0.2981 [0.25 ; 0.35], R/R 0.873, perte reelle 13.763 % (gap inclus), EV -0.2233 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 31.0 % x 12.02 % + P(rien) 39.2 % x 0.40 % ne couvrent pas P(stop) 29.8 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.956 %) — p(stop avant cible) 0.2538 [0.21 ; 0.30], R/R 0.836, perte reelle 14.376 % (gap inclus), EV 0.0921 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 13.043 %) — p(stop avant cible) 0.208 [0.17 ; 0.25], R/R 0.737, perte reelle 16.302 % (gap inclus), EV 0.0869 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.05 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 15.217 %) — p(stop avant cible) 0.1472 [0.11 ; 0.19], R/R 0.67, perte reelle 17.932 % (gap inclus), EV 0.3452 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.22 % > budget 12.00 %
   - ⚪ grid_snapped a 4.01 ATR (stop 18.752 %) — p(stop avant cible) 0.0796 [0.05 ; 0.11], R/R 0.641, perte reelle 18.752 % (gap inclus), EV 0.9549 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.75 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.739 %) — p(stop avant cible) 0.0354 [0.02 ; 0.06], R/R 0.553, perte reelle 21.739 % (gap inclus), EV 1.1725 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.74 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 23.913 %) — p(stop avant cible) 0.0094 [0.00 ; 0.02], R/R 0.503, perte reelle 23.913 % (gap inclus), EV 1.2956 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.91 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 26.087 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 0.461, perte reelle 26.087 % (gap inclus), EV 1.32 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.09 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 28.261 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.425, perte reelle 28.261 % (gap inclus), EV 1.3335 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.26 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 30.435 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.395, perte reelle 30.435 % (gap inclus), EV 1.3251 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.43 % > budget 12.00 %
   - 🟢 grid_snapped a 7.72 ATR (stop 34.887 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.344, perte reelle 34.887 % (gap inclus), EV 1.3357 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.89 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 177.5, ATR14 7.7174 (4.348 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 1.557 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.217 % | 177.1141 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.67 % |
| 0.1 ATR | 0.435 % | 176.7283 | 84.49 % | 89.01 % | 90.82 % | 93.02 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.652 % | 176.3424 | 77.04 % | 83.37 % | 85.67 % | 89.38 % | 92.17 % | 94.25 % |
| 0.2 ATR | 0.87 % | 175.9565 | 68.98 % | 78.02 % | 81.33 % | 85.95 % | 89.94 % | 92.4 % |
| 0.25 ATR | 1.087 % | 175.5707 | 62.03 % | 73.59 % | 77.4 % | 82.71 % | 87.6 % | 91.07 % |
| 0.35 ATR | 1.522 % | 174.7989 | 50.76 % | 65.62 % | 71.14 % | 78.06 % | 83.74 % | 87.99 % |
| 0.5 ATR | 2.174 % | 173.6413 | 36.25 % | 52.92 % | 59.74 % | 69.06 % | 78.25 % | 83.68 % |
| 0.75 ATR | 3.261 % | 171.712 | 19.34 % | 35.28 % | 44.6 % | 55.51 % | 67.38 % | 76.59 % |
| 1.0 ATR | 4.348 % | 169.7826 | 8.96 % | 22.78 % | 32.49 % | 44.08 % | 56.71 % | 68.17 % |
| 1.25 ATR | 5.435 % | 167.8533 | 4.43 % | 15.52 % | 23.41 % | 34.58 % | 47.05 % | 59.55 % |
| 1.5 ATR | 6.522 % | 165.924 | 2.01 % | 10.38 % | 17.46 % | 26.69 % | 40.14 % | 54.62 % |
| 2.0 ATR | 8.696 % | 162.0653 | 0.6 % | 3.63 % | 9.18 % | 15.47 % | 29.07 % | 40.76 % |
| 2.5 ATR | 10.87 % | 158.2066 | 0.1 % | 1.41 % | 3.13 % | 9.0 % | 19.11 % | 30.18 % |
| 3.0 ATR | 13.043 % | 154.3479 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 17.391 % | 146.6306 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 26.087 % | 131.1958 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.53 ATR | 1.90 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR | 1.39 ATR | 1.95 ATR | 2.35 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.57 ATR | 1.80 ATR | 2.42 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.32 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.80 ATR | 1.67 ATR | 1.85 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.174 %, prix 173.6412), p(touche) 36.25 % (en stress 82.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.612–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.261 %, prix 171.7117), p(touche) 35.28 % (en stress 95.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.743–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.261 %, prix 171.7117), p(touche) 44.6 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.98–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.348 %, prix 169.7823), p(touche) 44.08 % (en stress 100.0 %)  ✅ optimum identifie (80.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.324–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.522 %, prix 165.9235), p(touche) 40.14 % (en stress 100.0 %)  ✅ optimum identifie (89.4 % des re-echantillons)
- **20 seance(s)** : plage utile 1.847–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.043 %, prix 154.3487), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (95.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.06 | EV/share : $0.256 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 13 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.008 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 24.1 | side 70.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 355.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→50% · +3.0%→29% · +5.0%→10% · +8.0%→4%
- Range intraday médian 3.92% (p90 7.17%) · excursion haute méd. +2.0% / basse méd. −1.71%
- Profil de vol intra : ouverture 3.051% vs midi 0.761% vs clôture 0.858% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 23% · trend ↑2%/↓0% ; spike-down 53% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.675% ; recovery-V 31%
- **σ réalisé intraday** 2.659% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 42% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 179.079 (VA 177.603–181.539 ; dernier close 179.94)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 48% · **stop −3.39%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.29 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 53% (gap-down >1% 26% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.96% · range méd 1.97%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.8%) · haut méd +1.17% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −3.47%) · haut méd +1.22% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.63%) · haut méd +1.39% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 179.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (119/159) · gap 36% · délai 0.0min · rebond 59% (67/119) (MFE +1.23%)
   - −1.0% : fill 30min 54% · séance 66% (109/159) · gap 26% · délai 0.0min · rebond 64% (65/109) (MFE +1.5%)
   - −1.5% : fill 30min 42% · séance 53% (90/159) · gap 20% · délai 0.7min · rebond 65% (57/90) (MFE +1.28%)
   - −2.0% : fill 30min 36% · séance 47% (78/159) · gap 12% · délai 1.9min · rebond 67% (50/78) (MFE +1.39%)
   - −3.0% : fill 30min 21% · séance 30% (56/159) · gap 7% · délai 4.6min · rebond 56% (27/56) (MFE +1.41%)
   - −4.0% : fill 30min 14% · séance 19% (37/159) · gap 4% · délai 13.3min · rebond 48% (17/37) (MFE +0.99%)
   - −5.0% : fill 30min 9% · séance 15% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.0%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −1.82%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.37%) → stop au-delà de −1.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=553 jambes) : jambe baissière méd −1.04% (p90 −2.46%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 90% (69/73) · rebond 65% (42/69)
      · −2.0% : fill 72% (56/73) · rebond 66% (35/56)
      · −3.0% : fill 52% (41/73) · rebond 54% (20/41)
      · −4.0% : fill 35% (29/73) · rebond 50% (13/29)
      · −5.0% : fill 29% (23/73) · rebond 58% (12/23)
   - **flat** (27 séances) :
      · −1.0% : fill 73% (23/27) · rebond 42% (11/23)
      · −2.0% : fill 56% (15/27) · rebond 63% (10/15)
      · −3.0% : fill 31% (11/27) · rebond 59% (6/11)
      · −4.0% : fill 18% (7/27) · rebond 44% (4/7)
      · −5.0% : fill 9% (3/27) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 33% (17/59) · rebond 80% (12/17)
      · −2.0% : fill 12% (7/59) · rebond 79% (5/7)
      · −3.0% : fill 5% (4/59) · rebond 67% (1/4)
      · −4.0% : fill 1% (1/59) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/59) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 70% si les 15 1res min sont vertes (80 cas) · 34% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 84% si début vert vs 24% si rouge (base 53% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -0.94% (q20 -1.73%) → **SL/trailing à −1.73%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.22% → **scale +1.4% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 40%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.67% .. +3.82%] · haut q95 +4.25% · bas q05 -4.05%
   - 60min (n=160) : retour [-3.62% .. +3.98%] · haut q95 +4.9% · bas q05 -4.38%
   - 2h (n=160) : retour [-3.91% .. +5.61%] · haut q95 +6.6% · bas q05 -4.56%
   - 4h (n=160) : retour [-4.25% .. +5.66%] · haut q95 +6.64% · bas q05 -5.5%
   - 6h (n=160) : retour [-4.6% .. +6.2%] · haut q95 +7.22% · bas q05 -5.61%
   - session (n=160) : retour [-4.24% .. +6.06%] · haut q95 +7.22% · bas q05 -5.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 3.1% / strong 3.7%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 19% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.39% / p90 1.52%) · ~2.55 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 33.99 min, n=35)
   - −1.0% → **41%** (reprise méd 64.44 min, n=10)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.67% (q75 +7.59% / q95 +12.13%), MFE méd +6.82% / q90 +12.87%
   - Échelle scale-out : +6.82% (33%) / +8.47% (33%) / +12.87% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.87% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.36%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 67.5  _(momentum haussier)_
- **ADX** : 34.2  _(tendance etablie)_
- **MACD** : hist -0.272  _(bearish_recent)_
- **BB** : %B 0.67 · largeur 45.5%
- **ATR** : 7.72 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.225  _(accumulation)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 59.5  _(transition)_
- **MA** : MA20 164.68 · MA50 141.58 · MA200 151.37  _(prix > MA20)_
- **Dist MA** : MA20 +7.8% · MA50 +25.4% · MA200 +17.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (803369 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
