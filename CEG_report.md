# CEG

**Generated** : 2026-09-14T00:42:40.261330+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $284.75  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $284.75 (+4.2% vs entrée) · entrée $273.22 · stop $263.96 · T1 $280.47 · R/R 0.78  
> ↳ P(T1 av. stop) 70 % · EV/risk 0.11 · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $271.77–$274.67 (mid $273.22)
- Spot actuel : $284.75 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $263.96 (stop swing_plan-based (-7.3%))
- Targets : T1 $280.47 · R/R 0.78 | T2 $287.71 · R/R 1.56 | T3 $294.96 · R/R 2.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $263.96


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.97 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.3 %)** : le gap seul le franchit 0.258 % des séances (3 fois sur 1165).
   - exécution **2.619 pt plus bas** dans le cas TYPIQUE (médiane), 7.343 au p90, **8.524 au pire**
   - perte réelle **11.211 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 7.3 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0101 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.823 % | p01 -4.436 % | pire -15.824 % _(sur 1165 séances)_
- **P(stop avant cible)** _(source : daily, 1166 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3878** [0.3176 ; 0.4618] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.431** [0.3795 ; 0.4836] _(largeur 10.4 pt, n_eff 345.4)_
   - deep : **0.4147** [0.3636 ; 0.4672] _(largeur 10.4 pt, n_eff 345.4)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.0 pt), swing (58.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.28 %** | CVaR **-6.2 %** | vol 2.99 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.90 % contre 2.70 % aujourd'hui, rapport 2.19)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.61 % vs -9.56 % si l'on extrapolait par √5 _(rapport 1.006 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1885** (β de hausse 1.1867, asymétrie 1.0015) vs SPY — 536 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 256.9614 sur sr_based (2.36 ATR, 9.759 %) — p(stop avant cible) 0.2919 [0.25 ; 0.34], R/R 2.463, perte reelle 12.871 % (gap inclus), CVaR 9.764 %, EV -0.9533 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.882 %) — p(stop avant cible) 0.5618 [0.51 ; 0.61], R/R 4.19, perte reelle 7.568 % (gap inclus), EV -1.2803 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.562, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 0.9 % x 31.71 % + P(rien) 42.9 % x 6.23 % ne couvrent pas P(stop) 56.2 % x 7.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.01 ATR (stop 8.606 %) — p(stop avant cible) 0.3315 [0.28 ; 0.38], R/R 2.463, perte reelle 12.871 % (gap inclus), EV -1.4029 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 0.9 % x 31.71 % + P(rien) 65.9 % x 3.89 % ne couvrent pas P(stop) 33.1 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.36 ATR (stop 9.759 %) — p(stop avant cible) 0.2919 [0.25 ; 0.34], R/R 2.463, perte reelle 12.871 % (gap inclus), EV -0.9533 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 0.9 % x 31.71 % + P(rien) 69.9 % x 3.59 % ne couvrent pas P(stop) 29.2 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.09 ATR (stop 21.905 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 1.447, perte reelle 21.905 % (gap inclus), EV 0.3378 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.91 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.814 %) — p(stop avant cible) 0.9384 [0.91 ; 0.96], R/R 15.728, perte reelle 2.016 % (gap inclus), EV -1.2474 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 15.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.938, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.3 % x 31.71 % + P(rien) 5.9 % x 9.34 % ne couvrent pas P(stop) 93.8 % x 2.02 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.627 %) — p(stop avant cible) 0.8361 [0.79 ; 0.87], R/R 9.961, perte reelle 3.183 % (gap inclus), EV -1.1211 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 9.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.836, borne haute 0.872 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 0.7 % x 31.71 % + P(rien) 15.7 % x 8.36 % ne couvrent pas P(stop) 83.6 % x 3.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.441 %) — p(stop avant cible) 0.7364 [0.69 ; 0.78], R/R 7.482, perte reelle 4.238 % (gap inclus), EV -0.8452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 7.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.736, borne haute 0.781 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 0.8 % x 31.71 % + P(rien) 25.6 % x 7.91 % ne couvrent pas P(stop) 73.6 % x 4.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.255 %) — p(stop avant cible) 0.6666 [0.62 ; 0.71], R/R 5.58, perte reelle 5.682 % (gap inclus), EV -1.1568 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.667, borne haute 0.715 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 0.9 % x 31.71 % + P(rien) 32.4 % x 7.20 % ne couvrent pas P(stop) 66.7 % x 5.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.068 %) — p(stop avant cible) 0.6122 [0.56 ; 0.66], R/R 5.12, perte reelle 6.193 % (gap inclus), EV -0.8938 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.612, borne haute 0.662 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.9 % x 31.71 % + P(rien) 37.8 % x 6.87 % ne couvrent pas P(stop) 61.2 % x 6.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.696 %) — p(stop avant cible) 0.5209 [0.47 ; 0.57], R/R 3.399, perte reelle 9.329 % (gap inclus), EV -1.8563 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.521, borne haute 0.573 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.86 %) : P(cible) 0.9 % x 31.71 % + P(rien) 47.0 % x 5.76 % ne couvrent pas P(stop) 52.1 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.01 ATR (stop 7.509 %) — p(stop avant cible) 0.3839 [0.33 ; 0.44], R/R 2.828, perte reelle 11.211 % (gap inclus), EV -1.3238 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.9 % x 31.71 % + P(rien) 60.7 % x 4.42 % ne couvrent pas P(stop) 38.4 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.391 %) — p(stop avant cible) 0.2261 [0.18 ; 0.27], R/R 2.004, perte reelle 15.824 % (gap inclus), EV -0.9821 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 1.0 % x 31.71 % + P(rien) 76.4 % x 2.99 % ne couvrent pas P(stop) 22.6 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.018 %) — p(stop avant cible) 0.1774 [0.14 ; 0.22], R/R 2.004, perte reelle 15.824 % (gap inclus), EV -0.4673 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 1.0 % x 31.71 % + P(rien) 81.3 % x 2.49 % ne couvrent pas P(stop) 17.7 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 14.646 %) — p(stop avant cible) 0.1274 [0.10 ; 0.17], R/R 2.004, perte reelle 15.824 % (gap inclus), EV -0.0622 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 1.0 % x 31.71 % + P(rien) 86.3 % x 1.90 % ne couvrent pas P(stop) 12.7 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 16.273 %) — p(stop avant cible) 0.0694 [0.05 ; 0.10], R/R 1.948, perte reelle 16.273 % (gap inclus), EV 0.1798 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.9 %) — p(stop avant cible) 0.0504 [0.03 ; 0.08], R/R 1.771, perte reelle 17.9 % (gap inclus), EV 0.184 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.90 % > budget 12.00 %
   - 🟢 grid_snapped a 6.09 ATR (stop 20.808 %) — p(stop avant cible) 0.0139 [0.01 ; 0.03], R/R 1.524, perte reelle 20.808 % (gap inclus), EV 0.3343 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.81 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 22.782 %) — p(stop avant cible) 0.0099 [0.00 ; 0.02], R/R 1.392, perte reelle 22.782 % (gap inclus), EV 0.3412 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.78 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.41 %) — p(stop avant cible) 0.0079 [0.00 ; 0.02], R/R 1.299, perte reelle 24.41 % (gap inclus), EV 0.3625 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.41 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 26.037 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 1.218, perte reelle 26.037 % (gap inclus), EV 0.3596 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.04 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 284.75, ATR14 9.2675 (3.255 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.386 ATR = 1.256 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.163 % | 284.2866 | 91.49 % | 94.47 % | 95.46 % | 96.67 % | 97.54 % | 97.97 % |
| 0.1 ATR | 0.325 % | 283.8233 | 85.41 % | 90.27 % | 92.25 % | 94.01 % | 95.54 % | 96.73 % |
| 0.15 ATR | 0.488 % | 283.3599 | 78.9 % | 85.95 % | 88.26 % | 90.46 % | 93.64 % | 95.37 % |
| 0.2 ATR | 0.651 % | 282.8965 | 71.93 % | 80.53 % | 83.83 % | 86.57 % | 91.18 % | 94.02 % |
| 0.25 ATR | 0.814 % | 282.4331 | 64.97 % | 74.89 % | 78.96 % | 82.8 % | 88.39 % | 91.99 % |
| 0.35 ATR | 1.139 % | 281.5064 | 53.59 % | 65.38 % | 70.99 % | 76.36 % | 83.82 % | 88.37 % |
| 0.5 ATR | 1.627 % | 280.1163 | 38.45 % | 52.32 % | 58.91 % | 65.7 % | 76.45 % | 82.51 % |
| 0.75 ATR | 2.441 % | 277.7994 | 20.22 % | 36.17 % | 44.52 % | 52.72 % | 65.85 % | 75.4 % |
| 1.0 ATR | 3.255 % | 275.4825 | 11.16 % | 23.78 % | 32.67 % | 42.73 % | 56.7 % | 68.96 % |
| 1.25 ATR | 4.068 % | 273.1656 | 5.75 % | 15.93 % | 23.81 % | 34.96 % | 50.67 % | 62.75 % |
| 1.5 ATR | 4.882 % | 270.8488 | 2.76 % | 10.51 % | 17.17 % | 28.63 % | 43.97 % | 57.0 % |
| 2.0 ATR | 6.509 % | 266.215 | 0.88 % | 4.31 % | 9.08 % | 17.65 % | 31.14 % | 45.94 % |
| 2.5 ATR | 8.137 % | 261.5813 | 0.44 % | 2.21 % | 4.65 % | 10.77 % | 20.76 % | 36.12 % |
| 3.0 ATR | 9.764 % | 256.9475 | 0.0 % | 1.11 % | 2.77 % | 6.66 % | 15.29 % | 28.22 % |
| 4.0 ATR | 13.018 % | 247.68 | 0.0 % | 0.22 % | 0.89 % | 2.55 % | 6.7 % | 14.11 % |
| 6.0 ATR | 19.528 % | 229.145 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.78 % | 2.71 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.54 ATR | 1.94 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.94 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.89 ATR | 2.59 ATR | 3.40 ATR |
| **10 s.** | 0.53 ATR | 1.27 ATR | 1.46 ATR | 1.93 ATR | 2.30 ATR | 2.57 ATR | 3.62 ATR | 4.57 ATR |
| **20 s.** | 0.77 ATR | 1.82 ATR | 2.05 ATR | 2.70 ATR | 3.23 ATR | 3.58 ATR | 4.72 ATR | 5.60 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.435–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.627 %, prix 280.1171), p(touche) 38.45 % (en stress 81.32 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.441 %, prix 277.7993), p(touche) 36.17 % (en stress 89.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.742–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.441 %, prix 277.7993), p(touche) 44.52 % (en stress 97.8 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.943–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.255 %, prix 275.4814), p(touche) 42.73 % (en stress 96.7 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.462–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.882 %, prix 270.8485), p(touche) 43.97 % (en stress 98.89 %)  ✅ optimum identifie (74.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.048–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.137 %, prix 261.5799), p(touche) 36.12 % (en stress 95.51 %)  ✅ optimum identifie (87.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.043 | EV/share : $0.397 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 39 % | T3 20 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.5 | bear 8.8 | side 76.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 285.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.838% → cible +1.186% / stop −1.5%, p_fill 31%, n_eff≈14.3) : P(cible|rempli) **29%** · **EV/risk -0.085** (×p_fill ; si rempli -0.41% du capital)
  - **swing** (entrée dip −4.045% → cible +2.652% / stop −3.392%, p_fill 14%, n_eff≈8.6) : P(cible|rempli) **44%** · **EV/risk +0.005** (×p_fill ; si rempli +0.12% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=15, n_eff=7))
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.0  _(momentum haussier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 0.275  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 12.5%
- **ATR** : 9.27 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.157  _(distribution)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 281.5 · MA50 269.27 · MA200 294.42  _(prix > MA20)_
- **Dist MA** : MA20 +1.2% · MA50 +5.7% · MA200 -3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (762016 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
