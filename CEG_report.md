# CEG

**Generated** : 2026-09-01T00:30:46.458773+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $274.77  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $274.77 (+1.8% vs entrée) · entrée $269.88 · stop $262.03 · T1 $276.01 · R/R 0.78  
> ↳ P(T1 av. stop) 49 % _(réel 5 s)_ · EV/risk -0.082 _(réel 5 s)_ (GBM 0.071) · ¼-Kelly 0.014 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -54 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.280 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $268.65–$271.11 (mid $269.88)
- Spot actuel : $274.77 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $262.03 (stop swing_plan-based (-4.64%))
- Targets : T1 $276.01 · R/R 0.78 | T2 $282.13 · R/R 1.56 | T3 $288.26 · R/R 2.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $262.03


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.99 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.64 %)** : le gap seul le franchit 0.864 % des séances (10 fois sur 1157).
   - exécution **1.362 pt plus bas** dans le cas TYPIQUE (médiane), 5.869 au p90, **11.184 au pire**
   - perte réelle **7.297 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 4.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.023 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.822 % | p01 -4.437 % | pire -15.824 % _(sur 1157 séances)_
- **P(stop avant cible)** _(source : daily, 1158 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4831** [0.4095 ; 0.5573] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4263** [0.3749 ; 0.4789] _(largeur 10.4 pt, n_eff 345.4)_
   - deep : **0.4326** [0.3811 ; 0.4852] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 21.1 observations effectives », dont la borne haute a 95 % vaut environ 14.2 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 21.9 observations effectives », dont la borne haute a 95 % vaut environ 13.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.2 pt), swing (40.4 pt), deep (37.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.1 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.67 % contre 2.85 % aujourd'hui, rapport 1.99)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.63 % vs -9.57 % si l'on extrapolait par √5 _(rapport 1.006 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1836** (β de hausse 1.1919, asymétrie 0.993) vs SPY — 531 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 243.3747 sur atr_grid (4.0 ATR, 11.426 %) — p(stop avant cible) 0.2355 [0.19 ; 0.28], R/R 2.316, perte reelle 15.824 % (gap inclus), CVaR 11.43 %, EV -1.241 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.285 %) — p(stop avant cible) 0.6238 [0.57 ; 0.67], R/R 5.658, perte reelle 6.477 % (gap inclus), EV -1.2044 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.624, borne haute 0.674 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.5 % x 36.65 % + P(rien) 37.2 % x 7.18 % ne couvrent pas P(stop) 62.4 % x 6.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.47 ATR (stop 5.929 %) — p(stop avant cible) 0.5333 [0.48 ; 0.59], R/R 3.928, perte reelle 9.329 % (gap inclus), EV -2.076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.533, borne haute 0.586 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 0.5 % x 36.65 % + P(rien) 46.2 % x 5.91 % ne couvrent pas P(stop) 53.3 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.41 ATR (stop 14.34 %) — p(stop avant cible) 0.1434 [0.11 ; 0.18], R/R 2.316, perte reelle 15.824 % (gap inclus), EV -0.339 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.5 % x 36.65 % + P(rien) 85.1 % x 2.04 % ne couvrent pas P(stop) 14.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.92 ATR (stop 18.657 %) — p(stop avant cible) 0.0341 [0.02 ; 0.06], R/R 1.964, perte reelle 18.657 % (gap inclus), EV 0.0355 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.66 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.714 %) — p(stop avant cible) 0.9518 [0.93 ; 0.97], R/R 20.025, perte reelle 1.83 % (gap inclus), EV -1.2133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 20.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.952, borne haute 0.971 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 0.1 % x 36.65 % + P(rien) 4.7 % x 10.25 % ne couvrent pas P(stop) 95.2 % x 1.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.428 %) — p(stop avant cible) 0.8615 [0.82 ; 0.89], R/R 12.926, perte reelle 2.835 % (gap inclus), EV -1.1384 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 12.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.862, borne haute 0.895 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.3 % x 36.65 % + P(rien) 13.6 % x 8.87 % ne couvrent pas P(stop) 86.2 % x 2.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.142 %) — p(stop avant cible) 0.7904 [0.75 ; 0.83], R/R 9.285, perte reelle 3.947 % (gap inclus), EV -1.2208 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.790, borne haute 0.831 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.4 % x 36.65 % + P(rien) 20.5 % x 8.48 % ne couvrent pas P(stop) 79.0 % x 3.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.857 %) — p(stop avant cible) 0.7061 [0.66 ; 0.75], R/R 7.228, perte reelle 5.07 % (gap inclus), EV -1.1695 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.706, borne haute 0.752 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.4 % x 36.65 % + P(rien) 29.0 % x 7.78 % ne couvrent pas P(stop) 70.6 % x 5.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.47 ATR (stop 5.049 %) — p(stop avant cible) 0.5854 [0.53 ; 0.64], R/R 4.842, perte reelle 7.568 % (gap inclus), EV -1.5461 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.55 %) : P(cible) 0.5 % x 36.65 % + P(rien) 41.0 % x 6.62 % ne couvrent pas P(stop) 58.5 % x 7.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.427 %) — p(stop avant cible) 0.488 [0.44 ; 0.54], R/R 3.928, perte reelle 9.329 % (gap inclus), EV -1.5944 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 0.5 % x 36.65 % + P(rien) 50.7 % x 5.50 % ne couvrent pas P(stop) 48.8 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.141 %) — p(stop avant cible) 0.4378 [0.39 ; 0.49], R/R 3.269, perte reelle 11.211 % (gap inclus), EV -1.9604 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.96 %) : P(cible) 0.5 % x 36.65 % + P(rien) 55.8 % x 4.98 % ne couvrent pas P(stop) 43.8 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.855 %) — p(stop avant cible) 0.3775 [0.33 ; 0.43], R/R 3.269, perte reelle 11.211 % (gap inclus), EV -1.3799 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 0.5 % x 36.65 % + P(rien) 61.8 % x 4.34 % ne couvrent pas P(stop) 37.8 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 8.57 %) — p(stop avant cible) 0.3473 [0.30 ; 0.40], R/R 2.847, perte reelle 12.871 % (gap inclus), EV -1.7063 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 0.5 % x 36.65 % + P(rien) 64.8 % x 4.00 % ne couvrent pas P(stop) 34.7 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 9.998 %) — p(stop avant cible) 0.289 [0.24 ; 0.34], R/R 2.316, perte reelle 15.824 % (gap inclus), EV -1.8951 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 0.5 % x 36.65 % + P(rien) 70.6 % x 3.55 % ne couvrent pas P(stop) 28.9 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 11.426 %) — p(stop avant cible) 0.2355 [0.19 ; 0.28], R/R 2.316, perte reelle 15.824 % (gap inclus), EV -1.241 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 0.5 % x 36.65 % + P(rien) 75.9 % x 3.02 % ne couvrent pas P(stop) 23.5 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.41 ATR (stop 13.46 %) — p(stop avant cible) 0.1808 [0.14 ; 0.22], R/R 2.316, perte reelle 15.824 % (gap inclus), EV -0.6563 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 0.5 % x 36.65 % + P(rien) 81.4 % x 2.47 % ne couvrent pas P(stop) 18.1 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 15.711 %) — p(stop avant cible) 0.0946 [0.07 ; 0.13], R/R 2.316, perte reelle 15.824 % (gap inclus), EV -0.0683 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.5 % x 36.65 % + P(rien) 90.0 % x 1.38 % ne couvrent pas P(stop) 9.5 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 5.92 ATR (stop 17.777 %) — p(stop avant cible) 0.0528 [0.03 ; 0.08], R/R 2.061, perte reelle 17.777 % (gap inclus), EV -0.0314 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.5 % x 36.65 % + P(rien) 94.2 % x 0.76 % ne couvrent pas P(stop) 5.3 % x 17.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 19.996 %) — p(stop avant cible) 0.0208 [0.01 ; 0.04], R/R 1.833, perte reelle 19.996 % (gap inclus), EV 0.0736 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.00 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.424 %) — p(stop avant cible) 0.0139 [0.01 ; 0.03], R/R 1.711, perte reelle 21.424 % (gap inclus), EV 0.1209 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.42 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.852 %) — p(stop avant cible) 0.0104 [0.00 ; 0.03], R/R 1.604, perte reelle 22.852 % (gap inclus), EV 0.1257 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.85 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 274.77, ATR14 7.8488 (2.857 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.386 ATR = 1.103 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.143 % | 274.3775 | 91.53 % | 94.53 % | 95.53 % | 96.64 % | 97.52 % | 97.95 % |
| 0.1 ATR | 0.286 % | 273.9851 | 85.51 % | 90.29 % | 92.29 % | 93.95 % | 95.61 % | 96.7 % |
| 0.15 ATR | 0.428 % | 273.5927 | 78.93 % | 85.94 % | 88.27 % | 90.37 % | 93.69 % | 95.33 % |
| 0.2 ATR | 0.571 % | 273.2002 | 72.02 % | 80.58 % | 83.91 % | 86.67 % | 91.22 % | 93.96 % |
| 0.25 ATR | 0.714 % | 272.8078 | 65.11 % | 75.0 % | 79.11 % | 82.98 % | 88.4 % | 92.03 % |
| 0.35 ATR | 1.0 % | 272.0229 | 53.62 % | 65.4 % | 71.06 % | 76.48 % | 83.78 % | 88.38 % |
| 0.5 ATR | 1.428 % | 270.8456 | 38.57 % | 52.23 % | 58.88 % | 65.85 % | 76.46 % | 82.57 % |
| 0.75 ATR | 2.142 % | 268.8834 | 20.18 % | 35.94 % | 44.36 % | 52.63 % | 66.1 % | 75.51 % |
| 1.0 ATR | 2.857 % | 266.9212 | 11.15 % | 23.66 % | 32.63 % | 42.67 % | 56.98 % | 69.13 % |
| 1.25 ATR | 3.571 % | 264.9589 | 5.8 % | 16.07 % | 23.8 % | 35.05 % | 51.01 % | 62.87 % |
| 1.5 ATR | 4.285 % | 262.9967 | 2.79 % | 10.6 % | 17.09 % | 28.67 % | 44.26 % | 57.18 % |
| 2.0 ATR | 5.713 % | 259.0723 | 0.89 % | 4.35 % | 9.16 % | 17.81 % | 31.42 % | 46.36 % |
| 2.5 ATR | 7.141 % | 255.1479 | 0.45 % | 2.23 % | 4.69 % | 10.86 % | 20.95 % | 36.45 % |
| 3.0 ATR | 8.57 % | 251.2235 | 0.0 % | 1.12 % | 2.79 % | 6.72 % | 15.43 % | 28.47 % |
| 4.0 ATR | 11.426 % | 243.3747 | 0.0 % | 0.22 % | 0.89 % | 2.58 % | 6.76 % | 14.24 % |
| 6.0 ATR | 17.139 % | 227.677 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.79 % | 2.73 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.68 ATR | 0.76 ATR | 1.05 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.95 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.90 ATR | 2.60 ATR | 3.42 ATR |
| **10 s.** | 0.54 ATR | 1.29 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.59 ATR | 3.63 ATR | 4.59 ATR |
| **20 s.** | 0.77 ATR | 1.83 ATR | 2.07 ATR | 2.72 ATR | 3.24 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.436–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.428 %, prix 270.8463), p(touche) 38.57 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.142 %, prix 268.8844), p(touche) 35.94 % (en stress 88.89 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.739–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.142 %, prix 268.8844), p(touche) 44.36 % (en stress 97.78 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.942–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.857 %, prix 266.9198), p(touche) 42.67 % (en stress 96.67 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.473–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.285 %, prix 262.9961), p(touche) 44.26 % (en stress 98.88 %)  ✅ optimum identifie (74.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.069–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.141 %, prix 255.1487), p(touche) 36.45 % (en stress 95.45 %)  ✅ optimum identifie (88.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.071 | EV/share : $0.558 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 42 % | T3 26 %
- Kelly (position) : f* 0.057 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 77.4 | bear 5.5 | side 17.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 275.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.812% → cible +2.647% / stop −1.5%, p_fill 59%, n_eff≈26.7) : P(cible|rempli) **12%** · **EV/risk -0.193** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −1.784% → cible +2.27% / stop −2.908%, p_fill 50%, n_eff≈21.1) : P(cible|rempli) **49%** · **EV/risk -0.082** (×p_fill ; si rempli -0.47% du capital)
  - **deep** (entrée dip −2.755% → cible +3.211% / stop −4.406%, p_fill 58%, n_eff≈21.9) : P(cible|rempli) **65%** · **EV/risk +0.063** (×p_fill ; si rempli +0.47% du capital)
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
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.5  _(neutre)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist -0.158  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 8.6%
- **ATR** : 7.85 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.276  _(distribution)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 61.4  _(transition)_
- **MA** : MA20 273.9 · MA50 264.66 · MA200 296.5  _(prix > MA20)_
- **Dist MA** : MA20 +0.3% · MA50 +3.8% · MA200 -7.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (792181 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
