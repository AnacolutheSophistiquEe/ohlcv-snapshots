# PLTR

**Generated** : 2026-08-25T22:04:00.924380+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $172.73  

> 🟡 **WAIT-FOR-DIP** — spot +4.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $172.73 (+4.1% vs entrée) · entrée $165.93 · stop $153.84 · T1 $190.10 · R/R 2.0  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk 0.071 _(réel 5 s)_ (GBM 0.062) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $163.31–$168.55 (mid $165.93)
- Spot actuel : $172.73 (+4.1% au-dessus de la zone — repli à attendre)
- Stop : $153.84 (stop swing_plan-based (-10.93%))
- Targets : T1 $190.10 · R/R 2.0 | T2 $197.63 · R/R 2.62 | T3 $205.15 · R/R 3.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $153.84


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.93 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **1.843 pt plus bas** dans le cas TYPIQUE (médiane), 5.698 au p90, **7.002 au pire**
   - perte réelle **13.763 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 10.93 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0113 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3119** [0.2464 ; 0.3836] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.2569** [0.213 ; 0.3048] _(largeur 9.2 pt, n_eff 345.7)_
   - deep : **0.4467** [0.3949 ; 0.4994] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.1 observations effectives », dont la borne haute a 95 % vaut environ 14.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.4 pt), swing (44.7 pt), deep (44.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7038** (β de hausse 1.4149, asymétrie 1.2042) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : un couple (stop, cible) tient les contraintes : stop 161.5676 sur atr_based, cible 18.77 %**
- **Couple retenu** : stop 161.5676 sur atr_based (1.5 ATR, 6.462 %) — p(stop avant cible) 0.4957 [0.44 ; 0.55], R/R 1.823, perte reelle 10.298 % (gap inclus), CVaR 6.499 %, EV -0.22 % — **CONFORME**
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.6 ATR (stop 4.531 %) — p(stop avant cible) 0.6384 [0.59 ; 0.69], R/R 2.454, perte reelle 7.65 % (gap inclus), EV -0.7236 % — **REFUSE**
      - refuse : cible atteinte seulement 14.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.638, borne haute 0.688 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 14.3 % x 18.77 % + P(rien) 21.9 % x 6.75 % ne couvrent pas P(stop) 63.8 % x 7.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 6.462 %) — p(stop avant cible) 0.4957 [0.44 ; 0.55], R/R 1.823, perte reelle 10.298 % (gap inclus), EV -0.22 % — **retenu**
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 16.3 % x 18.77 % + P(rien) 34.1 % x 5.34 % ne couvrent pas P(stop) 49.6 % x 10.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.76 ATR (stop 9.546 %) — p(stop avant cible) 0.3459 [0.30 ; 0.40], R/R 1.43, perte reelle 13.126 % (gap inclus), EV 0.4442 % — **REFUSE**
      - refuse : R/R 1.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.38 ATR (stop 16.528 %) — p(stop avant cible) 0.12 [0.09 ; 0.16], R/R 1.047, perte reelle 17.932 % (gap inclus), EV 1.6128 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.53 % > budget 12.00 %
   - 🟢 support a 7.37 ATR (stop 33.705 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.557, perte reelle 33.705 % (gap inclus), EV 2.321 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.70 % > budget 12.00 %
   - 🔴 support a 8.92 ATR (stop 40.374 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.465, perte reelle 40.374 % (gap inclus), EV 2.3265 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.37 % > budget 12.00 %
      - ⚠ support DETECTE a 8.92 ATR du spot — compartiment >=6, mesure a 46.5 % de casse (IC clusterise [0.333 ; 0.591] sur 43 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 1.077 %) — p(stop avant cible) 0.9063 [0.87 ; 0.93], R/R 7.419, perte reelle 2.53 % (gap inclus), EV -1.0624 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 7.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.906, borne haute 0.934 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 3.9 % x 18.77 % + P(rien) 5.5 % x 9.13 % ne couvrent pas P(stop) 90.6 % x 2.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.6 ATR (stop 3.867 %) — p(stop avant cible) 0.6904 [0.64 ; 0.74], R/R 2.793, perte reelle 6.72 % (gap inclus), EV -0.9988 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 12.3 % x 18.77 % + P(rien) 18.7 % x 7.14 % ne couvrent pas P(stop) 69.0 % x 6.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.385 %) — p(stop avant cible) 0.5633 [0.51 ; 0.61], R/R 2.094, perte reelle 8.963 % (gap inclus), EV -0.7109 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.563, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 14.5 % x 18.77 % + P(rien) 29.2 % x 5.53 % ne couvrent pas P(stop) 56.3 % x 8.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.76 ATR (stop 8.882 %) — p(stop avant cible) 0.3631 [0.31 ; 0.41], R/R 1.498, perte reelle 12.528 % (gap inclus), EV 0.4846 % — **REFUSE**
      - refuse : R/R 1.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 10.771 %) — p(stop avant cible) 0.3111 [0.26 ; 0.36], R/R 1.364, perte reelle 13.763 % (gap inclus), EV 0.522 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 11.848 %) — p(stop avant cible) 0.2627 [0.22 ; 0.31], R/R 1.306, perte reelle 14.376 % (gap inclus), EV 1.0022 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 12.925 %) — p(stop avant cible) 0.2171 [0.18 ; 0.26], R/R 1.151, perte reelle 16.302 % (gap inclus), EV 1.0055 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.93 % > budget 12.00 %
   - 🟢 grid_snapped a 3.38 ATR (stop 15.864 %) — p(stop avant cible) 0.1346 [0.10 ; 0.17], R/R 1.047, perte reelle 17.932 % (gap inclus), EV 1.4956 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.87 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 17.233 %) — p(stop avant cible) 0.1143 [0.08 ; 0.15], R/R 1.047, perte reelle 17.932 % (gap inclus), EV 1.6835 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.23 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 19.387 %) — p(stop avant cible) 0.0622 [0.04 ; 0.09], R/R 0.968, perte reelle 19.387 % (gap inclus), EV 2.0359 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.39 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.541 %) — p(stop avant cible) 0.0363 [0.02 ; 0.06], R/R 0.871, perte reelle 21.541 % (gap inclus), EV 2.1617 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 23.695 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 0.792, perte reelle 23.695 % (gap inclus), EV 2.2688 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.69 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 25.849 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 0.726, perte reelle 25.849 % (gap inclus), EV 2.2835 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.85 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 28.004 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.67, perte reelle 28.004 % (gap inclus), EV 2.3175 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.00 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 30.158 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.622, perte reelle 30.158 % (gap inclus), EV 2.3101 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.16 % > budget 12.00 %
   - 🟢 grid_snapped a 7.37 ATR (stop 33.041 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.568, perte reelle 33.041 % (gap inclus), EV 2.3211 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.04 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 34.466 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.545, perte reelle 34.466 % (gap inclus), EV 2.3198 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.47 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 172.73, ATR14 7.4416 (4.308 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 1.538 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.215 % | 172.3579 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.67 % |
| 0.1 ATR | 0.431 % | 171.9858 | 84.49 % | 89.01 % | 90.82 % | 93.02 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.646 % | 171.6138 | 77.04 % | 83.37 % | 85.67 % | 89.38 % | 92.17 % | 94.25 % |
| 0.2 ATR | 0.862 % | 171.2417 | 68.88 % | 77.92 % | 81.23 % | 85.84 % | 89.84 % | 92.4 % |
| 0.25 ATR | 1.077 % | 170.8696 | 61.93 % | 73.49 % | 77.3 % | 82.61 % | 87.5 % | 91.07 % |
| 0.35 ATR | 1.508 % | 170.1254 | 50.65 % | 65.52 % | 71.14 % | 78.06 % | 83.64 % | 87.99 % |
| 0.5 ATR | 2.154 % | 169.0092 | 36.15 % | 52.82 % | 59.74 % | 69.06 % | 78.15 % | 83.68 % |
| 0.75 ATR | 3.231 % | 167.1488 | 19.34 % | 35.18 % | 44.6 % | 55.51 % | 67.38 % | 76.59 % |
| 1.0 ATR | 4.308 % | 165.2884 | 8.96 % | 22.78 % | 32.49 % | 44.08 % | 56.71 % | 68.17 % |
| 1.25 ATR | 5.385 % | 163.428 | 4.43 % | 15.52 % | 23.41 % | 34.58 % | 47.05 % | 59.55 % |
| 1.5 ATR | 6.462 % | 161.5676 | 2.01 % | 10.38 % | 17.46 % | 26.69 % | 40.14 % | 54.62 % |
| 2.0 ATR | 8.616 % | 157.8468 | 0.6 % | 3.63 % | 9.18 % | 15.47 % | 29.07 % | 40.76 % |
| 2.5 ATR | 10.771 % | 154.126 | 0.1 % | 1.41 % | 3.13 % | 9.0 % | 19.11 % | 30.18 % |
| 3.0 ATR | 12.925 % | 150.4051 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 17.233 % | 142.9635 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 25.849 % | 128.0803 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.10 ATR | 1.53 ATR | 1.90 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR | 1.39 ATR | 1.95 ATR | 2.35 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.57 ATR | 1.80 ATR | 2.42 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.32 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.80 ATR | 1.67 ATR | 1.85 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.154 %, prix 169.0094), p(touche) 36.15 % (en stress 82.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.231 %, prix 167.1491), p(touche) 35.18 % (en stress 95.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.743–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.231 %, prix 167.1491), p(touche) 44.6 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.98–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.308 %, prix 165.2888), p(touche) 44.08 % (en stress 100.0 %)  ✅ optimum identifie (80.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.324–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.462 %, prix 161.5682), p(touche) 40.14 % (en stress 100.0 %)  ✅ optimum identifie (89.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.847–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (12.925 %, prix 150.4046), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (95.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.062 | EV/share : $0.752 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 6 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 34.4 | side 60.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 345.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.795% → cible +4.812% / stop −2.5%, p_fill 44%, n_eff≈20.1) : P(cible|rempli) **0%** · **EV/risk +0.011** (×p_fill ; si rempli +0.06% du capital)
  - **swing** (entrée dip −3.933% → cible +14.567% / stop −7.284%, p_fill 27%, n_eff≈16.2) : P(cible|rempli) **15%** · **EV/risk +0.071** (×p_fill ; si rempli +1.90% du capital)
  - **deep** (entrée dip −6.088% → cible +11.143% / stop −6.881%, p_fill 32%, n_eff≈16.6) : P(cible|rempli) **42%** · **EV/risk +0.139** (×p_fill ; si rempli +2.98% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 62.0  _(momentum haussier)_
- **ADX** : 34.1  _(tendance etablie)_
- **MACD** : hist -0.07  _(bearish_recent)_
- **BB** : %B 0.63 · largeur 51.0%
- **ATR** : 7.44 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.179  _(accumulation)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 47.5  _(transition)_
- **MA** : MA20 161.95 · MA50 140.72 · MA200 151.36  _(prix > MA20)_
- **Dist MA** : MA20 +6.7% · MA50 +22.7% · MA200 +14.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (803969 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
