# HOOD

**Generated** : 2026-08-27T00:35:44.202018+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $108.54  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $108.54 (+2.7% vs entrée) · entrée $105.64 · stop $99.79 · T1 $115.09 · R/R 1.62  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.023 _(réel 5 s)_ (GBM 0.037) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $104.48–$106.81 (mid $105.64)
- Spot actuel : $108.54 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : $99.79 (stop swing_plan-based (-8.06%))
- Targets : T1 $115.09 · R/R 1.62 | T2 $121.68 · R/R 2.74 | T3 $123.02 · R/R 2.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $99.79


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.06 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **2.606 pt plus bas** dans le cas TYPIQUE (médiane), 6.432 au p90, **9.725 au pire**
   - perte réelle **11.287 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 8.06 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0258 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.458 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3095** [0.2442 ; 0.3811] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.4775** [0.4252 ; 0.5302] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4562** [0.4042 ; 0.5089] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.2 pt), swing (37.2 pt), deep (38.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.35 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.05 % contre 4.48 % aujourd'hui, rapport 0.46)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.5 % si l'on extrapolait par √5 _(rapport 1.003 ; < 1 = le √5 surestime)_
- **β de baisse : 1.752** (β de hausse 1.6148, asymétrie 1.0849) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.49× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 96.8286 sur atr_grid (2.0 ATR, 10.79 %) — p(stop avant cible) 0.3556 [0.31 ; 0.41], R/R 1.011, perte reelle 13.192 % (gap inclus), CVaR 10.8 %, EV 0.3203 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 24 des 24 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 55.6 % de la queue et il ne reste que -172.39 EUR a partager. Prix du risque -0.087 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.1 ATR (stop 8.296 %) — p(stop avant cible) 0.4489 [0.40 ; 0.50], R/R 1.182, perte reelle 11.287 % (gap inclus), EV -0.2521 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.90 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.451 ; 0.510] sur 1199 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 33.1 % x 13.34 % + P(rien) 22.0 % x 1.80 % ne couvrent pas P(stop) 44.9 % x 11.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.92 ATR (stop 18.118 %) — p(stop avant cible) 0.1224 [0.09 ; 0.16], R/R 0.736, perte reelle 18.118 % (gap inclus), EV 1.5331 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.12 % > budget 12.00 %
   - 🟢 support a 5.06 ATR (stop 29.643 %) — p(stop avant cible) 0.0257 [0.01 ; 0.05], R/R 0.45, perte reelle 29.643 % (gap inclus), EV 1.5683 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.64 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.349 %) — p(stop avant cible) 0.8906 [0.85 ; 0.92], R/R 4.386, perte reelle 3.041 % (gap inclus), EV -1.4048 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 8.9 % x 13.34 % + P(rien) 2.0 % x 5.67 % ne couvrent pas P(stop) 89.1 % x 3.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.697 %) — p(stop avant cible) 0.7848 [0.74 ; 0.83], R/R 2.813, perte reelle 4.741 % (gap inclus), EV -1.1319 % — **REFUSE**
      - refuse : p_stop_first 0.785, borne haute 0.826 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 18.1 % x 13.34 % + P(rien) 3.5 % x 5.23 % ne couvrent pas P(stop) 78.5 % x 4.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.046 %) — p(stop avant cible) 0.6851 [0.63 ; 0.73], R/R 2.015, perte reelle 6.619 % (gap inclus), EV -1.0317 % — **REFUSE**
      - refuse : p_stop_first 0.685, borne haute 0.732 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 23.8 % x 13.34 % + P(rien) 7.7 % x 4.26 % ne couvrent pas P(stop) 68.5 % x 6.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 1.1 ATR (stop 7.552 %) — p(stop avant cible) 0.5 [0.45 ; 0.55], R/R 1.271, perte reelle 10.494 % (gap inclus), EV -0.676 % — **REFUSE**
      - refuse : p_stop_first 0.500, borne haute 0.552 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 31.7 % x 13.34 % + P(rien) 18.3 % x 1.89 % ne couvrent pas P(stop) 50.0 % x 10.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.441 %) — p(stop avant cible) 0.3952 [0.34 ; 0.45], R/R 1.082, perte reelle 12.322 % (gap inclus), EV 0.1474 % — **REFUSE**
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 10.79 %) — p(stop avant cible) 0.3556 [0.31 ; 0.41], R/R 1.011, perte reelle 13.192 % (gap inclus), EV 0.3203 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 12.139 %) — p(stop avant cible) 0.3002 [0.25 ; 0.35], R/R 0.836, perte reelle 15.955 % (gap inclus), EV 0.3021 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.15 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.487 %) — p(stop avant cible) 0.2581 [0.21 ; 0.31], R/R 0.836, perte reelle 15.955 % (gap inclus), EV 0.7465 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.49 % > budget 12.00 %
   - 🟢 grid_snapped a 2.92 ATR (stop 17.373 %) — p(stop avant cible) 0.1353 [0.10 ; 0.17], R/R 0.75, perte reelle 17.785 % (gap inclus), EV 1.4562 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.37 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 18.882 %) — p(stop avant cible) 0.1085 [0.08 ; 0.14], R/R 0.706, perte reelle 18.882 % (gap inclus), EV 1.523 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.88 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 21.58 %) — p(stop avant cible) 0.0792 [0.05 ; 0.11], R/R 0.618, perte reelle 21.58 % (gap inclus), EV 1.4966 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.58 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.277 %) — p(stop avant cible) 0.0387 [0.02 ; 0.06], R/R 0.549, perte reelle 24.277 % (gap inclus), EV 1.5901 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.28 % > budget 12.00 %
   - 🟢 grid_snapped a 5.06 ATR (stop 28.899 %) — p(stop avant cible) 0.0273 [0.01 ; 0.05], R/R 0.462, perte reelle 28.899 % (gap inclus), EV 1.5533 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.90 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 32.37 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 0.412, perte reelle 32.37 % (gap inclus), EV 1.6317 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.37 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.067 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.38, perte reelle 35.067 % (gap inclus), EV 1.7027 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.07 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 37.765 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.353, perte reelle 37.765 % (gap inclus), EV 1.7157 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.76 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 40.462 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.33, perte reelle 40.462 % (gap inclus), EV 1.7358 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.46 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 43.16 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.309, perte reelle 43.16 % (gap inclus), EV 1.7358 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.16 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 108.54, ATR14 5.8557 (5.395 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.372 ATR = 2.007 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.27 % | 108.2472 | 92.85 % | 94.96 % | 95.86 % | 96.36 % | 96.95 % | 97.95 % |
| 0.1 ATR | 0.539 % | 107.9544 | 85.5 % | 90.32 % | 92.03 % | 93.43 % | 94.51 % | 96.41 % |
| 0.15 ATR | 0.809 % | 107.6616 | 77.64 % | 85.08 % | 87.79 % | 89.89 % | 92.28 % | 94.97 % |
| 0.2 ATR | 1.079 % | 107.3689 | 71.6 % | 79.94 % | 83.55 % | 86.55 % | 90.14 % | 93.22 % |
| 0.25 ATR | 1.349 % | 107.0761 | 64.35 % | 74.09 % | 78.91 % | 83.01 % | 87.5 % | 90.97 % |
| 0.35 ATR | 1.888 % | 106.4905 | 52.27 % | 65.02 % | 71.64 % | 77.15 % | 83.13 % | 88.09 % |
| 0.5 ATR | 2.697 % | 105.6121 | 36.76 % | 53.12 % | 60.54 % | 67.95 % | 76.42 % | 82.75 % |
| 0.75 ATR | 4.046 % | 104.1482 | 19.44 % | 35.99 % | 45.61 % | 55.41 % | 65.65 % | 73.72 % |
| 1.0 ATR | 5.395 % | 102.6843 | 9.26 % | 22.68 % | 32.29 % | 43.68 % | 54.98 % | 66.22 % |
| 1.25 ATR | 6.744 % | 101.2204 | 4.83 % | 14.42 % | 22.2 % | 33.16 % | 47.05 % | 59.96 % |
| 1.5 ATR | 8.092 % | 99.7564 | 2.42 % | 9.98 % | 16.25 % | 26.59 % | 40.04 % | 54.21 % |
| 2.0 ATR | 10.79 % | 96.8286 | 0.5 % | 3.93 % | 7.37 % | 15.57 % | 29.98 % | 44.76 % |
| 2.5 ATR | 13.487 % | 93.9007 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.54 % | 35.11 % |
| 3.0 ATR | 16.185 % | 90.9729 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.69 % |
| 4.0 ATR | 21.58 % | 85.1172 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 32.37 % | 73.4057 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.08 ATR | 1.50 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.18 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.57 ATR | 1.80 ATR | 2.38 ATR | 3.09 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.32 ATR | 1.85 ATR | 2.29 ATR | 2.63 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.71 ATR | 1.72 ATR | 1.99 ATR | 2.62 ATR | 3.14 ATR | 3.57 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.42–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.619–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.046 %, prix 104.1485), p(touche) 35.99 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.761–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.395 %, prix 102.6843), p(touche) 32.29 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.5 % des re-echantillons)
- **5 seance(s)** : plage utile 0.972–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.395 %, prix 102.6843), p(touche) 43.68 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.323–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.092 %, prix 99.7569), p(touche) 40.04 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.987–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.79 %, prix 96.8285), p(touche) 44.76 % (en stress 97.96 %)  ✅ optimum identifie (62.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : $0.218 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 14 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 75.4 | bear 16.5 | side 8.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 543.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.216% → cible +4.769% / stop −3.0%, p_fill 74%, n_eff≈30.8) : P(cible|rempli) **17%** · **EV/risk +0.069** (×p_fill ; si rempli +0.28% du capital)
  - **swing** (entrée dip −2.665% → cible +8.938% / stop −5.543%, p_fill 60%, n_eff≈24.8) : P(cible|rempli) **22%** · **EV/risk -0.023** (×p_fill ; si rempli -0.21% du capital)
  - **deep** (entrée dip −4.127% → cible +16.924% / stop −8.462%, p_fill 47%, n_eff≈22.3) : P(cible|rempli) **17%** · **EV/risk -0.060** (×p_fill ; si rempli -1.09% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→56% · +3.0%→36% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.11% (p90 8.97%) · excursion haute méd. +2.18% / basse méd. −2.27%
- Profil de vol intra : ouverture 3.796% vs midi 1.047% vs clôture 1.151% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 68% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr -0.001)_ ; drift intra méd. 0.049% ; recovery-V 36%
- **σ réalisé intraday** 3.62% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 46% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 107.6269 (VA 106.8176–108.4361 ; dernier close 108.13)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 29% · rebond 81% · **stop −4.58%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. 0.04% · baisse 48% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.68%) · haut méd +0.93% · range méd 2.18%
- Excursion ouverture 15min (n=160) : bas méd −1.24% (p90 −3.85%) · haut méd +1.26% · range méd 2.84%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −4.15%) · haut méd +1.7% · range méd 3.44%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −4.65%) · haut méd +1.73% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 108.13 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 78% (124/159) · gap 41% · délai 0.0min · rebond 57% (66/124) (MFE +1.44%)
   - −1.0% : fill 30min 59% · séance 69% (110/159) · gap 32% · délai 0.0min · rebond 63% (65/110) (MFE +1.54%)
   - −1.5% : fill 30min 50% · séance 59% (100/159) · gap 24% · délai 0.3min · rebond 60% (58/100) (MFE +1.34%)
   - −2.0% : fill 30min 39% · séance 50% (88/159) · gap 16% · délai 0.1min · rebond 68% (55/88) (MFE +1.39%)
   - −3.0% : fill 30min 28% · séance 38% (68/159) · gap 7% · délai 6.6min · rebond 75% (47/68) (MFE +1.86%)
   - −4.0% : fill 30min 18% · séance 29% (50/159) · gap 3% · délai 10.7min · rebond 81% (34/50) (MFE +2.4%)
   - −5.0% : fill 30min 10% · séance 17% (33/159) · gap 2% · délai 19.6min · rebond 74% (24/33) (MFE +2.77%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.64% (p90 −2.43%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.4%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.43%) → stop au-delà de −1.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=768 jambes) : jambe baissière méd −1.13% (p90 −2.84%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 98% (70/72) · rebond 51% (36/70)
      · −2.0% : fill 82% (60/72) · rebond 62% (36/60)
      · −3.0% : fill 69% (50/72) · rebond 72% (34/50)
      · −4.0% : fill 53% (39/72) · rebond 83% (29/39)
      · −5.0% : fill 32% (27/72) · rebond 70% (19/27)
   - **flat** (20 séances) :
      · −1.0% : fill 64% (14/20) · rebond 80% (9/14)
      · −2.0% : fill 40% (11/20) · rebond 61% (7/11)
      · −3.0% : fill 14% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 13% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 6% (3/20) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 43% (26/67) · rebond 82% (20/26)
      · −2.0% : fill 22% (17/67) · rebond 90% (12/17)
      · −3.0% : fill 15% (12/67) · rebond 98% (11/12)
      · −4.0% : fill 10% (6/67) · rebond 91% (4/6)
      · −5.0% : fill 4% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 67% si les 15 1res min sont vertes (76 cas) · 33% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 79% si début vert vs 23% si rouge (base 49% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **79%** · continue >prix actuel 49% ; creux résiduel méd -1.18% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.27% / q75 +2.68% → **scale +1.27% / runner +2.68%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **23%** (continue à baisser 54%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.54%** (au-delà de la MAE q10 -3.54%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.44% .. +4.55%] · haut q95 +5.1% · bas q05 -5.19%
   - 60min (n=160) : retour [-4.07% .. +4.77%] · haut q95 +6.34% · bas q05 -5.74%
   - 2h (n=160) : retour [-4.97% .. +5.19%] · haut q95 +7.59% · bas q05 -6.14%
   - 4h (n=160) : retour [-5.09% .. +6.33%] · haut q95 +8.38% · bas q05 -6.84%
   - 6h (n=160) : retour [-5.77% .. +6.12%] · haut q95 +8.39% · bas q05 -7.13%
   - session (n=160) : retour [-5.53% .. +6.46%] · haut q95 +8.44% · bas q05 -7.22%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 3% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.51% / p90 2.85%) · ~3.22 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 18.0 min, n=47)
   - −1.0% → **60%** (reprise méd 33.9 min, n=22)
   - −1.5% → **33%** (reprise méd 52.28 min, n=12)
   - −2.0% → **14%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.85%** (p90, défaut prudent ; serré/agressif −1.51%) ; extension open→close méd +6.37% (q75 +9.03% / q95 +12.96%), MFE méd +8.27% / q90 +14.38%
   - Échelle scale-out : +8.27% (33%) / +9.8% (33%) / +14.38% (34%)
- **DÉSARMER** : repli > **−2.85%** depuis le plus-haut = décay → P(retournement) **80%** (préavis méd 259.06 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.38% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 83% du temps (retour médian dernière heure +0.49%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 66.9  _(momentum haussier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist 2.042  _(pas de croisement recent)_
- **BB** : %B 0.94 · largeur 28.9%
- **ATR** : 5.86 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.083  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 51.6  _(transition)_
- **MA** : MA20 96.18 · MA50 101.12 · MA200 95.67  _(prix > MA20)_
- **Dist MA** : MA20 +12.9% · MA50 +7.3% · MA200 +13.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (809613 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
