# CEG

**Generated** : 2026-08-31T00:30:45.786103+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $276.75  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $276.75 (+2.7% vs entrée) · entrée $269.48 · stop $261.30 · T1 $276.25 · R/R 0.83  
> ↳ P(T1 av. stop) 52 % _(réel 5 s)_ · EV/risk -0.034 _(réel 5 s)_ (GBM 0.058) · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $268.12–$270.83 (mid $269.48)
- Spot actuel : $276.75 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : $261.30 (stop swing_plan-based (-5.58%))
- Targets : T1 $276.25 · R/R 0.83 | T2 $283.03 · R/R 1.66 | T3 $289.81 · R/R 2.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $261.30


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.99 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.58 %)** : le gap seul le franchit 0.433 % des séances (5 fois sur 1156).
   - exécution **2.31 pt plus bas** dans le cas TYPIQUE (médiane), 7.882 au p90, **10.244 au pire**
   - perte réelle **9.329 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 5.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0162 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.822 % | p01 -4.437 % | pire -15.824 % _(sur 1156 séances)_
- **P(stop avant cible)** _(source : daily, 1157 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4723** [0.3989 ; 0.5466] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4315** [0.38 ; 0.4841] _(largeur 10.4 pt, n_eff 345.4)_
   - deep : **0.4436** [0.3919 ; 0.4963] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.4 observations effectives », dont la borne haute a 95 % vaut environ 16.3 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.1 observations effectives », dont la borne haute a 95 % vaut environ 18.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.2 pt), swing (42.8 pt), deep (35.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.1 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.67 % contre 2.86 % aujourd'hui, rapport 1.99)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.63 % vs -9.58 % si l'on extrapolait par √5 _(rapport 1.005 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1843** (β de hausse 1.1919, asymétrie 0.9936) vs SPY — 530 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 244.0447 sur atr_grid (4.0 ATR, 11.818 %) — p(stop avant cible) 0.2216 [0.18 ; 0.27], R/R 2.252, perte reelle 15.824 % (gap inclus), CVaR 11.821 %, EV -1.0681 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.432 %) — p(stop avant cible) 0.6144 [0.56 ; 0.66], R/R 5.219, perte reelle 6.827 % (gap inclus), EV -1.3153 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.614, borne haute 0.665 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.6 % x 35.63 % + P(rien) 38.0 % x 7.05 % ne couvrent pas P(stop) 61.4 % x 6.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.66 ATR (stop 6.532 %) — p(stop avant cible) 0.475 [0.42 ; 0.53], R/R 3.178, perte reelle 11.211 % (gap inclus), EV -2.321 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.32 %) : P(cible) 0.6 % x 35.63 % + P(rien) 51.9 % x 5.40 % ne couvrent pas P(stop) 47.5 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.93 ATR (stop 19.145 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 1.861, perte reelle 19.145 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.15 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.739 %) — p(stop avant cible) 0.9504 [0.92 ; 0.97], R/R 18.883, perte reelle 1.887 % (gap inclus), EV -1.2407 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 18.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.950, borne haute 0.970 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 0.1 % x 35.63 % + P(rien) 4.8 % x 10.48 % ne couvrent pas P(stop) 95.0 % x 1.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.477 %) — p(stop avant cible) 0.8578 [0.82 ; 0.89], R/R 12.296, perte reelle 2.898 % (gap inclus), EV -1.118 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 12.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.858, borne haute 0.892 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 0.3 % x 35.63 % + P(rien) 13.9 % x 9.03 % ne couvrent pas P(stop) 85.8 % x 2.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.216 %) — p(stop avant cible) 0.7658 [0.72 ; 0.81], R/R 9.028, perte reelle 3.947 % (gap inclus), EV -0.9587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 9.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.766, borne haute 0.808 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 0.5 % x 35.63 % + P(rien) 22.9 % x 8.26 % ne couvrent pas P(stop) 76.6 % x 3.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.954 %) — p(stop avant cible) 0.6919 [0.64 ; 0.74], R/R 6.787, perte reelle 5.25 % (gap inclus), EV -1.1289 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.692, borne haute 0.739 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 0.5 % x 35.63 % + P(rien) 30.3 % x 7.66 % ne couvrent pas P(stop) 69.2 % x 5.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.693 %) — p(stop avant cible) 0.6554 [0.60 ; 0.70], R/R 6.001, perte reelle 5.938 % (gap inclus), EV -1.2037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.655, borne haute 0.704 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.6 % x 35.63 % + P(rien) 33.9 % x 7.34 % ne couvrent pas P(stop) 65.5 % x 5.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.66 ATR (stop 5.788 %) — p(stop avant cible) 0.5386 [0.49 ; 0.59], R/R 3.82, perte reelle 9.329 % (gap inclus), EV -2.0902 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.539, borne haute 0.591 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 0.6 % x 35.63 % + P(rien) 45.6 % x 6.00 % ne couvrent pas P(stop) 53.9 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.386 %) — p(stop avant cible) 0.4187 [0.37 ; 0.47], R/R 3.178, perte reelle 11.211 % (gap inclus), EV -1.7422 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 0.6 % x 35.63 % + P(rien) 57.6 % x 4.78 % ne couvrent pas P(stop) 41.9 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.125 %) — p(stop avant cible) 0.3659 [0.32 ; 0.42], R/R 2.768, perte reelle 12.871 % (gap inclus), EV -1.8544 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.85 %) : P(cible) 0.6 % x 35.63 % + P(rien) 62.8 % x 4.23 % ne couvrent pas P(stop) 36.6 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 8.863 %) — p(stop avant cible) 0.3424 [0.29 ; 0.39], R/R 2.768, perte reelle 12.871 % (gap inclus), EV -1.6226 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.62 %) : P(cible) 0.6 % x 35.63 % + P(rien) 65.2 % x 3.96 % ne couvrent pas P(stop) 34.2 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.34 %) — p(stop avant cible) 0.2777 [0.23 ; 0.33], R/R 2.252, perte reelle 15.824 % (gap inclus), EV -1.7346 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 0.6 % x 35.63 % + P(rien) 71.7 % x 3.43 % ne couvrent pas P(stop) 27.8 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 11.818 %) — p(stop avant cible) 0.2216 [0.18 ; 0.27], R/R 2.252, perte reelle 15.824 % (gap inclus), EV -1.0681 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 0.6 % x 35.63 % + P(rien) 77.2 % x 2.87 % ne couvrent pas P(stop) 22.2 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.295 %) — p(stop avant cible) 0.1829 [0.14 ; 0.23], R/R 2.252, perte reelle 15.824 % (gap inclus), EV -0.6634 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 0.6 % x 35.63 % + P(rien) 81.1 % x 2.48 % ne couvrent pas P(stop) 18.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 14.772 %) — p(stop avant cible) 0.1343 [0.10 ; 0.17], R/R 2.252, perte reelle 15.824 % (gap inclus), EV -0.2757 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.6 % x 35.63 % + P(rien) 86.0 % x 1.89 % ne couvrent pas P(stop) 13.4 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 16.249 %) — p(stop avant cible) 0.0731 [0.05 ; 0.10], R/R 2.193, perte reelle 16.249 % (gap inclus), EV -0.0174 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.6 % x 35.63 % + P(rien) 92.1 % x 1.03 % ne couvrent pas P(stop) 7.3 % x 16.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 5.93 ATR (stop 18.401 %) — p(stop avant cible) 0.0477 [0.03 ; 0.07], R/R 1.936, perte reelle 18.401 % (gap inclus), EV -0.0254 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.6 % x 35.63 % + P(rien) 94.6 % x 0.67 % ne couvrent pas P(stop) 4.8 % x 18.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 20.681 %) — p(stop avant cible) 0.0146 [0.01 ; 0.03], R/R 1.723, perte reelle 20.681 % (gap inclus), EV 0.1462 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.68 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.158 %) — p(stop avant cible) 0.012 [0.00 ; 0.03], R/R 1.608, perte reelle 22.158 % (gap inclus), EV 0.1442 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.16 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 23.635 %) — p(stop avant cible) 0.0091 [0.00 ; 0.02], R/R 1.508, perte reelle 23.635 % (gap inclus), EV 0.1599 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.63 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 276.75, ATR14 8.1763 (2.954 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.386 ATR = 1.14 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.148 % | 276.3412 | 91.52 % | 94.53 % | 95.53 % | 96.64 % | 97.52 % | 97.95 % |
| 0.1 ATR | 0.295 % | 275.9324 | 85.49 % | 90.28 % | 92.28 % | 93.95 % | 95.6 % | 96.69 % |
| 0.15 ATR | 0.443 % | 275.5236 | 78.91 % | 85.92 % | 88.26 % | 90.36 % | 93.69 % | 95.32 % |
| 0.2 ATR | 0.591 % | 275.1147 | 71.99 % | 80.56 % | 83.89 % | 86.66 % | 91.21 % | 93.96 % |
| 0.25 ATR | 0.739 % | 274.7059 | 65.07 % | 74.97 % | 79.08 % | 83.07 % | 88.39 % | 92.02 % |
| 0.35 ATR | 1.034 % | 273.8883 | 53.57 % | 65.36 % | 71.14 % | 76.57 % | 83.77 % | 88.37 % |
| 0.5 ATR | 1.477 % | 272.6618 | 38.5 % | 52.18 % | 58.95 % | 65.92 % | 76.44 % | 82.67 % |
| 0.75 ATR | 2.216 % | 270.6178 | 20.2 % | 35.98 % | 44.41 % | 52.69 % | 66.07 % | 75.6 % |
| 1.0 ATR | 2.954 % | 268.5737 | 11.16 % | 23.69 % | 32.66 % | 42.71 % | 56.93 % | 69.21 % |
| 1.25 ATR | 3.693 % | 266.5296 | 5.8 % | 16.09 % | 23.83 % | 35.09 % | 50.96 % | 62.94 % |
| 1.5 ATR | 4.432 % | 264.4855 | 2.79 % | 10.61 % | 17.11 % | 28.7 % | 44.19 % | 57.24 % |
| 2.0 ATR | 5.909 % | 260.3974 | 0.89 % | 4.36 % | 9.17 % | 17.83 % | 31.45 % | 46.41 % |
| 2.5 ATR | 7.386 % | 256.3092 | 0.45 % | 2.23 % | 4.7 % | 10.87 % | 20.97 % | 36.49 % |
| 3.0 ATR | 8.863 % | 252.2211 | 0.0 % | 1.12 % | 2.8 % | 6.73 % | 15.45 % | 28.51 % |
| 4.0 ATR | 11.818 % | 244.0447 | 0.0 % | 0.22 % | 0.89 % | 2.58 % | 6.76 % | 14.25 % |
| 6.0 ATR | 17.726 % | 227.6921 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.79 % | 2.74 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 1.05 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.90 ATR | 2.60 ATR | 3.42 ATR |
| **10 s.** | 0.54 ATR | 1.28 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.59 ATR | 3.63 ATR | 4.59 ATR |
| **20 s.** | 0.77 ATR | 1.83 ATR | 2.07 ATR | 2.72 ATR | 3.25 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.435–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.477 %, prix 272.6624), p(touche) 38.5 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.216 %, prix 270.6172), p(touche) 35.98 % (en stress 88.89 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.74–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.216 %, prix 270.6172), p(touche) 44.41 % (en stress 97.78 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.943–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.954 %, prix 268.5748), p(touche) 42.71 % (en stress 96.67 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.47–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.432 %, prix 264.4844), p(touche) 44.19 % (en stress 98.88 %)  ✅ optimum identifie (73.9 % des re-echantillons)
- **20 seance(s)** : plage utile 2.071–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.386 %, prix 256.3092), p(touche) 36.49 % (en stress 95.45 %)  ✅ optimum identifie (87.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.058 | EV/share : $0.477 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 39 % | T3 22 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 77.7 | bear 5.0 | side 17.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 277.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.198% → cible +2.224% / stop −1.5%, p_fill 44%, n_eff≈20.1) : P(cible|rempli) **9%** · **EV/risk -0.203** (×p_fill ; si rempli -0.69% du capital)
  - **swing** (entrée dip −2.626% → cible +2.515% / stop −3.034%, p_fill 42%, n_eff≈18.4) : P(cible|rempli) **52%** · **EV/risk -0.034** (×p_fill ; si rempli -0.25% du capital)
  - **deep** (entrée dip −4.058% → cible +3.556% / stop −4.619%, p_fill 42%, n_eff≈16.1) : P(cible|rempli) **82%** · **EV/risk +0.185** (×p_fill ; si rempli +2.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→69% · +2.0%→38% · +3.0%→15% · +5.0%→2% · +8.0%→0%
- Range intraday médian 3.25% (p90 5.36%) · excursion haute méd. +1.45% / basse méd. −1.21%
- Profil de vol intra : ouverture 2.421% vs midi 0.657% vs clôture 0.781% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 45% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.064)_ ; drift intra méd. -0.298% ; recovery-V 6%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 66% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 278.1162 (VA 276.2937–280.9512 ; dernier close 276.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 41% · **stop −2.16%** sous le fill (sous le bruit) · cible +0.71% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 33% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −1.84%) · haut méd +0.84% · range méd 1.6%
- Excursion ouverture 15min (n=160) : bas méd −0.6% (p90 −2.21%) · haut méd +1.04% · range méd 1.99%
- Excursion ouverture 30min (n=160) : bas méd −0.71% (p90 −2.58%) · haut méd +1.14% · range méd 2.22%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.94%) · haut méd +1.32% · range méd 2.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 276.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 44% · séance 61% (105/159) · gap 17% · délai 2.1min · rebond 55% (60/105) (MFE +1.09%)
   - −1.0% : fill 30min 33% · séance 50% (90/159) · gap 10% · délai 5.3min · rebond 47% (49/90) (MFE +0.97%)
   - −1.5% : fill 30min 25% · séance 38% (70/159) · gap 6% · délai 10.3min · rebond 39% (35/70) (MFE +0.8%)
   - −2.0% : fill 30min 20% · séance 32% (59/159) · gap 4% · délai 15.1min · rebond 53% (33/59) (MFE +1.07%)
   - −3.0% : fill 30min 6% · séance 17% (32/159) · gap 1% · délai 46.4min · rebond 41% (13/32) (MFE +0.71%)
   - −4.0% : fill 30min 4% · séance 10% (19/159) · gap 1% · délai 43.2min · rebond 62% (11/19) (MFE +1.19%)
   - −5.0% : fill 30min 2% · séance 4% (12/159) · gap 0% · délai 47.8min · rebond 88% (10/12) (MFE +1.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −1.13%) → stop au-delà de −0.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.27% (p90 −1.0%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.41% (p90 −1.38%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=469 jambes) : jambe baissière méd −1.06% (p90 −2.57%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (41 séances) :
      · −1.0% : fill 95% (39/41) · rebond 65% (26/39)
      · −2.0% : fill 73% (31/41) · rebond 52% (18/31)
      · −3.0% : fill 40% (17/41) · rebond 27% (6/17)
      · −4.0% : fill 35% (14/41) · rebond 64% (8/14)
      · −5.0% : fill 18% (10/41) · rebond 87% (8/10)
   - **flat** (27 séances) :
      · −1.0% : fill 59% (20/27) · rebond 12% (5/20)
      · −2.0% : fill 38% (12/27) · rebond 46% (6/12)
      · −3.0% : fill 17% (7/27) · rebond 22% (2/7)
      · −4.0% : fill 6% (3/27) · rebond 42% (2/3)
      · −5.0% : fill 1% (1/27) · rebond 100% (1/1)
   - **gap-up** (91 séances) :
      · −1.0% : fill 30% (31/91) · rebond 46% (18/31)
      · −2.0% : fill 15% (16/91) · rebond 61% (9/16)
      · −3.0% : fill 8% (8/91) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/91) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/91) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 64% si les 15 1res min sont vertes (92 cas) · 30% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 83% si début vert vs 10% si rouge (base 49% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **83%** · continue >prix actuel 49% ; creux résiduel méd -0.97% (q20 -1.93%) → **SL/trailing à −1.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.87% / q75 +1.36% → **scale +0.87% / runner +1.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.34%** (au-delà de la MAE q10 -2.34%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.1% .. +2.28%] · haut q95 +2.59% · bas q05 -3.45%
   - 60min (n=160) : retour [-3.64% .. +2.56%] · haut q95 +3.19% · bas q05 -4.63%
   - 2h (n=160) : retour [-3.71% .. +2.89%] · haut q95 +3.75% · bas q05 -4.68%
   - 4h (n=160) : retour [-3.08% .. +3.35%] · haut q95 +4.14% · bas q05 -4.72%
   - 6h (n=160) : retour [-4.17% .. +3.12%] · haut q95 +4.43% · bas q05 -4.72%
   - session (n=160) : retour [-3.72% .. +3.25%] · haut q95 +4.46% · bas q05 -4.72%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 12% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 56.6  _(momentum haussier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist 0.167  _(bullish_recent)_
- **BB** : %B 0.62 · largeur 8.6%
- **ATR** : 8.18 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.203  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 62.9  _(marche en range (choppy))_
- **MA** : MA20 273.83 · MA50 264.64 · MA200 296.88  _(prix > MA20)_
- **Dist MA** : MA20 +1.1% · MA50 +4.6% · MA200 -6.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (904610 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
