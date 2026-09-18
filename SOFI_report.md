# SOFI

**Generated** : 2026-09-18T05:53:16.436347+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.73  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.73 (+0.8% vs entrée) · entrée $16.59 · stop $15.93 · T1 $16.89 · R/R 0.45  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk -0.072 _(réel 5 s)_ (GBM 0.021) · ¼-Kelly 0.053 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.53–$16.65 (mid $16.59)
- Spot actuel : $16.73 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $15.93 (stop swing_plan-based (-6.1%))
- Targets : T1 $16.89 · R/R 0.45 | T2 $17.18 · R/R 0.89 | T3 $17.47 · R/R 1.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.93


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.1 %)** : le gap seul le franchit 1.277 % des séances (16 fois sur 1253).
   - exécution **1.379 pt plus bas** dans le cas TYPIQUE (médiane), 3.717 au p90, **5.005 au pire**
   - perte réelle **7.942 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 6.1 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0235 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.229 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1343** [0.0897 ; 0.191] _(largeur 10.1 pt, n_eff 173.1)_
   - swing : **0.4656** [0.4135 ; 0.5183] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4324** [0.3809 ; 0.485] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.5 pt), swing (35.2 pt), deep (33.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1080 séances)** : VaR **-5.98 %** | CVaR **-8.42 %** | vol 3.96 %/j
   - _fenêtre arrêtée : rupture de regime a 1140 seances en arriere (volatilite 5.68 % contre 3.55 % aujourd'hui, rapport 1.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8215** (β de hausse 1.706, asymétrie 1.0677) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.355× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 15.1132 sur atr_grid (2.25 ATR, 9.664 %) — p(stop avant cible) 0.367 [0.32 ; 0.42], R/R 4.957, perte reelle 10.246 % (gap inclus), CVaR 9.665 %, EV -0.7458 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.86 ATR (stop 5.919 %) — p(stop avant cible) 0.5669 [0.51 ; 0.62], R/R 6.572, perte reelle 7.728 % (gap inclus), EV -1.278 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.567, borne haute 0.618 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 0.0 % x 50.79 % + P(rien) 43.3 % x 7.12 % ne couvrent pas P(stop) 56.7 % x 7.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 2.57 ATR (stop 13.27 %) — p(stop avant cible) 0.1886 [0.15 ; 0.23], R/R 3.827, perte reelle 13.27 % (gap inclus), EV 0.0015 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.27 % > budget 12.00 %
      - ⚠ support DETECTE a 0.76 ATR du spot — compartiment <1, mesure a 50.6 % de casse (IC clusterise [0.471 ; 0.543] sur 1124 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 1.074 %) — p(stop avant cible) 0.9292 [0.90 ; 0.95], R/R 19.869, perte reelle 2.556 % (gap inclus), EV -1.4236 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.929, borne haute 0.953 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 0.0 % x 50.79 % + P(rien) 7.1 % x 13.39 % ne couvrent pas P(stop) 92.9 % x 2.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.148 %) — p(stop avant cible) 0.8758 [0.84 ; 0.91], R/R 13.619, perte reelle 3.729 % (gap inclus), EV -1.7417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 13.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.876, borne haute 0.907 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 0.0 % x 50.79 % + P(rien) 12.4 % x 12.17 % ne couvrent pas P(stop) 87.6 % x 3.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.86 ATR (stop 4.996 %) — p(stop avant cible) 0.6211 [0.57 ; 0.67], R/R 7.003, perte reelle 7.252 % (gap inclus), EV -1.5046 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.621, borne haute 0.671 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 0.0 % x 50.79 % + P(rien) 37.9 % x 7.88 % ne couvrent pas P(stop) 62.1 % x 7.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.516 %) — p(stop avant cible) 0.4579 [0.41 ; 0.51], R/R 5.531, perte reelle 9.182 % (gap inclus), EV -1.0389 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.0 % x 50.79 % + P(rien) 54.2 % x 5.81 % ne couvrent pas P(stop) 45.8 % x 9.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.59 %) — p(stop avant cible) 0.4058 [0.35 ; 0.46], R/R 5.232, perte reelle 9.707 % (gap inclus), EV -0.823 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.0 % x 50.79 % + P(rien) 59.4 % x 5.21 % ne couvrent pas P(stop) 40.6 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.664 %) — p(stop avant cible) 0.367 [0.32 ; 0.42], R/R 4.957, perte reelle 10.246 % (gap inclus), EV -0.7458 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.0 % x 50.79 % + P(rien) 63.3 % x 4.73 % ne couvrent pas P(stop) 36.7 % x 10.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 2.57 ATR (stop 12.347 %) — p(stop avant cible) 0.2313 [0.19 ; 0.28], R/R 4.113, perte reelle 12.347 % (gap inclus), EV -0.201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.0 % x 50.79 % + P(rien) 76.8 % x 3.43 % ne couvrent pas P(stop) 23.1 % x 12.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 15.033 %) — p(stop avant cible) 0.1255 [0.09 ; 0.16], R/R 3.378, perte reelle 15.033 % (gap inclus), EV 0.1471 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.03 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 17.18 %) — p(stop avant cible) 0.0771 [0.05 ; 0.11], R/R 2.956, perte reelle 17.18 % (gap inclus), EV 0.2205 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.18 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 19.328 %) — p(stop avant cible) 0.0561 [0.04 ; 0.08], R/R 2.628, perte reelle 19.328 % (gap inclus), EV 0.205 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.33 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.476 %) — p(stop avant cible) 0.0346 [0.02 ; 0.06], R/R 2.365, perte reelle 21.476 % (gap inclus), EV 0.1832 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.48 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 23.623 %) — p(stop avant cible) 0.0243 [0.01 ; 0.04], R/R 2.15, perte reelle 23.623 % (gap inclus), EV 0.1853 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.62 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 25.771 %) — p(stop avant cible) 0.0155 [0.01 ; 0.03], R/R 1.971, perte reelle 25.771 % (gap inclus), EV 0.2231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.77 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 27.918 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.819, perte reelle 27.918 % (gap inclus), EV 0.305 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.92 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 30.066 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 1.689, perte reelle 30.066 % (gap inclus), EV 0.3126 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.07 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 32.213 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.577, perte reelle 32.213 % (gap inclus), EV 0.3217 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.21 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 34.361 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 1.478, perte reelle 34.361 % (gap inclus), EV 0.3244 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.36 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.73, ATR14 0.7186 (4.295 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 1.602 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.215 % | 16.6941 | 92.65 % | 95.67 % | 96.97 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.43 % | 16.6581 | 84.99 % | 89.31 % | 91.93 % | 93.23 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.644 % | 16.6222 | 78.75 % | 84.58 % | 87.89 % | 90.29 % | 92.78 % | 94.76 % |
| 0.2 ATR | 0.859 % | 16.5863 | 71.4 % | 79.33 % | 83.25 % | 86.75 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.074 % | 16.5504 | 66.06 % | 74.8 % | 79.82 % | 84.02 % | 88.82 % | 91.79 % |
| 0.35 ATR | 1.503 % | 16.4785 | 52.27 % | 65.12 % | 71.85 % | 78.16 % | 85.26 % | 88.5 % |
| 0.5 ATR | 2.148 % | 16.3707 | 37.46 % | 53.02 % | 61.35 % | 68.86 % | 79.17 % | 84.29 % |
| 0.75 ATR | 3.221 % | 16.1911 | 20.24 % | 36.49 % | 46.42 % | 56.62 % | 69.41 % | 77.41 % |
| 1.0 ATR | 4.295 % | 16.0114 | 8.76 % | 24.29 % | 33.6 % | 44.79 % | 59.15 % | 68.79 % |
| 1.25 ATR | 5.369 % | 15.8318 | 4.13 % | 14.82 % | 23.51 % | 35.19 % | 49.9 % | 62.01 % |
| 1.5 ATR | 6.443 % | 15.6521 | 2.01 % | 9.27 % | 16.45 % | 27.2 % | 41.97 % | 55.54 % |
| 2.0 ATR | 8.59 % | 15.2929 | 0.7 % | 4.33 % | 8.27 % | 15.07 % | 28.96 % | 44.56 % |
| 2.5 ATR | 10.738 % | 14.9336 | 0.3 % | 1.92 % | 3.83 % | 9.4 % | 19.51 % | 35.11 % |
| 3.0 ATR | 12.885 % | 14.5743 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 13.62 % | 27.82 % |
| 4.0 ATR | 17.18 % | 13.8557 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.68 % |
| 6.0 ATR | 25.771 % | 12.4186 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.11 ATR | 1.47 ATR | 1.93 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.01 ATR | 1.21 ATR | 1.37 ATR | 1.89 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.59 ATR | 1.80 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.40 ATR | 1.84 ATR | 2.21 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.82 ATR | 1.75 ATR | 1.98 ATR | 2.65 ATR | 3.21 ATR | 3.60 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.424–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.148 %, prix 16.3706), p(touche) 37.46 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.621–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.221 %, prix 16.1911), p(touche) 36.49 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.778–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.295 %, prix 16.0114), p(touche) 33.6 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.996–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.295 %, prix 16.0114), p(touche) 44.79 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.404–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.443 %, prix 15.6521), p(touche) 41.97 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.98–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.59 %, prix 15.2929), p(touche) 44.56 % (en stress 98.98 %)  ✅ optimum identifie (75.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.021 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 27 % | T3 14 %
- Kelly (position) : f* 0.214 | ¼-Kelly 0.053 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 79.4 | bear 8.4 | side 12.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.823% → cible +1.761% / stop −4.0%, p_fill 70%, n_eff≈31.4) : P(cible|rempli) **41%** · **EV/risk -0.072** (×p_fill ; si rempli -0.41% du capital)
  - **swing** (entrée dip −1.805% → cible +3.937% / stop −4.374%, p_fill 68%, n_eff≈27.8) : P(cible|rempli) **58%** · **EV/risk +0.126** (×p_fill ; si rempli +0.81% du capital)
  - **deep** (entrée dip −2.788% → cible +5.568% / stop −6.627%, p_fill 65%, n_eff≈27.1) : P(cible|rempli) **69%** · **EV/risk +0.188** (×p_fill ; si rempli +1.92% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→71% · +2.0%→50% · +3.0%→38% · +5.0%→14% · +8.0%→1%
- Range intraday médian 4.39% (p90 7.54%) · excursion haute méd. +2.04% / basse méd. −2.17%
- Profil de vol intra : ouverture 3.063% vs midi 0.835% vs clôture 0.985% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑2%/↓0% ; spike-down 59% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.15 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.123% ; recovery-V 26%
- **σ réalisé intraday** 2.603% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 52% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 18.1833 (VA 18.1547–18.2972 ; dernier close 18.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 67% · **stop −3.09%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 43% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.69%) · haut méd +0.72% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −0.92% (p90 −2.67%) · haut méd +1.07% · range méd 2.26%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −3.18%) · haut méd +1.23% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.28% (p90 −3.59%) · haut méd +1.33% · range méd 3.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (121/159) · gap 31% · délai 0.0min · rebond 51% (64/121) (MFE +1.13%)
   - −1.0% : fill 30min 52% · séance 64% (109/159) · gap 24% · délai 1.2min · rebond 53% (62/109) (MFE +1.01%)
   - −1.5% : fill 30min 41% · séance 60% (100/159) · gap 21% · délai 7.1min · rebond 62% (66/100) (MFE +1.35%)
   - −2.0% : fill 30min 35% · séance 47% (80/159) · gap 11% · délai 3.8min · rebond 67% (55/80) (MFE +1.72%)
   - −3.0% : fill 30min 11% · séance 32% (57/159) · gap 2% · délai 50.3min · rebond 54% (37/57) (MFE +1.08%)
   - −4.0% : fill 30min 8% · séance 17% (36/159) · gap 2% · délai 48.8min · rebond 52% (23/36) (MFE +1.2%)
   - −5.0% : fill 30min 3% · séance 10% (20/159) · gap 2% · délai 192.2min · rebond 44% (10/20) (MFE +0.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.73%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.81%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.44%) → stop au-delà de −1.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=664 jambes) : jambe baissière méd −1.08% (p90 −2.75%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 98% (65/66) · rebond 51% (38/65)
      · −2.0% : fill 86% (56/66) · rebond 72% (40/56)
      · −3.0% : fill 63% (42/66) · rebond 57% (28/42)
      · −4.0% : fill 36% (28/66) · rebond 60% (20/28)
      · −5.0% : fill 21% (16/66) · rebond 54% (9/16)
   - **flat** (21 séances) :
      · −1.0% : fill 59% (12/21) · rebond 42% (5/12)
      · −2.0% : fill 40% (7/21) · rebond 55% (4/7)
      · −3.0% : fill 31% (6/21) · rebond 38% (3/6)
      · −4.0% : fill 19% (3/21) · rebond 30% (1/3)
      · −5.0% : fill 11% (1/21) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 41% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 20% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 10% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 64% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **52min** → P(séance verte=clôture>ouverture) 82% si début vert vs 12% si rouge (base 44% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **82%** · continue >prix actuel 61% ; creux résiduel méd -0.98% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.83% → **scale +1.34% / runner +2.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **12%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +3.66%] · haut q95 +4.01% · bas q05 -3.38%
   - 60min (n=160) : retour [-3.12% .. +4.25%] · haut q95 +4.63% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +4.46%] · haut q95 +5.16% · bas q05 -4.56%
   - 4h (n=160) : retour [-4.23% .. +4.54%] · haut q95 +5.67% · bas q05 -5.12%
   - 6h (n=160) : retour [-4.69% .. +4.63%] · haut q95 +5.7% · bas q05 -5.61%
   - session (n=160) : retour [-4.65% .. +4.94%] · haut q95 +5.7% · bas q05 -5.84%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 30.4  _(momentum baissier)_
- **ADX** : 11.4  _(pas de tendance nette)_
- **MACD** : hist -0.163  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 16.6%
- **ATR** : 0.72 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.105  _(distribution)_
- **Vol ratio** : 1.08  _(volume normal)_
- **Choppiness** : 46.3  _(transition)_
- **MA** : MA20 17.89 · MA50 17.75 · MA200 19.58  _(prix < MA20)_
- **Dist MA** : MA20 -6.5% · MA50 -5.7% · MA200 -14.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (749584 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
