# EVT

**Generated** : 2026-09-24T00:06:30.460554+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €2.82  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €2.82 (+4.4% vs entrée) · entrée €2.70 · stop €2.59 · T1 €2.73 · R/R 0.27  
> ↳ P(T1 av. stop) 69 % · EV/risk -0.036 · ¼-Kelly 0.061 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.430 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €2.69–€2.71 (mid €2.70)
- Spot actuel : €2.82 (+4.4% au-dessus de la zone — repli à attendre)
- Stop : €2.59 (stop swing_plan-based (-12.28%))
- Targets : T1 €2.73 · R/R 0.27 | T2 €2.77 · R/R 0.64 | T3 €2.80 · R/R 0.91
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €2.59


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.28 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **9.331 pt plus bas** dans le cas TYPIQUE (médiane), 17.973 au p90, **20.133 au pire**
   - perte réelle **22.616 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 12.28 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0243 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0983** [0.0606 ; 0.1493] _(largeur 8.9 pt, n_eff 173.1)_
   - swing : **0.3738** [0.324 ; 0.4257] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3568** [0.3077 ; 0.4083] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.98 %** | CVaR **-9.06 %** | vol 3.74 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1136** (β de hausse 0.9517, asymétrie 1.1701) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.5278 sur atr_grid (2.5 ATR, 10.235 %) — p(stop avant cible) 0.3277 [0.28 ; 0.38], R/R 2.192, perte reelle 18.001 % (gap inclus), CVaR 10.265 %, EV -3.9275 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.63 ATR (stop 4.606 %) — p(stop avant cible) 0.6508 [0.60 ; 0.70], R/R 3.368, perte reelle 11.717 % (gap inclus), EV -5.054 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.651, borne haute 0.700 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.05 %) : P(cible) 0.1 % x 39.46 % + P(rien) 34.8 % x 7.23 % ne couvrent pas P(stop) 65.1 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 6.14 %) — p(stop avant cible) 0.5398 [0.49 ; 0.59], R/R 3.036, perte reelle 12.996 % (gap inclus), EV -4.3252 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.540, borne haute 0.592 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.33 %) : P(cible) 0.2 % x 39.46 % + P(rien) 45.8 % x 5.71 % ne couvrent pas P(stop) 54.0 % x 13.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.023 %) — p(stop avant cible) 0.9097 [0.88 ; 0.94], R/R 15.228, perte reelle 2.591 % (gap inclus), EV -1.4037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 15.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.910, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 0.1 % x 39.46 % + P(rien) 8.9 % x 10.30 % ne couvrent pas P(stop) 91.0 % x 2.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.63 ATR (stop 3.824 %) — p(stop avant cible) 0.7085 [0.66 ; 0.75], R/R 4.386, perte reelle 8.996 % (gap inclus), EV -4.1227 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.709, borne haute 0.754 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.12 %) : P(cible) 0.1 % x 39.46 % + P(rien) 29.0 % x 7.60 % ne couvrent pas P(stop) 70.9 % x 9.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.164 %) — p(stop avant cible) 0.4661 [0.41 ; 0.52], R/R 2.192, perte reelle 18.001 % (gap inclus), EV -5.9076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.91 %) : P(cible) 0.2 % x 39.46 % + P(rien) 53.2 % x 4.53 % ne couvrent pas P(stop) 46.6 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.188 %) — p(stop avant cible) 0.4117 [0.36 ; 0.46], R/R 2.192, perte reelle 18.001 % (gap inclus), EV -5.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.07 %) : P(cible) 0.2 % x 39.46 % + P(rien) 58.6 % x 3.87 % ne couvrent pas P(stop) 41.2 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.211 %) — p(stop avant cible) 0.3587 [0.31 ; 0.41], R/R 2.192, perte reelle 18.001 % (gap inclus), EV -4.3303 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.33 %) : P(cible) 0.2 % x 39.46 % + P(rien) 63.9 % x 3.21 % ne couvrent pas P(stop) 35.9 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.235 %) — p(stop avant cible) 0.3277 [0.28 ; 0.38], R/R 2.192, perte reelle 18.001 % (gap inclus), EV -3.9275 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.93 %) : P(cible) 0.2 % x 39.46 % + P(rien) 67.0 % x 2.83 % ne couvrent pas P(stop) 32.8 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.258 %) — p(stop avant cible) 0.2977 [0.25 ; 0.35], R/R 1.98, perte reelle 19.926 % (gap inclus), EV -4.1361 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.14 %) : P(cible) 0.2 % x 39.46 % + P(rien) 70.0 % x 2.46 % ne couvrent pas P(stop) 29.8 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.282 %) — p(stop avant cible) 0.2451 [0.20 ; 0.29], R/R 1.745, perte reelle 22.616 % (gap inclus), EV -4.1724 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.17 %) : P(cible) 0.2 % x 39.46 % + P(rien) 75.3 % x 1.72 % ne couvrent pas P(stop) 24.5 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 14.329 %) — p(stop avant cible) 0.1713 [0.13 ; 0.21], R/R 1.461, perte reelle 27.012 % (gap inclus), EV -3.8914 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.89 %) : P(cible) 0.2 % x 39.46 % + P(rien) 82.7 % x 0.80 % ne couvrent pas P(stop) 17.1 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 16.376 %) — p(stop avant cible) 0.1277 [0.10 ; 0.17], R/R 1.461, perte reelle 27.012 % (gap inclus), EV -3.1341 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.13 %) : P(cible) 0.2 % x 39.46 % + P(rien) 87.0 % x 0.28 % ne couvrent pas P(stop) 12.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 18.423 %) — p(stop avant cible) 0.1018 [0.07 ; 0.14], R/R 1.461, perte reelle 27.012 % (gap inclus), EV -2.6908 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.69 %) : P(cible) 0.2 % x 39.46 % + P(rien) 89.6 % x -0.02 % ne couvrent pas P(stop) 10.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 20.47 %) — p(stop avant cible) 0.0944 [0.07 ; 0.13], R/R 1.461, perte reelle 27.012 % (gap inclus), EV -2.5876 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.59 %) : P(cible) 0.2 % x 39.46 % + P(rien) 90.4 % x -0.12 % ne couvrent pas P(stop) 9.4 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 22.517 %) — p(stop avant cible) 0.0908 [0.06 ; 0.12], R/R 1.217, perte reelle 32.413 % (gap inclus), EV -3.0427 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.04 %) : P(cible) 0.2 % x 39.46 % + P(rien) 90.7 % x -0.19 % ne couvrent pas P(stop) 9.1 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 24.564 %) — p(stop avant cible) 0.0798 [0.05 ; 0.11], R/R 1.217, perte reelle 32.413 % (gap inclus), EV -2.8913 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 0.2 % x 39.46 % + P(rien) 91.8 % x -0.41 % ne couvrent pas P(stop) 8.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 26.611 %) — p(stop avant cible) 0.0696 [0.05 ; 0.10], R/R 1.217, perte reelle 32.413 % (gap inclus), EV -2.7909 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.79 %) : P(cible) 0.2 % x 39.46 % + P(rien) 92.8 % x -0.66 % ne couvrent pas P(stop) 7.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 28.658 %) — p(stop avant cible) 0.0537 [0.03 ; 0.08], R/R 1.217, perte reelle 32.413 % (gap inclus), EV -2.6721 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.67 %) : P(cible) 0.2 % x 39.46 % + P(rien) 94.4 % x -1.07 % ne couvrent pas P(stop) 5.4 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 30.705 %) — p(stop avant cible) 0.0439 [0.03 ; 0.07], R/R 1.217, perte reelle 32.413 % (gap inclus), EV -2.5995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.60 %) : P(cible) 0.2 % x 39.46 % + P(rien) 95.4 % x -1.31 % ne couvrent pas P(stop) 4.4 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 32.752 %) — p(stop avant cible) 0.0439 [0.03 ; 0.07], R/R 1.205, perte reelle 32.752 % (gap inclus), EV -2.6144 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.2 % x 39.46 % + P(rien) 95.4 % x -1.31 % ne couvrent pas P(stop) 4.4 % x 32.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.816, ATR14 0.1153 (4.094 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.498 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.205 % | 2.8102 | 88.95 % | 91.81 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.409 % | 2.8045 | 81.46 % | 86.97 % | 89.62 % | 92.67 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.614 % | 2.7987 | 75.25 % | 83.12 % | 86.56 % | 89.9 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.819 % | 2.7929 | 68.93 % | 79.17 % | 83.3 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.023 % | 2.7872 | 63.21 % | 75.91 % | 80.24 % | 84.75 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.433 % | 2.7756 | 51.78 % | 67.62 % | 73.72 % | 79.8 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.047 % | 2.7584 | 35.5 % | 54.99 % | 62.75 % | 70.69 % | 80.1 % | 88.24 % |
| 0.75 ATR | 3.07 % | 2.7295 | 19.13 % | 37.91 % | 47.63 % | 59.5 % | 71.94 % | 81.91 % |
| 1.0 ATR | 4.094 % | 2.7007 | 10.06 % | 24.88 % | 35.87 % | 47.52 % | 62.49 % | 75.28 % |
| 1.25 ATR | 5.117 % | 2.6719 | 4.83 % | 17.28 % | 27.37 % | 39.5 % | 55.72 % | 70.05 % |
| 1.5 ATR | 6.141 % | 2.6431 | 2.96 % | 11.25 % | 19.66 % | 31.49 % | 48.66 % | 64.72 % |
| 2.0 ATR | 8.188 % | 2.5854 | 1.28 % | 4.94 % | 9.49 % | 19.41 % | 35.02 % | 52.66 % |
| 2.5 ATR | 10.235 % | 2.5278 | 0.49 % | 2.67 % | 5.63 % | 12.28 % | 27.76 % | 44.92 % |
| 3.0 ATR | 12.282 % | 2.4701 | 0.39 % | 1.68 % | 3.66 % | 8.61 % | 20.8 % | 37.99 % |
| 4.0 ATR | 16.376 % | 2.3549 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.64 % | 24.22 % |
| 6.0 ATR | 24.564 % | 2.1243 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.00 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.08 ATR | 1.33 ATR | 1.49 ATR | 1.98 ATR | 2.66 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.81 ATR | 3.81 ATR |
| **10 s.** | 0.66 ATR | 1.45 ATR | 1.63 ATR | 2.14 ATR | 2.70 ATR | 3.09 ATR | 4.51 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.17 ATR | 2.50 ATR | 3.36 ATR | 3.94 ATR | 4.80 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.07 %, prix 2.7295), p(touche) 37.91 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.806–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.094 %, prix 2.7007), p(touche) 35.87 % (en stress 96.08 %)  ✅ optimum identifie (63.5 % des re-echantillons)
- **5 seance(s)** : plage utile 1.079–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.117 %, prix 2.6719), p(touche) 39.5 % (en stress 95.05 %)  ✅ optimum identifie (77.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.634–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.188 %, prix 2.5854), p(touche) 35.02 % (en stress 97.03 %)  ✅ optimum identifie (74.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.495–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.235 %, prix 2.5278), p(touche) 44.92 % (en stress 98.0 %)  ✅ optimum identifie (84.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.02 | EV/share : €-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 29 % | T3 13 %
- Kelly (position) : f* 0.246 | ¼-Kelly 0.061 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 73.4 | bear 5.0 | side 21.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→69% · +2.0%→41% · +3.0%→21% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.26%) · excursion haute méd. +1.57% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.39% vs midi 1.183% vs clôture 1.156% _(ouverture ~2.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.092 ; mean-reverting — autocorr -0.184)_ ; drift intra méd. -0.657% ; recovery-V 22%
- **σ réalisé intraday** 2.883% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 75% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 3.2156 (VA 3.191–3.2341 ; dernier close 3.203)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 55% · rebond 63% · **stop −2.51%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 40% (gap-down >1% 9% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.2%) · haut méd +0.37% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.65%) · haut méd +0.56% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.77%) · haut méd +0.71% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.93%) · haut méd +0.88% · range méd 2.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.212 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 79% (131/159) · gap 22% · délai 1.0min · rebond 65% (88/131) (MFE +1.39%)
   - −1.0% : fill 30min 38% · séance 67% (112/159) · gap 9% · délai 6.9min · rebond 63% (74/112) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 55% (95/159) · gap 5% · délai 25.1min · rebond 63% (61/95) (MFE +1.33%)
   - −2.0% : fill 30min 19% · séance 44% (79/159) · gap 5% · délai 43.0min · rebond 50% (44/79) (MFE +0.99%)
   - −3.0% : fill 30min 9% · séance 23% (49/159) · gap 3% · délai 59.4min · rebond 66% (35/49) (MFE +1.5%)
   - −4.0% : fill 30min 4% · séance 10% (26/159) · gap 1% · délai 46.7min · rebond 53% (16/26) (MFE +1.13%)
   - −5.0% : fill 30min 3% · séance 6% (15/159) · gap 1% · délai 30.3min · rebond 59% (10/15) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −2.19%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.83%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −1.85%) → stop au-delà de −1.58% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=808 jambes) : jambe baissière méd −1.07% (p90 −2.28%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (47/55) · rebond 64% (32/47)
      · −2.0% : fill 62% (37/55) · rebond 48% (21/37)
      · −3.0% : fill 35% (25/55) · rebond 68% (18/25)
      · −4.0% : fill 21% (18/55) · rebond 42% (11/18)
      · −5.0% : fill 15% (12/55) · rebond 40% (7/12)
   - **flat** (35 séances) :
      · −1.0% : fill 85% (28/35) · rebond 49% (16/28)
      · −2.0% : fill 62% (21/35) · rebond 44% (9/21)
      · −3.0% : fill 35% (13/35) · rebond 79% (10/13)
      · −4.0% : fill 7% (3/35) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/35) · rebond 100% (1/1)
   - **gap-up** (69 séances) :
      · −1.0% : fill 49% (37/69) · rebond 73% (26/37)
      · −2.0% : fill 24% (21/69) · rebond 60% (14/21)
      · −3.0% : fill 9% (11/69) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/69) · rebond 95% (4/5)
      · −5.0% : fill 3% (2/69) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 62% si début vert vs 33% si rouge (base 45% · écart 29 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **62%** · continue >prix actuel 35% ; creux résiduel méd -1.77% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.42% → **scale +1.38% / runner +2.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **33%** (continue à baisser 55%) → **RÉDUIRE ~67%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.16%** (au-delà de la MAE q10 -4.16%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +2.07%] · haut q95 +2.96% · bas q05 -3.91%
   - 60min (n=160) : retour [-2.99% .. +2.44%] · haut q95 +3.08% · bas q05 -3.96%
   - 2h (n=160) : retour [-3.46% .. +2.37%] · haut q95 +3.72% · bas q05 -4.16%
   - 4h (n=160) : retour [-3.35% .. +3.62%] · haut q95 +4.28% · bas q05 -4.28%
   - 6h (n=160) : retour [-3.3% .. +3.75%] · haut q95 +5.24% · bas q05 -4.99%
   - session (n=160) : retour [-4.11% .. +4.05%] · haut q95 +5.66% · bas q05 -5.54%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 18.3  _(survente)_
- **ADX** : 35.8  _(tendance etablie)_
- **MACD** : hist -0.004  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 27.3%
- **ATR** : 0.12 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.435  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 41.6  _(transition)_
- **MA** : MA20 3.06 · MA50 3.3 · MA200 4.76  _(prix < MA20)_
- **Dist MA** : MA20 -7.9% · MA50 -14.7% · MA200 -40.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (847276 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
