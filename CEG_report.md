# CEG

**Generated** : 2026-09-02T00:30:24.435302+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $280.31  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $280.31 (+1.5% vs entrée) · entrée $276.11 · stop $271.97 · T1 $278.85 · R/R 0.66  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.057 _(réel 5 s)_ (GBM 0.057) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $275.57–$276.66 (mid $276.11)
- Spot actuel : $280.31 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $271.97 (stop swing_plan-based (-6.32%))
- Targets : T1 $278.85 · R/R 0.66 | T2 $281.59 · R/R 1.32 | T3 $284.33 · R/R 1.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $271.97


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.99 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.32 %)** : le gap seul le franchit 0.432 % des séances (5 fois sur 1158).
   - exécution **1.57 pt plus bas** dans le cas TYPIQUE (médiane), 7.142 au p90, **9.504 au pire**
   - perte réelle **9.329 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 6.32 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.013 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.829 % | p01 -4.437 % | pire -15.824 % _(sur 1158 séances)_
- **P(stop avant cible)** _(source : daily, 1159 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3921** [0.3216 ; 0.4661] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.41** [0.3591 ; 0.4624] _(largeur 10.3 pt, n_eff 345.4)_
   - deep : **0.4119** [0.3609 ; 0.4644] _(largeur 10.3 pt, n_eff 345.3)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 12.1 observations effectives », dont la borne haute a 95 % vaut environ 24.9 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.5 observations effectives », dont la borne haute a 95 % vaut environ 20.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.6 pt), swing (49.7 pt), deep (37.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.1 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.70 % contre 2.82 % aujourd'hui, rapport 2.02)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.62 % vs -9.57 % si l'on extrapolait par √5 _(rapport 1.006 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1843** (β de hausse 1.1919, asymétrie 0.9937) vs SPY — 532 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 254.8864 sur atr_grid (3.0 ATR, 9.07 %) — p(stop avant cible) 0.3267 [0.28 ; 0.38], R/R 2.632, perte reelle 12.871 % (gap inclus), CVaR 9.077 %, EV -1.4634 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.535 %) — p(stop avant cible) 0.6098 [0.56 ; 0.66], R/R 4.643, perte reelle 7.297 % (gap inclus), EV -1.6059 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.610, borne haute 0.660 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.61 %) : P(cible) 0.8 % x 33.88 % + P(rien) 38.2 % x 6.71 % ne couvrent pas P(stop) 61.0 % x 7.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.03 ATR (stop 8.035 %) — p(stop avant cible) 0.3631 [0.31 ; 0.41], R/R 2.632, perte reelle 12.871 % (gap inclus), EV -1.8689 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.87 %) : P(cible) 0.8 % x 33.88 % + P(rien) 62.9 % x 4.01 % ne couvrent pas P(stop) 36.3 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.14 ATR (stop 20.467 %) — p(stop avant cible) 0.0196 [0.01 ; 0.04], R/R 1.655, perte reelle 20.467 % (gap inclus), EV 0.0867 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.47 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.756 %) — p(stop avant cible) 0.9447 [0.92 ; 0.97], R/R 17.765, perte reelle 1.907 % (gap inclus), EV -1.1947 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 17.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.945, borne haute 0.965 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.2 % x 33.88 % + P(rien) 5.3 % x 10.07 % ne couvrent pas P(stop) 94.5 % x 1.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.512 %) — p(stop avant cible) 0.8575 [0.82 ; 0.89], R/R 11.445, perte reelle 2.96 % (gap inclus), EV -1.1598 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 11.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.858, borne haute 0.891 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 0.5 % x 33.88 % + P(rien) 13.7 % x 8.76 % ne couvrent pas P(stop) 85.8 % x 2.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.267 %) — p(stop avant cible) 0.7588 [0.71 ; 0.80], R/R 8.491, perte reelle 3.99 % (gap inclus), EV -0.9083 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 8.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.759, borne haute 0.802 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 0.7 % x 33.88 % + P(rien) 23.4 % x 8.06 % ne couvrent pas P(stop) 75.9 % x 3.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.023 %) — p(stop avant cible) 0.6931 [0.64 ; 0.74], R/R 6.334, perte reelle 5.349 % (gap inclus), EV -1.2111 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.693, borne haute 0.740 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 0.8 % x 33.88 % + P(rien) 29.9 % x 7.42 % ne couvrent pas P(stop) 69.3 % x 5.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.779 %) — p(stop avant cible) 0.653 [0.60 ; 0.70], R/R 5.705, perte reelle 5.938 % (gap inclus), EV -1.1647 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.653, borne haute 0.702 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 0.8 % x 33.88 % + P(rien) 33.9 % x 7.18 % ne couvrent pas P(stop) 65.3 % x 5.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.291 %) — p(stop avant cible) 0.5725 [0.52 ; 0.62], R/R 4.302, perte reelle 7.875 % (gap inclus), EV -1.6411 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.573, borne haute 0.624 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.64 %) : P(cible) 0.8 % x 33.88 % + P(rien) 41.9 % x 6.17 % ne couvrent pas P(stop) 57.2 % x 7.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.03 ATR (stop 7.038 %) — p(stop avant cible) 0.4411 [0.39 ; 0.49], R/R 3.022, perte reelle 11.211 % (gap inclus), EV -1.9878 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 0.8 % x 33.88 % + P(rien) 55.1 % x 4.86 % ne couvrent pas P(stop) 44.1 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.558 %) — p(stop avant cible) 0.3952 [0.34 ; 0.45], R/R 3.022, perte reelle 11.211 % (gap inclus), EV -1.5797 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 0.8 % x 33.88 % + P(rien) 59.7 % x 4.31 % ne couvrent pas P(stop) 39.5 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 9.07 %) — p(stop avant cible) 0.3267 [0.28 ; 0.38], R/R 2.632, perte reelle 12.871 % (gap inclus), EV -1.4634 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.46 %) : P(cible) 0.8 % x 33.88 % + P(rien) 66.5 % x 3.70 % ne couvrent pas P(stop) 32.7 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.581 %) — p(stop avant cible) 0.2669 [0.22 ; 0.32], R/R 2.141, perte reelle 15.824 % (gap inclus), EV -1.6297 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 0.8 % x 33.88 % + P(rien) 72.5 % x 3.19 % ne couvrent pas P(stop) 26.7 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.093 %) — p(stop avant cible) 0.2114 [0.17 ; 0.26], R/R 2.141, perte reelle 15.824 % (gap inclus), EV -1.0007 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 0.9 % x 33.88 % + P(rien) 78.0 % x 2.62 % ne couvrent pas P(stop) 21.1 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.605 %) — p(stop avant cible) 0.174 [0.14 ; 0.22], R/R 2.141, perte reelle 15.824 % (gap inclus), EV -0.6139 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 0.9 % x 33.88 % + P(rien) 81.7 % x 2.25 % ne couvrent pas P(stop) 17.4 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 15.116 %) — p(stop avant cible) 0.1129 [0.08 ; 0.15], R/R 2.141, perte reelle 15.824 % (gap inclus), EV -0.1873 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.9 % x 33.88 % + P(rien) 87.8 % x 1.48 % ne couvrent pas P(stop) 11.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 16.628 %) — p(stop avant cible) 0.0604 [0.04 ; 0.09], R/R 2.037, perte reelle 16.628 % (gap inclus), EV -0.002 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 0.9 % x 33.88 % + P(rien) 93.1 % x 0.76 % ne couvrent pas P(stop) 6.0 % x 16.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 6.14 ATR (stop 19.469 %) — p(stop avant cible) 0.0301 [0.02 ; 0.05], R/R 1.74, perte reelle 19.469 % (gap inclus), EV 0.0453 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.47 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.163 %) — p(stop avant cible) 0.0144 [0.01 ; 0.03], R/R 1.601, perte reelle 21.163 % (gap inclus), EV 0.1203 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.16 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.674 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.494, perte reelle 22.674 % (gap inclus), EV 0.1323 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.67 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.186 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 1.401, perte reelle 24.186 % (gap inclus), EV 0.1555 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.19 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 280.31, ATR14 8.4745 (3.023 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.386 ATR = 1.167 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.151 % | 279.8863 | 91.54 % | 94.54 % | 95.54 % | 96.64 % | 97.53 % | 97.95 % |
| 0.1 ATR | 0.302 % | 279.4625 | 85.41 % | 90.3 % | 92.3 % | 93.96 % | 95.61 % | 96.7 % |
| 0.15 ATR | 0.453 % | 279.0388 | 78.84 % | 85.95 % | 88.28 % | 90.38 % | 93.7 % | 95.34 % |
| 0.2 ATR | 0.605 % | 278.6151 | 71.94 % | 80.6 % | 83.93 % | 86.58 % | 91.23 % | 93.97 % |
| 0.25 ATR | 0.756 % | 278.1914 | 65.03 % | 75.03 % | 79.13 % | 82.89 % | 88.41 % | 92.04 % |
| 0.35 ATR | 1.058 % | 277.3439 | 53.56 % | 65.44 % | 71.09 % | 76.4 % | 83.8 % | 88.4 % |
| 0.5 ATR | 1.512 % | 276.0727 | 38.53 % | 52.29 % | 58.93 % | 65.66 % | 76.49 % | 82.59 % |
| 0.75 ATR | 2.267 % | 273.9541 | 20.16 % | 36.01 % | 44.42 % | 52.57 % | 66.14 % | 75.54 % |
| 1.0 ATR | 3.023 % | 271.8355 | 11.14 % | 23.63 % | 32.59 % | 42.62 % | 56.92 % | 69.17 % |
| 1.25 ATR | 3.779 % | 269.7169 | 5.79 % | 16.05 % | 23.77 % | 35.01 % | 50.96 % | 62.91 % |
| 1.5 ATR | 4.535 % | 267.5982 | 2.78 % | 10.59 % | 17.08 % | 28.64 % | 44.21 % | 57.22 % |
| 2.0 ATR | 6.047 % | 263.361 | 0.89 % | 4.35 % | 9.15 % | 17.79 % | 31.38 % | 46.3 % |
| 2.5 ATR | 7.558 % | 259.1237 | 0.45 % | 2.23 % | 4.69 % | 10.85 % | 20.92 % | 36.41 % |
| 3.0 ATR | 9.07 % | 254.8864 | 0.0 % | 1.11 % | 2.79 % | 6.71 % | 15.41 % | 28.44 % |
| 4.0 ATR | 12.093 % | 246.4119 | 0.0 % | 0.22 % | 0.89 % | 2.57 % | 6.75 % | 14.22 % |
| 6.0 ATR | 18.14 % | 229.4629 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.79 % | 2.73 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 1.05 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.95 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.81 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.90 ATR | 2.60 ATR | 3.41 ATR |
| **10 s.** | 0.54 ATR | 1.29 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.58 ATR | 3.62 ATR | 4.59 ATR |
| **20 s.** | 0.77 ATR | 1.83 ATR | 2.07 ATR | 2.71 ATR | 3.24 ATR | 3.59 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.435–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.512 %, prix 276.0717), p(touche) 38.53 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.612–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.267 %, prix 273.9554), p(touche) 36.01 % (en stress 88.89 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.74–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.267 %, prix 273.9554), p(touche) 44.42 % (en stress 97.78 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.94–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.023 %, prix 271.8362), p(touche) 42.62 % (en stress 96.67 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.471–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.535 %, prix 267.5979), p(touche) 44.21 % (en stress 98.88 %)  ✅ optimum identifie (73.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.066–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.558 %, prix 259.1242), p(touche) 36.41 % (en stress 95.45 %)  ✅ optimum identifie (88.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.057 | EV/share : $0.236 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 68 % | T2 37 % | T3 14 %
- Kelly (position) : f* 0.121 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.4 | bear 5.1 | side 12.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 280.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.492% → cible +0.992% / stop −1.5%, p_fill 38%, n_eff≈17.4) : P(cible|rempli) **44%** · **EV/risk -0.057** (×p_fill ; si rempli -0.22% du capital)
  - **swing** (entrée dip −3.297% → cible +2.219% / stop −3.126%, p_fill 25%, n_eff≈12.1) : P(cible|rempli) **63%** · **EV/risk +0.012** (×p_fill ; si rempli +0.15% du capital)
  - **deep** (entrée dip −5.085% → cible +3.138% / stop −4.778%, p_fill 38%, n_eff≈14.5) : P(cible|rempli) **82%** · **EV/risk +0.132** (×p_fill ; si rempli +1.67% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→70% · +2.0%→38% · +3.0%→15% · +5.0%→2% · +8.0%→0%
- Range intraday médian 3.19% (p90 5.25%) · excursion haute méd. +1.49% / basse méd. −1.16%
- Profil de vol intra : ouverture 2.337% vs midi 0.647% vs clôture 0.775% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. -0.278% ; recovery-V 6%
- **σ réalisé intraday** 2.233% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 68% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 277.9614 (VA 276.9034–279.0194 ; dernier close 274.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 41% · **stop −2.19%** sous le fill (sous le bruit) · cible +0.73% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.55% · baisse 34% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.84%) · haut méd +0.85% · range méd 1.57%
- Excursion ouverture 15min (n=160) : bas méd −0.6% (p90 −2.19%) · haut méd +1.04% · range méd 1.98%
- Excursion ouverture 30min (n=160) : bas méd −0.66% (p90 −2.56%) · haut méd +1.19% · range méd 2.18%
- Excursion ouverture 60min (n=160) : bas méd −0.83% (p90 −2.88%) · haut méd +1.34% · range méd 2.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 274.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 61% (105/159) · gap 19% · délai 1.8min · rebond 57% (61/105) (MFE +1.1%)
   - −1.0% : fill 30min 32% · séance 49% (89/159) · gap 10% · délai 5.3min · rebond 47% (48/89) (MFE +0.97%)
   - −1.5% : fill 30min 24% · séance 37% (69/159) · gap 6% · délai 10.5min · rebond 39% (34/69) (MFE +0.8%)
   - −2.0% : fill 30min 20% · séance 32% (58/159) · gap 4% · délai 15.4min · rebond 53% (32/58) (MFE +1.07%)
   - −3.0% : fill 30min 6% · séance 17% (31/159) · gap 1% · délai 46.4min · rebond 41% (13/31) (MFE +0.73%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 1% · délai 42.9min · rebond 63% (11/18) (MFE +1.2%)
   - −5.0% : fill 30min 2% · séance 4% (11/159) · gap 0% · délai 46.0min · rebond 88% (9/11) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −1.09%) → stop au-delà de −0.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.27% (p90 −1.0%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.41% (p90 −1.38%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.06% (p90 −2.55%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (41 séances) :
      · −1.0% : fill 88% (38/41) · rebond 65% (25/38)
      · −2.0% : fill 67% (30/41) · rebond 51% (17/30)
      · −3.0% : fill 36% (16/41) · rebond 27% (6/16)
      · −4.0% : fill 32% (13/41) · rebond 64% (8/13)
      · −5.0% : fill 16% (9/41) · rebond 87% (7/9)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 65% si les 15 1res min sont vertes (93 cas) · 30% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 84% si début vert vs 10% si rouge (base 50% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **84%** · continue >prix actuel 47% ; creux résiduel méd -1.2% (q20 -1.92%) → **SL/trailing à −1.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.8% / q75 +1.33% → **scale +0.8% / runner +1.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **10%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.34%** (au-delà de la MAE q10 -2.34%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.09% .. +2.28%] · haut q95 +2.58% · bas q05 -3.44%
   - 60min (n=160) : retour [-3.64% .. +2.56%] · haut q95 +3.17% · bas q05 -4.62%
   - 2h (n=160) : retour [-3.7% .. +2.89%] · haut q95 +3.72% · bas q05 -4.65%
   - 4h (n=160) : retour [-2.99% .. +3.35%] · haut q95 +4.14% · bas q05 -4.68%
   - 6h (n=160) : retour [-4.1% .. +3.11%] · haut q95 +4.42% · bas q05 -4.71%
   - session (n=160) : retour [-3.64% .. +3.24%] · haut q95 +4.45% · bas q05 -4.71%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 52.0  _(neutre)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist -0.031  _(bearish_recent)_
- **BB** : %B 0.75 · largeur 8.5%
- **ATR** : 8.47 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.225  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 64.3  _(marche en range (choppy))_
- **MA** : MA20 274.58 · MA50 264.76 · MA200 296.15  _(prix > MA20)_
- **Dist MA** : MA20 +2.1% · MA50 +5.9% · MA200 -5.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (788465 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
