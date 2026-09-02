# SOFI

**Generated** : 2026-09-02T00:34:50.916631+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.05  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.05 (+1.4% vs entrée) · entrée $16.81 · stop $16.14 · T1 $17.09 · R/R 0.42  
> ↳ P(T1 av. stop) 52 % _(réel 5 s)_ · EV/risk -0.003 _(réel 5 s)_ (GBM 0.011) · ¼-Kelly 0.055 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.76–$16.87 (mid $16.81)
- Spot actuel : $17.05 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $16.14 (stop swing_plan-based (-8.14%))
- Targets : T1 $17.09 · R/R 0.42 | T2 $17.37 · R/R 0.84 | T3 $17.65 · R/R 1.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.99 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.14 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **1.5 pt plus bas** dans le cas TYPIQUE (médiane), 2.342 au p90, **2.965 au pire**
   - perte réelle **9.707 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 8.14 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0075 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.268 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1479** [0.101 ; 0.2064] _(largeur 10.5 pt, n_eff 173.1)_
   - swing : **0.3721** [0.3224 ; 0.4239] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3727** [0.323 ; 0.4246] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.7 pt), swing (37.0 pt), deep (42.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.98 %** | CVaR **-8.48 %** | vol 3.87 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 5.99 % contre 3.53 % aujourd'hui, rapport 1.70)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8273** (β de hausse 1.7103, asymétrie 1.0684) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 15.1005 sur atr_grid (2.25 ATR, 11.434 %) — p(stop avant cible) 0.2885 [0.24 ; 0.34], R/R 1.347, perte reelle 11.434 % (gap inclus), CVaR 11.434 %, EV 0.2641 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.19 ATR (stop 8.587 %) — p(stop avant cible) 0.4024 [0.35 ; 0.45], R/R 1.586, perte reelle 9.707 % (gap inclus), EV -0.1175 % — **REFUSE**
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 18.8 % x 15.40 % + P(rien) 40.9 % x 2.17 % ne couvrent pas P(stop) 40.2 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.5 ATR (stop 15.248 %) — p(stop avant cible) 0.1283 [0.10 ; 0.17], R/R 1.01, perte reelle 15.248 % (gap inclus), EV 0.8587 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.25 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.27 %) — p(stop avant cible) 0.9113 [0.88 ; 0.94], R/R 5.536, perte reelle 2.781 % (gap inclus), EV -1.3395 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.911, borne haute 0.938 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 6.4 % x 15.40 % + P(rien) 2.5 % x 8.42 % ne couvrent pas P(stop) 91.1 % x 2.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.541 %) — p(stop avant cible) 0.8339 [0.79 ; 0.87], R/R 3.51, perte reelle 4.386 % (gap inclus), EV -1.6667 % — **REFUSE**
      - refuse : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.834, borne haute 0.870 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.67 %) : P(cible) 10.8 % x 15.40 % + P(rien) 5.8 % x 5.56 % ne couvrent pas P(stop) 83.4 % x 4.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.811 %) — p(stop avant cible) 0.7106 [0.66 ; 0.76], R/R 2.662, perte reelle 5.784 % (gap inclus), EV -1.1258 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.711, borne haute 0.756 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 14.5 % x 15.40 % + P(rien) 14.4 % x 5.17 % ne couvrent pas P(stop) 71.1 % x 5.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.19 ATR (stop 7.591 %) — p(stop avant cible) 0.4495 [0.40 ; 0.50], R/R 1.635, perte reelle 9.415 % (gap inclus), EV -0.4277 % — **REFUSE**
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 18.3 % x 15.40 % + P(rien) 36.7 % x 2.67 % ne couvrent pas P(stop) 45.0 % x 9.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 10.163 %) — p(stop avant cible) 0.3449 [0.30 ; 0.40], R/R 1.386, perte reelle 11.105 % (gap inclus), EV -0.1001 % — **REFUSE**
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 18.9 % x 15.40 % + P(rien) 46.6 % x 1.77 % ne couvrent pas P(stop) 34.5 % x 11.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.434 %) — p(stop avant cible) 0.2885 [0.24 ; 0.34], R/R 1.347, perte reelle 11.434 % (gap inclus), EV 0.2641 % — **REFUSE**
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.5 ATR (stop 14.252 %) — p(stop avant cible) 0.157 [0.12 ; 0.20], R/R 1.08, perte reelle 14.252 % (gap inclus), EV 0.7136 % — **REFUSE**
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.25 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.786 %) — p(stop avant cible) 0.0665 [0.04 ; 0.10], R/R 0.866, perte reelle 17.786 % (gap inclus), EV 0.9507 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.79 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 20.327 %) — p(stop avant cible) 0.05 [0.03 ; 0.08], R/R 0.757, perte reelle 20.327 % (gap inclus), EV 0.8941 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.33 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.868 %) — p(stop avant cible) 0.0298 [0.02 ; 0.05], R/R 0.673, perte reelle 22.868 % (gap inclus), EV 0.8902 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.408 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.606, perte reelle 25.408 % (gap inclus), EV 0.9118 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.41 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.949 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.551, perte reelle 27.949 % (gap inclus), EV 1.0098 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.95 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.49 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.505, perte reelle 30.49 % (gap inclus), EV 1.0148 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.49 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.031 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.466, perte reelle 33.031 % (gap inclus), EV 1.0254 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.03 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.572 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.433, perte reelle 35.572 % (gap inclus), EV 1.0265 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.113 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.404, perte reelle 38.113 % (gap inclus), EV 1.0358 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.11 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.654 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.379, perte reelle 40.654 % (gap inclus), EV 1.0354 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.65 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 17.05, ATR14 0.8664 (5.082 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 1.906 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.254 % | 17.0067 | 92.85 % | 95.77 % | 96.97 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.508 % | 16.9634 | 85.1 % | 89.52 % | 91.93 % | 93.23 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.762 % | 16.92 | 79.05 % | 84.98 % | 88.19 % | 90.39 % | 92.78 % | 94.76 % |
| 0.2 ATR | 1.016 % | 16.8767 | 71.6 % | 79.74 % | 83.55 % | 86.86 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.27 % | 16.8334 | 66.26 % | 75.2 % | 80.12 % | 84.13 % | 88.82 % | 91.79 % |
| 0.35 ATR | 1.779 % | 16.7467 | 52.47 % | 65.42 % | 72.15 % | 78.26 % | 85.26 % | 88.5 % |
| 0.5 ATR | 2.541 % | 16.6168 | 37.66 % | 53.43 % | 61.65 % | 68.96 % | 79.17 % | 84.29 % |
| 0.75 ATR | 3.811 % | 16.4002 | 20.24 % | 36.79 % | 46.92 % | 56.93 % | 69.61 % | 77.41 % |
| 1.0 ATR | 5.082 % | 16.1836 | 8.86 % | 24.4 % | 33.8 % | 44.99 % | 59.25 % | 68.58 % |
| 1.25 ATR | 6.352 % | 15.967 | 4.13 % | 14.92 % | 23.61 % | 35.39 % | 50.0 % | 61.91 % |
| 1.5 ATR | 7.623 % | 15.7504 | 2.01 % | 9.48 % | 16.65 % | 27.4 % | 41.87 % | 55.34 % |
| 2.0 ATR | 10.163 % | 15.3171 | 0.7 % | 4.33 % | 8.27 % | 15.27 % | 29.07 % | 45.07 % |
| 2.5 ATR | 12.704 % | 14.8839 | 0.3 % | 1.92 % | 3.73 % | 9.4 % | 19.72 % | 35.73 % |
| 3.0 ATR | 15.245 % | 14.4507 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 14.13 % | 28.34 % |
| 4.0 ATR | 20.327 % | 13.5843 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.52 % | 14.78 % |
| 6.0 ATR | 30.49 % | 11.8514 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.90 ATR | 1.00 ATR | 1.32 ATR | 1.60 ATR | 1.80 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.40 ATR | 1.85 ATR | 2.22 ATR | 2.48 ATR | 3.62 ATR | 4.76 ATR |
| **20 s.** | 0.82 ATR | 1.76 ATR | 2.00 ATR | 2.69 ATR | 3.25 ATR | 3.62 ATR | 4.82 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.541 %, prix 16.6168), p(touche) 37.66 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.627–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.811 %, prix 16.4002), p(touche) 36.79 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.787–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.082 %, prix 16.1835), p(touche) 33.8 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.082 %, prix 16.1835), p(touche) 44.99 % (en stress 97.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.404–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.623 %, prix 15.7503), p(touche) 41.87 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.004–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (12.704 %, prix 14.884), p(touche) 35.73 % (en stress 98.98 %)  ✅ optimum identifie (72.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.011 | EV/share : $0.007 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 30 % | T3 12 %
- Kelly (position) : f* 0.219 | ¼-Kelly 0.055 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 72.4 | bear 8.5 | side 19.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.386% → cible +1.668% / stop −4.0%, p_fill 64%, n_eff≈27.7) : P(cible|rempli) **52%** · **EV/risk -0.003** (×p_fill ; si rempli -0.02% du capital)
  - **swing** (entrée dip −3.058% → cible +3.731% / stop −5.242%, p_fill 47%, n_eff≈21.2) : P(cible|rempli) **70%** · **EV/risk +0.128** (×p_fill ; si rempli +1.43% du capital)
  - **deep** (entrée dip −4.727% → cible +5.276% / stop −8.001%, p_fill 32%, n_eff≈16.8) : P(cible|rempli) **67%** · **EV/risk +0.040** (×p_fill ; si rempli +1.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→70% · +2.0%→49% · +3.0%→36% · +5.0%→12% · +8.0%→1%
- Range intraday médian 4.41% (p90 7.54%) · excursion haute méd. +1.83% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.051% vs midi 0.863% vs clôture 0.995% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑2%/↓0% ; spike-down 62% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. -0.133% ; recovery-V 28%
- **σ réalisé intraday** 2.65% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 58% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 17.845 (VA 17.825–17.905 ; dernier close 17.89)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 69% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.8% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.32% · baisse 42% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.77%) · haut méd +0.72% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −2.8%) · haut méd +1.0% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.14% (p90 −3.2%) · haut méd +1.13% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.71%) · haut méd +1.33% · range méd 3.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 74% (120/159) · gap 30% · délai 0.1min · rebond 53% (64/120) (MFE +1.19%)
   - −1.0% : fill 30min 52% · séance 65% (109/159) · gap 22% · délai 1.5min · rebond 56% (64/109) (MFE +1.09%)
   - −1.5% : fill 30min 40% · séance 61% (100/159) · gap 19% · délai 10.3min · rebond 66% (67/100) (MFE +1.44%)
   - −2.0% : fill 30min 33% · séance 47% (79/159) · gap 10% · délai 10.4min · rebond 69% (55/79) (MFE +1.8%)
   - −3.0% : fill 30min 12% · séance 33% (56/159) · gap 3% · délai 48.9min · rebond 57% (37/56) (MFE +1.13%)
   - −4.0% : fill 30min 8% · séance 17% (35/159) · gap 2% · délai 39.2min · rebond 57% (23/35) (MFE +1.36%)
   - −5.0% : fill 30min 3% · séance 9% (19/159) · gap 2% · délai 99.6min · rebond 32% (9/19) (MFE +0.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.9%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −2.07%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.45%) → stop au-delà de −1.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=669 jambes) : jambe baissière méd −1.05% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 57% (39/64)
      · −2.0% : fill 84% (54/65) · rebond 75% (39/54)
      · −3.0% : fill 64% (41/65) · rebond 61% (28/41)
      · −4.0% : fill 34% (27/65) · rebond 70% (20/27)
      · −5.0% : fill 18% (15/65) · rebond 40% (8/15)
   - **flat** (22 séances) :
      · −1.0% : fill 67% (13/22) · rebond 42% (6/13)
      · −2.0% : fill 45% (8/22) · rebond 56% (5/8)
      · −3.0% : fill 35% (6/22) · rebond 38% (3/6)
      · −4.0% : fill 22% (3/22) · rebond 30% (1/3)
      · −5.0% : fill 13% (1/22) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 42% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 21% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 11% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 61% si les 15 1res min sont vertes (75 cas) · 26% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **52min** → P(séance verte=clôture>ouverture) 79% si début vert vs 13% si rouge (base 42% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **79%** · continue >prix actuel 56% ; creux résiduel méd -1.09% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.39% / q75 +2.94% → **scale +1.39% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **13%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.27%** (au-delà de la MAE q10 -3.27%), cible rebond +1.24% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.91% .. +3.73%] · haut q95 +4.02% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.13% .. +3.73%] · haut q95 +4.54% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.94%] · haut q95 +5.28% · bas q05 -4.64%
   - 4h (n=160) : retour [-4.56% .. +4.61%] · haut q95 +5.68% · bas q05 -5.14%
   - 6h (n=160) : retour [-4.79% .. +4.08%] · haut q95 +5.71% · bas q05 -5.8%
   - session (n=160) : retour [-4.73% .. +5.08%] · haut q95 +5.71% · bas q05 -6.02%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 44.2  _(momentum baissier)_
- **ADX** : 14.9  _(pas de tendance nette)_
- **MACD** : hist -0.123  _(bearish_recent)_
- **BB** : %B -0.11 · largeur 10.8%
- **ATR** : 0.87 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.237  _(distribution)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 59.6  _(transition)_
- **MA** : MA20 18.25 · MA50 17.83 · MA200 20.11  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 -4.4% · MA200 -15.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (767018 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
