# CEG

**Generated** : 2026-09-28T00:42:45.089476+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $263.27  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $263.27 (+3.5% vs entrée) · entrée $254.29 · stop $250.48 · T1 $257.97 · R/R 0.97  
> ↳ P(T1 av. stop) 55 % · EV/risk 0.176 · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.240 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $253.56–$255.03 (mid $254.29)
- Spot actuel : $263.27 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $250.48 (stop swing_plan-based (-10.23%))
- Targets : T1 $257.97 · R/R 0.97 | T2 $261.65 · R/R 1.93 | T3 $265.33 · R/R 2.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $250.48


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.96 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.23 %)** : le gap seul le franchit 0.085 % des séances (1 fois sur 1175).
   - exécution **5.594 pt plus bas** dans le cas TYPIQUE (médiane), 5.594 au p90, **5.594 au pire**
   - perte réelle **15.824 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 10.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0048 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.834 % | p01 -4.434 % | pire -15.824 % _(sur 1175 séances)_
- **P(stop avant cible)** _(source : daily, 1176 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4538** [0.3809 ; 0.5282] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4713** [0.4191 ; 0.524] _(largeur 10.5 pt, n_eff 345.4)_
   - deep : **0.4046** [0.3538 ; 0.457] _(largeur 10.3 pt, n_eff 345.4)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.27 %** | CVaR **-6.17 %** | vol 2.85 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.22 % contre 2.69 % aujourd'hui, rapport 1.94)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.04 % vs -9.58 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1802** (β de hausse 1.1944, asymétrie 0.9881) vs SPY — 542 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 231.8462 sur atr_grid (3.5 ATR, 11.936 %) — p(stop avant cible) 0.2242 [0.18 ; 0.27], R/R 2.685, perte reelle 15.824 % (gap inclus), CVaR 11.939 %, EV -1.3155 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.115 %) — p(stop avant cible) 0.5672 [0.51 ; 0.62], R/R 5.395, perte reelle 7.875 % (gap inclus), EV -1.6865 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.567, borne haute 0.619 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.69 %) : P(cible) 0.1 % x 42.49 % + P(rien) 43.1 % x 6.32 % ne couvrent pas P(stop) 56.7 % x 7.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.62 ATR (stop 7.416 %) — p(stop avant cible) 0.4131 [0.36 ; 0.47], R/R 3.79, perte reelle 11.211 % (gap inclus), EV -1.8375 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 0.1 % x 42.49 % + P(rien) 58.6 % x 4.68 % ne couvrent pas P(stop) 41.3 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.853 %) — p(stop avant cible) 0.9375 [0.91 ; 0.96], R/R 20.594, perte reelle 2.063 % (gap inclus), EV -1.2916 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 20.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.938, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 0.0 % x 42.49 % + P(rien) 6.2 % x 10.28 % ne couvrent pas P(stop) 93.8 % x 2.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.705 %) — p(stop avant cible) 0.84 [0.80 ; 0.88], R/R 12.812, perte reelle 3.316 % (gap inclus), EV -1.2702 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 12.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.840, borne haute 0.876 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 0.1 % x 42.49 % + P(rien) 15.9 % x 9.26 % ne couvrent pas P(stop) 84.0 % x 3.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.558 %) — p(stop avant cible) 0.743 [0.69 ; 0.79], R/R 9.307, perte reelle 4.565 % (gap inclus), EV -1.1895 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 9.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.743, borne haute 0.787 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.1 % x 42.49 % + P(rien) 25.6 % x 8.44 % ne couvrent pas P(stop) 74.3 % x 4.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.41 %) — p(stop avant cible) 0.6805 [0.63 ; 0.73], R/R 7.315, perte reelle 5.808 % (gap inclus), EV -1.411 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.680, borne haute 0.728 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.41 %) : P(cible) 0.1 % x 42.49 % + P(rien) 31.8 % x 7.81 % ne couvrent pas P(stop) 68.0 % x 5.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.263 %) — p(stop avant cible) 0.6128 [0.56 ; 0.66], R/R 6.56, perte reelle 6.477 % (gap inclus), EV -1.2503 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.613, borne haute 0.663 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.1 % x 42.49 % + P(rien) 38.6 % x 6.90 % ne couvrent pas P(stop) 61.3 % x 6.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.62 ATR (stop 6.537 %) — p(stop avant cible) 0.4704 [0.42 ; 0.52], R/R 3.79, perte reelle 11.211 % (gap inclus), EV -2.4068 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.41 %) : P(cible) 0.1 % x 42.49 % + P(rien) 52.8 % x 5.32 % ne couvrent pas P(stop) 47.0 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.526 %) — p(stop avant cible) 0.3538 [0.30 ; 0.41], R/R 3.301, perte reelle 12.871 % (gap inclus), EV -1.8731 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.87 %) : P(cible) 0.1 % x 42.49 % + P(rien) 64.5 % x 4.07 % ne couvrent pas P(stop) 35.4 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.378 %) — p(stop avant cible) 0.32 [0.27 ; 0.37], R/R 3.301, perte reelle 12.871 % (gap inclus), EV -1.5437 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 42.49 % + P(rien) 67.9 % x 3.71 % ne couvrent pas P(stop) 32.0 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.231 %) — p(stop avant cible) 0.2839 [0.24 ; 0.33], R/R 2.685, perte reelle 15.824 % (gap inclus), EV -1.9874 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 0.1 % x 42.49 % + P(rien) 71.5 % x 3.43 % ne couvrent pas P(stop) 28.4 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.936 %) — p(stop avant cible) 0.2242 [0.18 ; 0.27], R/R 2.685, perte reelle 15.824 % (gap inclus), EV -1.3155 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.1 % x 42.49 % + P(rien) 77.5 % x 2.81 % ne couvrent pas P(stop) 22.4 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.641 %) — p(stop avant cible) 0.1806 [0.14 ; 0.22], R/R 2.685, perte reelle 15.824 % (gap inclus), EV -0.8987 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 0.1 % x 42.49 % + P(rien) 81.8 % x 2.33 % ne couvrent pas P(stop) 18.1 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.346 %) — p(stop avant cible) 0.1089 [0.08 ; 0.14], R/R 2.685, perte reelle 15.824 % (gap inclus), EV -0.4006 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 0.1 % x 42.49 % + P(rien) 89.0 % x 1.42 % ne couvrent pas P(stop) 10.9 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 17.051 %) — p(stop avant cible) 0.0559 [0.04 ; 0.08], R/R 2.492, perte reelle 17.051 % (gap inclus), EV -0.2482 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.1 % x 42.49 % + P(rien) 94.3 % x 0.69 % ne couvrent pas P(stop) 5.6 % x 17.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 18.756 %) — p(stop avant cible) 0.0307 [0.02 ; 0.05], R/R 2.265, perte reelle 18.756 % (gap inclus), EV -0.198 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.1 % x 42.49 % + P(rien) 96.8 % x 0.33 % ne couvrent pas P(stop) 3.1 % x 18.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 20.462 %) — p(stop avant cible) 0.0177 [0.01 ; 0.04], R/R 2.076, perte reelle 20.462 % (gap inclus), EV -0.1516 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.1 % x 42.49 % + P(rien) 98.1 % x 0.16 % ne couvrent pas P(stop) 1.8 % x 20.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 22.167 %) — p(stop avant cible) 0.0108 [0.00 ; 0.03], R/R 1.917, perte reelle 22.167 % (gap inclus), EV -0.1198 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.1 % x 42.49 % + P(rien) 98.8 % x 0.07 % ne couvrent pas P(stop) 1.1 % x 22.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 23.872 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 1.78, perte reelle 23.872 % (gap inclus), EV -0.1077 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 0.1 % x 42.49 % + P(rien) 99.1 % x 0.03 % ne couvrent pas P(stop) 0.8 % x 23.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 25.577 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 1.661, perte reelle 25.577 % (gap inclus), EV -0.0929 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.1 % x 42.49 % + P(rien) 99.2 % x 0.03 % ne couvrent pas P(stop) 0.7 % x 25.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 27.282 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 1.557, perte reelle 27.282 % (gap inclus), EV -0.1027 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.1 % x 42.49 % + P(rien) 99.2 % x 0.01 % ne couvrent pas P(stop) 0.6 % x 27.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 263.27, ATR14 8.9782 (3.41 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 1.327 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 262.8211 | 91.58 % | 94.53 % | 95.51 % | 96.6 % | 97.57 % | 97.99 % |
| 0.1 ATR | 0.341 % | 262.3722 | 85.57 % | 90.37 % | 92.33 % | 93.96 % | 95.58 % | 96.76 % |
| 0.15 ATR | 0.512 % | 261.9233 | 79.13 % | 86.11 % | 88.39 % | 90.45 % | 93.71 % | 95.42 % |
| 0.2 ATR | 0.682 % | 261.4743 | 72.24 % | 80.74 % | 84.01 % | 86.61 % | 91.28 % | 94.08 % |
| 0.25 ATR | 0.853 % | 261.0254 | 65.36 % | 75.16 % | 79.19 % | 82.88 % | 88.52 % | 92.08 % |
| 0.35 ATR | 1.194 % | 260.1276 | 53.99 % | 65.75 % | 71.3 % | 76.51 % | 84.0 % | 88.5 % |
| 0.5 ATR | 1.705 % | 258.7809 | 38.8 % | 52.74 % | 59.36 % | 66.08 % | 76.71 % | 82.7 % |
| 0.75 ATR | 2.558 % | 256.5363 | 20.22 % | 36.43 % | 44.91 % | 53.13 % | 66.23 % | 75.67 % |
| 1.0 ATR | 3.41 % | 254.2918 | 11.15 % | 23.85 % | 32.97 % | 43.14 % | 57.17 % | 69.31 % |
| 1.25 ATR | 4.263 % | 252.0472 | 5.68 % | 15.97 % | 24.1 % | 35.35 % | 51.1 % | 63.17 % |
| 1.5 ATR | 5.115 % | 249.8027 | 2.73 % | 10.61 % | 17.31 % | 28.87 % | 44.37 % | 57.25 % |
| 2.0 ATR | 6.821 % | 245.3136 | 0.87 % | 4.38 % | 9.31 % | 18.0 % | 31.57 % | 45.98 % |
| 2.5 ATR | 8.526 % | 240.8245 | 0.44 % | 2.3 % | 4.82 % | 11.09 % | 21.3 % | 36.05 % |
| 3.0 ATR | 10.231 % | 236.3353 | 0.0 % | 1.09 % | 2.85 % | 7.03 % | 15.78 % | 28.12 % |
| 4.0 ATR | 13.641 % | 227.3571 | 0.0 % | 0.22 % | 0.88 % | 2.74 % | 7.17 % | 13.95 % |
| 6.0 ATR | 20.462 % | 209.4007 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.77 % | 2.68 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.00 ATR | 1.23 ATR | 1.40 ATR | 1.96 ATR | 2.48 ATR |
| **5 s.** | 0.37 ATR | 0.83 ATR | 0.95 ATR | 1.34 ATR | 1.68 ATR | 1.91 ATR | 2.63 ATR | 3.47 ATR |
| **10 s.** | 0.54 ATR | 1.29 ATR | 1.48 ATR | 1.94 ATR | 2.32 ATR | 2.62 ATR | 3.67 ATR | 4.68 ATR |
| **20 s.** | 0.78 ATR | 1.82 ATR | 2.05 ATR | 2.69 ATR | 3.22 ATR | 3.57 ATR | 4.70 ATR | 5.59 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.705 %, prix 258.7812), p(touche) 38.8 % (en stress 81.52 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.619–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.558 %, prix 256.5355), p(touche) 36.43 % (en stress 88.04 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.558 %, prix 256.5355), p(touche) 44.91 % (en stress 97.83 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.953–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.41 %, prix 254.2925), p(touche) 43.14 % (en stress 96.74 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.477–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.115 %, prix 249.8037), p(touche) 44.37 % (en stress 98.9 %)  ✅ optimum identifie (73.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.049–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.526 %, prix 240.8236), p(touche) 36.05 % (en stress 95.56 %)  ✅ optimum identifie (88.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.107 | EV/share : $0.410 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 20 % | T3 6 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 33.3 | bear 22.2 | side 44.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→41% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.29% (p90 5.36%) · excursion haute méd. +1.62% / basse méd. −1.05%
- Profil de vol intra : ouverture 2.272% vs midi 0.634% vs clôture 0.766% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 43% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.145 ; mean-reverting — autocorr -0.05)_ ; drift intra méd. 0.205% ; recovery-V 6%
- **σ réalisé intraday** 2.217% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 60% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 294.8769 (VA 290.6501–297.1824 ; dernier close 298.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 41% · **stop −2.19%** sous le fill (sous le bruit) · cible +0.73% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 37% (gap-down >1% 11% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.78%) · haut méd +0.88% · range méd 1.53%
- Excursion ouverture 15min (n=160) : bas méd −0.6% (p90 −2.1%) · haut méd +1.05% · range méd 1.91%
- Excursion ouverture 30min (n=160) : bas méd −0.65% (p90 −2.52%) · haut méd +1.26% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −0.84% (p90 −2.75%) · haut méd +1.39% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 298.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 62% (105/159) · gap 19% · délai 1.4min · rebond 57% (61/105) (MFE +1.13%)
   - −1.0% : fill 30min 32% · séance 49% (88/159) · gap 11% · délai 5.3min · rebond 47% (46/88) (MFE +0.97%)
   - −1.5% : fill 30min 24% · séance 38% (70/159) · gap 8% · délai 10.4min · rebond 45% (36/70) (MFE +0.86%)
   - −2.0% : fill 30min 20% · séance 33% (59/159) · gap 3% · délai 15.3min · rebond 53% (33/59) (MFE +1.07%)
   - −3.0% : fill 30min 6% · séance 16% (31/159) · gap 1% · délai 46.4min · rebond 41% (13/31) (MFE +0.73%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 1% · délai 42.9min · rebond 63% (11/18) (MFE +1.2%)
   - −5.0% : fill 30min 2% · séance 4% (11/159) · gap 0% · délai 46.0min · rebond 88% (9/11) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −0.98%) → stop au-delà de −0.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −0.98%) → stop au-delà de −0.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.52% (p90 −1.17%) → stop au-delà de −0.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.06% (p90 −2.57%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 82% (38/42) · rebond 68% (25/38)
      · −2.0% : fill 65% (31/42) · rebond 56% (18/31)
      · −3.0% : fill 32% (16/42) · rebond 27% (6/16)
      · −4.0% : fill 28% (13/42) · rebond 64% (8/13)
      · −5.0% : fill 14% (9/42) · rebond 87% (7/9)
   - **flat** (28 séances) :
      · −1.0% : fill 53% (20/28) · rebond 12% (5/20)
      · −2.0% : fill 34% (12/28) · rebond 46% (6/12)
      · −3.0% : fill 16% (7/28) · rebond 22% (2/7)
      · −4.0% : fill 5% (3/28) · rebond 42% (2/3)
      · −5.0% : fill 1% (1/28) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 32% (30/89) · rebond 41% (16/30)
      · −2.0% : fill 18% (16/89) · rebond 51% (9/16)
      · −3.0% : fill 8% (8/89) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/89) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/89) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 64% si les 15 1res min sont vertes (93 cas) · 36% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 85% si début vert vs 9% si rouge (base 52% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **85%** · continue >prix actuel 49% ; creux résiduel méd -0.97% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.92% / q75 +1.46% → **scale +0.92% / runner +1.46%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **9%** (continue à baisser 67%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.33%** (au-delà de la MAE q10 -2.33%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +2.26%] · haut q95 +2.56% · bas q05 -3.33%
   - 60min (n=160) : retour [-3.64% .. +2.77%] · haut q95 +3.06% · bas q05 -4.54%
   - 2h (n=160) : retour [-3.69% .. +3.01%] · haut q95 +4.2% · bas q05 -4.61%
   - 4h (n=160) : retour [-2.93% .. +3.48%] · haut q95 +4.39% · bas q05 -4.64%
   - 6h (n=160) : retour [-3.85% .. +3.99%] · haut q95 +5.02% · bas q05 -4.7%
   - session (n=160) : retour [-3.6% .. +3.78%] · haut q95 +5.18% · bas q05 -4.7%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 5.6% / strong 2.5%) · base = 13 séances trend-up (n_eff 8.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **46%**. Lecture précoce 30 min : signature présente → 19% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.09% (p75 1.89% / p90 2.34%) · ~1.0 replis/séance, durée méd 156.17 min. P(nouveau plus-haut après repli) :
   - −0.5% → **66%** (reprise méd 24.0 min, n=25)
   - −1.0% → **65%** (reprise méd 179.97 min, n=12)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.34%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.6% (q75 +4.62% / q95 +6.15%), MFE méd +4.44% / q90 +5.76%
   - Échelle scale-out : +4.44% (33%) / +5.28% (33%) / +5.76% (34%)
- **DÉSARMER** : repli > **−2.34%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.76% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 97% du temps (retour médian dernière heure +0.44%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 22.1  _(survente)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist -1.88  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 21.0%
- **ATR** : 8.98 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.241  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 31.1  _(marche directionnel)_
- **MA** : MA20 274.27 · MA50 271.76 · MA200 289.59  _(prix < MA20)_
- **Dist MA** : MA20 -4.0% · MA50 -3.1% · MA200 -9.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (876412 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
