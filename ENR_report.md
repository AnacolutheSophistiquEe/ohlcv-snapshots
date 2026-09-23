# ENR

**Generated** : 2026-09-23T00:08:12.705722+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €145.98  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €145.98 (+0.5% vs entrée) · entrée €145.25 · stop €133.63 · T1 €147.54 · R/R 0.2  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.042 _(réel 5 s)_ (GBM -0.06) · ¼-Kelly 0.079 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €144.79–€145.71 (mid €145.25)
- Spot actuel : €145.98 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €133.63 (stop swing_plan-based (-4.51%))
- Targets : T1 €147.54 · R/R 0.2 | T2 €149.83 · R/R 0.39 | T3 €152.13 · R/R 0.59
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €133.63


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.51 %)** : le gap seul le franchit 1.413 % des séances (18 fois sur 1274).
   - exécution **1.345 pt plus bas** dans le cas TYPIQUE (médiane), 9.886 au p90, **31.247 au pire**
   - perte réelle **8.475 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 4.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.056 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0082** [0.0013 ; 0.031] _(largeur 3.0 pt, n_eff 173.1)_
   - swing : **0.5173** [0.4647 ; 0.5696] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4956** [0.4431 ; 0.5482] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 33.6 observations effectives », dont la borne haute a 95 % vaut environ 8.9 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 31.3 observations effectives », dont la borne haute a 95 % vaut environ 9.6 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 33.1 observations effectives », dont la borne haute a 95 % vaut environ 9.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.4 pt), swing (27.9 pt), deep (30.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.65 %** | CVaR **-6.68 %** | vol 3.21 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.89 % contre 3.20 % aujourd'hui, rapport 1.84)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3534** (β de hausse 1.0885, asymétrie 1.2433) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.352× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 137.2675 sur atr_grid (1.75 ATR, 5.968 %) — p(stop avant cible) 0.5323 [0.48 ; 0.58], R/R 2.271, perte reelle 12.609 % (gap inclus), CVaR 6.01 %, EV -3.8343 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1632 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 6.01 % > budget 5.46 %
- Budget de queue : **5.46 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.313 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 45.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.69 ATR (stop 4.552 %) — p(stop avant cible) 0.63 [0.58 ; 0.68], R/R 3.193, perte reelle 8.968 % (gap inclus), EV -2.8918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.630, borne haute 0.680 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 0.5 % x 28.64 % + P(rien) 36.4 % x 7.14 % ne couvrent pas P(stop) 63.0 % x 8.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.15 ATR (stop 12.958 %) — p(stop avant cible) 0.106 [0.08 ; 0.14], R/R 1.31, perte reelle 21.854 % (gap inclus), EV -0.2683 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 0.5 % x 28.64 % + P(rien) 88.8 % x 2.13 % ne couvrent pas P(stop) 10.6 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 7.21 ATR (stop 26.799 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.801, perte reelle 35.757 % (gap inclus), EV 1.1103 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.81 % > budget 5.46 %
      - ⚠ support DETECTE a 0.59 ATR du spot — compartiment <1, mesure a 47.1 % de casse (IC clusterise [0.438 ; 0.505] sur 1121 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 10.44 ATR (stop 37.815 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.757, perte reelle 37.815 % (gap inclus), EV 1.153 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.81 % > budget 5.46 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.853 %) — p(stop avant cible) 0.9385 [0.91 ; 0.96], R/R 13.143, perte reelle 2.179 % (gap inclus), EV -1.3865 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.939, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 0.1 % x 28.64 % + P(rien) 6.0 % x 10.26 % ne couvrent pas P(stop) 93.8 % x 2.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.69 ATR (stop 3.369 %) — p(stop avant cible) 0.7216 [0.67 ; 0.77], R/R 4.18, perte reelle 6.851 % (gap inclus), EV -2.6122 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.722, borne haute 0.767 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.5 % x 28.64 % + P(rien) 27.4 % x 8.03 % ne couvrent pas P(stop) 72.2 % x 6.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 5.116 %) — p(stop avant cible) 0.6133 [0.56 ; 0.66], R/R 2.883, perte reelle 9.934 % (gap inclus), EV -3.2871 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.613, borne haute 0.663 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.29 %) : P(cible) 0.5 % x 28.64 % + P(rien) 38.1 % x 6.95 % ne couvrent pas P(stop) 61.3 % x 9.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.968 %) — p(stop avant cible) 0.5323 [0.48 ; 0.58], R/R 2.271, perte reelle 12.609 % (gap inclus), EV -3.8343 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.01 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.83 %) : P(cible) 0.5 % x 28.64 % + P(rien) 46.2 % x 5.88 % ne couvrent pas P(stop) 53.2 % x 12.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.821 %) — p(stop avant cible) 0.4874 [0.43 ; 0.54], R/R 1.943, perte reelle 14.737 % (gap inclus), EV -4.3299 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.86 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.33 %) : P(cible) 0.5 % x 28.64 % + P(rien) 50.7 % x 5.32 % ne couvrent pas P(stop) 48.7 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.674 %) — p(stop avant cible) 0.4171 [0.37 ; 0.47], R/R 1.542, perte reelle 18.578 % (gap inclus), EV -4.8236 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.71 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.82 %) : P(cible) 0.5 % x 28.64 % + P(rien) 57.7 % x 4.79 % ne couvrent pas P(stop) 41.7 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.526 %) — p(stop avant cible) 0.348 [0.30 ; 0.40], R/R 1.542, perte reelle 18.578 % (gap inclus), EV -3.6854 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.56 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.69 %) : P(cible) 0.5 % x 28.64 % + P(rien) 64.6 % x 4.06 % ne couvrent pas P(stop) 34.8 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.379 %) — p(stop avant cible) 0.2997 [0.25 ; 0.35], R/R 1.31, perte reelle 21.854 % (gap inclus), EV -3.8248 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.41 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.82 %) : P(cible) 0.5 % x 28.64 % + P(rien) 69.5 % x 3.70 % ne couvrent pas P(stop) 30.0 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.15 ATR (stop 11.775 %) — p(stop avant cible) 0.1565 [0.12 ; 0.20], R/R 1.31, perte reelle 21.854 % (gap inclus), EV -1.2539 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.80 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.5 % x 28.64 % + P(rien) 83.8 % x 2.40 % ne couvrent pas P(stop) 15.7 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.642 %) — p(stop avant cible) 0.0918 [0.06 ; 0.13], R/R 1.103, perte reelle 25.963 % (gap inclus), EV -0.4498 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.66 % > budget 5.46 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.5 % x 28.64 % + P(rien) 90.3 % x 1.97 % ne couvrent pas P(stop) 9.2 % x 25.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.347 %) — p(stop avant cible) 0.0514 [0.03 ; 0.08], R/R 1.103, perte reelle 25.963 % (gap inclus), EV 0.3478 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.36 % > budget 5.46 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.052 %) — p(stop avant cible) 0.0336 [0.02 ; 0.06], R/R 0.801, perte reelle 35.757 % (gap inclus), EV 0.3335 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.07 % > budget 5.46 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.757 %) — p(stop avant cible) 0.0241 [0.01 ; 0.04], R/R 0.801, perte reelle 35.757 % (gap inclus), EV 0.5908 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.77 % > budget 5.46 %
   - ⚪ atr_grid a 6.0 ATR (stop 20.463 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 0.801, perte reelle 35.757 % (gap inclus), EV 0.8815 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.48 % > budget 5.46 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.168 %) — p(stop avant cible) 0.0076 [0.00 ; 0.02], R/R 0.801, perte reelle 35.757 % (gap inclus), EV 0.9684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.18 % > budget 5.46 %
   - 🔴 grid_snapped a 7.21 ATR (stop 25.615 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.801, perte reelle 35.757 % (gap inclus), EV 1.0899 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.62 % > budget 5.46 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.284 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.801, perte reelle 35.757 % (gap inclus), EV 1.1103 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.29 % > budget 5.46 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 145.98, ATR14 4.9786 (3.41 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.248 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 145.7311 | 91.52 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.341 % | 145.4821 | 83.83 % | 88.15 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.512 % | 145.2332 | 76.23 % | 82.33 % | 85.87 % | 88.71 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.682 % | 144.9843 | 70.32 % | 79.07 % | 83.0 % | 86.53 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.853 % | 144.7354 | 63.81 % | 74.83 % | 79.45 % | 83.47 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.194 % | 144.2375 | 51.68 % | 64.96 % | 70.45 % | 76.04 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.705 % | 143.4907 | 36.19 % | 51.83 % | 59.49 % | 66.53 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.558 % | 142.2461 | 19.72 % | 35.93 % | 45.26 % | 54.55 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.41 % | 141.0014 | 11.14 % | 25.37 % | 34.29 % | 44.06 % | 56.72 % | 64.92 % |
| 1.25 ATR | 4.263 % | 139.7568 | 6.11 % | 17.37 % | 25.1 % | 35.74 % | 48.26 % | 57.29 % |
| 1.5 ATR | 5.116 % | 138.5121 | 2.76 % | 11.06 % | 17.79 % | 27.82 % | 41.09 % | 50.95 % |
| 2.0 ATR | 6.821 % | 136.0229 | 0.79 % | 3.95 % | 8.6 % | 16.24 % | 28.16 % | 39.8 % |
| 2.5 ATR | 8.526 % | 133.5336 | 0.3 % | 1.97 % | 3.95 % | 9.41 % | 19.3 % | 30.05 % |
| 3.0 ATR | 10.231 % | 131.0443 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.24 % | 22.21 % |
| 4.0 ATR | 13.642 % | 126.0657 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.36 % |
| 6.0 ATR | 20.463 % | 116.1086 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.57 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.39 ATR |
| **5 s.** | 0.37 ATR | 0.86 ATR | 0.98 ATR | 1.34 ATR | 1.62 ATR | 1.84 ATR | 2.46 ATR | 2.98 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.18 ATR | 2.46 ATR | 3.38 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.77 ATR | 2.35 ATR | 2.82 ATR | 3.22 ATR | 4.67 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.415–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.607–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.558 %, prix 142.2458), p(touche) 35.93 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.756–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.41 %, prix 141.0021), p(touche) 34.29 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.2 % des re-echantillons)
- **5 seance(s)** : plage utile 0.978–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.41 %, prix 141.0021), p(touche) 44.06 % (en stress 99.01 %)  ✅ optimum identifie (90.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.364–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.116 %, prix 138.5117), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (93.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.767–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.821 %, prix 136.0227), p(touche) 39.8 % (en stress 99.0 %)  ✅ optimum identifie (89.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : €-0.698 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 19 % | T3 8 %
- Kelly (position) : f* 0.314 | ¼-Kelly 0.079 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 15.2 | side 79.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 146.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.5% → cible +1.578% / stop −8.0%, p_fill 85%, n_eff≈33.6) : P(cible|rempli) **44%** · **EV/risk -0.042** (×p_fill ; si rempli -0.39% du capital)
  - **swing** (entrée dip −1.099% → cible +3.529% / stop −3.448%, p_fill 80%, n_eff≈31.3) : P(cible|rempli) **21%** · **EV/risk -0.476** (×p_fill ; si rempli -2.06% du capital)
  - **deep** (entrée dip −1.704% → cible +4.991% / stop −5.204%, p_fill 84%, n_eff≈33.1) : P(cible|rempli) **33%** · **EV/risk -0.330** (×p_fill ; si rempli -2.06% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→59% · +2.0%→39% · +3.0%→20% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.81% (p90 6.15%) · excursion haute méd. +1.47% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.113% vs midi 0.87% vs clôture 1.056% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑1%/↓0% ; spike-down 58% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr -0.022)_ ; drift intra méd. -0.48% ; recovery-V 14%
- **σ réalisé intraday** 2.425% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 69% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 147.6975 (VA 146.6265–147.9355 ; dernier close 146.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 66% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.27% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 33% (gap-down >1% 18% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −1.67%) · haut méd +0.43% · range méd 1.16%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.21%) · haut méd +0.58% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.63% · range méd 1.92%
- Excursion ouverture 60min (n=160) : bas méd −1.0% (p90 −2.6%) · haut méd +0.74% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 73% (116/159) · gap 25% · délai 0.4min · rebond 59% (65/116) (MFE +1.2%)
   - −1.0% : fill 30min 46% · séance 67% (107/159) · gap 18% · délai 6.9min · rebond 62% (62/107) (MFE +1.53%)
   - −1.5% : fill 30min 30% · séance 53% (89/159) · gap 14% · délai 10.1min · rebond 62% (53/89) (MFE +1.52%)
   - −2.0% : fill 30min 21% · séance 42% (74/159) · gap 10% · délai 33.3min · rebond 65% (50/74) (MFE +1.49%)
   - −3.0% : fill 30min 11% · séance 28% (52/159) · gap 4% · délai 208.4min · rebond 53% (33/52) (MFE +1.05%)
   - −4.0% : fill 30min 7% · séance 19% (38/159) · gap 2% · délai 129.6min · rebond 66% (27/38) (MFE +1.27%)
   - −5.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 398.5min · rebond 36% (13/25) (MFE +0.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.58%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.68%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.43% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=543 jambes) : jambe baissière méd −1.09% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 98% (51/52) · rebond 58% (28/51)
      · −2.0% : fill 73% (39/52) · rebond 49% (23/39)
      · −3.0% : fill 60% (31/52) · rebond 40% (18/31)
      · −4.0% : fill 48% (26/52) · rebond 71% (20/26)
      · −5.0% : fill 36% (18/52) · rebond 39% (11/18)
   - **flat** (14 séances) :
      · −1.0% : fill 85% (12/14) · rebond 91% (10/12)
      · −2.0% : fill 51% (8/14) · rebond 88% (6/8)
      · −3.0% : fill 25% (5/14) · rebond 76% (3/5)
      · −4.0% : fill 14% (4/14) · rebond 52% (2/4)
      · −5.0% : fill 11% (3/14) · rebond 0% (0/3)
   - **gap-up** (93 séances) :
      · −1.0% : fill 48% (44/93) · rebond 56% (24/44)
      · −2.0% : fill 25% (27/93) · rebond 78% (21/27)
      · −3.0% : fill 12% (16/93) · rebond 74% (12/16)
      · −4.0% : fill 5% (8/93) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/93) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 75% si les 15 1res min sont vertes (75 cas) · 20% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:26** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 45% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **76%** · continue >prix actuel 56% ; creux résiduel méd -1.11% (q20 -2.16%) → **SL/trailing à −2.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.28% → **scale +1.46% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **21%** (continue à baisser 56%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.96%** (au-delà de la MAE q10 -3.96%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.05% .. +1.95%] · haut q95 +2.65% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.48% .. +2.32%] · haut q95 +2.69% · bas q05 -2.94%
   - 2h (n=160) : retour [-2.79% .. +2.64%] · haut q95 +2.9% · bas q05 -3.6%
   - 4h (n=160) : retour [-3.15% .. +2.61%] · haut q95 +3.68% · bas q05 -3.96%
   - 6h (n=160) : retour [-3.7% .. +3.22%] · haut q95 +4.1% · bas q05 -4.58%
   - session (n=160) : retour [-4.9% .. +3.93%] · haut q95 +5.13% · bas q05 -6.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 54.0  _(neutre)_
- **ADX** : 13.1  _(pas de tendance nette)_
- **MACD** : hist 0.479  _(bullish_recent)_
- **BB** : %B 0.62 · largeur 14.5%
- **ATR** : 4.98 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.197  _(distribution)_
- **Vol ratio** : 0.34  _(volume atone)_
- **Choppiness** : 48.7  _(transition)_
- **MA** : MA20 143.5 · MA50 148.6 · MA200 152.3  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 -1.8% · MA200 -4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (860938 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
