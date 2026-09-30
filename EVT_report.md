# EVT

**Generated** : 2026-09-30T00:09:49.922473+00:00  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €2.94  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €2.94 (+4.3% vs entrée) · entrée €2.82 · stop €2.69 · T1 €2.85 · R/R 0.23  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.5% cohérent avec le bruit 5 s (EV-optimal ≈ −4.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.280 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €2.81–€2.82 (mid €2.82)
- Spot actuel : €2.94 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : €2.69 (plancher anti-bruit 5 s — stop EV-optimal −4.5% (first-passage 5 s réel) ; -4.61 % depuis l'entree)
- Targets : T1 €2.85 · R/R 0.23 | T2 €2.89 · R/R 0.54 | T3 €2.93 · R/R 0.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €2.69


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.97 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **8.641 pt plus bas** dans le cas TYPIQUE (médiane), 17.283 au p90, **19.443 au pire**
   - perte réelle **22.616 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 12.97 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0227 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0639** [0.0345 ; 0.1077] _(largeur 7.3 pt, n_eff 173.1)_
   - swing : **0.3654** [0.3159 ; 0.4171] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.3418** [0.2933 ; 0.3929] _(largeur 10.0 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.94 %** | CVaR **-9.56 %** | vol 3.56 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.17 % contre 3.71 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1189** (β de hausse 0.9429, asymétrie 1.1867) vs GDAXI — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.8167 sur atr_grid (1.0 ATR, 4.324 %) — p(stop avant cible) 0.6811 [0.63 ; 0.73], R/R 6.855, perte reelle 4.853 % (gap inclus), CVaR 10.971 %, EV -0.9357 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2974 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.484 %) — p(stop avant cible) 0.5232 [0.47 ; 0.58], R/R 4.421, perte reelle 7.525 % (gap inclus), EV -1.3572 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.523, borne haute 0.576 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 16.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 0.7 % x 33.27 % + P(rien) 47.0 % x 5.00 % ne couvrent pas P(stop) 52.3 % x 7.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 2.04 ATR (stop 10.781 %) — p(stop avant cible) 0.3196 [0.27 ; 0.37], R/R 2.674, perte reelle 12.444 % (gap inclus), EV -2.126 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 0.7 % x 33.27 % + P(rien) 67.3 % x 2.40 % ne couvrent pas P(stop) 32.0 % x 12.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.081 %) — p(stop avant cible) 0.9073 [0.87 ; 0.93], R/R 26.358, perte reelle 1.262 % (gap inclus), EV -0.1918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 26.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.907, borne haute 0.934 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.1 % x 33.27 % + P(rien) 9.1 % x 9.91 % ne couvrent pas P(stop) 90.7 % x 1.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.162 %) — p(stop avant cible) 0.8388 [0.80 ; 0.87], R/R 12.957, perte reelle 2.568 % (gap inclus), EV -0.6939 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.839, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 0.2 % x 33.27 % + P(rien) 15.9 % x 8.72 % ne couvrent pas P(stop) 83.9 % x 2.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 3.243 %) — p(stop avant cible) 0.7392 [0.69 ; 0.78], R/R 9.058, perte reelle 3.673 % (gap inclus), EV -0.6163 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 9.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.739, borne haute 0.783 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 0.3 % x 33.27 % + P(rien) 25.8 % x 7.76 % ne couvrent pas P(stop) 73.9 % x 3.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 4.324 %) — p(stop avant cible) 0.6811 [0.63 ; 0.73], R/R 6.855, perte reelle 4.853 % (gap inclus), EV -0.9357 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.4 % x 33.27 % + P(rien) 31.5 % x 7.09 % ne couvrent pas P(stop) 68.1 % x 4.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 5.404 %) — p(stop avant cible) 0.5909 [0.54 ; 0.64], R/R 5.378, perte reelle 6.187 % (gap inclus), EV -0.9988 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.591, borne haute 0.642 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 0.6 % x 33.27 % + P(rien) 40.3 % x 6.10 % ne couvrent pas P(stop) 59.1 % x 6.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 7.566 %) — p(stop avant cible) 0.4426 [0.39 ; 0.50], R/R 3.631, perte reelle 9.162 % (gap inclus), EV -1.6828 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 0.7 % x 33.27 % + P(rien) 55.0 % x 3.89 % ne couvrent pas P(stop) 44.3 % x 9.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.04 ATR (stop 10.112 %) — p(stop avant cible) 0.3437 [0.30 ; 0.39], R/R 2.833, perte reelle 11.746 % (gap inclus), EV -2.0373 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 0.7 % x 33.27 % + P(rien) 64.9 % x 2.72 % ne couvrent pas P(stop) 34.4 % x 11.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 11.89 %) — p(stop avant cible) 0.2696 [0.22 ; 0.32], R/R 2.437, perte reelle 13.655 % (gap inclus), EV -2.1891 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.19 %) : P(cible) 0.7 % x 33.27 % + P(rien) 72.3 % x 1.74 % ne couvrent pas P(stop) 27.0 % x 13.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 12.971 %) — p(stop avant cible) 0.2285 [0.19 ; 0.27], R/R 2.242, perte reelle 14.843 % (gap inclus), EV -2.2478 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 0.7 % x 33.27 % + P(rien) 76.4 % x 1.19 % ne couvrent pas P(stop) 22.9 % x 14.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 15.132 %) — p(stop avant cible) 0.1508 [0.12 ; 0.19], R/R 1.899, perte reelle 17.52 % (gap inclus), EV -2.2246 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 0.7 % x 33.27 % + P(rien) 84.2 % x 0.22 % ne couvrent pas P(stop) 15.1 % x 17.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 17.294 %) — p(stop avant cible) 0.1154 [0.09 ; 0.15], R/R 1.69, perte reelle 19.686 % (gap inclus), EV -2.1661 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.17 %) : P(cible) 0.7 % x 33.27 % + P(rien) 87.8 % x -0.14 % ne couvrent pas P(stop) 11.5 % x 19.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 19.456 %) — p(stop avant cible) 0.0983 [0.07 ; 0.13], R/R 1.556, perte reelle 21.388 % (gap inclus), EV -2.1968 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 0.7 % x 33.27 % + P(rien) 89.5 % x -0.37 % ne couvrent pas P(stop) 9.8 % x 21.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 21.618 %) — p(stop avant cible) 0.0921 [0.07 ; 0.13], R/R 1.463, perte reelle 22.737 % (gap inclus), EV -2.2719 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.27 %) : P(cible) 0.7 % x 33.27 % + P(rien) 90.1 % x -0.46 % ne couvrent pas P(stop) 9.2 % x 22.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 23.78 %) — p(stop avant cible) 0.084 [0.06 ; 0.12], R/R 1.363, perte reelle 24.408 % (gap inclus), EV -2.3746 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.37 %) : P(cible) 0.7 % x 33.27 % + P(rien) 90.9 % x -0.61 % ne couvrent pas P(stop) 8.4 % x 24.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 25.941 %) — p(stop avant cible) 0.0699 [0.05 ; 0.10], R/R 1.267, perte reelle 26.25 % (gap inclus), EV -2.4512 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 0.7 % x 33.27 % + P(rien) 92.3 % x -0.92 % ne couvrent pas P(stop) 7.0 % x 26.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 28.103 %) — p(stop avant cible) 0.0541 [0.03 ; 0.08], R/R 1.174, perte reelle 28.332 % (gap inclus), EV -2.5412 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.54 %) : P(cible) 0.7 % x 33.27 % + P(rien) 93.9 % x -1.32 % ne couvrent pas P(stop) 5.4 % x 28.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 30.265 %) — p(stop avant cible) 0.0429 [0.03 ; 0.07], R/R 1.093, perte reelle 30.45 % (gap inclus), EV -2.5937 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.59 %) : P(cible) 0.7 % x 33.27 % + P(rien) 95.0 % x -1.60 % ne couvrent pas P(stop) 4.3 % x 30.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 32.427 %) — p(stop avant cible) 0.0429 [0.03 ; 0.07], R/R 1.023, perte reelle 32.52 % (gap inclus), EV -2.6825 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 0.7 % x 33.27 % + P(rien) 95.0 % x -1.60 % ne couvrent pas P(stop) 4.3 % x 32.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 34.589 %) — p(stop avant cible) 0.0426 [0.03 ; 0.07], R/R 0.961, perte reelle 34.606 % (gap inclus), EV -2.7679 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.77 %) : P(cible) 0.7 % x 33.27 % + P(rien) 95.0 % x -1.61 % ne couvrent pas P(stop) 4.3 % x 34.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.944, ATR14 0.1273 (4.324 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.587 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.216 % | 2.9376 | 88.95 % | 91.91 % | 93.68 % | 95.64 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.432 % | 2.9313 | 81.36 % | 86.97 % | 89.72 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.649 % | 2.9249 | 75.15 % | 83.12 % | 86.66 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.865 % | 2.9185 | 68.84 % | 79.17 % | 83.4 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.081 % | 2.9122 | 63.12 % | 75.91 % | 80.34 % | 84.85 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.513 % | 2.8995 | 51.87 % | 67.82 % | 73.91 % | 80.0 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.162 % | 2.8804 | 35.6 % | 55.18 % | 62.94 % | 70.89 % | 80.1 % | 88.24 % |
| 0.75 ATR | 3.243 % | 2.8485 | 19.13 % | 37.91 % | 47.73 % | 59.8 % | 71.94 % | 81.91 % |
| 1.0 ATR | 4.324 % | 2.8167 | 10.06 % | 24.88 % | 35.97 % | 47.72 % | 62.49 % | 75.28 % |
| 1.25 ATR | 5.404 % | 2.7849 | 4.83 % | 17.28 % | 27.47 % | 39.7 % | 55.82 % | 70.05 % |
| 1.5 ATR | 6.485 % | 2.7531 | 2.96 % | 11.25 % | 19.76 % | 31.68 % | 48.76 % | 64.92 % |
| 2.0 ATR | 8.647 % | 2.6894 | 1.28 % | 4.94 % | 9.49 % | 19.5 % | 35.32 % | 53.07 % |
| 2.5 ATR | 10.809 % | 2.6258 | 0.49 % | 2.67 % | 5.63 % | 12.28 % | 27.96 % | 45.33 % |
| 3.0 ATR | 12.971 % | 2.5621 | 0.39 % | 1.68 % | 3.66 % | 8.61 % | 21.0 % | 38.39 % |
| 4.0 ATR | 17.294 % | 2.4349 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.74 % | 24.62 % |
| 6.0 ATR | 25.941 % | 2.1803 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.00 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.49 ATR | 1.98 ATR | 2.66 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.46 ATR | 1.77 ATR | 1.98 ATR | 2.81 ATR | 3.81 ATR |
| **10 s.** | 0.66 ATR | 1.46 ATR | 1.64 ATR | 2.16 ATR | 2.71 ATR | 3.11 ATR | 4.53 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.20 ATR | 2.52 ATR | 3.39 ATR | 3.97 ATR | 4.84 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.647–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.243 %, prix 2.8485), p(touche) 37.91 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (63.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.808–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.324 %, prix 2.8167), p(touche) 35.97 % (en stress 96.08 %)  ✅ optimum identifie (65.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.085–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.404 %, prix 2.7849), p(touche) 39.7 % (en stress 95.05 %)  ✅ optimum identifie (76.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.64–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.647 %, prix 2.6894), p(touche) 35.32 % (en stress 97.03 %)  ✅ optimum identifie (76.1 % des re-echantillons)
- **20 seance(s)** : plage utile 2.524–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (12.971 %, prix 2.5621), p(touche) 38.39 % (en stress 98.0 %)  ✅ optimum identifie (85.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : €-0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 30 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 68.0 | bear 5.0 | side 27.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=11))
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→83% · +1.0%→68% · +2.0%→42% · +3.0%→23% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.22% (p90 7.19%) · excursion haute méd. +1.72% / basse méd. −2.03%
- Profil de vol intra : ouverture 2.705% vs midi 1.282% vs clôture 1.242% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 59% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.092 ; mean-reverting — autocorr -0.183)_ ; drift intra méd. -0.646% ; recovery-V 22%
- **σ réalisé intraday** 2.904% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 75% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 3.2156 (VA 3.191–3.2341 ; dernier close 3.203)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 22% · rebond 69% · **stop −4.42%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 42% (gap-down >1% 8% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.17%) · haut méd +0.37% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.61%) · haut méd +0.55% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.77%) · haut méd +0.71% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.95%) · haut méd +0.88% · range méd 2.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.212 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 79% (130/159) · gap 22% · délai 0.4min · rebond 66% (88/130) (MFE +1.42%)
   - −1.0% : fill 30min 39% · séance 67% (111/159) · gap 8% · délai 6.9min · rebond 64% (73/111) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 55% (93/159) · gap 4% · délai 27.6min · rebond 62% (58/93) (MFE +1.26%)
   - −2.0% : fill 30min 19% · séance 44% (77/159) · gap 4% · délai 51.8min · rebond 51% (42/77) (MFE +1.14%)
   - −3.0% : fill 30min 10% · séance 22% (46/159) · gap 3% · délai 87.9min · rebond 69% (32/46) (MFE +1.52%)
   - −4.0% : fill 30min 4% · séance 10% (24/159) · gap 1% · délai 41.4min · rebond 36% (13/24) (MFE +0.65%)
   - −5.0% : fill 30min 3% · séance 6% (14/159) · gap 1% · délai 35.5min · rebond 34% (8/14) (MFE +0.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −2.17%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.82%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.85%) → stop au-delà de −1.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=805 jambes) : jambe baissière méd −1.07% (p90 −2.28%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 82% (46/54) · rebond 63% (30/46)
      · −2.0% : fill 61% (35/54) · rebond 44% (18/35)
      · −3.0% : fill 34% (23/54) · rebond 61% (15/23)
      · −4.0% : fill 19% (16/54) · rebond 36% (9/16)
      · −5.0% : fill 14% (11/54) · rebond 35% (6/11)
   - **flat** (37 séances) :
      · −1.0% : fill 86% (30/37) · rebond 53% (18/30)
      · −2.0% : fill 64% (22/37) · rebond 49% (10/22)
      · −3.0% : fill 39% (14/37) · rebond 82% (11/14)
      · −4.0% : fill 12% (4/37) · rebond 14% (1/4)
      · −5.0% : fill 8% (2/37) · rebond 23% (1/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 47% (35/68) · rebond 74% (25/35)
      · −2.0% : fill 22% (20/68) · rebond 68% (14/20)
      · −3.0% : fill 6% (9/68) · rebond 55% (6/9)
      · −4.0% : fill 3% (4/68) · rebond 89% (3/4)
      · −5.0% : fill 0% (1/68) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (74 cas) · 35% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 62% si début vert vs 32% si rouge (base 45% · écart 30 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **62%** · continue >prix actuel 35% ; creux résiduel méd -1.77% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.37% / q75 +2.42% → **scale +1.37% / runner +2.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **32%** (continue à baisser 56%) → **RÉDUIRE ~68%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.18%** (au-delà de la MAE q10 -4.18%), cible rebond +1.55% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +2.09%] · haut q95 +2.96% · bas q05 -3.92%
   - 60min (n=160) : retour [-3.01% .. +2.45%] · haut q95 +3.1% · bas q05 -3.97%
   - 2h (n=160) : retour [-3.47% .. +2.37%] · haut q95 +3.73% · bas q05 -4.2%
   - 4h (n=160) : retour [-3.35% .. +3.63%] · haut q95 +4.29% · bas q05 -4.28%
   - 6h (n=160) : retour [-3.31% .. +3.81%] · haut q95 +5.24% · bas q05 -5.04%
   - session (n=160) : retour [-4.12% .. +4.05%] · haut q95 +5.68% · bas q05 -5.56%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.2 · part idiosyncratique 0.8
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.1  _(momentum baissier)_
- **ADX** : 33.4  _(tendance etablie)_
- **MACD** : hist 0.022  _(bullish_recent)_
- **BB** : %B 0.47 · largeur 24.8%
- **ATR** : 0.13 (9.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.276  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 52.5  _(transition)_
- **MA** : MA20 2.97 · MA50 3.25 · MA200 4.72  _(prix < MA20)_
- **Dist MA** : MA20 -0.8% · MA50 -9.3% · MA200 -37.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (853139 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
