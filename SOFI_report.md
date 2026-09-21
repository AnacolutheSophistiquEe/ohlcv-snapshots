# SOFI

**Generated** : 2026-09-21T00:47:54.027898+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.96  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.96 (+1.1% vs entrée) · entrée $16.77 · stop $16.09 · T1 $17.06 · R/R 0.43  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk -0.043 _(réel 5 s)_ (GBM 0.021) · ¼-Kelly 0.054 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.71–$16.82 (mid $16.77)
- Spot actuel : $16.96 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $16.09 (stop swing_plan-based (-6.31%))
- Targets : T1 $17.06 · R/R 0.43 | T2 $17.35 · R/R 0.85 | T3 $17.65 · R/R 1.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.90 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.31 %)** : le gap seul le franchit 1.196 % des séances (15 fois sur 1254).
   - exécution **1.241 pt plus bas** dans le cas TYPIQUE (médiane), 3.515 au p90, **4.795 au pire**
   - perte réelle **8.058 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 6.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0209 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.226 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1327** [0.0884 ; 0.1892] _(largeur 10.1 pt, n_eff 173.1)_
   - swing : **0.5192** [0.4666 ; 0.5715] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4862** [0.4338 ; 0.5388] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.8 pt), swing (38.4 pt), deep (38.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1080 séances)** : VaR **-5.98 %** | CVaR **-8.42 %** | vol 3.96 %/j
   - _fenêtre arrêtée : rupture de regime a 1140 seances en arriere (volatilite 5.67 % contre 3.53 % aujourd'hui, rapport 1.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8245** (β de hausse 1.706, asymétrie 1.0694) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.35× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 15.1931 sur atr_grid (2.75 ATR, 10.418 %) — p(stop avant cible) 0.321 [0.27 ; 0.37], R/R 4.401, perte reelle 11.105 % (gap inclus), CVaR 10.419 %, EV -0.7232 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.25 ATR (stop 3.404 %) — p(stop avant cible) 0.76 [0.71 ; 0.80], R/R 9.304, perte reelle 5.253 % (gap inclus), EV -1.8199 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.760, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 0.0 % x 48.88 % + P(rien) 24.0 % x 9.00 % ne couvrent pas P(stop) 76.0 % x 5.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.683 %) — p(stop avant cible) 0.5834 [0.53 ; 0.63], R/R 6.485, perte reelle 7.537 % (gap inclus), EV -1.3155 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.583, borne haute 0.634 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.0 % x 48.88 % + P(rien) 41.6 % x 7.36 % ne couvrent pas P(stop) 58.3 % x 7.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.31 ATR (stop 7.437 %) — p(stop avant cible) 0.4653 [0.41 ; 0.52], R/R 5.323, perte reelle 9.182 % (gap inclus), EV -1.1201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 0.0 % x 48.88 % + P(rien) 53.4 % x 5.86 % ne couvrent pas P(stop) 46.5 % x 9.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.24 ATR (stop 14.734 %) — p(stop avant cible) 0.1311 [0.10 ; 0.17], R/R 3.317, perte reelle 14.734 % (gap inclus), EV 0.0324 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.73 % > budget 12.00 %
   - ⚪ grid_snapped a 0.25 ATR (stop 2.071 %) — p(stop avant cible) 0.882 [0.84 ; 0.91], R/R 13.31, perte reelle 3.672 % (gap inclus), EV -1.7995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 13.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.882, borne haute 0.913 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.80 %) : P(cible) 0.0 % x 48.88 % + P(rien) 11.8 % x 12.14 % ne couvrent pas P(stop) 88.2 % x 3.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.841 %) — p(stop avant cible) 0.8298 [0.79 ; 0.87], R/R 10.437, perte reelle 4.683 % (gap inclus), EV -2.1119 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.830, borne haute 0.867 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.11 %) : P(cible) 0.0 % x 48.88 % + P(rien) 17.0 % x 10.36 % ne couvrent pas P(stop) 83.0 % x 4.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.63 %) — p(stop avant cible) 0.5117 [0.46 ; 0.56], R/R 5.873, perte reelle 8.322 % (gap inclus), EV -1.1044 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.512, borne haute 0.564 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 0.0 % x 48.88 % + P(rien) 48.8 % x 6.42 % ne couvrent pas P(stop) 51.2 % x 8.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.524 %) — p(stop avant cible) 0.4061 [0.36 ; 0.46], R/R 5.035, perte reelle 9.707 % (gap inclus), EV -0.8732 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 0.0 % x 48.88 % + P(rien) 59.4 % x 5.14 % ne couvrent pas P(stop) 40.6 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.471 %) — p(stop avant cible) 0.3777 [0.33 ; 0.43], R/R 4.858, perte reelle 10.061 % (gap inclus), EV -0.8024 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 0.0 % x 48.88 % + P(rien) 62.2 % x 4.79 % ne couvrent pas P(stop) 37.8 % x 10.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.418 %) — p(stop avant cible) 0.321 [0.27 ; 0.37], R/R 4.401, perte reelle 11.105 % (gap inclus), EV -0.7232 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 0.0 % x 48.88 % + P(rien) 67.9 % x 4.16 % ne couvrent pas P(stop) 32.1 % x 11.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.24 ATR (stop 13.401 %) — p(stop avant cible) 0.1854 [0.15 ; 0.23], R/R 3.647, perte reelle 13.401 % (gap inclus), EV -0.0627 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.0 % x 48.88 % + P(rien) 81.4 % x 2.95 % ne couvrent pas P(stop) 18.5 % x 13.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 17.047 %) — p(stop avant cible) 0.0768 [0.05 ; 0.11], R/R 2.867, perte reelle 17.047 % (gap inclus), EV 0.1856 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.942 %) — p(stop avant cible) 0.0583 [0.04 ; 0.09], R/R 2.58, perte reelle 18.942 % (gap inclus), EV 0.1719 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.94 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.836 %) — p(stop avant cible) 0.0425 [0.02 ; 0.07], R/R 2.346, perte reelle 20.836 % (gap inclus), EV 0.1484 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.84 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.73 %) — p(stop avant cible) 0.031 [0.02 ; 0.05], R/R 2.15, perte reelle 22.73 % (gap inclus), EV 0.1274 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.73 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.624 %) — p(stop avant cible) 0.0212 [0.01 ; 0.04], R/R 1.985, perte reelle 24.624 % (gap inclus), EV 0.1609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.62 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.518 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 1.843, perte reelle 26.518 % (gap inclus), EV 0.2645 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.52 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.412 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 1.72, perte reelle 28.412 % (gap inclus), EV 0.261 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.41 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.307 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 1.613, perte reelle 30.307 % (gap inclus), EV 0.2669 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.31 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.96, ATR14 0.6425 (3.788 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 1.413 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 16.9279 | 92.66 % | 95.67 % | 96.98 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.379 % | 16.8957 | 85.01 % | 89.33 % | 91.94 % | 93.23 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.568 % | 16.8636 | 78.77 % | 84.59 % | 87.9 % | 90.3 % | 92.79 % | 94.77 % |
| 0.2 ATR | 0.758 % | 16.8315 | 71.43 % | 79.36 % | 83.27 % | 86.77 % | 90.46 % | 93.23 % |
| 0.25 ATR | 0.947 % | 16.7994 | 66.1 % | 74.82 % | 79.84 % | 84.04 % | 88.83 % | 91.79 % |
| 0.35 ATR | 1.326 % | 16.7351 | 52.31 % | 65.16 % | 71.88 % | 78.18 % | 85.28 % | 88.51 % |
| 0.5 ATR | 1.894 % | 16.6387 | 37.53 % | 53.07 % | 61.39 % | 68.89 % | 79.19 % | 84.31 % |
| 0.75 ATR | 2.841 % | 16.4781 | 20.32 % | 36.56 % | 46.47 % | 56.67 % | 69.44 % | 77.44 % |
| 1.0 ATR | 3.788 % | 16.3175 | 8.75 % | 24.27 % | 33.67 % | 44.85 % | 59.19 % | 68.82 % |
| 1.25 ATR | 4.735 % | 16.1569 | 4.12 % | 14.8 % | 23.59 % | 35.15 % | 49.95 % | 62.05 % |
| 1.5 ATR | 5.682 % | 15.9962 | 2.01 % | 9.26 % | 16.43 % | 27.17 % | 42.03 % | 55.59 % |
| 2.0 ATR | 7.577 % | 15.675 | 0.7 % | 4.33 % | 8.27 % | 15.05 % | 28.93 % | 44.62 % |
| 2.5 ATR | 9.471 % | 15.3537 | 0.3 % | 1.91 % | 3.83 % | 9.39 % | 19.49 % | 35.18 % |
| 3.0 ATR | 11.365 % | 15.0325 | 0.1 % | 0.91 % | 2.82 % | 6.06 % | 13.6 % | 27.9 % |
| 4.0 ATR | 15.153 % | 14.39 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.41 % | 14.67 % |
| 6.0 ATR | 22.73 % | 13.105 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.37 ATR | 0.42 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.11 ATR | 1.47 ATR | 1.93 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.89 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.59 ATR | 1.80 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.41 ATR | 1.84 ATR | 2.21 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.82 ATR | 1.75 ATR | 1.98 ATR | 2.65 ATR | 3.22 ATR | 3.60 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.424–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.894 %, prix 16.6388), p(touche) 37.53 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.622–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.841 %, prix 16.4782), p(touche) 36.56 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.779–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.788 %, prix 16.3176), p(touche) 33.67 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.997–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.788 %, prix 16.3176), p(touche) 44.85 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.406–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.682 %, prix 15.9963), p(touche) 42.03 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.983–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.577 %, prix 15.6749), p(touche) 44.62 % (en stress 98.98 %)  ✅ optimum identifie (74.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.021 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 28 % | T3 14 %
- Kelly (position) : f* 0.215 | ¼-Kelly 0.054 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 77.0 | bear 7.1 | side 15.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.146% → cible +1.749% / stop −4.0%, p_fill 63%, n_eff≈29.2) : P(cible|rempli) **39%** · **EV/risk -0.043** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −2.522% → cible +3.911% / stop −3.886%, p_fill 58%, n_eff≈23.4) : P(cible|rempli) **54%** · **EV/risk +0.077** (×p_fill ; si rempli +0.51% du capital)
  - **deep** (entrée dip −3.898% → cible +5.531% / stop −5.913%, p_fill 49%, n_eff≈22.2) : P(cible|rempli) **58%** · **EV/risk +0.080** (×p_fill ; si rempli +0.96% du capital)
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

- **RSI** : 39.7  _(momentum baissier)_
- **ADX** : 11.3  _(pas de tendance nette)_
- **MACD** : hist -0.145  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 17.3%
- **ATR** : 0.64 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.038  _(neutre)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 53.7  _(transition)_
- **MA** : MA20 17.84 · MA50 17.72 · MA200 19.52  _(prix < MA20)_
- **Dist MA** : MA20 -4.9% · MA50 -4.3% · MA200 -13.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (807234 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
