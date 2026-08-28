# CEG

**Generated** : 2026-08-28T00:31:27.834323+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $282.41  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $282.41 (+1.5% vs entrée) · entrée $278.10 · stop $273.93 · T1 $281.13 · R/R 0.73  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk -0.101 _(réel 5 s)_ (GBM -0.019) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

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

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $277.50–$278.71 (mid $278.10)
- Spot actuel : $282.41 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $273.93 (stop swing_plan-based (-6.22%))
- Targets : T1 $281.13 · R/R 0.73 | T2 $284.15 · R/R 1.45 | T3 $287.18 · R/R 2.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $273.93


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.99 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.22 %)** : le gap seul le franchit 0.433 % des séances (5 fois sur 1155).
   - exécution **1.67 pt plus bas** dans le cas TYPIQUE (médiane), 7.242 au p90, **9.604 au pire**
   - perte réelle **9.329 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 6.22 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0135 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.822 % | p01 -4.437 % | pire -15.824 % _(sur 1155 séances)_
- **P(stop avant cible)** _(source : daily, 1156 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3978** [0.3271 ; 0.4719] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4333** [0.3818 ; 0.4859] _(largeur 10.4 pt, n_eff 345.4)_
   - deep : **0.4378** [0.3862 ; 0.4905] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.9 observations effectives », dont la borne haute a 95 % vaut environ 25.3 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 15.2 observations effectives », dont la borne haute a 95 % vaut environ 19.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.1 pt), swing (51.3 pt), deep (42.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.11 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.66 % contre 2.85 % aujourd'hui, rapport 1.98)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.63 % vs -9.58 % si l'on extrapolait par √5 _(rapport 1.005 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1874** (β de hausse 1.1919, asymétrie 0.9962) vs SPY — 529 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 250.1049 sur atr_grid (4.0 ATR, 11.439 %) — p(stop avant cible) 0.2383 [0.20 ; 0.29], R/R 2.081, perte reelle 15.824 % (gap inclus), CVaR 11.443 %, EV -1.24 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.29 %) — p(stop avant cible) 0.6194 [0.57 ; 0.67], R/R 5.083, perte reelle 6.477 % (gap inclus), EV -1.1379 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.619, borne haute 0.669 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.9 % x 32.92 % + P(rien) 37.1 % x 6.91 % ne couvrent pas P(stop) 61.9 % x 6.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.38 ATR (stop 8.631 %) — p(stop avant cible) 0.3513 [0.30 ; 0.40], R/R 2.558, perte reelle 12.871 % (gap inclus), EV -1.7067 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 0.9 % x 32.92 % + P(rien) 63.9 % x 3.92 % ne couvrent pas P(stop) 35.1 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.7 ATR (stop 20.998 %) — p(stop avant cible) 0.0147 [0.01 ; 0.03], R/R 1.568, perte reelle 20.998 % (gap inclus), EV 0.1357 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.00 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.715 %) — p(stop avant cible) 0.9513 [0.92 ; 0.97], R/R 17.884, perte reelle 1.841 % (gap inclus), EV -1.208 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 17.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.951, borne haute 0.970 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 0.3 % x 32.92 % + P(rien) 4.6 % x 9.68 % ne couvrent pas P(stop) 95.1 % x 1.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.43 %) — p(stop avant cible) 0.8599 [0.82 ; 0.89], R/R 11.614, perte reelle 2.835 % (gap inclus), EV -1.1114 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 11.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.860, borne haute 0.893 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 0.6 % x 32.92 % + P(rien) 13.4 % x 8.41 % ne couvrent pas P(stop) 86.0 % x 2.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.145 %) — p(stop avant cible) 0.7879 [0.74 ; 0.83], R/R 8.342, perte reelle 3.947 % (gap inclus), EV -1.1879 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 8.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.788, borne haute 0.829 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.8 % x 32.92 % + P(rien) 20.4 % x 8.13 % ne couvrent pas P(stop) 78.8 % x 3.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.86 %) — p(stop avant cible) 0.7027 [0.65 ; 0.75], R/R 6.494, perte reelle 5.07 % (gap inclus), EV -1.1177 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.703, borne haute 0.749 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 0.9 % x 32.92 % + P(rien) 28.8 % x 7.44 % ne couvrent pas P(stop) 70.3 % x 5.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.575 %) — p(stop avant cible) 0.6605 [0.61 ; 0.71], R/R 5.545, perte reelle 5.938 % (gap inclus), EV -1.2305 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.660, borne haute 0.709 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 0.9 % x 32.92 % + P(rien) 33.0 % x 7.22 % ne couvrent pas P(stop) 66.0 % x 5.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.005 %) — p(stop avant cible) 0.5822 [0.53 ; 0.63], R/R 4.351, perte reelle 7.568 % (gap inclus), EV -1.4914 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 0.9 % x 32.92 % + P(rien) 40.8 % x 6.38 % ne couvrent pas P(stop) 58.2 % x 7.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.72 %) — p(stop avant cible) 0.5445 [0.49 ; 0.60], R/R 3.529, perte reelle 9.329 % (gap inclus), EV -2.137 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.544, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 0.9 % x 32.92 % + P(rien) 44.6 % x 5.90 % ne couvrent pas P(stop) 54.4 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.38 ATR (stop 7.658 %) — p(stop avant cible) 0.3934 [0.34 ; 0.45], R/R 2.937, perte reelle 11.211 % (gap inclus), EV -1.5036 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 0.9 % x 32.92 % + P(rien) 59.7 % x 4.35 % ne couvrent pas P(stop) 39.3 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.009 %) — p(stop avant cible) 0.2923 [0.25 ; 0.34], R/R 2.081, perte reelle 15.824 % (gap inclus), EV -1.8973 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 0.9 % x 32.92 % + P(rien) 69.8 % x 3.46 % ne couvrent pas P(stop) 29.2 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 11.439 %) — p(stop avant cible) 0.2383 [0.20 ; 0.29], R/R 2.081, perte reelle 15.824 % (gap inclus), EV -1.24 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 1.0 % x 32.92 % + P(rien) 75.2 % x 2.93 % ne couvrent pas P(stop) 23.8 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 12.869 %) — p(stop avant cible) 0.1888 [0.15 ; 0.23], R/R 2.081, perte reelle 15.824 % (gap inclus), EV -0.7193 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 1.0 % x 32.92 % + P(rien) 80.1 % x 2.42 % ne couvrent pas P(stop) 18.9 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 14.299 %) — p(stop avant cible) 0.1498 [0.12 ; 0.19], R/R 2.081, perte reelle 15.824 % (gap inclus), EV -0.3847 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 1.0 % x 32.92 % + P(rien) 84.0 % x 1.97 % ne couvrent pas P(stop) 15.0 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 15.729 %) — p(stop avant cible) 0.0957 [0.07 ; 0.13], R/R 2.081, perte reelle 15.824 % (gap inclus), EV -0.0527 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 1.0 % x 32.92 % + P(rien) 89.4 % x 1.27 % ne couvrent pas P(stop) 9.6 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 17.159 %) — p(stop avant cible) 0.0564 [0.04 ; 0.08], R/R 1.919, perte reelle 17.159 % (gap inclus), EV 0.0078 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.16 % > budget 12.00 %
   - 🟢 grid_snapped a 6.7 ATR (stop 20.025 %) — p(stop avant cible) 0.021 [0.01 ; 0.04], R/R 1.644, perte reelle 20.025 % (gap inclus), EV 0.0913 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.03 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.448 %) — p(stop avant cible) 0.0127 [0.00 ; 0.03], R/R 1.535, perte reelle 21.448 % (gap inclus), EV 0.1447 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.45 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.878 %) — p(stop avant cible) 0.0105 [0.00 ; 0.03], R/R 1.439, perte reelle 22.878 % (gap inclus), EV 0.144 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.88 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 282.41, ATR14 8.0763 (2.86 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.386 ATR = 1.104 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.143 % | 282.0062 | 91.51 % | 94.63 % | 95.52 % | 96.63 % | 97.52 % | 97.95 % |
| 0.1 ATR | 0.286 % | 281.6024 | 85.47 % | 90.38 % | 92.27 % | 93.94 % | 95.6 % | 96.69 % |
| 0.15 ATR | 0.429 % | 281.1986 | 78.99 % | 86.02 % | 88.24 % | 90.35 % | 93.68 % | 95.32 % |
| 0.2 ATR | 0.572 % | 280.7947 | 72.07 % | 80.65 % | 83.99 % | 86.64 % | 91.2 % | 93.95 % |
| 0.25 ATR | 0.715 % | 280.3909 | 65.14 % | 75.06 % | 79.17 % | 83.05 % | 88.37 % | 92.01 % |
| 0.35 ATR | 1.001 % | 279.5833 | 53.63 % | 65.44 % | 71.22 % | 76.54 % | 83.75 % | 88.36 % |
| 0.5 ATR | 1.43 % | 278.3719 | 38.55 % | 52.24 % | 59.01 % | 65.77 % | 76.41 % | 82.65 % |
| 0.75 ATR | 2.145 % | 276.3528 | 20.22 % | 36.02 % | 44.46 % | 52.75 % | 66.03 % | 75.68 % |
| 1.0 ATR | 2.86 % | 274.3337 | 11.17 % | 23.71 % | 32.7 % | 42.76 % | 56.88 % | 69.29 % |
| 1.25 ATR | 3.575 % | 272.3146 | 5.81 % | 16.11 % | 23.85 % | 35.13 % | 50.9 % | 63.01 % |
| 1.5 ATR | 4.29 % | 270.2956 | 2.79 % | 10.63 % | 17.13 % | 28.73 % | 44.13 % | 57.31 % |
| 2.0 ATR | 5.72 % | 266.2574 | 0.89 % | 4.36 % | 9.18 % | 17.85 % | 31.49 % | 46.46 % |
| 2.5 ATR | 7.149 % | 262.2193 | 0.45 % | 2.24 % | 4.7 % | 10.89 % | 20.99 % | 36.53 % |
| 3.0 ATR | 8.579 % | 258.1812 | 0.0 % | 1.12 % | 2.8 % | 6.73 % | 15.46 % | 28.54 % |
| 4.0 ATR | 11.439 % | 250.1049 | 0.0 % | 0.22 % | 0.9 % | 2.58 % | 6.77 % | 14.27 % |
| 6.0 ATR | 17.159 % | 233.9523 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.79 % | 2.74 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.90 ATR | 2.61 ATR | 3.42 ATR |
| **10 s.** | 0.53 ATR | 1.28 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.59 ATR | 3.63 ATR | 4.59 ATR |
| **20 s.** | 0.78 ATR | 1.84 ATR | 2.07 ATR | 2.72 ATR | 3.25 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.436–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.43 %, prix 278.3715), p(touche) 38.55 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.612–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.145 %, prix 276.3523), p(touche) 36.02 % (en stress 88.89 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.741–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.145 %, prix 276.3523), p(touche) 44.46 % (en stress 97.78 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.944–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.86 %, prix 274.3331), p(touche) 42.76 % (en stress 96.67 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.468–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.29 %, prix 270.2946), p(touche) 44.13 % (en stress 98.88 %)  ✅ optimum identifie (73.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.074–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.149 %, prix 262.2205), p(touche) 36.53 % (en stress 95.45 %)  ✅ optimum identifie (87.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.019 | EV/share : $-0.078 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 32 % | T3 10 %
- Kelly (position) : f* 0.058 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.4 | bear 6.5 | side 9.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 282.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.523% → cible +1.088% / stop −1.5%, p_fill 46%, n_eff≈18.2) : P(cible|rempli) **39%** · **EV/risk -0.101** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −3.36% → cible +2.434% / stop −2.959%, p_fill 29%, n_eff≈11.9) : P(cible|rempli) **56%** · **EV/risk -0.007** (×p_fill ; si rempli -0.07% du capital)
  - **deep** (entrée dip −5.19% → cible +3.442% / stop −4.524%, p_fill 34%, n_eff≈15.2) : P(cible|rempli) **73%** · **EV/risk +0.088** (×p_fill ; si rempli +1.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→68% · +2.0%→38% · +3.0%→16% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.36% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.41%
- Profil de vol intra : ouverture 2.487% vs midi 0.665% vs clôture 0.785% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. -0.434% ; recovery-V 7%
- **σ réalisé intraday** 2.331% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 275.8521 (VA 273.1364–276.4911 ; dernier close 272.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 41% · **stop −2.26%** sous le fill (sous le bruit) · cible +0.7% · R/R 0.31 (high win-rate)
- Gaps overnight (n=159) : méd. 0.64% · baisse 31% (gap-down >1% 11% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.86%) · haut méd +0.86% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −0.66% (p90 −2.25%) · haut méd +1.02% · range méd 2.01%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.8%) · haut méd +1.1% · range méd 2.25%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −3.05%) · haut méd +1.3% · range méd 2.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 272.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 47% · séance 63% (107/159) · gap 19% · délai 1.4min · rebond 56% (61/107) (MFE +1.09%)
   - −1.0% : fill 30min 34% · séance 51% (91/159) · gap 11% · délai 3.7min · rebond 47% (49/91) (MFE +0.9%)
   - −1.5% : fill 30min 27% · séance 39% (72/159) · gap 7% · délai 8.1min · rebond 42% (37/72) (MFE +0.82%)
   - −2.0% : fill 30min 22% · séance 34% (59/159) · gap 4% · délai 12.8min · rebond 56% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 7% · séance 19% (33/159) · gap 2% · délai 46.4min · rebond 41% (13/33) (MFE +0.7%)
   - −4.0% : fill 30min 4% · séance 10% (20/159) · gap 1% · délai 42.9min · rebond 61% (11/20) (MFE +1.17%)
   - −5.0% : fill 30min 2% · séance 5% (13/159) · gap 0% · délai 46.1min · rebond 86% (10/13) (MFE +1.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.16%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.38%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=469 jambes) : jambe baissière méd −1.09% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 94% (40/42) · rebond 61% (25/40)
      · −2.0% : fill 79% (32/42) · rebond 51% (18/32)
      · −3.0% : fill 43% (18/42) · rebond 26% (6/18)
      · −4.0% : fill 38% (15/42) · rebond 63% (8/15)
      · −5.0% : fill 20% (11/42) · rebond 85% (8/11)
   - **flat** (24 séances) :
      · −1.0% : fill 70% (19/24) · rebond 14% (5/19)
      · −2.0% : fill 40% (11/24) · rebond 63% (6/11)
      · −3.0% : fill 25% (7/24) · rebond 22% (2/7)
      · −4.0% : fill 8% (3/24) · rebond 42% (2/3)
      · −5.0% : fill 2% (1/24) · rebond 100% (1/1)
   - **gap-up** (93 séances) :
      · −1.0% : fill 31% (32/93) · rebond 47% (19/32)
      · −2.0% : fill 16% (16/93) · rebond 61% (9/16)
      · −3.0% : fill 8% (8/93) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/93) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/93) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 63% si les 15 1res min sont vertes (93 cas) · 24% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 46% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **82%** · continue >prix actuel 45% ; creux résiduel méd -1.01% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.82% / q75 +1.41% → **scale +0.82% / runner +1.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **8%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.11% .. +2.29%] · haut q95 +2.63% · bas q05 -3.47%
   - 60min (n=160) : retour [-3.68% .. +2.57%] · haut q95 +3.28% · bas q05 -4.68%
   - 2h (n=160) : retour [-3.72% .. +2.9%] · haut q95 +3.97% · bas q05 -4.78%
   - 4h (n=160) : retour [-3.56% .. +3.35%] · haut q95 +4.16% · bas q05 -4.83%
   - 6h (n=160) : retour [-4.25% .. +3.15%] · haut q95 +4.47% · bas q05 -4.87%
   - session (n=160) : retour [-3.99% .. +3.29%] · haut q95 +4.5% · bas q05 -4.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 64.0  _(momentum haussier)_
- **ADX** : 18.0  _(pas de tendance nette)_
- **MACD** : hist 0.418  _(bullish_recent)_
- **BB** : %B 0.86 · largeur 9.4%
- **ATR** : 8.08 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.196  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 62.5  _(marche en range (choppy))_
- **MA** : MA20 273.11 · MA50 264.44 · MA200 297.29  _(prix > MA20)_
- **Dist MA** : MA20 +3.4% · MA50 +6.8% · MA200 -5.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (850681 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
