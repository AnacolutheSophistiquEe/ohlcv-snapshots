# EVT

**Generated** : 2026-10-26T21:41:56.906702+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €2.80 (+0.7% vs entrée) · entrée €2.78 · stop €2.67 · T1 €2.86 · R/R 0.73  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.210 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-26 : 2.8 · ATR Wilder 0.1428 (5.1 %)_
- **Swing** : plage **2.61 → 2.47** (-6.86 % a -11.91 % sous la cloture, 0.99 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.33 (-5.79 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **2.47 → 1.88** (-11.91 % a -32.94 % sous la cloture, 4.13 ATR) — touchee 48 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 1.74 (-7.6 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.37 ATR sous le plus haut 20 s., RSI(2) 47.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Resistances reelles au-dessus : 3.1-3.14 (A, 10.56 %) ; 3.18-3.24 (B, 13.35 %) ; 3.37-3.41 (A, 20.41 %) ; 3.88-3.88 (C, 38.47 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.17 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **5.654 pt plus bas** dans le cas TYPIQUE (médiane), 19.922 au p90, **24.243 au pire**
   - perte réelle **18.001 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 8.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0386 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1201** [0.078 ; 0.1747] _(largeur 9.7 pt, n_eff 173.1)_
   - swing : **0.3428** [0.2942 ; 0.394] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.416** [0.3649 ; 0.4685] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.8 %** | CVaR **-8.97 %** | vol 3.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 6.08 % contre 3.62 % aujourd'hui, rapport 1.68)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1114** (β de hausse 0.9404, asymétrie 1.1818) vs GDAXI — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.663 sur grid_snapped (0.59 ATR, 4.96 %) — p(stop avant cible) 0.638 [0.59 ; 0.69], R/R 7.021, perte reelle 5.657 % (gap inclus), CVaR 13.385 %, EV -1.1232 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.3563 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.638, borne haute 0.687 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 13.38 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.59 ATR (stop 5.753 %) — p(stop avant cible) 0.5797 [0.53 ; 0.63], R/R 6.02, perte reelle 6.597 % (gap inclus), EV -1.265 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.580, borne haute 0.631 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.15 % > budget 12.00 %
      - ⚠ support DETECTE a 0.59 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.448 ; 0.508] sur 1233 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.2 % x 39.71 % + P(rien) 41.9 % x 5.95 % ne couvrent pas P(stop) 58.0 % x 6.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 8.383 %) — p(stop avant cible) 0.4233 [0.37 ; 0.48], R/R 4.065, perte reelle 9.768 % (gap inclus), EV -1.95 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 0.2 % x 39.71 % + P(rien) 57.5 % x 3.68 % ne couvrent pas P(stop) 42.3 % x 9.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.53 ATR (stop 16.602 %) — p(stop avant cible) 0.145 [0.11 ; 0.18], R/R 2.153, perte reelle 18.446 % (gap inclus), EV -2.4254 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.43 %) : P(cible) 0.2 % x 39.71 % + P(rien) 85.3 % x 0.21 % ne couvrent pas P(stop) 14.5 % x 18.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.397 %) — p(stop avant cible) 0.8841 [0.85 ; 0.91], R/R 25.252, perte reelle 1.573 % (gap inclus), EV -0.2615 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 25.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.884, borne haute 0.915 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 0.1 % x 39.71 % + P(rien) 11.5 % x 9.56 % ne couvrent pas P(stop) 88.4 % x 1.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+39.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 grid_snapped a 0.59 ATR (stop 4.96 %) — p(stop avant cible) 0.638 [0.59 ; 0.69], R/R 7.021, perte reelle 5.657 % (gap inclus), EV -1.1232 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.638, borne haute 0.687 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 13.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 0.1 % x 39.71 % + P(rien) 36.1 % x 6.75 % ne couvrent pas P(stop) 63.8 % x 5.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 6.985 %) — p(stop avant cible) 0.4989 [0.45 ; 0.55], R/R 4.856, perte reelle 8.179 % (gap inclus), EV -1.6619 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.499, borne haute 0.551 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 18.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 0.2 % x 39.71 % + P(rien) 49.9 % x 4.71 % ne couvrent pas P(stop) 49.9 % x 8.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 9.779 %) — p(stop avant cible) 0.3677 [0.32 ; 0.42], R/R 3.545, perte reelle 11.203 % (gap inclus), EV -2.1258 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 0.2 % x 39.71 % + P(rien) 63.1 % x 3.05 % ne couvrent pas P(stop) 36.8 % x 11.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 11.176 %) — p(stop avant cible) 0.3299 [0.28 ; 0.38], R/R 3.162, perte reelle 12.56 % (gap inclus), EV -2.4072 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.41 %) : P(cible) 0.2 % x 39.71 % + P(rien) 66.8 % x 2.50 % ne couvrent pas P(stop) 33.0 % x 12.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 12.573 %) — p(stop avant cible) 0.2691 [0.22 ; 0.32], R/R 2.819, perte reelle 14.088 % (gap inclus), EV -2.5131 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 0.2 % x 39.71 % + P(rien) 72.9 % x 1.66 % ne couvrent pas P(stop) 26.9 % x 14.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.53 ATR (stop 15.809 %) — p(stop avant cible) 0.1616 [0.13 ; 0.20], R/R 2.248, perte reelle 17.667 % (gap inclus), EV -2.4744 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 0.2 % x 39.71 % + P(rien) 83.7 % x 0.37 % ne couvrent pas P(stop) 16.2 % x 17.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 19.557 %) — p(stop avant cible) 0.1095 [0.08 ; 0.15], R/R 1.883, perte reelle 21.091 % (gap inclus), EV -2.4094 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.41 %) : P(cible) 0.2 % x 39.71 % + P(rien) 88.9 % x -0.19 % ne couvrent pas P(stop) 10.9 % x 21.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 22.351 %) — p(stop avant cible) 0.0803 [0.06 ; 0.11], R/R 1.709, perte reelle 23.241 % (gap inclus), EV -2.4157 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 0.2 % x 39.71 % + P(rien) 91.8 % x -0.67 % ne couvrent pas P(stop) 8.0 % x 23.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 25.145 %) — p(stop avant cible) 0.067 [0.04 ; 0.10], R/R 1.561, perte reelle 25.445 % (gap inclus), EV -2.514 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 0.2 % x 39.71 % + P(rien) 93.1 % x -0.94 % ne couvrent pas P(stop) 6.7 % x 25.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 27.939 %) — p(stop avant cible) 0.0499 [0.03 ; 0.08], R/R 1.41, perte reelle 28.167 % (gap inclus), EV -2.6268 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.63 %) : P(cible) 0.2 % x 39.71 % + P(rien) 94.8 % x -1.36 % ne couvrent pas P(stop) 5.0 % x 28.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 30.733 %) — p(stop avant cible) 0.0384 [0.02 ; 0.06], R/R 1.285, perte reelle 30.895 % (gap inclus), EV -2.6914 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.69 %) : P(cible) 0.2 % x 39.71 % + P(rien) 96.0 % x -1.64 % ne couvrent pas P(stop) 3.8 % x 30.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 33.527 %) — p(stop avant cible) 0.0384 [0.02 ; 0.06], R/R 1.183, perte reelle 33.58 % (gap inclus), EV -2.7945 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.79 %) : P(cible) 0.2 % x 39.71 % + P(rien) 96.0 % x -1.64 % ne couvrent pas P(stop) 3.8 % x 33.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 36.321 %) — p(stop avant cible) 0.0255 [0.01 ; 0.05], R/R 1.093, perte reelle 36.321 % (gap inclus), EV -2.8116 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.81 %) : P(cible) 0.2 % x 39.71 % + P(rien) 97.3 % x -2.01 % ne couvrent pas P(stop) 2.5 % x 36.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 39.115 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 1.015, perte reelle 39.115 % (gap inclus), EV -2.6822 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 0.2 % x 39.71 % + P(rien) 99.7 % x -2.70 % ne couvrent pas P(stop) 0.1 % x 39.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 41.909 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.948, perte reelle 41.909 % (gap inclus), EV -2.6762 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 0.2 % x 39.71 % + P(rien) 99.8 % x -2.74 % ne couvrent pas P(stop) 0.0 % x 41.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 44.703 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.888, perte reelle 44.703 % (gap inclus), EV -2.6762 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 0.2 % x 39.71 % + P(rien) 99.8 % x -2.75 % ne couvrent pas P(stop) 0.0 % x 44.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.802, ATR14 0.1566 (5.588 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 2.051 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.279 % | 2.7942 | 88.86 % | 91.61 % | 93.48 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.559 % | 2.7863 | 81.36 % | 86.67 % | 89.62 % | 92.77 % | 95.72 % | 97.19 % |
| 0.15 ATR | 0.838 % | 2.7785 | 75.35 % | 82.92 % | 86.66 % | 90.1 % | 94.03 % | 96.08 % |
| 0.2 ATR | 1.118 % | 2.7707 | 69.23 % | 79.17 % | 83.6 % | 87.52 % | 92.14 % | 94.77 % |
| 0.25 ATR | 1.397 % | 2.7629 | 63.31 % | 75.72 % | 80.34 % | 84.95 % | 90.25 % | 93.57 % |
| 0.35 ATR | 1.956 % | 2.7472 | 51.87 % | 67.52 % | 73.81 % | 80.0 % | 86.37 % | 91.56 % |
| 0.5 ATR | 2.794 % | 2.7237 | 35.6 % | 54.99 % | 62.94 % | 71.09 % | 80.6 % | 88.34 % |
| 0.75 ATR | 4.191 % | 2.6846 | 19.13 % | 37.81 % | 47.53 % | 59.6 % | 72.14 % | 82.11 % |
| 1.0 ATR | 5.588 % | 2.6454 | 10.06 % | 25.07 % | 36.07 % | 47.82 % | 62.89 % | 75.68 % |
| 1.25 ATR | 6.985 % | 2.6063 | 4.83 % | 17.37 % | 27.57 % | 39.9 % | 56.42 % | 70.65 % |
| 1.5 ATR | 8.382 % | 2.5671 | 3.06 % | 11.45 % | 19.86 % | 31.88 % | 49.25 % | 65.63 % |
| 2.0 ATR | 11.176 % | 2.4889 | 1.38 % | 5.13 % | 9.68 % | 19.8 % | 35.82 % | 53.97 % |
| 2.5 ATR | 13.97 % | 2.4106 | 0.49 % | 2.86 % | 5.93 % | 12.57 % | 28.46 % | 46.53 % |
| 3.0 ATR | 16.764 % | 2.3323 | 0.39 % | 1.68 % | 3.85 % | 8.91 % | 21.59 % | 39.6 % |
| 4.0 ATR | 22.351 % | 2.1757 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 12.14 % | 25.23 % |
| 6.0 ATR | 33.527 % | 1.8626 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.50 ATR | 1.98 ATR | 2.72 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.09 ATR | 1.47 ATR | 1.78 ATR | 1.99 ATR | 2.85 ATR | 3.82 ATR |
| **10 s.** | 0.67 ATR | 1.47 ATR | 1.66 ATR | 2.19 ATR | 2.75 ATR | 3.17 ATR | 4.61 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.27 ATR | 2.61 ATR | 3.46 ATR | 4.04 ATR | 4.91 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (61.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.191 %, prix 2.6846), p(touche) 37.81 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (72.5 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.588 %, prix 2.6454), p(touche) 36.07 % (en stress 96.08 %)  ✅ optimum identifie (72.4 % des re-echantillons)
- **5 seance(s)** : plage utile 1.089–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.985 %, prix 2.6063), p(touche) 39.9 % (en stress 94.06 %)  ✅ optimum identifie (79.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.658–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.176 %, prix 2.4888), p(touche) 35.82 % (en stress 98.02 %)  ✅ optimum identifie (73.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.61–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (16.764 %, prix 2.3323), p(touche) 39.6 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (86.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.029 | EV/share : €-0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.8 | bear 6.0 | side 17.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 57 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.821% → cible +2.818% / stop −4.001%, p_fill 78%, n_eff≈82.3) : P(cible|rempli) **24%** · **EV/risk -0.063** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −1.803% → cible +12.968% / stop −6.484%, p_fill 63%, n_eff≈71.2) : P(cible|rempli) **3%** · **EV/risk -0.176** (×p_fill ; si rempli -1.81% du capital)
  - **deep** (entrée dip −2.786% → cible +14.113% / stop −8.624%, p_fill 66%, n_eff≈72.2) : P(cible|rempli) **7%** · **EV/risk -0.259** (×p_fill ; si rempli -3.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→67% · +2.0%→44% · +3.0%→26% · +5.0%→8% · +8.0%→1%
- Range intraday médian 4.09% (p90 6.5%) · excursion haute méd. +1.72% / basse méd. −1.92%
- Profil de vol intra : ouverture 2.643% vs midi 1.227% vs clôture 1.2% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.139)_ ; drift intra méd. -0.506% ; recovery-V 28%
- **σ réalisé intraday** 3.475% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 81% / whipsaw 51%
- POC intraday (dernière séance, temps-au-prix) : 2.7892 (VA 2.7604–2.8204 ; dernier close 2.806)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 28% · rebond 80% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.91% · R/R 0.81 (high win-rate)
- Gaps overnight (n=159) : méd. 0.35% · baisse 41% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.26%) · haut méd +0.43% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −0.96% (p90 −2.47%) · haut méd +0.78% · range méd 1.98%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −2.82%) · haut méd +1.06% · range méd 2.33%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.16%) · haut méd +1.11% · range méd 2.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2.81 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 84% (129/159) · gap 21% · délai 0.3min · rebond 63% (86/129) (MFE +1.64%)
   - −1.0% : fill 30min 42% · séance 72% (112/159) · gap 10% · délai 4.8min · rebond 65% (76/112) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 56% (91/159) · gap 5% · délai 30.8min · rebond 68% (61/91) (MFE +1.46%)
   - −2.0% : fill 30min 19% · séance 47% (76/159) · gap 4% · délai 68.0min · rebond 60% (45/76) (MFE +1.59%)
   - −3.0% : fill 30min 8% · séance 28% (44/159) · gap 2% · délai 112.8min · rebond 80% (32/44) (MFE +1.91%)
   - −4.0% : fill 30min 2% · séance 12% (20/159) · gap 0% · délai 390.8min · rebond 36% (10/20) (MFE +0.51%)
   - −5.0% : fill 30min 1% · séance 6% (11/159) · gap 0% · délai 215.4min · rebond 14% (5/11) (MFE +0.65%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.43%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.02%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.0%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=832 jambes) : jambe baissière méd −1.06% (p90 −2.31%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 80% (41/49) · rebond 67% (29/41)
      · −2.0% : fill 63% (32/49) · rebond 69% (20/32)
      · −3.0% : fill 36% (19/49) · rebond 79% (13/19)
      · −4.0% : fill 15% (10/49) · rebond 15% (4/10)
      · −5.0% : fill 12% (7/49) · rebond 15% (3/7)
   - **flat** (32 séances) :
      · −1.0% : fill 75% (25/32) · rebond 70% (16/25)
      · −2.0% : fill 50% (18/32) · rebond 65% (10/18)
      · −3.0% : fill 36% (11/32) · rebond 90% (9/11)
      · −4.0% : fill 14% (4/32) · rebond 60% (2/4)
      · −5.0% : fill 4% (2/32) · rebond 23% (1/2)
   - **gap-up** (78 séances) :
      · −1.0% : fill 67% (46/78) · rebond 61% (31/46)
      · −2.0% : fill 38% (26/78) · rebond 50% (15/26)
      · −3.0% : fill 20% (14/78) · rebond 73% (10/14)
      · −4.0% : fill 9% (6/78) · rebond 36% (4/6)
      · −5.0% : fill 3% (2/78) · rebond 7% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (79 cas) · 28% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 22% si rouge (base 42% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 281min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **66%** · continue >prix actuel 46% ; creux résiduel méd -1.84% (q20 -2.76%) → **SL/trailing à −2.76%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.97% / q75 +2.56% → **scale +1.97% / runner +2.56%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **22%** (continue à baisser 66%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.22%** (au-delà de la MAE q10 -4.22%), cible rebond +1.56% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +3.32%] · haut q95 +3.93% · bas q05 -3.48%
   - 60min (n=160) : retour [-2.85% .. +3.84%] · haut q95 +4.96% · bas q05 -3.74%
   - 2h (n=160) : retour [-2.98% .. +3.29%] · haut q95 +5.01% · bas q05 -3.91%
   - 4h (n=160) : retour [-3.29% .. +3.8%] · haut q95 +5.1% · bas q05 -4.32%
   - 6h (n=160) : retour [-3.66% .. +4.62%] · haut q95 +5.27% · bas q05 -4.33%
   - session (n=160) : retour [-4.52% .. +4.02%] · haut q95 +5.67% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 3.11%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.07 · part idiosyncratique 0.93
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.0  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist 0.035  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 27.3%
- **ATR** : 0.16 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.206  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 52.9  _(transition)_
- **MA** : MA20 2.78 · MA50 2.97 · MA200 4.44  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -5.7% · MA200 -36.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (817654 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
