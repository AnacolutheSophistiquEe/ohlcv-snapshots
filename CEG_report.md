# CEG

**Generated** : 2026-09-03T00:30:40.949226+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $290.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $290.10 (+2.3% vs entrée) · entrée $283.46 · stop $279.21 · T1 $286.45 · R/R 0.7  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.029 _(réel 5 s)_ (GBM 0.077) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.9 % ≠ (strike 275.0 − spot 290.10)/spot = -5.2 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -562 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 1.06 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $282.86–$284.06 (mid $283.46)
- Spot actuel : $290.10 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : $279.21 (stop swing_plan-based (-8.13%))
- Targets : T1 $286.45 · R/R 0.7 | T2 $289.44 · R/R 1.41 | T3 $292.43 · R/R 2.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $279.21


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.98 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.13 %)** : le gap seul le franchit 0.173 % des séances (2 fois sur 1159).
   - exécution **4.741 pt plus bas** dans le cas TYPIQUE (médiane), 7.104 au p90, **7.694 au pire**
   - perte réelle **12.871 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 8.13 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0082 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.827 % | p01 -4.437 % | pire -15.824 % _(sur 1159 séances)_
- **P(stop avant cible)** _(source : daily, 1160 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3901** [0.3197 ; 0.4641] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.4036** [0.3528 ; 0.456] _(largeur 10.3 pt, n_eff 345.4)_
   - deep : **0.4128** [0.3618 ; 0.4653] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (50.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.1 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.72 % contre 2.84 % aujourd'hui, rapport 2.02)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.62 % vs -9.57 % si l'on extrapolait par √5 _(rapport 1.006 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1843** (β de hausse 1.1894, asymétrie 0.9958) vs SPY — 532 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 257.7552 sur swing_based (3.02 ATR, 11.15 %) — p(stop avant cible) 0.2438 [0.20 ; 0.29], R/R 1.852, perte reelle 15.824 % (gap inclus), CVaR 11.154 %, EV -1.3533 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.636 %) — p(stop avant cible) 0.6023 [0.55 ; 0.65], R/R 4.017, perte reelle 7.297 % (gap inclus), EV -1.5783 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.602, borne haute 0.653 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 1.2 % x 29.31 % + P(rien) 38.6 % x 6.41 % ne couvrent pas P(stop) 60.2 % x 7.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.02 ATR (stop 11.15 %) — p(stop avant cible) 0.2438 [0.20 ; 0.29], R/R 1.852, perte reelle 15.824 % (gap inclus), EV -1.3533 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 1.2 % x 29.31 % + P(rien) 74.4 % x 2.89 % ne couvrent pas P(stop) 24.4 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.9 ATR (stop 23.127 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.267, perte reelle 23.127 % (gap inclus), EV 0.1152 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.13 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.773 %) — p(stop avant cible) 0.9389 [0.91 ; 0.96], R/R 15.147, perte reelle 1.935 % (gap inclus), EV -1.1915 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 15.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.939, borne haute 0.961 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.3 % x 29.31 % + P(rien) 5.8 % x 9.21 % ne couvrent pas P(stop) 93.9 % x 1.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.545 %) — p(stop avant cible) 0.8518 [0.81 ; 0.89], R/R 9.692, perte reelle 3.024 % (gap inclus), EV -1.1865 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 9.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.852, borne haute 0.886 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.7 % x 29.31 % + P(rien) 14.1 % x 8.33 % ne couvrent pas P(stop) 85.2 % x 3.02 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.318 %) — p(stop avant cible) 0.7506 [0.70 ; 0.79], R/R 7.138, perte reelle 4.106 % (gap inclus), EV -0.9602 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 7.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.751, borne haute 0.794 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 0.9 % x 29.31 % + P(rien) 24.1 % x 7.77 % ne couvrent pas P(stop) 75.1 % x 4.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.09 %) — p(stop avant cible) 0.6865 [0.64 ; 0.73], R/R 5.375, perte reelle 5.453 % (gap inclus), EV -1.2629 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.686, borne haute 0.734 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 1.1 % x 29.31 % + P(rien) 30.3 % x 7.16 % ne couvrent pas P(stop) 68.7 % x 5.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.863 %) — p(stop avant cible) 0.6474 [0.60 ; 0.70], R/R 4.834, perte reelle 6.063 % (gap inclus), EV -1.2361 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.647, borne haute 0.696 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 1.2 % x 29.31 % + P(rien) 34.1 % x 6.89 % ne couvrent pas P(stop) 64.7 % x 6.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.408 %) — p(stop avant cible) 0.5574 [0.50 ; 0.61], R/R 3.559, perte reelle 8.236 % (gap inclus), EV -1.732 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.557, borne haute 0.609 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 1.2 % x 29.31 % + P(rien) 43.1 % x 5.84 % ne couvrent pas P(stop) 55.7 % x 8.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.181 %) — p(stop avant cible) 0.5092 [0.46 ; 0.56], R/R 3.142, perte reelle 9.329 % (gap inclus), EV -1.8561 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.509, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.86 %) : P(cible) 1.2 % x 29.31 % + P(rien) 47.9 % x 5.33 % ne couvrent pas P(stop) 50.9 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.954 %) — p(stop avant cible) 0.4449 [0.39 ; 0.50], R/R 2.614, perte reelle 11.211 % (gap inclus), EV -2.0704 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 1.2 % x 29.31 % + P(rien) 54.4 % x 4.74 % ne couvrent pas P(stop) 44.5 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.726 %) — p(stop avant cible) 0.3809 [0.33 ; 0.43], R/R 2.614, perte reelle 11.211 % (gap inclus), EV -1.4689 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.47 %) : P(cible) 1.2 % x 29.31 % + P(rien) 60.8 % x 4.05 % ne couvrent pas P(stop) 38.1 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.499 %) — p(stop avant cible) 0.3454 [0.30 ; 0.40], R/R 2.277, perte reelle 12.871 % (gap inclus), EV -1.7022 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.70 %) : P(cible) 1.2 % x 29.31 % + P(rien) 64.3 % x 3.74 % ne couvrent pas P(stop) 34.5 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.02 ATR (stop 10.259 %) — p(stop avant cible) 0.274 [0.23 ; 0.32], R/R 1.852, perte reelle 15.824 % (gap inclus), EV -1.7434 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 1.2 % x 29.31 % + P(rien) 71.4 % x 3.15 % ne couvrent pas P(stop) 27.4 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.362 %) — p(stop avant cible) 0.2012 [0.16 ; 0.25], R/R 1.852, perte reelle 15.824 % (gap inclus), EV -0.9288 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 1.2 % x 29.31 % + P(rien) 78.7 % x 2.41 % ne couvrent pas P(stop) 20.1 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.907 %) — p(stop avant cible) 0.159 [0.12 ; 0.20], R/R 1.852, perte reelle 15.824 % (gap inclus), EV -0.5235 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 1.2 % x 29.31 % + P(rien) 82.9 % x 1.97 % ne couvrent pas P(stop) 15.9 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 15.452 %) — p(stop avant cible) 0.1026 [0.07 ; 0.14], R/R 1.852, perte reelle 15.824 % (gap inclus), EV -0.1358 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 1.2 % x 29.31 % + P(rien) 88.5 % x 1.28 % ne couvrent pas P(stop) 10.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 16.998 %) — p(stop avant cible) 0.0551 [0.03 ; 0.08], R/R 1.724, perte reelle 16.998 % (gap inclus), EV -0.0051 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 1.2 % x 29.31 % + P(rien) 93.3 % x 0.62 % ne couvrent pas P(stop) 5.5 % x 17.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 18.543 %) — p(stop avant cible) 0.0382 [0.02 ; 0.06], R/R 1.581, perte reelle 18.543 % (gap inclus), EV -0.0171 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 1.2 % x 29.31 % + P(rien) 95.0 % x 0.35 % ne couvrent pas P(stop) 3.8 % x 18.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 20.088 %) — p(stop avant cible) 0.0205 [0.01 ; 0.04], R/R 1.459, perte reelle 20.088 % (gap inclus), EV 0.0663 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.09 % > budget 12.00 %
   - 🟢 grid_snapped a 6.9 ATR (stop 22.237 %) — p(stop avant cible) 0.0112 [0.00 ; 0.03], R/R 1.318, perte reelle 22.237 % (gap inclus), EV 0.1224 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.24 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.724 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 1.185, perte reelle 24.724 % (gap inclus), EV 0.1388 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.72 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 290.1, ATR14 8.9655 (3.09 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.385 ATR = 1.19 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.155 % | 289.6517 | 91.55 % | 94.54 % | 95.54 % | 96.65 % | 97.53 % | 97.95 % |
| 0.1 ATR | 0.309 % | 289.2035 | 85.43 % | 90.31 % | 92.31 % | 93.97 % | 95.51 % | 96.7 % |
| 0.15 ATR | 0.464 % | 288.7552 | 78.87 % | 85.97 % | 88.29 % | 90.39 % | 93.6 % | 95.34 % |
| 0.2 ATR | 0.618 % | 288.3069 | 71.86 % | 80.62 % | 83.95 % | 86.59 % | 91.12 % | 93.98 % |
| 0.25 ATR | 0.773 % | 287.8586 | 64.96 % | 75.06 % | 79.15 % | 82.91 % | 88.31 % | 92.05 % |
| 0.35 ATR | 1.082 % | 286.9621 | 53.5 % | 65.48 % | 71.13 % | 76.42 % | 83.71 % | 88.41 % |
| 0.5 ATR | 1.545 % | 285.6172 | 38.49 % | 52.34 % | 58.97 % | 65.7 % | 76.4 % | 82.61 % |
| 0.75 ATR | 2.318 % | 283.3759 | 20.13 % | 36.08 % | 44.48 % | 52.63 % | 66.07 % | 75.57 % |
| 1.0 ATR | 3.09 % | 281.1345 | 11.12 % | 23.61 % | 32.66 % | 42.68 % | 56.85 % | 69.09 % |
| 1.25 ATR | 3.863 % | 278.8931 | 5.78 % | 16.04 % | 23.86 % | 34.97 % | 50.9 % | 62.84 % |
| 1.5 ATR | 4.636 % | 276.6517 | 2.78 % | 10.58 % | 17.17 % | 28.6 % | 44.16 % | 57.16 % |
| 2.0 ATR | 6.181 % | 272.1689 | 0.89 % | 4.34 % | 9.14 % | 17.77 % | 31.35 % | 46.25 % |
| 2.5 ATR | 7.726 % | 267.6862 | 0.44 % | 2.23 % | 4.68 % | 10.84 % | 20.9 % | 36.36 % |
| 3.0 ATR | 9.271 % | 263.2034 | 0.0 % | 1.11 % | 2.79 % | 6.7 % | 15.39 % | 28.41 % |
| 4.0 ATR | 12.362 % | 254.2379 | 0.0 % | 0.22 % | 0.89 % | 2.57 % | 6.74 % | 14.2 % |
| 6.0 ATR | 18.543 % | 236.3068 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.79 % | 2.73 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.95 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.90 ATR | 2.60 ATR | 3.41 ATR |
| **10 s.** | 0.53 ATR | 1.28 ATR | 1.47 ATR | 1.94 ATR | 2.30 ATR | 2.58 ATR | 3.62 ATR | 4.58 ATR |
| **20 s.** | 0.77 ATR | 1.83 ATR | 2.06 ATR | 2.71 ATR | 3.24 ATR | 3.59 ATR | 4.73 ATR | 5.60 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.435–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.545 %, prix 285.618), p(touche) 38.49 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.318 %, prix 283.3755), p(touche) 36.08 % (en stress 88.89 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.741–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.318 %, prix 283.3755), p(touche) 44.48 % (en stress 97.78 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.942–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.09 %, prix 281.1359), p(touche) 42.68 % (en stress 96.67 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.469–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.636 %, prix 276.651), p(touche) 44.16 % (en stress 98.88 %)  ✅ optimum identifie (73.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.063–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.726 %, prix 267.6869), p(touche) 36.36 % (en stress 95.45 %)  ✅ optimum identifie (87.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.077 | EV/share : $0.326 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 67 % | T2 35 % | T3 12 %
- Kelly (position) : f* 0.137 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 81.2 | bear 5.8 | side 13.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 290.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.294% → cible +1.055% / stop −1.5%, p_fill 22%, n_eff≈12.2) : P(cible|rempli) **46%** · **EV/risk -0.029** (×p_fill ; si rempli -0.19% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→71% · +2.0%→39% · +3.0%→16% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.19% (p90 5.36%) · excursion haute méd. +1.53% / basse méd. −1.13%
- Profil de vol intra : ouverture 2.336% vs midi 0.648% vs clôture 0.766% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.061)_ ; drift intra méd. -0.094% ; recovery-V 6%
- **σ réalisé intraday** 2.25% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 65% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 279.8442 (VA 277.5613–281.3663 ; dernier close 280.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 41% · **stop −2.19%** sous le fill (sous le bruit) · cible +0.73% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.54% · baisse 36% (gap-down >1% 12% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −1.83%) · haut méd +0.88% · range méd 1.6%
- Excursion ouverture 15min (n=160) : bas méd −0.61% (p90 −2.17%) · haut méd +1.04% · range méd 1.98%
- Excursion ouverture 30min (n=160) : bas méd −0.71% (p90 −2.55%) · haut méd +1.22% · range méd 2.18%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.85%) · haut méd +1.36% · range méd 2.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 280.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 62% (105/159) · gap 20% · délai 1.4min · rebond 58% (61/105) (MFE +1.13%)
   - −1.0% : fill 30min 34% · séance 50% (89/159) · gap 12% · délai 4.5min · rebond 49% (48/89) (MFE +0.98%)
   - −1.5% : fill 30min 26% · séance 38% (70/159) · gap 8% · délai 8.0min · rebond 42% (35/70) (MFE +0.82%)
   - −2.0% : fill 30min 21% · séance 33% (59/159) · gap 3% · délai 12.9min · rebond 56% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 6% · séance 16% (31/159) · gap 1% · délai 46.4min · rebond 41% (13/31) (MFE +0.73%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 1% · délai 42.9min · rebond 63% (11/18) (MFE +1.2%)
   - −5.0% : fill 30min 2% · séance 4% (11/159) · gap 0% · délai 46.0min · rebond 88% (9/11) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −1.04%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −0.98%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.52% (p90 −1.29%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=466 jambes) : jambe baissière méd −1.06% (p90 −2.51%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 88% (39/42) · rebond 68% (26/39)
      · −2.0% : fill 70% (31/42) · rebond 56% (18/31)
      · −3.0% : fill 34% (16/42) · rebond 27% (6/16)
      · −4.0% : fill 30% (13/42) · rebond 64% (8/13)
      · −5.0% : fill 15% (9/42) · rebond 87% (7/9)
   - **flat** (27 séances) :
      · −1.0% : fill 59% (20/27) · rebond 12% (5/20)
      · −2.0% : fill 38% (12/27) · rebond 46% (6/12)
      · −3.0% : fill 17% (7/27) · rebond 22% (2/7)
      · −4.0% : fill 6% (3/27) · rebond 42% (2/3)
      · −5.0% : fill 1% (1/27) · rebond 100% (1/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 30% (30/90) · rebond 46% (17/30)
      · −2.0% : fill 15% (16/90) · rebond 61% (9/16)
      · −3.0% : fill 8% (8/90) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/90) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/90) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 65% si les 15 1res min sont vertes (92 cas) · 33% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 84% si début vert vs 10% si rouge (base 51% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **84%** · continue >prix actuel 46% ; creux résiduel méd -1.23% (q20 -1.9%) → **SL/trailing à −1.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.87% / q75 +1.31% → **scale +0.87% / runner +1.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **10%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.34%** (au-delà de la MAE q10 -2.34%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.09% .. +2.27%] · haut q95 +2.58% · bas q05 -3.42%
   - 60min (n=160) : retour [-3.64% .. +2.82%] · haut q95 +3.15% · bas q05 -4.61%
   - 2h (n=160) : retour [-3.7% .. +3.01%] · haut q95 +4.21% · bas q05 -4.64%
   - 4h (n=160) : retour [-2.97% .. +3.35%] · haut q95 +4.47% · bas q05 -4.67%
   - 6h (n=160) : retour [-4.04% .. +3.54%] · haut q95 +4.74% · bas q05 -4.71%
   - session (n=160) : retour [-3.62% .. +3.56%] · haut q95 +4.69% · bas q05 -4.71%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 5.0% / strong 1.9%) · base = 11 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 16% vs absente 3% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.37% / p90 2.39%) · ~2.0 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **61%** (reprise méd 20.0 min, n=24)
   - −1.0% → **56%** (reprise méd 54.64 min, n=11)
   - −1.5% → **7%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.39%** (p90, défaut prudent ; serré/agressif −1.37%) ; extension open→close méd +3.51% (q75 +3.93% / q95 +5.58%), MFE méd +4.09% / q90 +5.3%
   - Échelle scale-out : +4.09% (33%) / +5.12% (33%) / +5.3% (34%)
- **DÉSARMER** : repli > **−2.39%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.3% : P(retournement après) 0% (mèche méd 0.83%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.9  _(momentum haussier)_
- **ADX** : 16.0  _(pas de tendance nette)_
- **MACD** : hist 0.642  _(pas de croisement recent)_
- **BB** : %B 1.06 · largeur 9.2%
- **ATR** : 8.97 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.146  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 59.7  _(transition)_
- **MA** : MA20 275.85 · MA50 265.17 · MA200 295.93  _(prix > MA20)_
- **Dist MA** : MA20 +5.2% · MA50 +9.4% · MA200 -2.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (504093 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
